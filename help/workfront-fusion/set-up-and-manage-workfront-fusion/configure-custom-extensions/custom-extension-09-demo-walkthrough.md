---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 사용자 지정 확장 데모 연습
description: 사용자 지정 확장 데모 연습
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 0%

---


# Fusion에서 사용자 지정 확장 프로그램 만들기에 대한 데모 연습

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

이 데모는 사용자 지정 확장을 만들고, 배포하고, Fusion에서 실행하는 과정을 안내합니다.

이러한 서비스에는 다음이 포함됩니다.

* 일반 Experience Cloud 셸 템플릿에서 App Builder 앱을 스캐폴드합니다.
* 앱을 Fusion 확장 지점으로 재타겟팅합니다.
* 앱을 스테이지 작업 영역에 배포합니다.
* Fusion에서 스테이지 테스트를 켜고 실행 중인 앱을 표시합니다.

빈 `--standalone-app`이(가) 아닌 템플릿에서 시작하면 SPA 부트스트랩이 생성됩니다. `index.js`, `exc-runtime.js`, `App.js`(라우팅 및 `ErrorBoundary` 포함) 및 샘플 `ExtensionRegistration`. 데모의 라이브 단계는 구성을 다시 타겟팅하고 두 개의 파일을 편집하는 것입니다. 이는 실제 `fusion-uix-guest`이(가) 빌드된 방식입니다.

>[!NOTE]
>
> **시간:** 도구를 설정한 후 라이브 데모에는 약 10분이 소요됩니다. 데모에서 1회 설정(노드 18/20, `aio` CLI, `aio login`)을 **이전**&#x200B;해야 합니다. 자세한 내용은 [UI 확장 도구 및 계정 설정](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)을 참조하세요.


## 시작하기 전에

이 작업은 한 번만 수행해야 하며 데모 전에 바로 수행할 수 있습니다.

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

데모 조직에서는 다음 두 가지 사항이 사실이어야 합니다.

* `fusion/nav-organization/1` 확장 지점이 조직에 대해 온보딩되었습니다. 온보딩되지 않은 경우 배포가 실패하고 오류 1060이 표시됩니다. 자세한 내용은 [사용자 지정 확장 문제 해결](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)을 참조하십시오.
* 사용자 지정 확장 기능은 Fusion 호스트에서 활성화됩니다. (이 기능은 기본적으로 켜져 있습니다.) 게시된 빌드가 아닌 Stage 빌드를 시연하므로 Fusion 프로필에서 **Stage 확장** 스위치도 켭니다. (이 스위치는 7단계에 표시되어 있습니다.) Fusion은 사용자가 게시하기 전까지 게시된 확장만 표시합니다.

## 1단계: 일반 템플릿에서 앱 생성

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

* 메시지가 표시되면 **새 프로젝트 만들기**&#x200B;를 선택하고 제안된 이름을 수락합니다.
* `@adobe/generator-app-excshell`은(는) 일반 **Experience Cloud 셸** UI 확장 템플릿이며 제품별로 다르지 않습니다. `src/dx-excshell-1/` 아래에 작동 중인 전체 SPA를 스캐폴딩합니다.

>[!NOTE]
>
>메뉴를 선호하는 경우 `aio app init my-fusion-extension`을(를) 실행하고 **확장 또는 독립 실행형 앱 추가** > **템플릿**&#x200B;을(를) 선택한 다음 **&quot;Experience Cloud 셸용 App Builder UIX 확장&quot;**&#x200B;을(를) 선택하십시오.

다음을 포함한 파일 세트를 가져옵니다.

```
my-fusion-extension/
|-- app.config.yaml
|-- src/dx-excshell-1/
    |-- ext.config.yaml
    |-- web-src/src/
        |-- index.js          // SPA bootstrap (exc-app Runtime + React render)
        |-- exc-runtime.js    // Experience Cloud Shell runtime glue
        |-- components/
            |-- App.js                    // Router + ErrorBoundary (generated)
            |-- ExtensionRegistration.js  // sample registration (generated)
```

## 2단계: Fusion 게스트 라이브러리 추가

템플릿에는 이미 React, React Spectrum 및 exc-app이 포함되어 있습니다. Fusion 호스트에 말하는 라이브러리를 추가합니다.

```sh
npm install @adobe/uix-guest
```

## 3단계: 구성을 Fusion으로 재타겟팅

**`app.config.yaml`**&#x200B;을(를) 열고 **확장 지점 키**&#x200B;만 Experience Cloud 셸 지점에서 Fusion 키로 변경합니다(`$include` 경로는 그대로 유지).

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

구성에서 다른 내용을 변경할 필요가 없습니다. 폴더 이름 `dx-excshell-1`은(는) 내부이며 Fusion에 영향을 주지 않으므로 그대로 둘 수 있습니다. 이름을 바꾸면 모든 작업 경로를 업데이트하는 의미도 있습니다. 데모에 대해서는 건너뛰십시오.

>[!NOTE]
>
>**팀** 섹션을 대상으로 하는 경우 대신 `fusion/nav-team/1`을(를) 사용하십시오. 프로덕션에 **조직과 팀을 모두**&#x200B;하려면 **별도의 프로젝트 두 개**&#x200B;를 사용하십시오. 레지스트리 이름당 하나의 확장 지점 번들로 인해 공유 앱 충돌이 방지됩니다.

## 4단계: 등록 및 위젯 파일 편집

모든 경로는 `src/dx-excshell-1/web-src/src/components/` 아래에 있습니다.

### **`ExtensionRegistration.js`**

생성된 파일이 Experience Cloud 셸 샘플을 등록합니다. Fusion이 사용자의 제목과 UI의 위치를 알 수 있도록 해당 `methods`을(를) Fusion **`dashboard.getWidget`** 계약으로 바꿉니다.

```js
import { Text } from "@adobe/react-spectrum";
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

function ExtensionRegistration() {
  const init = async () => {
    await register({
      id: extensionId,
      metadata,
      methods: {
        dashboard: {
          getWidget() {
            return {
              id: extensionId,
              title: "My Fusion tool",          // label on the Fusion nav button
              description: "Hello from App Builder",
              url: "/index.html#/widget",       // route to the visible UI (4b)
              widgetSize: { defaultWidth: 6, defaultHeight: 6 },
              hideWidgetHeader: false,
            };
          },
        },
      },
    });
  };
  init().catch(console.error);

  return <Text>Registering with Fusion...</Text>;
}

export default ExtensionRegistration;
```

`Constants.js`이(가) 옆에 없으면 만드십시오.

```js
module.exports = { extensionId: "my-fusion-extension" };
```

### `DashboardWidget.js`

이 파일을 만듭니다. 핸드셰이크가 완료되고 라이브 Fusion 컨텍스트가 표시됩니다.

```js
import { useEffect, useState } from "react";
import { Flex, Heading, Text, View } from "@adobe/react-spectrum";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

export default function DashboardWidget() {
  const [ctx, setCtx] = useState(null);

  useEffect(() => {
    attach({ id: extensionId })
      .then((guest) => {
        const read = () =>
          KEYS.reduce((acc, k) => ({ ...acc, [k]: guest.sharedContext.get(k) }), {});
        setCtx(read());
        guest.addEventListener("contextchange", () => setCtx(read()));
      })
      .catch((e) => console.error("attach failed", e));
  }, []);

  return (
    <View padding="size-300">
      <Heading level={2}>Hello from App Builder</Heading>
      {!ctx ? (
        <Text>Connecting to Fusion...</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "-"}</Text>
        </Flex>
      )}
    </View>
  );
}
```

### `App.js`

생성된 라우터가 이미 `index`/`index.html`을(를) `ExtensionRegistration`(으)로 보냅니다. 위젯에 대한 경로를 추가하고 가져옵니다.

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> 경로 경로 경로(`widget`)는 `getWidget().url`(`/index.html#/widget`)의 해시와 일치해야 합니다. 생성된 `index.js`/`exc-runtime.js` 및 나머지 `App.js`은(는) 템플릿에서 제공하려는 부트스트랩이므로 스캐폴딩으로 정확하게 유지합니다.

## 5단계: 빌드

```sh
aio app build
```

이렇게 하면 프런트 엔드가 컴파일되고 `app-metadata.json`을(를) 생성하는 메타데이터 후크가 실행됩니다. 계속하기 전에 오류를 모두 수정하십시오.

## 6단계: 스테이지에 배포

```sh
aio console workspace select     # choose Stage
aio app deploy
```

`deploy`이(가) Adobe의 CDN에서 UI를 호스팅하고 확장 끝점을 Stage 작업 영역에 등록합니다. 이렇게 하면 Fusion에서 해당 끝점을 검색할 수 있습니다. CLI가 `https://<project>-stage.adobeio-static.net`과(와) 같은 끝점 URL을 인쇄합니다.

## 7단계: 스테이지 테스트 켜기 및 Fusion 확장 표시

1. 배포한 동일한 조직에 로그인한 Experience Cloud에서 Fusion을 엽니다.
1. 사용자 아바타 메뉴를 열고 **제품 설정** > **Fusion 프로필** > **환경 설정**(으)로 이동합니다.
1. **Stage 확장** 스위치를 켜고 다시 로드를 확인합니다.

   이제 Fusion은 Stage 작업 영역에서 확장을 로드하고 **(Stage)**&#x200B;에 표시합니다.
1. 왼쪽 탐색 영역에서 **조직** 영역으로 이동합니다.

   **&quot;내 Fusion 도구(단계)&quot;** 단추가 나타납니다.
1. **&quot;내 Fusion 도구(단계)&quot;** 단추를 클릭합니다.
UI가 기본 패널에 로드되고 라이브 사용자, 조직 및 팀이 표시됩니다.
1. Fusion에서 **활성 조직 또는 팀 전환**

   패널이 업데이트되어 라이브 컨텍스트(`contextchange`)를 보여 줍니다.

>[!TIP]
>
>단추가 표시되지 않으면 세션당 검색이 캐시되므로 한 번 다시 로드하십시오. [사용자 지정 확장 문제 해결](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)을 참조하세요.


## 데모 도중 반복

변경한 다음 다시 빌드하고 재배포합니다.  사용자가 다음에 업데이트된 확장을 열면 해당 확장이 표시됩니다.

```sh
aio app build && aio app deploy
```

## 데모 후 프로덕션으로 이동

무대는 데모하기에 충분하다. 조직 전체에 릴리스하려면 프로덕션 작업 공간으로 전환하고, 을 배포하고 승인 요청을 제출합니다. 시스템 관리자 역할을 사용하여 요청을 제출해야 합니다. 전체 프로세스를 보려면 [프로덕션 릴리스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md#release-on-production)를 참조하십시오.

## 데모 토크 트랙(선택 사항)

라이브 데모 중에 다음과 같은 사항을 강조하고 싶을 수 있습니다.

* **&quot;일반 Experience Cloud 셸 템플릿에서 시작했습니다.&quot;** 전체 SPA 셸을 스캐폴드하므로 확장자만 다시 타겟팅하고 파일 두 개를 편집했습니다.
* **&quot;Fusion은 호스트이고, 내 앱은 게스트입니다.&quot;** 별도의 프레임으로 실행하고 사용자 지정 네트워킹 없이 Adobe의 UI 확장성 SDK을 통해 대화합니다.
* **&quot;등록과 보기 비교.&quot;** 내가 제공하는 숨겨진 프레임 *등록*(`dashboard.getWidget`) 및 보이는 프레임 *연결*&#x200B;되고 컨텍스트를 읽습니다.
* **&quot;스테이지 테스트는 사용자별 스위치입니다.&quot;** Fusion은 기본적으로 게시된 확장만 표시합니다. 프로덕션 릴리스 없이 Fusion 프로필의 Stage 확장을 플립하여 Stage 빌드를 로드했습니다.
* **&quot;라이브 컨텍스트.&quot;** 조직 또는 팀을 전환하면 컨텍스트가 다시 전송되고 게스트는 다시 렌더링됩니다.
