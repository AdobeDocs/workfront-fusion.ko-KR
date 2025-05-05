---
title: 시나리오를 만들기 위한 워크플로
description: 시나리오를 만들려면 이 일반 워크플로를 따르십시오.
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: 394f80a2d7c124bbd00e1a5b51ad3dc6e73a996b
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# 시나리오를 만들기 위한 워크플로

시나리오는 사용 사례를 처리하는 애플리케이션 및 모듈을 통해 조직의 요구 사항을 충족하도록 구축됩니다. 그러나 시나리오를 만드는 것은 사용 사례에 관계없이 동일한 기본 워크플로우를 따릅니다. 이 문서에서는 시나리오를 만드는 기본 프로세스에 대해 설명합니다.


* [시나리오 만들기 및 이름 지정](#create-and-name-the-scenario)
* [첫 번째 모듈 추가 및 구성](#configure-the-first-module)
* [연결 만들기](#create-connections)
* [추가 모듈 추가 및 구성](#add-and-configure-additional-modules)
* [모듈 간 데이터 매핑](#map-data-between-modules)
* [라우팅 구성](#configure-routing)
* [오류 처리 구성](#configure-error-handling)
* [시나리오 설정 구성](#onfigure-scenario-settings)
* [테스트 및 개정](#test-and-revise)
* [시나리오 활성화](#activate-the-scenario)
* [Workfront Fusion 시나리오 키보드 단축키](#workfront-fusion-scenario-keyboard-shortcuts)

키보드 단축키



## 시나리오 만들기 및 이름 지정

1. [!DNL Workfront Fusion] 계정에 로그인합니다.
1. 왼쪽 패널에서 **[!UICONTROL Scenarios]** ![시나리오 아이콘](assets/scenarios-icon.png)을 클릭합니다.

   >[!NOTE]
   >
   >왼쪽 탐색 패널이나 해당 아이콘이 보이지 않으면 메뉴 ![메뉴](assets/main-menu-icon-left-nav.png) 아이콘을 클릭합니다.

1. (선택 사항) [!UICONTROL **폴더**] 패널에서 **[!UICONTROL Add folder]** 아이콘 ![폴더 추가 아이콘](assets/add-folder-icon.png)을 클릭한 다음 첫 번째 폴더의 이름을 &quot;연습 시나리오&quot;와 같이 입력합니다.

1. (선택 사항) 폴더를 연 다음 페이지의 오른쪽 상단에 있는 **[!UICONTROL Create a new scenario]**&#x200B;을(를) 클릭합니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL New scenario]** 자리 표시자 이름을 선택한 다음 &quot;연습 시나리오 1&quot;과 같은 이름을 입력하십시오.

   ![시나리오 이름 지정](assets/name-the-scenario.png)

1. 아래의 [첫 번째 모듈에 연결](#2-connect-the-first-module)을 사용하여 계속합니다.

## 첫 번째 모듈 추가 및 구성

시나리오의 첫 번째 모듈은 특정 조건이 충족될 때 시나리오를 시작하는 트리거 모듈입니다.

시나리오에 첫 번째 모듈을 추가하는 방법에 대한 지침은 시나리오에 모듈 추가 문서의 [시나리오에 첫 번째 모듈 추가](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario)를 참조하십시오.

모듈 구성에 대한 지침은 [모듈 구성](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)을 참조하세요.

## 연결 만들기

모듈을 구성할 때는 연결을 입력하거나 만들어야 합니다. 모듈은 이 연결 및 이 연결에 포함된 권한을 사용하여 애플리케이션의 날짜에 액세스합니다.

연결을 만드는 방법에 대한 기본 지침은 [연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

Google, Microsoft 또는 전용 커넥터가 없는 응용 프로그램과 관련된 특정 사용 사례에 대해서는 [응용 프로그램에 연결: 문서 색인](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md)의 다른 문서를 참조하십시오.

## 추가 모듈 추가 및 구성

추가 모듈 추가 및 구성을 계속합니다.

모듈을 추가하는 방법에 대한 지침은 [모듈 추가: 문서 인덱스](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)에 나열된 문서를 참조하십시오.

## 모듈 간 데이터 매핑

이전 모듈의 출력을 후속 모듈에 대한 입력으로 사용할 수 있습니다. 예를 들어 한 모듈에서 Workfront 프로젝트를 만들고 후속 모듈의 해당 모듈에 문서를 업로드할 수 있습니다.

자세한 내용은 [맵 데이터: 문서 인덱스](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md)의 문서를 참조하십시오.

## 라우팅 구성

라우팅을 사용하면 시나리오가 데이터 값을 기반으로 다양한 작업을 수행할 수 있습니다.

자세한 내용은 [라우터 모듈 추가 및 경로 구성](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)을 참조하십시오.

## 오류 처리 구성

오류 처리를 통해 시나리오를 오류에서 복구할 수 있습니다. 시나리오가 다양한 오류 상황에서 어떻게 반응할지 선택할 수 있습니다.

자세한 내용은 [오류 처리 추가](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)를 참조하십시오.

## 시나리오 설정 구성

시나리오 예약, 메모 작성 또는 데이터 저장 방법 결정과 같이 시나리오에 대한 설정을 전체적으로 구성할 수 있습니다.

지침은 [시나리오 설정 구성: 문서 인덱스](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md)의 문서를 참조하십시오.

## 테스트 및 개정

시나리오를 테스트하면 시나리오가 의도한 대로 작동하는지 확인할 수 있습니다. 그런 다음 결과에 따라 시나리오를 수정한 다음 다시 테스트할 수 있습니다.

1. 시나리오 편집기의 왼쪽 아래에서 **[!UICONTROL Run once]**&#x200B;을(를) 클릭합니다.
1. 시나리오 실행이 끝나면 각 모듈 위의 실행 검사기 버블을 클릭하여 정보 입력과 해당 모듈의 출력을 확인합니다.

   * 시나리오 실행 정보를 읽는 방법에 대한 일반 정보는 [시나리오 실행 흐름](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)을 참조하십시오.
   * 처리된 번들에 대한 자세한 내용은  [!DNL Adobe Workfront Fusion][&#128279;](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)의 시나리오 실행, 주기 및 단계를 참조하십시오.

1. [!DNL Workfront Fusion]에서 왼쪽 아래 모서리 근처에 있는 **[!UICONTROL Save]** ![저장 아이콘](assets/save-icon.png)을 클릭하여 시나리오에 대한 진행률을 저장합니다.

   >[!IMPORTANT]
   >
   >원하는 만큼 자주 저장하고 시나리오를 테스트합니다.

## 시나리오 활성화

이 예제 시나리오에는 트리거 모듈이 없습니다. 실제 데이터에 사용하는 시나리오인 경우 트리거 모듈로 시작하고 마지막으로 활성화할 수 있습니다. 시나리오를 활성화하면 기본적으로 15분마다 실행됩니다. 실행할 시기와 빈도를 정의하여 변경할 수 있습니다.

시나리오 활성화에 대한 자세한 내용은 [시나리오 활성화 또는 비활성화](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md)를 참조하십시오.

일정에 대한 자세한 내용은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하십시오.

## Workfront Fusion 시나리오 키보드 단축키

시나리오를 만들거나 편집할 때 다음 키보드 단축키를 사용할 수 있습니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <thead> 
  <tr> 
   <th> <p>액션</p> </th> 
   <th>[!DNL Windows]</th> 
   <th> <p>[!DNL MacOS]</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save] </td> 
   <td>Ctrl+Shift+S</td> 
   <td>Cmd+Shift+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Run Once]</td> 
   <td>Ctrl+Shift+Enter</td> 
   <td>Cmd+Shift+Enter</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Open the DevTool]</td> 
   <td>F12</td> 
   <td>Ctrl+Fn+F12</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select multiple modules]</td> 
   <td>Shift+드래그</td> 
   <td>Shift+드래그</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy]</td> 
   <td>Ctrl+C</td> 
   <td>Cmd+C</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Paste]</td> 
   <td>Ctrl+V</td> 
   <td>Cmd+V</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">시나리오에 cURL을 붙여넣어 HTTP 모듈을 만듭니다.</td> 
   <td colspan="2">cURL을 복사한 다음 시나리오 편집기의 아무 곳에나 붙여넣습니다.<p>자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/add-modules/use-curl-create-http.md">cURL을 사용하여 HTTP 모듈 추가</a>를 참조하십시오.</td> 
  </tr> 
 </tbody> 
</table>





