---
title: 특정 시나리오 실행 다시 트리거
description: 특정 시나리오 실행을 재시도하여 업데이트된 시나리오 블루프린트를 사용하여 데이터를 처리하거나 해당 데이터 흐름을 볼 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 0c732add9c1ec75d7aed43bb7097bb1c95aa6408
workflow-type: tm+mt
source-wordcount: 523
ht-degree: 18%

---

# 특정 시나리오 실행 다시 트리거

특정 시나리오 실행을 재시도하여 업데이트된 시나리오 블루프린트를 사용하여 데이터를 처리하거나 해당 데이터 흐름을 볼 수 있습니다. 실행을 재시도할 때 해당 실행의 데이터를 사용하여 시나리오가 실행됩니다.

예를 들어, 시나리오를 업데이트하여 문제 생성과 같은 작업을 추가하는 경우 업데이트 전에 발생한 실행을 다시 시도할 수 있습니다. 업데이트된 시나리오는 원래 시나리오의 트리거 이벤트를 사용하여 실행되지만, 업데이트된 작업이 포함됩니다. 이 예에서는 시나리오가 새 실행의 일부로 문제를 만듭니다.

Webhook 트리거가 있는 시나리오와 하위 시나리오에 대해 검색을 사용할 수 있습니다.

웹후크를 사용하는 시나리오를 검색할 때 원래 웹후크 이벤트를 다시 사용할 수 있으므로 시나리오를 다시 검색하기 위해 이벤트를 다시 만들 필요가 없습니다.

체인 시나리오를 사용할 때 하위 시나리오에도 검색을 적용할 수 있습니다. 하위 시나리오는 상위 시나리오를 검색하지 않고도 원래 실행에서 상위 시나리오로부터 전송된 데이터를 사용하여 검색할 수 있습니다.

웹후크에 대한 자세한 내용은 [인스턴트 트리거(웹후크)](/help/workfront-fusion/references/modules/webhooks-reference.md)를 참조하십시오.

체인 시나리오에 대한 자세한 내용은 [여러 시나리오를 함께 연결](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)을 참조하십시오.

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

## 실행 다시 트리거

시나리오의 다이어그램, 시나리오의 내역 영역 또는 특정 시나리오 실행의 페이지에서 시나리오 실행을 다시 시도할 수 있습니다.

### 시나리오 다이어그램에서 실행 다시 트리거

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 다시 시도할 실행을 실행한 시나리오를 선택합니다.

   시나리오의 다이어그램이 열립니다.
1. 페이지 오른쪽의 실행 목록에서 재시도할 실행을 찾습니다.
1. 해당 시나리오에 대해 **다시 시도**&#x200B;를 클릭합니다.

![다이어그램에서 검색기](assets/retrigger-from-diagram.png)

### 시나리오 기록에서 실행 다시 트리거

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 다시 시도할 실행을 실행한 시나리오를 선택합니다.

   시나리오의 다이어그램이 열립니다.

1. 시나리오 이름 바로 아래에 있는 **기록** 탭을 클릭합니다.
1. 다시 시도할 실행을 찾습니다. 필요한 경우 전체 텍스트 검색을 사용하여 찾을 수 있습니다.
1. 해당 시나리오에 대해 **다시 시도**&#x200B;를 클릭합니다.

![기록에서 다시 트리거](assets/retrigger-from-history.png)

### 시나리오 실행 페이지에서 시나리오 재트리거

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 다시 시도할 실행을 실행한 시나리오를 선택합니다.

   시나리오의 다이어그램이 열립니다.
1. 페이지 오른쪽의 실행 목록에서 재시도할 실행을 찾습니다.
1. 실행을 클릭하여 엽니다.
1. 실행 페이지에서 **다시 시도**&#x200B;를 클릭합니다.


![실행에서 다시 트리거](assets/retrigger-from-execution.png)






