---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: UI 확장성을 위한 프로젝트 만들기
description: UI 확장성을 위한 프로젝트 만들기
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1360
ht-degree: 0%

---

# UI 확장성을 위한 프로젝트 만들기

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

사용자 정의 UI 확장을 만들려면 해당 사용자 정의 UI 확장에 대한 App Builder 프로젝트를 만들어야 합니다.

이 페이지에서는 `aio` 명령줄을 사용하여 일반 App Builder 프로젝트를 생성하는 방법에 대해 설명합니다. &quot;일반&quot;은 프로젝트가 제품별 템플릿에서 시작하지 **않음을 의미합니다**. 일반 앱으로 시작하면 프로젝트가 단순하게 유지되며 Workfront Fusion과 연결할 수 있습니다.

Adobe Fusion AI Extensibility에 사용할 프로젝트 만들기에 대해 다음 개념 및 용어를 숙지하는 것이 유용할 수 있습니다.

* **Adobe Developer Console**(<https://developer.adobe.com/console>)은 프로젝트가 있는 웹 대시보드입니다.

* **용어**:

  | 용어 | 의미 |
  | ------ | --------------- |
  | **조직** | 회사의 Adobe 조직 Fusion에서 사용하는 것과 동일한 조직 |
  | **프로젝트** | 하나의 앱/확장에 대한 컨테이너입니다. 확장에 대해 하나의 프로젝트를 만듭니다. |
  | **작업 공간** | 작업 단계에 대한 프로젝트 구성의 사본. 모든 프로젝트에는 **프로덕션** 작업 영역이 있으며 일반적으로 테스트를 위해 **스테이지** 작업 영역도 사용합니다. &quot;환경&quot;과 같은 작업 영역을 생각해 보십시오. |
  | **자격 증명/서비스** | 앱에서 사용할 수 있는 권한. 생성된 기본값은 시작하기에 충분합니다. |

* 프로젝트를 만드는 방법에는 두 가지가 있습니다.

  * **자동(권장):** `aio app init` 명령은 코드를 생성하는 동안 프로젝트와 작업 공간을 만듭니다. 이 문서에서는 이 프로세스에 대해 설명합니다.
  * **수동:** 먼저 Developer Console에서 프로젝트를 직접 만든 다음 `aio`을(를) 가리킵니다. 조직에서 프로젝트를 중앙에서 만들어야 하는 경우에만 이 작업을 수행하는 것이 좋습니다.

* 사용할 작업 영역을 결정할 때 먼저 **Stage**&#x200B;에 개발 및 배포합니다. Fusion은 사용자가 Fusion 프로필에서 스테이지 테스트를 켤 때만 스테이지 빌드를 로드합니다(사용자 아바타 메뉴 > 제품 설정 > Fusion 프로필 > 환경 설정 > 스테이지 확장). 그렇지 않은 경우 게시된 프로덕션 확장만 표시됩니다. `aio app run`을(를) 사용하여 로컬에서 미리 본 다음 나중에 **프로덕션**(으)로 승격할 수도 있습니다.

  프로덕션으로 승격하는 방법에 대한 자세한 내용은 [확장 게시](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md)를 참조하십시오.


## `aio app init` 실행

1. 터미널을 엽니다.
1. 터미널에서 프로젝트를 보관하는 폴더로 이동합니다.
1. 실행:

   ```sh
   aio app init my-fusion-extension --standalone-app
   ```

   * `my-fusion-extension`은(는) 폴더/앱 이름입니다. 이 이름을 선택할 수 있지만 소문자, 하이픈을 사용하고 공백을 사용하지 않습니다.
   * `--standalone-app`은(는) 제품 템플릿을 선택하라는 대신 CLI에 **일반 응용 프로그램 구조**&#x200B;를 만들도록 지시합니다. 이는 AEM(또는 기타) 템플릿을 피하는 데 필요한 핵심 요소입니다.

1. 메시지가 표시되면 **조직을 선택**&#x200B;합니다(둘 이상의 조직에 속해 있는 경우).
1. 메시지가 표시되면 **새 프로젝트 만들기**&#x200B;를 선택하고 제안된 이름을 수락하거나 기존 빈 프로젝트를 선택하십시오.

   명령이 **Stage** 및 **Production** 작업 영역을 자동으로 설정합니다.

   또한 이 명령은 `my-fusion-extension` 폴더에 파일을 생성하고 `npm install`을(를) 실행합니다.

1. [프로젝트 만들기 확인](#confirm-project-creation)을 계속합니다.

>[!NOTE]
>
> **대화형 메뉴를 선호하는 경우:** `aio app init my-fusion-extension` > (`--standalone-app` 없이) 실행 **에게 &quot;어떤 템플릿을 검색하시겠습니까?&quot;**&#x200B;라고 묻는 경우 또는 템플릿 체크리스트를 표시합니다. AEM과 같은 제품 템플릿을 선택하지 마십시오. **독립 실행형 응용 프로그램**/**&quot;모든 확장 지점 → 없음&quot;**&#x200B;을(를) 만드는 옵션을 선택하십시오.

## 프로젝트 생성 확인

1. 터미널에서 생성된 폴더로 이동합니다.

   ```sh
   cd my-fusion-extension
   ```

   다음과 유사한 구조가 표시되어야 합니다(일부 파일 생략).

   ```
   my-fusion-extension/
   |--- app.config.yaml   // main configuration (you will edit this)
   |---  package.json   //dependencies and scripts
   |---  src/    // your source code
   |---  web-src/  or  src/.../web-src/  // front-end files (HTML/JS)
   ```

   가장 중요한 두 파일은 다음과 같습니다.

   * **`app.config.yaml`**: 중앙 구성. 나중에 이 프로세스에서 앱을 Fusion 확장 지점에 연결하는 `extensions:` 섹션을 여기에 추가합니다.
   * **`package.json`**: 앱에서 사용하는 라이브러리를 나열합니다. 여기에 Adobe UI 확장성 게스트 라이브러리를 추가합니다.

1. [필요한 라이브러리 추가](#add-required-libraries)를 계속합니다.

>[!TIP]
>
> 생성된 레이아웃이 CLI 버전 간에 약간 다르더라도 걱정하지 마십시오. 이 절차에서는 만들 파일과 그 안에 넣을 내용을 정확히 알려주므로 시작 지점에 관계없이 예상 구조를 일치시킬 수 있습니다.

## 필수 라이브러리 추가

확장에는 두 개의 라이브러리가 필요합니다.

* **`@adobe/uix-guest`**: 앱이 Fusion(호스트)에 연결할 수 있도록 해줍니다.
* **`@adobe/react-spectrum`**: Adobe의 React UI 구성 요소이므로 화면이 Adobe의 모양과 느낌과 일치합니다. (선택 사항이지만 권장됨. 대신 일반 HTML을 사용할 수 있습니다.)

이러한 라이브러리를 설치하려면 다음을 수행하십시오.

1. 터미널에서 다음을 실행합니다.

   ```sh
   npm install @adobe/uix-guest @adobe/react-spectrum
   ```

1. (조건부) 생성된 프로젝트에 React가 아직 포함되지 않은 경우 설치하십시오.

   ```sh
   npm install react react-dom react-router-dom
   ```

1. [프로젝트 빌드 확인](#confirm-the-project-builds)을 계속합니다.

## 프로젝트 빌드 확인

변경하기 전에 빈 프로젝트가 빌드되었는지 확인하십시오.

1. 터미널에서 다음을 실행합니다.

   ```sh
   aio app build
   ```

   오류 없이 완료되면 도구 및 프로젝트가 올바르게 구성됩니다. 프로젝트를 Fusion에 연결할 준비가 되었습니다.

   >[!TIP]
   >
   > **빌드가 실패하면** 가장 일반적인 원인은 지원되지 않는 Node.js 버전입니다. `node --version`을(를) 실행하고 18 또는 20인지 확인하십시오.
   >
   >* Node.js 설치에 대한 자세한 내용은 [도구 설정](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)을 참조하십시오.
   >* 기타 가능한 오류에 대한 자세한 내용은 [문제 해결](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)을 참조하십시오.

1. [Fusion용 프로젝트 구성](#configure-the-project-for-fusion)을 계속합니다.

## Fusion에 대한 프로젝트 구성

사용자 지정 확장을 설정하는 다음 단계는 일반 프로젝트를 Workfront Fusion에 연결하는 것입니다.

다음을 수행할 수 있습니다.

1. [확장에 사용할 폴더 만들기](#create-a-folder-for-your-extension)
1. App Builder에 Fusion **확장 지점**(`app.config.yaml`의)에 대해 알려 주십시오.
1. 확장의 일부를 설명합니다(`ext.config.yaml`).
1. Fusion이 위젯의 제목과 해당 UI의 위치를 알 수 있도록 위젯을 **등록**&#x200B;합니다.

`fusion/nav-organization/1`은(는) 전체에서 사용합니다. 대신 팀 섹션을 대상으로 지정하려면 `fusion/nav-team/1`에서 모든 위치에서 바꿉니다. 두 옵션을 모두 지원하려면 각각에 대해 패턴을 반복합니다.

## 확장에 사용할 폴더 만들기

1. 프로젝트가 다음과 같이 표시되도록 파일을 만듭니다.

   ```
   my-fusion-extension/
   |-- app.config.yaml
   |-- src/
          |-- fusion-nav-organization-1/          // one folder per extension point
             |-- ext.config.yaml
             |-- web-src/
                |-- src/
                   |-- components/
                      |-- App.js
                      |-- ExtensionRegistration.js
                      |-- DashboardWidget.js
                      |-- Constants.js
   ```

   확장 지점(`fusion-nav-organization-1`) 뒤에 폴더 이름을 지정하는 것이 좋습니다. 정확한 이름은 사용자가 지정하지만 `app.config.yaml`에서 참조하는 이름과 일치해야 합니다.

1. [계속 `app.config.yaml`](#declare-the-extension-point-in-appconfigyaml)에서 확장 지점을 선언합니다.

## `app.config.yaml`에서 확장 지점 선언

1. `app.config.yaml`을(를) 열고 내용을 다음으로 업데이트:

   ```yaml
   extensions:
     fusion/nav-organization/1:
       $include: src/fusion-nav-organization-1/ext.config.yaml
   ```

   이러한 내용은 다음을 설명합니다.

   * `extensions:`: 이 앱은 하나 이상의 확장 지점을 구현합니다.
   * `fusion/nav-organization/1`: 연결 중인 Fusion 슬롯입니다. **버전 `1`을(를) 포함하여**&#x200B;과(와) 정확히 일치해야 합니다.
   * `$include:`: 이 확장의 내용을 설명하는 두 번째 구성 파일(다음 단계에서 만들어짐)을 가리킵니다. 별도의 파일에 보관하면 `app.config.yaml`이(가) 깔끔하게 유지되고 나중에 더 많은 확장 지점을 추가할 수 있습니다.

   >[!NOTE]
   >
   >두 확장을 모두 타겟팅하는 경우 두 확장을 모두 나열하고 각각 고유한 폴더를 추가합니다.
   >
   > ```yaml
   > extensions:
   >     fusion/nav-organization/1:
   >         $include: src/fusion-nav-organization-1/ext.config.yaml
   >     fusion/nav-team/1:
   >         $include: src/fusion-nav-team-1/ext.config.yaml
   > ```

   1. [계속 `ext.config.yaml`](#describe-the-extension-in-extconfigyaml)에서 확장 설명

## `ext.config.yaml`에서 확장 설명

1. 다음을 사용하여 `src/fusion-nav-organization-1/ext.config.yaml` 만들기:

   ```yaml
   operations:
      view:
       - type: web
         impl: index.html
   web: web-src
   hooks:
     pre-app-build: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
      pre-app-run: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
   ```

   이러한 내용은 다음을 설명합니다.

   * **`operations.view`**: 확장이 `index.html`에서 제공되는 **보기**(표시되는 UI)를 제공함을 선언합니다. 이렇게 하면 확장 프로그램이 백그라운드에서만 실행되는 것이 아니라 화면을 표시합니다.
   * **`web: web-src`**: 프런트 엔드 파일이 들어 있는 폴더입니다. App Builder은 여기에 모든 것을 빌드하고 Adobe의 CDN(Content Delivery Network)에서 호스팅합니다.
   * **`hooks`**: 빌드/실행 시 자동으로 실행되는 작은 명령입니다. `generate-metadata.js` 스크립트는 `@adobe/uix-guest`과(와) 함께 제공되며 등록 코드에 필요한 `app-metadata.json` 파일을 생성합니다(4단계 참조). 이 스크립트를 작성하지 않고 참조만 하면 됩니다.

   >[!NOTE]
   >
   > 서버측 논리도 필요한 경우 서버를 사용하지 않는 `actions`(작은 백엔드 함수)을 추가할 수도 있습니다. 작업은 선택 사항이며 UI 렌더링에 필요하지 않으므로 이 안내서를 중점적으로 유지하기 위해 생략합니다. 나중에 추가하면 여기에 `actions:` 폴더를 선언하고 `app.config.yaml`에 `runtimeManifest:`을(를) 선언하십시오. 하나를 추가하는 가장 일반적인 이유는 브라우저 CORS에 도달하지 않고 Workfront/Fusion API를 호출하기 위해서입니다.
   > API 호출에 대한 자세한 내용은 [Workfront 및 Fusion API 호출](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md)을 참조하십시오.
1. [안정적인 확장 ID를 설정](#set-a-stable-extension-id)합니다.

## 안정적인 확장 ID 설정

확장에는 두 프레임이 공유하는 고유 ID가 필요합니다.

사용자 지정 확장과 관련된 프레임에 대한 자세한 내용은 [UI 확장에 포함된 프레임](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension)을 참조하십시오.

1. `src/fusion-nav-organization-1/web-src/src/components/Constants.js` 만들기:

   ```js
   module.exports = {
     extensionId: 'my-fusion-extension'
   };
   ```

   코드가 확장 ID를 참조하는 모든 곳에서 동일한 값을 사용합니다.
1. [위젯 등록](#register-your-widget)을 계속합니다.


## 위젯 등록

&quot;등록&quot;은 숨겨진 배경 프레임이 확장에서 제공하는 것을 Fusion에 알리는 방법입니다. 위젯의 제목과 표시되는 UI의 URL을 반환하는 `dashboard.getWidget()` 메서드를 선언합니다.

1. `src/fusion-nav-organization-1/web-src/src/components/ExtensionRegistration.js` 만들기.
중요한 부분은 `register(...)` 호출입니다.

   ```js
   import { register } from "@adobe/uix-guest";
   import metadata from "../../../../app-metadata.json";
   import { extensionId } from "./Constants";
   
   async function init() {
     await register({
       id: extensionId,
       metadata,
       methods: {
         dashboard: {
           getWidget() {
             return {
               id: extensionId,
               title: "My Fusion tool",        // shown on the Fusion nav button
               description: "What this tool does",
               url: "/index.html#/my-widget",  // route to your visible UI
               hideWidgetHeader: false          // false = Fusion shows the title
             };
           }
         }
       }
      });
   }
   
   init().catch(console.error);
   ```

   주요 사항:

   * **`title`**&#x200B;은(는) Fusion이 탐색 단추에 입력하는 레이블입니다. `hideWidgetHeader`이(가) `false`인 경우 Fusion은 제목도 UI 위에 헤더로 표시합니다.
   * **`url`**&#x200B;은(는) 이 동일한 앱 내에서 *보이는* UI에 대한 경로입니다. 다음 페이지에 설정된 프런트 엔드 라우터에서 처리하는 해시 경로(`#/my-widget`)입니다. 화면을 렌더링하는 구성 요소로 확인해야 합니다.
   * **`metadata`**&#x200B;은(는) 빌드 시 `generate-metadata` 후크에서 만들어지는 `app-metadata.json`에서 가져옵니다. 표시된 대로 가져옵니다.
   * `dashboard.getWidget` 메서드 이름은 위젯을 검색하기 위해 합의된 약정 Fusion 호출입니다. `dashboard` 네임스페이스와 `getWidget` 이름을 유지합니다.

이제 확장의 백엔드가 완료되었습니다. 확장의 UI를 빌드하는 다음 단계입니다.

UI 빌드에 대한 지침은 [사용자 지정 확장 UI 빌드](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)를 참조하십시오.
