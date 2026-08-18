---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 사용자 지정 확장 게시
description: 사용자 지정 확장 게시
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 1%

---

# 사용자 지정 확장 게시

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

확장 프로그램은 조직의 **빌드**, **Adobe에 배포** 및 **승인**&#x200B;된 후에만 Fusion에서 실행됩니다. 이 페이지의 절차에는 확장을 게시하는 방법과 결과를 확인하는 방법이 표시됩니다.

이 정보는 Adobe의 공식 문서에서 채택되었으며 특히 Workfront Fusion에 적용됩니다. 일반적인 Adobe 정보는 Adobe 설명서에서 [UI 확장 개발 흐름](https://developer.adobe.com/uix/docs/guides/development-flow/) 및 [UI 확장 관리](https://developer.adobe.com/uix/docs/guides/publication/)를 참조하십시오.

## 작업 영역

모든 App Builder 프로젝트에는 **단계**&#x200B;와 **프로덕션** 작업 영역이 있습니다. 이를 환경으로 간주합니다.

* **단계**&#x200B;은(는) 개발 및 테스트용입니다. 반복하는 동안 여기에 배포합니다. 승인이 필요하지 않으며, 결과는 아래 설명된 스테이지 테스트 스위치(또는 로컬 미리보기)를 통해서만 볼 수 있습니다.
* **프로덕션**&#x200B;은(는) 모든 사람에게 릴리스할 예정입니다. 프로덕션에 배포한 후 **승인 요청**&#x200B;을 제출하고 승인이 완료되면 확장이 Adobe 앱 레지스트리에 등록되고 조직 전체에 표시됩니다.

>[!NOTE]
>
> **역할:**&#x200B;을(를) 만들고 배포하려면 **개발자** 역할이 필요합니다. 게시하도록 승인 요청을 제출하려면 **시스템 관리자** 역할이 필요합니다.
>자세한 내용은 다음 문서를 참조하십시오.
>
> * [UI 확장 도구 및 계정 설정](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)
> * Adobe 설명서에서 [액세스 권한을 받는 방법](https://developer.adobe.com/uix/docs/guides/get-access/).

기본적으로 Fusion은 **게시된** 확장만 표시합니다. **프로덕션** 작업 영역에 배포한 다음 **승인**&#x200B;을 위해 제출한 확장입니다. 이는 안전한 기본값이므로 진행 중인 배포 작업이 실수로 전체 조직에 표시되지 않습니다.

**Stage** 작업 영역에 대한 배포가 게시되지 않았으므로 Fusion에 자체적으로 나타나지 않습니다. 확장을 게시하기 전에 두 가지 방법으로 확장을 시도할 수 있습니다.

* **로컬에서 미리 보기**&#x200B;를 `aio app run`(Adobe 설명서에서 [UI 확장의 로컬 미리 보기](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/) 참조)로 사용합니다. 배포된 항목이 없으며 사용자만 볼 수 있습니다.
* Fusion 프로필에서 사용자별 테스트 스위치를 켜서 **Fusion 내부의 스테이지에서 로드합니다**. 이 설명은 이 문서의 [Fusion에서 스테이지 빌드 테스트](#test-a-stage-build-in-fusion)에 나와 있습니다.

## Fusion에서 스테이지 빌드 테스트

게시 전에 Fusion 내에 스테이징 배포를 보려면 이 흐름을 사용하십시오.

### 1단계: 스테이지 작업 영역 선택

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### 2단계: 빌드

```sh
aio app build
```

이렇게 하면 프런트 엔드가 컴파일되고 메타데이터 후크가 실행되며 `app-metadata.json`이(가) 생성됩니다. 계속하기 전에 보고된 오류를 모두 수정하십시오.

### 3단계: 배포

```sh
aio app deploy
```

`deploy`은(는) 다음 두 가지 작업을 수행합니다.

* `https://<project>-stage.adobeio-static.net`과(와) 같은 URL에서 Adobe의 컨텐츠 전달 네트워크에서 **UI를 호스팅**&#x200B;합니다. 완료되면 CLI가 이 **확장 끝점 URL**&#x200B;을 인쇄합니다. iframe에 로드되는 URL Fusion입니다.
* **확장 끝점을 등록합니다** 확장 지점(`fusion/nav-organization/1`)에 대한 끝점을 스테이지 작업 영역에 등록합니다.

>[!TIP]
>
> **배포가 실패하고 &quot;확장 지점 &#39;fusion/nav-organization/1&#39;이 존재하지 않음&quot;(오류 1060):** 조직에 대해 Fusion 확장 지점이 아직 활성화되지 않았습니다. 이는 온보딩 단계이며 코드의 실수는 아닙니다.
>자세한 내용은 문제 해결 문서에서 [확장 지점이 존재하지 않습니다](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md#error-1060-extension-point-does-not-exist)를 참조하십시오.

### 4단계: Fusion 프로필에서 스테이지 테스트 켜기

Fusion은 사용자가 옵트인할 때만 사용자별로 스테이지 확장을 로드합니다.

1. 배포한 **동일한 조직**&#x200B;의 계정으로 Fusion에 로그인합니다.
1. 상단 모서리에서 사용자 아바타 메뉴를 열고 **제품 설정** > **Fusion 프로필** > **환경 설정**(으)로 이동합니다.
1. **단계 확장** 스위치를 켭니다.

   Fusion을 다시 로드하라는 메시지가 표시됩니다.
1. 다시 로드를 확인합니다.

다시 로드한 후 Fusion은 게시된 집합 대신 Stage 작업 영역에서 확장을 로드하고 탐색에서 각 **(Stage)**&#x200B;에 레이블을 지정하여 구분합니다.

이 스위치는 브라우저에 저장된 개인 테스트 설정이며 조직 설정이 아닙니다. 게시된 확장으로 돌아가려면 이 기능을 끄고(및 다시 로드하십시오). 로컬에 저장되므로 다른 브라우저나 시스템으로 이동하지 않습니다.

### 5단계: Fusion에서 확인

1. 확장 포인트와 일치하는 섹션을 엽니다.
   * `fusion/nav-organization/1`이(가) 왼쪽 탐색 영역에 있는 **조직** 영역을 →.
   * `fusion/nav-team/1`이(가) **팀** 영역을 →(먼저 팀을 선택).

   `getWidget()`에 설정한 제목이 포함된 단추가 **(단계)**&#x200B;로 표시되어 나타납니다.
1. 표시된 버튼을 클릭합니다.

UI가 [Fusion 컨텍스트](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)를 로드하고 받습니다.

단추가 나타나지 않거나 패널에 오류가 표시되면 [문제 해결](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)을 참조하십시오.

## 프로덕션 릴리스

확장이 스테이지에서 작동하며 모든 사용자에 대해 준비가 되면 다음 작업을 수행하십시오.

### 1단계: 프로덕션 작업 공간으로 전환

```sh
aio console workspace select       # choose Production
```

CLI에서 `.env` 파일에 대한 프롬프트가 표시되면 **병합**&#x200B;을 선택하여 환경 변수를 유지합니다.

### 2단계: 프로덕션에 빌드 및 배포

```sh
aio app build
aio app deploy
```

### 3단계: 승인 요청 실행

게시는 **프로덕션 작업 영역에서 제출된 승인 요청입니다**:

1. [Adobe Developer Console](https://developer.adobe.com/console)을(를) 열고 **조직**&#x200B;을(를) 선택하고 **프로젝트**&#x200B;을(를) 열고 **프로덕션** 작업 영역으로 전환합니다.
1. **승인/게시**&#x200B;를 위해 앱을 제출하세요. **시스템 관리자** 역할이 필요합니다.
1. 승인 후 확장이 **Adobe 앱 레지스트리**&#x200B;에 추가되고, 귀사에서 Fusion을 포함하여 [Adobe Experience Cloud](https://experience.adobe.com)에서 사용할 수 있게 됩니다.

자세한 지침은 Adobe Developer 설명서의 [UI 확장 관리](https://developer.adobe.com/uix/docs/guides/publication/)를 참조하십시오.

## 상태 및 업데이트

몇 가지 행동은 알고 있어야 할 가치가 있으므로 &quot;무언가 잘못되었음&quot;과는 별개로 &quot;아직 작업 중&quot;이라고 말할 수 있습니다.

* 프로덕션에 배포된 **이(가) 표시되는 것과 동일하지 않습니다.** 프로덕션에 `aio app deploy`이(가) 앱을 업로드하지만 확장이 나타나지 않습니다. 승인 요청이 제출되고 승인된 후에만 나타납니다. 프로덕션에 배포했지만 Fusion에서 표시되지 않는 경우 일반적인 이유는 아직 승인되지 않았기 때문입니다.
* **코드 전용 업데이트는 새 승인이 필요하지 않습니다.** 확장이 이미 게시되어 있고 코드(UI 또는 런타임 작업)만 변경한 경우 다음을 사용하여 동일한 URL에 재배포합니다.

  ```sh
  aio app deploy --force-deploy
  ```

  사용자가 다음에 확장을 열 때 새 버전을 받습니다. 설치할 항목이 없습니다. **등록** 자체를 변경하는 경우(예: 새 확장 지점을 추가하거나 `getWidget()`에서 광고하는 내용을 변경하는 경우)에만 새 승인 요청을 제출하면 됩니다.
* **해지되거나 철회된 확장이 사라집니다.** 사용자가 확장을 취소하거나 취소하면 오류 메시지가 표시되지 않고 Fusion에서 확장이 표시되지 않습니다. 이전에 작동하던 확장이 모든 사람에게 사라지는 경우 코드 문제를 검색하기 전에 해지되었는지 확인하십시오.

## 확장 제거(취소)

게시된 확장을 제거하는 작업은 Adobe Exchange에서 **취소**&#x200B;하면 수행됩니다.

1. **Adobe Exchange**&#x200B;에 로그인합니다.
1. **관리** > **App Builder 앱**(으)로 이동합니다.
1. 제거할 확장 옆의 **취소**&#x200B;를 선택하고 확인합니다.

취소 후 확장은 Extension Manager에 *취소됨* 상태를 표시하며 더 이상 Fusion에 나타나지 않습니다. 완전히 제거하려면 Developer Console에서 프로젝트를 삭제합니다. 확장이 취소될 때까지 프로젝트를 삭제할 수 없습니다.

스테이지 전용 테스트 배포의 경우 다음을 사용하여 배포를 제거할 수 있습니다.

```sh
aio app undeploy
```

## 추가 리소스

Adobe 설명서에서 사용할 수 있는 리소스는 다음과 같습니다.

* [UI 확장 개발 흐름](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [UI 확장 관리(게시/승인/취소)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Developer Console에서 프로젝트 만들기](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
* [액세스 권한을 받는 방법(역할)](https://developer.adobe.com/uix/docs/guides/get-access/)
* [UI 확장의 로컬 미리보기](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)
