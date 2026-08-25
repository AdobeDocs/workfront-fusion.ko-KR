---
title: 모듈을 체인으로 이동
description: 매핑이나 데이터 구조를 수동으로 다시 만들지 않고도 시나리오에서 모듈 그룹을 선택하고 새 체인 시나리오로 이동할 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: f1a80f64edc410ae76bfbba1280df7232e2d09c5
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 17%

---

# 모듈을 체인으로 이동

>[!IMPORTANT]
>
>이 기능은 Beta에 있으며 미션 크리티컬 프로덕션 워크플로우에는 권장되지 않습니다. Beta 기능에서는 동작이 변경되고 극단적 사례는 완전히 처리되지 않을 수 있습니다.

매핑이나 데이터 구조를 수동으로 다시 만들지 않고도 시나리오에서 모듈 그룹을 선택하고 새 체인 시나리오로 이동할 수 있습니다. 이렇게 하면 대규모 시나리오를 모듈화할 수 있는 손쉬운 방법이 제공됩니다.

모듈 그룹을 체인으로 이동하면 Workfront Fusion은

* 선택한 모듈을 새로 만든 시나리오로 이동합니다.
* 별도의 브라우저 창에서 새 시나리오를 엽니다.
* 원래 시나리오에서 선택한 모듈을 체인 > 하위 시나리오 모듈 호출로 바꿉니다.
* 새 자식 시나리오에 필요한 입력 및 출력 데이터 구조를 자동으로 만듭니다.
* 기존 시나리오 비헤이비어를 유지하므로 모듈이 이동되기 전과 동일한 방식으로 시나리오가 계속 실행됩니다.
* 매핑을 자동으로 업데이트:
  * 하위 시나리오로 이동한 모듈은 체인 > 상위 모듈의 입력에서 데이터 수신을 통해 데이터를 수신합니다.
  * 하위 시나리오의 출력은 자동으로 상위 시나리오에 다시 노출됩니다.
  * 블루프린트의 기존 매핑이 새 구조와 일치하도록 조정됩니다.

체인 시나리오 계획에 대한 자세한 내용은 [여러 시나리오를 함께 연결](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)을 참조하십시오.

체인 모듈 구성에 대한 지침은 [체인 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)을 참조하십시오.

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

## 전제 조건

체인으로 이동할 모듈은 시나리오에 이미 있어야 하며 둘 이상의 모듈을 선택해야 합니다.

## 제한 사항

다음과 같은 경우에는 모듈 선택을 체인으로 이동할 수 없습니다.

* 선택한 모듈은 끊기지 않은 단일 흐름의 일부가 아닙니다. 예를 들어 연결되지 않은 두 개의 서로 다른 경로에서 모듈을 동시에 선택할 수는 없습니다.
* 선택 항목에는 Webhook 모듈이 포함되어 있습니다.
* 선택 항목에는 다른 체인 모듈이 포함되어 있습니다.
* 선택한 항목에 라우터 모듈이 포함되어 있으며 해당 라우터의 경로를 모두 선택하지 않았습니다.
* 선택한 모듈에 오류 처리기 경로가 있으며 해당 경로도 선택하지 않았습니다.

## 모듈을 체인으로 이동

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 이동할 모듈이 포함된 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. [!UICONTROL Shift]를 누른 채 이동할 모듈을 클릭하여 체인으로 이동할 모듈을 선택합니다.
1. 선택한 모듈 중 하나를 마우스 오른쪽 단추로 클릭합니다.
1. **[!UICONTROL 체인으로 이동]**&#x200B;을 선택합니다.
