---
title: 체인 시나리오 관계 보기
description: 상위 시나리오와 하위 시나리오 간의 관계를 매핑할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 0782c6b1-42a5-48de-bfa0-3ced6ed2bf7f
source-git-commit: aee2b35919e240cce5346df6d94a610c34b26e88
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 18%

---

# 체인 시나리오 관계 보기 및 관리

상위 시나리오와 하위 시나리오 간의 관계를 매핑할 수 있습니다. 맵을 사용하여 체인의 다양한 시나리오로 이동할 수도 있습니다.

체인 시나리오에 대한 자세한 내용은 [여러 시나리오를 함께 연결](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)을 참조하십시오.

체인 시나리오 구성에 대한 자세한 내용은 [체인 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)을 참조하세요.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 체인 관계 맵 보기

현재 시나리오와 해당 상위 또는 하위 시나리오의 맵을 볼 수 있습니다. 맵에는 체인 시나리오 전체에 걸쳐 데이터 흐름 다이어그램이 표시됩니다.

![연결된 시나리오 관계](assets/chained-scenario-relationships-2.png)

<!--get a better picture-->

체인 시나리오에 대한 관계 맵을 보려면 다음과 같이 하십시오.

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭한 다음 시나리오를 클릭합니다.

   또는

   시나리오 편집기에서 시나리오 작업을 수행하는 경우 창의 왼쪽 상단 모서리 근처에 있는 왼쪽 화살표 ![편집 종료 화살표](assets/exit-editing-arrow.png)를 클릭합니다.

1. **관계** 탭을 클릭합니다.

   ![관계 탭](assets/relations-tab.png)

1. 각 체인 시나리오에 대한 일반적인 세부 사항은 태그를 확인하십시오.

   각 시나리오에는 다음 태그 중 하나 이상이 있습니다.

   * 루트: 시나리오는 체인의 시작이며 상위 시나리오가 없습니다.
   * 상위: 시나리오는 상위 시나리오입니다.
   * 하위: 시나리오가 하위 시나리오입니다. 시나리오는 상위 및 하위 모두 될 수 있습니다.
   * 현재: 사용자가 현재 보고 있는 시나리오입니다. 즉, 사용자가 관계 맵을 연 시나리오입니다.

   ![관계 맵의 시나리오 태그](assets/chained-scenario-maps-tag.png)
1. (선택 사항) 시나리오의 작은 다이어그램을 보려면 시나리오 위로 마우스를 가져갑니다.
1. (선택 사항) 맵에서 다른 시나리오로 직접 이동하려면 시나리오를 클릭합니다.

   클릭한 시나리오가 다른 창에 열립니다.
1. (선택 사항) 맵의 가로 보기와 세로 보기 간에 전환하려면 시나리오 세부 정보 페이지의 오른쪽 상단 근처에 있는 **가로** 또는 **세로**&#x200B;를 클릭하십시오.
1. (선택 사항) 맵의 간소화된 보기를 보려면 페이지의 오른쪽 아래 모서리를 확인하십시오.

   이는 체인 맵이 크거나 복잡한 경우 편리할 수 있습니다.

   * 맵의 일부만 보는 경우에는 단순화 맵에서 해당 부분이 더 어둡게 표시됩니다.
   * 현재 시나리오는 간소화된 맵에 파란색으로 표시됩니다.
1. 체인에 대한 실행 기록을 보려면 보기 상단의 기록 탭을 클릭합니다.

   히스토리를 클릭하여 연결된 시나리오 간에 전달된 특정 데이터를 볼 수 있습니다.
