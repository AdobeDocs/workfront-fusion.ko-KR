---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 확장에서 Workfront 및 Fusion API 호출
description: 확장에서 Workfront 및 Fusion API 호출
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1083
ht-degree: 0%

---


# 확장에서 Workfront 및 Fusion API 호출

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

Fusion 컨텍스트 참조는 로그인한 사용자의 IMS 토큰을 제공하므로 자연스러운 다음 단계는 Workfront 또는 Fusion API를 호출하고 실제 데이터를 표시하는 것입니다. 이는 CORS로 인해 가능하지 않습니다. 이 문서에서는 App Builder 런타임 작업을 서버측 프록시로 사용하여 이러한 제한을 해결하는 방법을 보여 주며 예제(이벤트 구독 대시보드)를 포함합니다.

## 직접 브라우저 호출이 실패하는 이유(CORS)

표시되는 UI는 Adobe의 CDN(`https://<your-app>.adobeio-static.net`)에서 제공된 `<iframe>`에서 실행됩니다. 해당 페이지가 **다른** 원본에서 Workfront 또는 Fusion API에 대해 `fetch(...)`하면 브라우저가 CORS(원본 간 리소스 공유)를 적용합니다. API가 CDN 원본에 대해 명시적으로 `Access-Control-Allow-Origin`을(를) 반환하지 않으면 브라우저가 응답을 차단합니다. 이러한 API는 임의 확장 기원을 호출하지 않으므로 게스트의 직접 호출은 실패합니다.

CORS에 대한 자세한 내용은 [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS)을(를) 참조하십시오.

## CORS 없이 자체 런타임 작업 호출

이에 대한 수정 사항은 CORS 없이 자체 런타임 작업을 호출하는 것입니다.

App Builder 앱에는 서버측에서 실행되는 소규모 서버리스 함수인 런타임 작업이 포함될 수 있습니다. 서버 간 호출은 브라우저 CORS의 적용을 받지 않습니다. 또한 작업은 앱의 일부이므로 게스트는 동일한 원본을 사용하여 차단되지 않은 상대 URL로 호출할 수 있습니다.

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

이 작업은 게스트에서 사용자의 IMS 토큰을 받고 업스트림으로 전달하므로, 권한을 사용하여 사용자를 대신하여 계속 호출됩니다.

## 1단계: 작업 선언

런타임 작업은 확장의 `runtimeManifest` 아래에 있는 `app.config.yaml`에서 선언됩니다. 확장 옆에 `wf-proxy` 작업을 추가합니다.

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
    runtimeManifest:
      packages:
        fusion-uix-guest:                # ← your package name; part of the action URL
          license: Apache-2.0
          actions:
            wf-proxy:
              function: src/fusion-nav-organization-1/actions/wf-proxy/index.js
              web: 'yes'                  # exposes it at /api/v1/web/<package>/wf-proxy
              runtime: nodejs:22
              inputs:
                LOG_LEVEL: debug
              annotations:
                require-adobe-auth: false # see note below
                final: true
```

다음 위치에 작업을 연결할 수 있습니다.

```
/api/v1/web/<package>/<action>     e.g.  /api/v1/web/fusion-uix-guest/wf-proxy
```

### `require-adobe-auth`: true와 false

이 주석은 작업이 실행되기 전에 Adobe 게이트웨이가 IMS 토큰의 유효성을 검사하는지 여부를 제어합니다.

* **`true`:** 보안 기본값입니다.  게이트웨이가 인증되지 않은 호출을 거부합니다. 그러나 유효성 검사기는 기대하는 헤더에 대해 엄격하며 요청을 거부하거나 업스트림 호출에 필요한 사용자 지정 헤더를 삭제할 수 있습니다. 이 경우 토큰이 유효해도 `401`(으)로 표시됩니다.
* **`false`:**&#x200B;에서 게이트웨이 검사를 건너뜁니다. 그런 다음 작업을 공개적으로 사용할 수 없으므로 **직접 인증을 적용해야** 합니다. 작업에 `Authorization` 전달자가 필요하며 누락된 경우 거부하고 Workfront 및 Fusion이 유효성을 검사하는 업스트림으로 전달합니다. 2단계에서 설명한 엄격한 target 허용 목록과 결합된 이 경로는 사용자 지정 헤더를 전달해야 하는 프록시의 안정적인 경로입니다.

>[!TIP]
>
> 먼저 `true`을(를) 시도하십시오. 토큰이 유효하고 다른 곳에서 작동하기 때문에 설명할 수 없는 `401`이(가) 표시되면 `false` **(으)로 전환한 다음 암호자 확인 및 허용 목록에 추가하다를 계속 유지하여 보안이 업스트림으로 적용되도록 하십시오.**

## 2단계: 허용 목록에추가된 프록시에 대한 작업 쓰기

`src/fusion-nav-organization-1/actions/wf-proxy/index.js` 만들기. 작업을 릴레이로 사용할 수 없도록 업스트림 타겟의 허용 목록에 추가하다와 업스트림으로 전달되는 필수 전달자 토큰의 두 가지 규칙이 이러한 안전을 유지합니다.

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Page-through query params (see "Paginate list results" below).
const pageQuery = (p) => {
  const q = new URLSearchParams()
  if (p.start != null) q.set('start', p.start)
  if (p.limit != null) q.set('limit', p.limit)
  return q
}

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => {
      const q = pageQuery(p)
      if (p.teamId) q.set('teamId', p.teamId)
      return `https://fusion.adobe.com/api/v3/hooks?${q.toString()}`
    },
  },
  scenarios: {
    method: 'GET',
    url: (p) => {
      const q = pageQuery(p)
      if (p.fusionOrgId) q.set('organizationId', p.fusionOrgId)
      return `https://fusion.adobe.com/api/v3/scenarios?${q.toString()}`
    },
  },
}

async function main (params) {
  const logger = Core.Logger('main', { level: params.LOG_LEVEL || 'info' })
  try {
    const missing = checkMissingRequestInputs(params, ['target'], ['Authorization'])
    if (missing) return errorResponse(400, missing, logger)

    const target = TARGETS[params.target]
    if (!target) return errorResponse(400, `unknown target '${params.target}'`, logger)

    const token = getBearerToken(params)              // reads params.__ow_headers.authorization
    const headers = { authorization: `Bearer ${token}`, 'content-type': 'application/json' }
    if (params.orgId) headers['x-gw-ims-org-id'] = params.orgId        // Adobe IMS org id
    if (params.fusionOrgId) headers['x-organization-id'] = params.fusionOrgId  // Fusion tenant id
    if (params.teamId) headers['x-team-id'] = params.teamId            // Fusion team id

    const res = await fetch(target.url(params), { method: target.method, headers })
    const text = await res.text()
    let body
    try { body = JSON.parse(text) } catch (e) { body = text }

    if (!res.ok) {
      return { statusCode: res.status, body: { error: `upstream ${res.status}`, target: params.target, details: body } }
    }
    return { statusCode: 200, body }
  } catch (error) {
    logger.error(error)
    return errorResponse(500, 'server error: ' + error.message, logger)
  }
}

exports.main = main
```

`getBearerToken`, `errorResponse` 및 `checkMissingRequestInputs`은(는) 생성된 `actions/utils.js`에서 옵니다. 여기서 템플릿은 이 값을 스캐폴딩합니다. `getBearerToken`은(는) 게이트웨이가 들어오는 `Authorization` 헤더를 넣는 위치인 `params.__ow_headers.authorization`을(를) 읽습니다.

## 3단계: 게스트에서 작업 호출

UI에서 상대(동일 원본) URL이 있는 작업을 `fetch`하고 IMS 토큰을 전달자로 보냅니다. 업스트림에 필요한 조직 및 팀 ID를 쿼리 매개 변수로 전달합니다.

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId, start, limit } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  if (start != null) params.set("start", start);        // pagination offset
  if (limit != null) params.set("limit", limit);        // pagination page size
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

컨텍스트에서 `token`, `imsOrgId`, `fusionOrgId` 및 `teamId` 가져오기:

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
```

컨텍스트에 대한 자세한 내용은 [Fusion 컨텍스트 참조](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)를 참조하십시오.

## Fusion v3 API 세부 사항

`https://fusion.adobe.com/api/v3`에 대한 대시보드의 작업 내용:

| 헤더 / 매개 변수 | 값 | 참고 |
| ---------------- | ------- | ------- |
| `Authorization` | `Bearer <imsToken>` | 컨텍스트에서 사용자의 IMS 토큰입니다. |
| `x-organization-id` | `organization.id` | IMS 조직 ID가 아닌 Fusion의 자체 테넌트 ID. Fusion은 이를 통해 테넌트를 식별합니다. |
| `x-team-id` | `team.id` | 호출이 팀으로 범위가 지정되면 보냅니다. |
| `x-gw-ims-org-id` | `imsOrgId` | 게이트웨이용 Adobe IMS 조직 ID. |

다음 주의 사항을 참고하십시오.

* **`GET /api/v3/hooks`이(가) 팀 범위:** `teamId`은(는) **필수 쿼리 매개 변수**(`/api/v3/hooks?teamId=...`)입니다. 이 옵션을 사용하지 않으면 `400`이(가) 제공됩니다. 즉, 조직, 루프 팀 및 병합을 처리하기 위해 *활성 팀만*&#x200B;에 대해 후크를 다시 가져옵니다.
* **`GET /api/v3/scenarios`**&#x200B;은(는) `organizationId`(`/api/v3/scenarios?organizationId=...`)에서 작동합니다.

>[!NOTE]
>
> 공식 참조는 Adobe의 [Workfront Fusion API](https://developer.adobe.com/workfront-fusion-apis/)입니다. 헤더/인증 요구 사항은 게이트웨이에 따라 다릅니다. 이 표는 데모에 실제로 필요한 사항을 반영합니다. 호출이 `401`/`400`을(를) 반환하는 경우 먼저 이러한 헤더를 다시 확인하십시오.

## 페이지의 게시물 목록 결과

Fusion v3 목록 끝점(후크, 시나리오)은 전체 집합이 아닌 한 번에 하나의 **페이지**&#x200B;을 반환합니다. 응답은 다음과 같습니다.

```json
{
  "items": [ /* ...this page of records... */ ],
  "_page": { "start": 0, "limit": 100, "total": 342 }
}
```

레코드가 **`items`**&#x200B;에 있고 페이지 매김 메타데이터는 **`_page`**&#x200B;에 있습니다. **`start`**(오프셋) 및 **`limit`**(페이지 크기) 쿼리 매개 변수를 사용하여 페이지를 작성합니다. 위의 프록시는 둘 다 통과하므로 모든 항목을 수집할 때까지 게스트에서 페이지를 반복해서 지정합니다.

```js
const PAGE_LIMIT = 100;

async function fetchAllPages(target, token, opts = {}) {
  const all = [];
  let start = 0;
  // Stop when a page returns fewer than PAGE_LIMIT items, or when _page.total is reached.
  for (;;) {
    const res = await callProxy(target, token, { ...opts, start, limit: PAGE_LIMIT });
    const items = res.items ?? [];
    all.push(...items);

    const total = res._page?.total;
    const done = items.length < PAGE_LIMIT || (total != null && all.length >= total);
    if (done) break;
    start += PAGE_LIMIT;
  }
  return all;
}
```

브라우저에서 페이징을 유지하려면 런타임 작업 내에서 동일한 루프를 수행하고 병합된 `items` 배열을 하나의 응답으로 반환합니다. 어느 경우든 첫 번째 페이지가 전체 결과 집합이라고 가정하지 마십시오. 두 페이지 이상의 후크가 있는 팀은 그렇지 않으면 누락된 시나리오가 있는 것처럼 보일 수 있습니다.

## 보안 검사 목록

* **스트림 업스트림** 원시 클라이언트 입력에서 대상 URL을 구성하지 않습니다. 2단계에서와 같이 짧은 `target` 키를 고정 URL에 매핑합니다. 이렇게 하면 작업이 오픈 릴레이가 되는 것을 방지할 수 있습니다.
* 작업에서 **전달자 토큰 필요** 및 업스트림으로 전달합니다. Workfront 및 Fusion에서 사용자의 권한을 적용하게 합니다.
* **토큰을 기록하지 마십시오.** `imsToken`은(는) 자격 증명입니다. `LOG_LEVEL`에게 `stringParameters`이(가) 인쇄한 내용에 주의하십시오.
* **HTTPS로만 전달**&#x200B;하여 신뢰할 수 있는 Adobe 및 Workfront 호스트로 전달합니다.

## 작용한 예: 이벤트 구독 대시보드

데모 대시보드는 Workfront 이벤트 구독당 일치하는 Fusion 시나리오의 정상 여부를 표시하기 위해 세 개의 소스를 결합합니다.

1. `fetchSubscriptions()` → Workfront 이벤트 구독(수신/전달된 카운터 포함).
1. `fetchHooks(teamId)`→ 활성 팀에 대한 Fusion 후크(`fetchAllPages`(으)로 페이징됨).
1. `fetchScenarios(fusionOrgId)`→ 조직의 Fusion 시나리오(`fetchAllPages`(으)로 페이징됨)입니다.

**join**&#x200B;은(는) 연결되어 있지만 호출할 가치가 있는 catch가 있습니다. Workfront 구독과 Fusion 후크는 **다른 호스트**&#x200B;에서 라이브를 가리키므로 URL 필드가 바이트별로 동일하지 않습니다. 안정적인 것은 웹후크 URL **(마지막 경로 세그먼트)의 끝에 있는**&#x200B;토큰입니다. 전체 URL이 아닌 후행 토큰에 일치합니다. 그러면 후크의 `scenarioId`이(가) 시나리오의 `id`과(와) 일치합니다.

```
subscription.targetUrl  ──(trailing token)──▶  hook.url
                                                hook.scenarioId  ──▶  scenario.id
```

```js
// Reduce a webhook URL to its trailing token so hosts/bases can differ.
function hookKey(url) {
  if (!url) return "";
  const path = String(url).trim().toLowerCase().split(/[?#]/)[0].replace(/\/+$/, "");
  const i = path.lastIndexOf("/");
  return i >= 0 ? path.slice(i + 1) : path;
}

// Index hooks by token, then look each subscription up by the same token.
const hooksByToken = new Map(hooks.map((h) => [hookKey(pick(h, ["url", "address", "targetUrl"], "")), h]));
const hook = hooksByToken.get(hookKey(pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")));
```

상태는 조인에서 파생됩니다.

* **끊김**: 일치하는 후크가 없거나 후크가 `gone`입니다.
* **필터링**: 일치하지만 `passed < received`(이벤트가 도착하지만 시나리오가 실행되기 전에 필터링됨)입니다.
* **정상**: 일치하며 전달됩니다.

실제 페이로드 형태가 다르므로 클라이언트는 필드당 여러 후보 키를 시도하여 필드를 방어적으로 매핑하므로 작은 API 차이로 테이블이 손상되지 않습니다.

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
```

이것은 단지 하나의 예입니다. 필요한 모든 Workfront 또는 Fusion API에 대해 동일한 프록시 패턴이 작동합니다.
