---
title: 조직의 성과 대시보드 보기
description: Fusion 관리자는 조직의 실행 지표를 표시하는 대시보드를 볼 수 있습니다.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: 85b7a5e07ef7d3169b31f91bc54d4cb246199443
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 9%

---

# 조직의 성과 대시보드 보기

Fusion Performance Dashboard를 사용하면 가장 많이 실행되고 있는 시나리오, 지연이 발생하는 위치 및 작업자 풀이 얼마나 효과적으로 작동하는지 빠르게 확인할 수 있습니다. 따라서 실행 볼륨, 대기열 길이, 풀 활용도 및 시나리오 수준의 성능을 실시간으로 파악할 수 있습니다.

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

## 성능 대시보드 구성 요소

>[!NOTE]
>
>지표는 작업자 풀별로 표시됩니다. 다른 작업자 풀을 보려면 대시보드의 왼쪽 상단 모서리 근처에 있는 풀 필드를 클릭한 다음 지표를 볼 풀을 선택합니다.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Fusion 성능 대시보드에서 다음 지표를 볼 수 있습니다.

* 실행 처리 대기 중
이 차트는 특정 시점에 처리 대기 중인 실행 수를 보여 줍니다.
* 풀 사용률
이 차트는 시간 경과에 따른 작업자 풀 사용률을 보여 줍니다. 이 차트가 정기적으로 작업자 풀 사용률을 표시하는 경우 일부 시나리오를 다른 풀에 할당할 수 있습니다.
* 시나리오별 실행
이 차트는 시나리오별 실행을 표시합니다. 서로 다른 색상은 서로 다른 시나리오를 나타냅니다. 차트 위에 마우스를 가져다 대면 어떤 색상이 어떤 시나리오인지 보여주는 창이 나타납니다.
* 실행 기간
이 차트는 시나리오별 실행을 표시합니다. 서로 다른 색상은 서로 다른 시나리오를 나타냅니다. 차트 위에 마우스를 가져다 대면 어떤 색상이 어떤 시나리오인지 보여주는 창이 나타납니다.

## Fusion 성능 대시보드 보기

1. Fusion에서 왼쪽 탐색 메뉴의 성능 을 클릭합니다.

   대시보드가 열립니다.

1. 특정 시점에 대한 데이터를 보려면 대시보드 위로 마우스를 가져간 후 보려는 시점 위로 커서를 조정하십시오.

   모든 그래프에서 해당 시간 동안 선이 나타나고 각 그래프에 해당 시간 동안의 데이터를 보여주는 창이 나타납니다.
1. 시나리오 별 실행 차트 또는 실행 기간 차트에서 특정 시나리오에 대한 데이터를 보려면 데이터를 보려는 시나리오 색상 막대를 누릅니다. 모든 시나리오를 보여주는 보기로 돌아가려면 다시 그래프를 클릭합니다.
1. [시나리오별 실행] 차트 또는 [실행 기간] 차트에 표시된 특정 시나리오로 이동하려면 해당 시나리오의 색상 막대를 마우스 오른쪽 단추로 클릭하고 **새 탭에서 시나리오 열기**&#x200B;를 선택합니다.
1. 차트를 확장하려면 해당 차트의 오른쪽 위 모서리에 있는 **확장** 아이콘 ![확장 아이콘](assets/expand-icon.png)을 클릭하십시오.
1. 대시보드의 시간 범위를 변경하려면 대시보드의 오른쪽 위 모서리에 있는 시간 범위 필드를 선택한 다음 새 시간대를 선택합니다. 이용 가능한 가장 긴 시간대는 24시간이며, 가장 짧은 시간대는 15분이다.
1. 차트를 새로 고치려면 대시보드의 오른쪽 상단 근처에 있는 새로 고침 아이콘을 클릭합니다.
1. 다른 작업자 풀을 보려면 대시보드의 왼쪽 상단 모서리 근처에 있는 풀 필드를 클릭한 다음 보려는 풀을 선택하십시오.



