---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 사용자 지정 확장 문제 해결
description: 사용자 지정 확장 문제 해결
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 0%

---


# 사용자 지정 확장 문제 해결

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

이 문서에서는 사용자 지정 확장을 만드는 동안 발생할 수 있는 문제에 대한 몇 가지 해결 방법을 개발 중에 발생하는 순서대로 제공합니다.

## 빠른 검사 목록

문제가 발생하면 먼저 다음 사항을 확인하십시오.

* Node.js는 버전 18 또는 20(`node --version`)입니다.
* 로그인(`aio login`) 및 올바른 조직/프로젝트/작업 공간(`aio console where`)에 있습니다.
* 확장 지점 이름이 버전 `fusion/nav-organization/1`을(를) 포함하여 정확히 일치합니다.
* `getWidget()`의 `url`이(가) 앱의 경로와 일치합니다.
* 표시되는 UI 호출 `attach({ id })`입니다.
* Fusion에서 올바른 확장 세트를 보고 있습니다.
  * 스테이지 빌드를 보려면 Stage를 배포하고 Fusion 프로필(제품 설정 > Fusion 프로필 > 환경 설정)에서 스테이지 확장 스위치를 켭니다.
  * 게시된 확장을 보려면 프로덕션에 배포하고 승인을 받습니다.

## 오류 1060: &quot;확장 지점이 존재하지 않습니다.&quot;

`aio app deploy` 동안 **전체 메시지:** `CoreConsoleAPISDK ... 1060: Extension point 'fusion/nav-organization/1' does not exist`.

**의미:** Adobe 조직에 대해 Fusion 확장 지점이 아직 활성화되지 않았습니다(&quot;온보딩&quot;). Adobe은 배포 시 조직의 카탈로그에 확장 지점이 존재하는지 확인합니다. 코드나 YAML에 문제가 **없습니다**.

**수정 사항:** Fusion 팀에 요청하여 IMS 조직의 확장 지점(`fusion/nav-organization/1` 및/또는 `fusion/nav-team/1`)을 온보딩하세요. 온보딩을 요청할 때 다음을 포함합니다.

* **IMS 조직 id**(`XXXX@AdobeOrg`),
* 필요한 **확장 지점**,
* **Developer Console 프로젝트 및 작업 영역** 이름.

온보딩이 확인되면 `aio app deploy`을(를) 다시 실행합니다.


## &quot;대상 iframe의 초기 메시지 대기 중&quot; / 패널이 영원히 회전합니다.

**의미:** Fusion에서 보이는 UI를 열었지만 핸드셰이크가 완료되지 않아 Fusion 시간이 초과되었습니다.

**일반적인 원인:**

* `attach`은(는) 등록 구성 요소에만 있으며 표시되는 위젯에는 없습니다.
* `getWidget()`의 `url`은(는) 위젯 대신 **등록** 구성 요소(또는 빈 페이지)를 렌더링하는 경로를 가리킵니다.
* `attach`에 전달된 `id`이(가) `register`에 사용된 `id`과(와) 다릅니다. 동일해야 하므로 둘 다 `Constants.js`에 유지합니다.

**수정:** **표시** 구성 요소 호출 `attach({ id })`을(를) 확인하십시오.

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

자세한 내용은 [사용자 지정 확장 UI 빌드](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)를 참조하십시오.



## 탐색 단추가 Fusion에 표시되지 않음

사용자 지정 확장에 대한 탐색 단추가 Fusion에 표시되지 않으면 다음 항목을 순서대로 확인하십시오.

1. **올바른 확장 집합을 보고 있습니까?** 기본적으로 Fusion은 프로덕션에 배포되고 승인된 게시된 확장만 표시합니다. 스테이지 빌드를 테스트하는 경우 Fusion 프로필(제품 설정 > Fusion 프로필 > 환경 설정)에서 스테이지 확장 스위치를 켜고 다시 로드합니다. 단계 항목에 **(단계)** 레이블이 지정되었습니다.
자세한 내용은 [사용자 지정 확장 게시](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md)를 참조하십시오.
1. **해지되었거나 철회되었습니까?** 취소되거나 철회된 확장이 오류 없이 Fusion에서 표시되지 않습니다. 이전에 작업한 버튼이 사라졌다면 코드 문제를 찾기 전에 Adobe Exchange에서 여전히 활성 상태인지 확인하십시오.
1. **올바른 작업 영역에 배포되었습니까?** 스테이지 테스트 스위치를 사용할 때 실제로 로드하는 작업 영역 스테이지 작업 영역을 배포합니다.
1. **올바른 조직에 배포되었습니까?** 배포한 **same** IMS 조직의 계정으로 Fusion에 로그인합니다.
1. **올바른 섹션에 있습니까?** `fusion/nav-organization/1`님은 **조직**&#x200B;에 표시되고, `fusion/nav-team/1`님은 **팀**&#x200B;에 표시됩니다(먼저 팀을 선택해야 함).
1. **확장 지점 이름이 오타가 있습니까?** `app.config.yaml`과(와) 폴더의 `ext.config.yaml` 포함 경로 모두에서 정확히 `fusion/nav-organization/1`을(를) 읽어야 합니다.


## 버튼이 표시되지만 패널이 비어 있습니다

버튼이 표시되지만 패널이 비어 있는 경우 다음을 확인하십시오.

* **경로 불일치:** `getWidget()`의 `url`(예: `/index.html#/my-widget`)은(는) `App.js`의 `<Route>`과(와) 일치해야 합니다. 불일치는 구성 요소가 없는 페이지를 로드합니다.
* **JavaScript 오류:** 브라우저의 개발자 도구(F12) > **콘솔** 탭을 열고 iframe에서 발생하는 오류를 찾습니다. 보고된 오류를 수정하고 다시 배포합니다.
* `getWidget()`의 **헤더 누락/중복:** `hideWidgetHeader`은(는) Fusion이 UI 위에 제목을 표시하는지 여부를 제어합니다. 자체 헤더를 렌더링하는 경우 `true`(으)로 설정하십시오.

## iframe이 차단됨(콘텐츠 보안 정책 / &quot;프레임 거부됨&quot;)

Fusion은 Adobe의 App Builder CDN(`*.adobeio-static.net`)에서 호스팅되는 확장만 허용합니다. 여기서 `aio app deploy`은(는) 기본적으로 파일을 저장합니다. 사용자 정의 도메인과 같은 다른 곳에서 UI를 호스트하는 경우 Fusion은 해당 UI 로드를 거부합니다. 문서화된 대로 App Builder을 통해 배포하거나 Fusion 팀에 도메인을 허용 목록에추가된으로 배포할 수 있는지 문의하십시오.

## 컨텍스트가 비어 있거나 오래됨

* **로드 후 바로 비어 있음:** 컨텍스트가 **후** `attach`이(가) 확인되기 전과는 다릅니다. 그때까지 &quot;연결 중...&quot; 상태를 표시합니다.
* **사용자가 조직 또는 팀을 전환할 때 업데이트되지 않음:** `contextchange` 이벤트를 구독하고 처리기 내의 키를 다시 읽습니다. 자세한 내용은 사용자 지정 확장 UI 빌드 문서의 [컨텍스트 Fusion 공유 읽기](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md#read-the-context-fusion-shares)를 참조하십시오.
* **날짜가 잘못된 것 같습니다.** 날짜 필드가 `Date` 개체가 아닌 ISO **문자열**&#x200B;으로 도착합니다. `new Date(...)`에 래핑합니다. Fusion 컨텍스트 참조 문서에서 [날짜](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md#dates)를 참조하십시오.

## CORS 오류로 API 호출이 실패합니다

**증상:** UI에서 Workfront/Fusion API를 직접 호출하는 경우 브라우저 콘솔에 *&quot;No &#39;Access-Control-Allow-Origin&#39; 헤더&quot;*(또는 요청이 차단됨)이 표시됩니다.

**수정:** 브라우저에서 해당 API를 호출하지 마십시오. 고유한 App Builder **런타임 작업**(서버측, CORS 없음)을 통해 호출을 라우팅하고 게스트가 상대 동일 원본 URL을 사용하여 작업을 호출하도록 합니다. 자세한 내용은 [Workfront 및 Fusion API 호출](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md)을 참조하십시오.


## 프록시 작업은 유효한 토큰이 있어도 401을 반환합니다.

**의미:** `require-adobe-auth: true`을(를) 사용하면 Adobe의 게이트웨이가 작업이 실행되기 전에 호출을 확인하고 이를 거부하거나 업스트림에 필요한 사용자 지정 헤더를 삭제하고 `401`(으)로 표시할 수 있습니다.

**수정:** 작업 **에 대해 `require-adobe-auth: false`을(를) 설정하고** 직접 인증을 적용합니다. 작업에 `Authorization` 전달자가 필요하여 업스트림으로 전달하고 엄격한 대상 허용 목록을 유지합니다. [require-adobe-auth: true와 false](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#require-adobe-auth-true-vs-false)를 참조하십시오.

## Fusion `GET /api/v3/hooks`이(가) 400을 반환합니다.

**의미:** 후크 끝점은 **팀 범위**&#x200B;이므로 `teamId`은(는) 필수 쿼리 매개 변수입니다.

**수정:** `/api/v3/hooks?teamId=<team.id>` 호출. 후크는 현역 팀에만 돌아옵니다. 조직을 다루려면 해당 팀을 반복하고 병합합니다. 이와는 대조적으로 시나리오에서는 `organizationId`을(를) 수락합니다. [Fusion v3 API 세부 정보](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#fusion-v3-api-specifics)를 참조하십시오.


## `aio`개 오류

* **`aio: command not found`:** CLI가 설치되지 않았거나 경로에 없습니다. `npm install -g @adobe/aio-cli`을(를) 다시 실행한 다음 새 터미널을 엽니다.
* **새 노드 버전에서 빌드/배포가 실패했습니다.** 노드 **18 또는 20개 LTS 사용**. 매우 새로운 비LTS 릴리스로 인해 도구 체인이 중단되는 경우가 있습니다.
* **&quot;개발자가 아닙니다&quot; / 조직을 볼 수 없습니다.** Adobe 조직 관리자는 **개발자** 역할 및 App Builder 액세스 권한을 부여해야 합니다. 자세한 내용은 [UI 확장 도구 및 계정 설정](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)을 참조하세요.
* **401 / 배포 또는 검색 중 잘못된 토큰:** 세션이 만료되었거나 환경이 혼합되었습니다. `aio logout`을(를) 실행한 후 `aio login`을(를) 실행하고 `aio console where`을(를) 확인한 후 로드 중인 작업 영역에 배포합니다.

## 지원을 위한 정보 수집

보다 신속하게 진단할 수 있도록 다음 정보를 수집합니다.

* 실행한 정확한 명령과 **full** 오류 출력입니다.
* **IMS 조직 ID**, **프로젝트** 및 **작업 공간**.
* 타깃팅하는 **확장 지점**&#x200B;입니다.
* `aio app deploy`의 성공 여부와 확장이 **published**&#x200B;인지 여부(또는 Stage 테스트의 경우 Stage 확장 스위치가 켜져 있는지 여부).
* Fusion에서 패널을 열 때 브라우저 **콘솔**(F12)에 오류가 발생합니다.
