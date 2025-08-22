---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: 잠긴 시나리오 관리
description: Adobe Workfront Fusion에서 잠긴 시나리오 관리
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 1%

---

# 잠긴 시나리오 관리

경우에 따라 Workfront Fusion에서 시나리오가 일시적으로 잠길 수 있습니다. 잠긴 시나리오는 2~4시간 내에 자동으로 잠금 해제됩니다. 시나리오의 잠금을 수동으로 해제할 수 있지만 일반적으로 권장되지는 않습니다.

다음과 같은 여러 가지 이유로 인해 시나리오가 잠길 수 있습니다.

* Workfront Fusion은 예약된 시나리오의 병렬 처리를 지원하지 않습니다. 이러한 시나리오는 시나리오 실행 시작 시 잠기고 완료되면 잠금 해제됩니다. 실행이 중단되면 시나리오가 잠금 해제되지 않을 수 있습니다. 사용자가 시나리오를 수동으로 중지하거나 시스템 문제가 있을 때 이러한 문제가 발생할 수 있습니다.

* Workfront Fusion 엔지니어링 팀은 성능 또는 기타 문제를 일으키는 시나리오를 잠글 수 있습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] Workfront 플랜: 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li><li>[!UICONTROL Ultimate] Workfront 계획: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성*</td> 
   <td> 
     <p>조직의 Workfront Fusion 관리자여야 합니다.</p>
     <p>팀의 Workfront Fusion 관리자여야 합니다.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++


## 잠긴 시나리오 잠금 해제

잠긴 시나리오는 잠긴 시간으로부터 2~4시간 후에 잠금 해제됩니다. 시나리오를 자동으로 잠금 해제하도록 예약하기 전에 수동으로 잠금 해제할 수 있습니다.

>[!WARNING]
>
>시나리오를 수동으로 잠금 해제하면 시나리오 실행에 오류가 발생할 수 있습니다. 시나리오 설계의 일부로 실행 실행 및 중지로 인해 시나리오가 잠긴 경우에만 시나리오를 수동으로 잠금 해제하는 것이 좋습니다. 다른 상황에서는 시나리오가 자동으로 잠금 해제될 때까지 기다리는 것이 좋습니다.


잠긴 시나리오를 수동으로 잠금 해제하려면

1. 잠긴 시나리오의 시나리오 세부 정보 페이지로 이동합니다.
1. 화면 오른쪽 상단의 **[!UICONTROL 옵션]**&#x200B;을 클릭합니다.
1. **[!UICONTROL 실행 잠금 해제]**&#x200B;를 선택하십시오.
1. **[!UICONTROL 잠금 해제]**를 클릭합니다.
   ![시나리오 잠금 해제](assets/unlock-scenario.png)
