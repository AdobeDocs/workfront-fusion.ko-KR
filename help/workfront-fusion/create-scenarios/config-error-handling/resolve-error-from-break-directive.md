---
title: Break 지시문에 의해 처리된 오류 해결
description: 경우에 따라 실패 사유가 빠르게 해결될 가능성이 있는 경우, 실패한 모듈을 다시 실행하는 것이 유용합니다.
author: Becky
feature: Workfront Fusion
exl-id: d568942c-2cd5-430c-bdbf-e1496da25b50
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Break 지시문에 의해 처리된 오류 해결

Break 지시문에 의해 오류가 처리되면 미완료 실행 폴더에 레코드가 생성됩니다. 이 레코드에는 이전 모듈의 데이터와 함께 시나리오 실행 상태가 저장됩니다. 레코드는 오류가 발생한 모듈을 참조하고 모듈에 의해 입력으로 수신된 데이터에 대한 정보를 포함합니다. 오류를 일으키는 각 데이터 번들에 대해 별도의 레코드가 만들어집니다.

자세한 내용은 [불완전한 실행 보기 및 해결](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)을 참조하십시오.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## Break 지시문으로 인한 오류 해결

필요한 경우 시나리오를 업데이트하고 한 번 실행하여 오류를 수동으로 해결할 수 있습니다.

시나리오를 다시 실행하여 불완전한 실행을 자동으로 처리하도록 시나리오를 구성할 수도 있습니다. 미완료 실행을 처리하도록 모듈을 구성하려면 다음을 수행합니다.

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 해결 방법을 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. **흐름 제어** 아이콘 ![흐름 제어](assets/flow-control-icon.png)를 클릭하고 **중단**&#x200B;을 선택합니다.
1. 브레이크 모듈 내에서 [!UICONTROL **자동으로 실행 완료**] 옵션을 사용하도록 설정합니다.
1. **시도 횟수** 필드에 모듈에서 실행을 다시 시도할 최대 시도 횟수를 입력하거나 매핑합니다

   이 숫자는 1에서 100 사이여야 합니다.
1. **시도 간격** 필드에 각 재시도 간격(분)을 입력하거나 매핑합니다.

이 옵션을 활성화하면 오류가 발생하면 불완전한 실행이 검색되고([!UICONTROL 시도 간격] 필드에 지정된 시간 이후) 원래 입력 데이터로 실행됩니다. 이 작업은 모듈 실행이 오류 없이 완료되거나 지정된 시도 횟수에 도달할 때까지 반복됩니다.

>[!NOTE]
>
>초기 재시도 시도가 실패하면 재시도 간격은 다른 시도마다 기하급수적으로 증가합니다.


자동 완료 실행 옵션이 활성화된 경우 브레이크 오류 처리기의 자동 재시도가 문제를 자동으로 처리하고 있으므로 시나리오 실행이 &quot;성공&quot;으로 표시됩니다. 이 경우 실패한 실행에 대한 이메일이 사용자에게 전송되지 않습니다.

자동 완료 실행 옵션이 꺼져 있으면 실행이 &quot;경고&quot;로 표시됩니다.

미완료 실행에 저장되는 실행은 예외적이며, 일부 오류 유형에서는 시나리오 실행의 자동 재시도가 불가능합니다.

## 리소스

자세한 내용은 시나리오 설정 구성 문서에서 [불완전한 실행 저장 허용](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions)을 참조하십시오.
