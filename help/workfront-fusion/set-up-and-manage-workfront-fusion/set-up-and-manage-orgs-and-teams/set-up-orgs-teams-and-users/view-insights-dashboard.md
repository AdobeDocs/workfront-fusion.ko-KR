---
title: 조직에 대한 인사이트 대시보드 보기
description: Fusion 관리자는 조직의 실행 지표를 표시하는 대시보드를 볼 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: 'https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 45c755a2f6152b6e230864e4c840d0334705bd22
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 2%
---
# 조직에 대한 인사이트 대시보드 보기

Fusion Insights 대시보드를 사용하면 가장 많이 실행 중인 시나리오, 지연이 발생하는 위치 및 작업자 풀이 얼마나 효과적으로 작동하는지 빠르게 확인할 수 있습니다. 따라서 실행 볼륨, 대기열 길이, 풀 활용도 및 시나리오 수준의 성능을 실시간으로 파악할 수 있습니다.

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>Adobe Workfront Workflow Ultimate 및 Adobe Workfront 자동화 및 통합 Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>표준</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성</td> 
   <td> 
     <p>조직의 Workfront Fusion 관리자여야 합니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 인사이트 대시보드 구성 요소

>[!NOTE]
>
>지표는 작업자 풀별로 표시됩니다. 다른 작업자 풀을 보려면 대시보드의 왼쪽 상단 모서리 근처에 있는 풀 필드를 클릭한 다음 지표를 볼 풀을 선택합니다.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Fusion Insights 대시보드에서 다음 지표를 볼 수 있습니다.

* **실패한 실행 로그**
이 표에는 조직 전체의 실패한 시나리오 실행이나 경고 시나리오가 모두 나열되므로 대시보드를 종료하지 않고도 문제 실행을 찾아 해결할 수 있습니다.
* **조직 작업**
이 차트를 통해 조직에서 사용한 작업 수를 볼 수 있습니다. 특정 팀이나 시나리오를 선택하고 지난 주, 월 또는 연도의 작업을 볼 수 있습니다.
* 작업별 **주요 시나리오**
이 차트를 통해 가장 많은 작업을 사용하는 시나리오를 볼 수 있습니다. 특정 팀을 선택하거나 마지막 일, 주 또는 월의 데이터를 볼 수 있습니다.

<!--

* **Executions waiting to be processed**
   This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time. 

   A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

   If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify which scenarios may be causing an execution backlog or high worker pool utilization. 
* **Duration of executions**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify scenarios that are taking longer than usual, including those affected by issues with a connected app or service.

-->

## Fusion Insights 대시보드 보기

1. Fusion의 왼쪽 탐색 메뉴에서 **인사이트**&#x200B;를 클릭합니다.

   대시보드가 열립니다.

1. 특정 시점에 대한 데이터를 보려면 대시보드 위로 마우스를 가져간 후 보려는 시점 위로 커서를 조정하십시오.

   모든 그래프에서 해당 시간 동안 선이 나타나고 각 그래프에 해당 시간 동안의 데이터를 보여주는 창이 나타납니다.
1. 시나리오 별 실행 차트 또는 실행 기간 차트에서 특정 시나리오에 대한 데이터를 보려면 데이터를 보려는 시나리오 색상 막대를 누릅니다. 모든 시나리오를 보여주는 보기로 돌아가려면 다시 그래프를 클릭합니다.
1. [시나리오별 실행] 차트 또는 [실행 기간] 차트에 표시된 특정 시나리오로 이동하려면 해당 시나리오의 색상 막대를 마우스 오른쪽 단추로 클릭하고 **새 탭에서 시나리오 열기**&#x200B;를 선택합니다.
1. 차트를 확장하려면 해당 차트의 오른쪽 위 모서리에 있는 **확장** 아이콘 ![확장 아이콘](assets/expand-icon.png)을 클릭하십시오.
1. 대시보드의 시간 범위를 변경하려면 대시보드의 오른쪽 위 모서리에 있는 시간 범위 필드를 선택한 다음 새 시간대를 선택합니다. 이용 가능한 가장 긴 시간대는 24시간이며, 가장 짧은 시간대는 15분이다.
1. 차트를 새로 고치려면 대시보드의 오른쪽 상단 근처에 있는 새로 고침 아이콘을 클릭합니다.
1. 다른 작업자 풀을 보려면 대시보드의 왼쪽 상단 모서리 근처에 있는 풀 필드를 클릭한 다음 보려는 풀을 선택하십시오.

## Insights 대시보드 사용자 지정

Insights 대시보드에 표시될 위젯과 순서를 선택할 수 있습니다.

### 위젯 추가, 제거 또는 순서 바꾸기

1. 왼쪽 탐색에서 **인사이트** ![인사이트 아이콘](assets/insights-icon.png)을 클릭합니다.
1. Insights 헤더에서 **[!UICONTROL 사용자 지정]**&#x200B;을 클릭합니다.

   사이드 패널이 열립니다. 모든 위젯이 미리보기, 위젯 이름 및 설명을 표시하는 카드로 나열됩니다.

1. 위젯을 표시하거나 숨기려면 해당 카드를 클릭하거나 카드의 **[!UICONTROL 위젯 추가]** 또는 **[!UICONTROL 위젯 제거]** 단추를 클릭합니다.

   표시되는 위젯에는 확인 표시가 있습니다.
1. 위젯의 순서를 조정하려면 위젯 카드를 패널의 새 위치로 드래그합니다.

   파선 자리 표시자와 드롭 막대는 카드가 도착할 위치를 보여 줍니다.

선택한 항목은 브라우저별로 저장됩니다. 이후 릴리스에 추가된 위젯은 패널에 자동으로 표시됩니다.

위젯을 모두 제거하면 페이지에 &quot;이 페이지에 위젯 없음&quot; 메시지가 표시됩니다.

## Insights 대시보드 새로 고침

모든 위젯의 데이터를 다시 로드하려면 **[!UICONTROL 사용자 지정]** 옆에 있는 **[!UICONTROL 새로 고침]**&#x200B;을 클릭하세요.

* 각 위젯은 필터를 유지합니다.
* **[!UICONTROL 새로 고침]** 단추는 모든 위젯 로드가 완료될 때까지 보류 상태를 표시합니다.
* 차트는 이전 차트를 로드 회전자에 보관하며, 실행 로그는 데이터가 다시 로드되는 동안 회전자에 있는 테이블을 흐리게 합니다.
* 새로 고침이 실패하면 위젯은 마지막 좋은 데이터를 유지합니다.

## Insights 둘러보기

인사이트 대시보드를 처음 열면 시작 대화 상자가 투어를 시작하거나 건너뛸 수 있는 옵션을 제공합니다.

둘러보기는 저장된 순서대로 각 위젯을 강조 표시하고, 제목 표시줄의 **[!UICONTROL 사용자 지정]** 단추 및 패널, **[!UICONTROL 새로 고침]** 단추 및 **[!UICONTROL 둘러보기 재생]** 단추를 강조 표시합니다.

언제든지 투어를 다시 시작하려면 제목 표시줄에서 투어 정보 아이콘 ![정보 아이콘](assets/insights-tour-information.png)을 클릭하세요.

시나리오의 링크에서 인사이트 대시보드를 열면 둘러보기가 시작되지 않습니다. 자세한 내용은 이 문서에서 [시나리오에서 인사이트 대시보드 열기](#open-the-insights-dashboard-from-a-scenario)를 참조하십시오.

## ID로 시나리오 및 팀 검색

**[!UICONTROL 조직 작업]** 및 **[!UICONTROL 작업별 상위 시나리오]** 위젯에서 **[!UICONTROL 시나리오]** 및 **[!UICONTROL 팀]** 필드가 ID와 이름에서 일치합니다. 각 옵션은 &quot;ID 123&quot;과 같은 이름 아래에 ID를 표시합니다.

* 이 목록은 처음 500개의 시나리오와 처음 200개의 팀을 로드합니다. 로드된 목록에 없는 ID를 입력하면 잠시 후에 자동으로 검색됩니다.
* 시나리오를 지우면 해당 시나리오에 대해 자동으로 채워진 팀도 지워집니다.

>[!NOTE]
>
>실행 로그의 시나리오 필터가 ID에서 일치하지 않습니다.

## 시나리오에서 Insights 대시보드 열기

특정 시나리오 및 팀으로 필터링된 **[!UICONTROL 조직 작업]** 위젯으로 인사이트 대시보드를 열 수 있습니다.

시나리오에서 Insights 페이지로 이동하려면 다음을 수행하십시오.

1. 시나리오 세부 사항 페이지를 엽니다.

   1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭한 다음 자세히 설명하려는 시나리오를 클릭합니다.

      또는

      시나리오 편집기에서 시나리오 작업을 수행하는 경우 창의 왼쪽 상단 모서리 근처에 있는 왼쪽 화살표 ![편집 종료 화살표](assets/exit-editing-arrow.png)를 클릭합니다.
      1. 페이지 상단 근처에 있는 **보고서** 탭을 클릭합니다.

* **[!UICONTROL 조직 작업]** 위젯이 해당 시나리오와 팀으로 필터링되어 열리고 페이지가 위젯으로 스크롤됩니다.
* 페이지에서 위젯을 제거한 경우 대신 **[!UICONTROL 위젯 추가]** 단추가 포함된 경고가 나타납니다.

## 다크 모드 사용

Insights 대시보드 및 해당 위젯은 자동으로 다크 모드 설정을 따릅니다. 설정을 변경하면 다시 로드하지 않고 페이지가 즉시 업데이트되며 현재 상태를 유지합니다. 조명 모드는 변경되지 않습니다.

## 성능 위젯 액세스

**[!UICONTROL 성능]** 위젯은 다음 권한 중 하나가 있는 사용자에게만 표시됩니다.

* 활성 조직의 조직 편집
* 관리 페이지의 조직 보기

위젯이 페이지 및 다른 사용자의 **[!UICONTROL 사용자 지정]** 패널에서 숨겨져 있습니다. 나중에 사용자에게 액세스 권한이 부여되면 위젯은 저장된 위치로 돌아갑니다. 인사이트 URL을 직접 열어도 이 확인이 무시되지 않습니다.

## 실행 로그에서 실행 필터링 및 분류

실행 로그를 사용하여 조직 전체에서 실패하거나 경고를 반환하는 시나리오 실행을 찾고, 반복 실패 후 자동으로 비활성화되는 시나리오를 다시 활성화합니다.

1. 실행 로그에서 다음 중 하나를 기준으로 실행을 필터링합니다.

   * [!UICONTROL 팀]
   * [!UICONTROL 시나리오]
   * [!UICONTROL 실행 형식]
   * [!UICONTROL 날짜 범위]
   * [!UICONTROL 비활성화 상태]
   * [!UICONTROL 오류 메시지]

   대부분의 필터에서 선택한 값만 일치시키거나 해당 값을 제외한 모든 값을 일치시키도록 선택할 수 있습니다.

1. 오류에 대한 자세한 내용을 보려면 실행을 클릭하십시오.
1. 반복 실패 후 자동으로 비활성화되는 하나 이상의 시나리오를 다시 활성화하려면 실행을 선택한 다음 **활성화**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >시나리오를 다시 활성화하기 전에 만료된 자격 증명 또는 커넥터 문제와 같은 실패의 원인을 조사하십시오. 그러면 시나리오가 즉시 다시 실패하지 않습니다.
