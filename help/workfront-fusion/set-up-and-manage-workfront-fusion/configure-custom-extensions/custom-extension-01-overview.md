---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: UI 확장성 개요
description: Workfront Fusion의 사용자 지정 확장
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
source-wordcount: 835
ht-degree: 0%

---

# UI 확장성 개요

UI 확장성을 사용하면 사용자 지정 논리 및 UI(사용자 인터페이스)를 Adobe Workfront Fusion으로 가져올 수 있습니다. Adobe App Builder을 사용하면 Fusion의 핵심 기능에 계속 의존하면서 조직의 요구 사항을 보다 잘 충족하도록 조직의 Workfront Fusion 환경을 수정할 수 있습니다.

이 문서에서는 UI 확장성 및 사용자 지정 확장이 Workfront Fusion과 통신하는 방법에 대한 개요를 제공합니다.

## 확장 구조

* [호스트 및 게스트](#hosts-and-guests)
* [그 아래의 기술](#the-technology-underneath)

### 호스트 및 게스트

Fusion은 Workfront Fusion 팀이 만들지 않은 UI를 표시할 수 있습니다. 이러한 UI 변경 사항이 Fusion의 핵심 기능에 영향을 주지 않도록 UI는 Fusion의 코드와 완전히 별개인 자체 격리된 브라우저 프레임(`<iframe>`)에서 실행됩니다.

* **호스트**: *확장에 포함된* 응용 프로그램입니다. **Fusion**&#x200B;입니다. 호스트는 확장을 표시할 수 있는 위치와 확장과 공유할 데이터를 결정합니다.
* **게스트**: *사용자* 확장. 호스트가 iframe에 로드하는 작은 웹 애플리케이션입니다.

UI 확장을 만들 때 Fusion을 수정하지 않습니다. 게스트가 게시된 후 Fusion에서 사용할 수 있는 게스트를 빌드하고 게시합니다.

### 그 아래의 기술

게스트는 두 가지 Adobe 기술을 사용하여 구축됩니다.

* **Adobe App Builder**: 소규모 웹 앱 및 서버를 사용하지 않는 작업을 위한 무료 호스팅 및 도구 플랫폼입니다. 확장 프로그램은 App Builder 앱입니다. App Builder에서는 UI(Adobe의 `*.adobeio-static.net` 콘텐츠 전달 네트워크)와 명령줄 도구 `aio`을(를) 호스팅하여 만들고 빌드하고 게시할 수 있는 위치를 제공합니다.
* **Adobe UI 확장성 SDK(UIX)**: 호스트와 게스트가 대화할 수 있도록 해주는 라이브러리입니다. 한 개의 패키지 `@adobe/uix-guest`을(를) 사용할 수 있습니다. Fusion은 해당 측면에서 일치하는 `@adobe/uix-host` 패키지를 사용합니다.

<!--

```
   ┌────────── Browser ─────────────────────────────┐
   │                                                                   │
   │   Fusion (Host)                      Your extension (Guest)       │
   │   ────────────                       ─────────────────────        │
   │   @adobe/uix-host   ◀── messages ──▶  @adobe/uix-guest            │
   │        │                                    │                     │
   │   renders an iframe ───────────────▶  your React/HTML UI          │
   │                                                                   │
   └───────────────────────────────────────────────────────────────────┘

   Your UI files are hosted by Adobe App Builder at
   https://<your-app>.adobeio-static.net
```

-->

## 확장 지점

확장 지점은 게스트가 나타날 수 있는 호스트에서 이름이 &quot;슬롯&quot;입니다. Fusion은 해당 슬롯을 정의하며 게스트가 사용할 슬롯을 선택합니다.

확장 지점 이름에 다음 세 부분이 있습니다. `service/name/version`.

Fusion은 다음 확장 지점을 제공합니다.

| 확장 지점 | Fusion에서 UI가 표시되는 위치 | 사용 시기 |
| --- | --- | ---- |
| `fusion/nav-organization/1` | 왼쪽 탐색 메뉴의 **조직** 섹션 아래에서 | 도구는 조직 전체에 대한 것입니다. |
| `fusion/nav-team/1` | 왼쪽 탐색 메뉴의 **팀** 섹션 아래(팀을 선택하면 표시됨). | 도구는 특정 팀에 대한 것입니다. |

* `fusion`은(는) **서비스**(제품, Fusion)입니다.
* `nav-organization` / `nav-team`은(는) **이름**(특정 슬롯)입니다.
* `1`은(는) **버전**&#x200B;입니다.

하나의 확장은 하나 또는 두 확장 지점을 모두 구현할 수 있습니다. 대부분의 확장은 한 지점을 사용합니다.

선택한 확장 지점에 따라 확장 제목이 있는 단추가 일치하는 탐색 섹션에 추가됩니다. 이 아이콘을 클릭하면 Fusion의 기본 콘텐츠 영역에서 전용 페이지가 열리고 해당 영역에 UI가 로드됩니다.

## UI 확장에 포함된 프레임

>[!IMPORTANT]
>
>이 섹션에서는 혼동을 일으킬 수 있는 UI 확장의 측면에 대해 설명합니다. 우리는 그것을 주의 깊게 읽는 것을 추천한다.

Fusion에서 게스트가 로드되면 확장이 **2** 프레임에서 실행됩니다.

1. **등록 프레임(보이지 않음)입니다.** 백그라운드에서 먼저 실행됩니다. 등록 프레임은 확장이 제공하는 내용을 Fusion에 알려줍니다. 예를 들어, 대시보드 위젯이 있음을 나타내고, 위젯의 제목과 해당 UI의 URL을 전송할 수 있습니다. 등록 프레임은 `register(...)`을(를) 호출하여 이를 수행합니다. 표시되는 UI가 렌더링되지 않습니다.
1. **UI 프레임(표시)입니다.** Fusion이 사용자에게 표시하는 페이지입니다. `attach(...)`을(를) 호출하여 호스트에 알립니다. `attach`을(를) 호출하지 않으면 Fusion이 대기했다가 결국 시간 초과되고 오류가 발생합니다.

>[!BEGINSHADEBOX]

이 예에서는 사용자가 확장 버튼을 클릭할 때의 흐름을 보여 줍니다.

1. 버튼을 클릭합니다.
1. Fusion은 등록 프레임을 로드합니다(숨겨짐).

   ```
   register({ methods: { dashboard: { getWidget() {...} } } })
   ```

   `getWidget()`이(가) 표시되는 UI의 URL을 반환합니다.
1. Fusion은 해당 URL에서 UI 프레임(표시)을 로드합니다.

   ```
   attach({ id }) 
   ```

   이 작업이 필요합니다. 그렇지 않으면 Fusion 시간이 초과됩니다.
1. Fusion은 컨텍스트를 전송하고 UI는 렌더링됩니다.

>[!ENDSHADEBOX]

두 프레임 모두 UI를 빌드할 때 작성됩니다. 중요한 것은 표시되는 페이지 **은(는) `attach`을(를) 호출해야 합니다**.

UI 빌드에 대한 자세한 내용은 [사용자 지정 확장 UI 빌드](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)를 참조하십시오.

## Fusion의 컨텍스트

확장을 연결하면 Fusion은 게스트와 `context` 개체를 공유합니다. 이 파일에는 다음이 포함되어 있습니다.

* **사용자**: 로그인한 사용자의 Fusion 프로필과 Adobe IMS 사용자 ID입니다.
* **조직**: 활성 조직의 전체 Fusion 조직 레코드 및 Adobe IMS 조직 ID입니다.
* **팀**: 해당되는 경우 활성 팀입니다.
* **Adobe IMS 액세스 토큰**: 필요한 경우 사용자를 대신하여 Adobe 또는 Fusion API를 호출합니다.

Fusion은 업데이트도 푸시합니다. 예를 들어 UI가 열려 있는 동안 사용자가 조직 또는 팀을 전환하면 Fusion은 새 컨텍스트를 전송하여 UI가 즉시 반응할 수 있도록 합니다.

전체 컨텍스트 필드 목록은 [Fusion 컨텍스트 참조](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)를 참조하십시오.

## UI 확장 만들기

UI 확장을 만들려면 다음 단계를 수행합니다.

1. [도구를 설치하고 Adobe 프로젝트를 만듭니다](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
1. [빈 App Builder 프로젝트를 생성하여 Fusion 확장 지점을 가리킨 다음 위젯을 등록합니다](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).
1. [UI를 빌드하고 Fusion에 연결](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
1. [Fusion 전송 컨텍스트를 사용](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)합니다.
1. [Fusion에서 찾을 수 있도록 게시](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. (선택 사항) [CORS가 없는 실제 데이터에 대해 Workfront/Fusion API를 호출합니다](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).

프로세스를 시작하려면 [도구 및 Adobe 계정 설정](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)(으)로 이동합니다.


