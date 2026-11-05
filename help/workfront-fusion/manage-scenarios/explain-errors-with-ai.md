---
title: AI로 시나리오 오류 설명
description: 시나리오 실행이 실패하면 오류 옆에 있는 설명 을 클릭하여 무엇이 잘못되었는지, 그리고 이를 수정하는 방법에 대한 간단한 일반 언어 설명을 얻을 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 565302f1d994819607051014d18779ccfb2645cb
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 15%
---
# AI로 시나리오 오류 설명

시나리오 실행에 실패하면 AI가 잘못된 사항과 이를 수정하는 방법에 대한 간단한 언어 설명을 제공할 수 있습니다. 원래 오류 옆에 설명이 표시되므로 두 가지를 함께 읽을 수 있습니다.

Workfront Fusion의 다음 영역에서 오류를 설명할 수 있습니다.

* 시나리오 디자이너의 모듈 오류 세부 정보
* 시나리오 실행 내역의 실행 세부 정보
* 인사이트 페이지의 [!UICONTROL 실패한 실행 로그] 테이블

>[!NOTE]
>
>**[!UICONTROL 설명]** 단추는 새 시나리오 디자이너에서만 사용할 수 있습니다. 기존 시나리오 디자이너에서는 사용할 수 없습니다.
>
>이 기능을 사용하려면 조직에 AI 라이선스가 있어야 합니다.

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>모든 Adobe Workfront 워크플로 패키지 및 모든 Adobe Workfront 자동화 및 통합 패키지</p><p>Workfront Ultimate</p><p>Workfront Prime 및 Select 패키지 및 Workfront Fusion 추가 구매.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>표준</p><p>작업 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 모듈 출력 세부 정보의 오류 설명

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 오류를 설명할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 예약된 대로 또는 **한 번 실행**&#x200B;을 클릭하여 시나리오를 실행합니다.
1. 모듈이 실패하면 모듈의 오류 세부 정보를 엽니다.
1. **[!UICONTROL 설명]**&#x200B;을 클릭합니다.

   버튼에 오류가 있습니다.

   ![모듈 출력의 오류 설명](assets/explain-in-module-output.png)

설명은 오류 아래에 나타납니다.

>[!NOTE]
>
> * AI가 설명을 생성하는 동안 로딩 상태가 나타납니다.
> * 설명이 생성되지 않으면 **[!UICONTROL 다시 시도]**&#x200B;를 클릭하십시오.
> * 조직이 AI 사용 제한에 도달하면 설명 대신 사용 제한 메시지가 표시됩니다.

## 시나리오 실행 내역의 오류 설명

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭한 다음 시나리오를 클릭합니다.
1. 시나리오 이름 근처에 있는 **[!UICONTROL 기록]**&#x200B;을 클릭합니다.
1. 보려는 실패한 실행을 클릭합니다.

   실행 세부 정보에 있는 각 오류 아래에는 **[!UICONTROL 설명]** 단추가 있습니다.

1. 설명하려는 오류 아래에 있는 **[!UICONTROL 설명]**&#x200B;을 클릭합니다.

   여러 모듈이 실행에서 실패한 경우 각 오류를 자체적으로 설명할 수 있습니다.

   ![실행 기록에서 설명](assets/explain-in-execution-details.png)

실행 보기에 대한 자세한 내용은 [시나리오의 실행 기록 보기](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md) 및 [특정 시나리오 실행 보기](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md)를 참조하십시오.

>[!NOTE]
>
> * AI가 설명을 생성하는 동안 로딩 상태가 나타납니다.
> * 설명이 생성되지 않으면 **[!UICONTROL 다시 시도]**&#x200B;를 클릭하십시오.
> * 조직이 AI 사용 제한에 도달하면 설명 대신 사용 제한 메시지가 표시됩니다.

## 인사이트 페이지의 오류 설명

1. Fusion의 왼쪽 탐색 메뉴에서 **[!UICONTROL 인사이트]**&#x200B;를 클릭합니다.
1. [!UICONTROL 실패한 실행] 테이블에서 보려는 실패한 행을 마우스로 가리킵니다.

   **[!UICONTROL 설명]** 단추가 나타납니다.

1. **[!UICONTROL 설명]**&#x200B;을 클릭합니다.

   ![인사이트 페이지에서 설명](assets/explain-failed-execution-log.png)

   오류와 AI 설명을 표시하는 팝업이 열립니다.

Insights 페이지에 대한 자세한 내용은 [조직의 Insights 대시보드 보기](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/view-insights-dashboard.md)를 참조하십시오.

>[!NOTE]
>
> * AI가 설명을 생성하는 동안 로딩 상태가 나타납니다.
> * 설명이 생성되지 않으면 **[!UICONTROL 다시 시도]**&#x200B;를 클릭하십시오.
> * 조직이 AI 사용 제한에 도달하면 설명 대신 사용 제한 메시지가 표시됩니다.
