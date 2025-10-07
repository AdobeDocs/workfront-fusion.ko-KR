---
title: 모듈을 새 버전으로 업데이트
description: Workfront Fusion이 연결되는 애플리케이션은 새 버전을 업데이트하거나 릴리스할 수 있으므로 Fusion에서 해당 애플리케이션에 대해 업데이트된 모듈을 릴리스해야 하는 경우가 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: b7f07fa5-9d81-48b3-b0ce-7a18b3b44508
source-git-commit: d0d9d7cdad993ecceaa0abf0ac69e9a9abd78b69
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 2%

---

# 모듈을 새 버전으로 업그레이드

Workfront Fusion이 연결되는 애플리케이션은 새 버전을 업데이트하거나 릴리스할 수 있으므로 Fusion에서 해당 애플리케이션에 대해 업데이트된 모듈을 릴리스해야 하는 경우가 있습니다.

시나리오의 모듈에 녹색 업그레이드 모듈 아이콘이 표시되면 Workfront Fusion에서 해당 모듈의 새 버전을 릴리스한 것입니다.

![업데이트 아이콘](assets/update-indicator-workfront.png)

새 시나리오를 만들지 않고 모듈을 업데이트할 수 있습니다.

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

## Workfront 모듈을 새 버전으로 업그레이드

1. 새 버전으로 업그레이드하려는 모듈에서 **업그레이드 모듈** 아이콘 ![업그레이드 아이콘](assets/upgrade-icon.png)을 클릭합니다.
   ![업데이트 아이콘](assets/update-indicator-workfront.png)
1. 다음 중 하나를 선택합니다.

   * 모듈을 업그레이드하지 않고 이 모듈을 대체할 새 모듈을 선택하려면 **새로 선택**&#x200B;을 클릭한 다음 [Workfront이 아닌 모듈을 새 버전으로 업그레이드](#upgrade-a-non-workfront-module-to-a-new-version)의 설명에 따라 계속 진행하십시오.
   * 모듈 구성을 유지하면서 이 모듈만 업그레이드하려면 **업그레이드**&#x200B;를 클릭하십시오.
   * 시나리오의 모든 Workfront 모듈을 업그레이드하려면 **모두 업그레이드**&#x200B;를 클릭하십시오.

1. 시나리오를 저장합니다.

>[!NOTE]
>
>Workfront 모듈을 업그레이드한 경우 해당 모듈을 열고 모듈 구성을 확인하는 것이 좋습니다.

## Workfront이 아닌 모듈을 새 버전으로 업그레이드

1. 새 버전으로 업그레이드하려는 모듈에서 **업그레이드 모듈** 아이콘 ![업그레이드 아이콘](assets/upgrade-icon.png)을 클릭합니다.
   ![업데이트 아이콘](assets/update-indicator.png)
1. **새로 선택**&#x200B;을 클릭합니다.
1. 이전 모듈을 바꿀 모듈을 선택합니다.
1. 기존 모듈과 동일한 설정으로 모듈을 구성합니다.
1. 새 모듈을 기존 모듈과 동일한 위치에서 시나리오에 연결합니다.
1. 이전 모듈을 삭제합니다.
1. 시나리오를 저장합니다.
