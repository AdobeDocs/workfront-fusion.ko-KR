---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: 연결 관리
description: 대부분의 앱에서 특정 시나리오의 설정에 따라 Adobe Workfront Fusion이 지정된 서드파티 서비스와 통신할 수 있는 연결을 만들어야 합니다.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
source-git-commit: d13312031955a697e10ddfcdc2e64dfe198b3dac
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 1%

---

# 연결 관리

연결은 Fusion이 애플리케이션에 액세스하는 데 사용하는 권한 및 권한을 나타냅니다. 각 애플리케이션에 대해 하나 이상의 연결을 만들 수 있으며 여러 모듈 또는 시나리오에서 동일한 연결을 사용할 수 있습니다.

연결 영역에서 이러한 연결을 관리할 수 있습니다.

연결에 대한 자세한 내용은 [연결 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md)를 참조하십시오.

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
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 연결 보기 및 관리

연결 영역에서 모든 연결을 관리할 수 있습니다.

>[!NOTE]
>
>연결은 팀에서 소유합니다. 찾고 있는 연결을 찾을 수 없는 경우 올바른 팀을 보고 있는지 확인하십시오.
>
>새 팀을 선택하려면 왼쪽 탐색에서 팀 이름을 클릭하고 새 팀을 선택합니다.

1. 연결 영역을 열려면 왼쪽 탐색에서 **연결** ![연결 아이콘](assets/connections-icon.png)을 클릭합니다.
1. 관리할 연결을 찾은 다음 해당 연결의 행에서 다음 단계 중 하나 이상을 수행합니다.
1. (선택 사항) **환경** 및 **유형** 드롭다운을 클릭하고 옵션을 선택하여 환경 및 연결 유형을 할당합니다.
1. (선택 사항) 연결에 대해 Workfront Fusion에 부여된 권한을 보려면 해당 연결에 대한 보기 아이콘 ![연결 권한 보기](assets/view-connection-permissions.png)를 클릭합니다.
1. (선택 사항) 연결 이름을 바꾸려면 연결 이름을 강조 표시하고 새 이름을 입력합니다.
1. (선택 사항) 연결을 다시 승인하려면 연결 옆에 있는 확인란을 선택한 다음 화면 하단 근처에 있는 **다시 승인**&#x200B;을 클릭합니다.
1. (선택 사항) 연결을 삭제하려면 연결 옆에 있는 확인란을 선택하고 화면 하단 근처에 있는 **삭제**&#x200B;를 클릭한 다음 **정말?**&#x200B;를 클릭합니다.
1. (선택 사항) 서비스에 대한 연결이 제대로 설정되었는지 확인하려면 연결 옆에 있는 확인란을 선택한 다음 화면 아래쪽의 **확인**&#x200B;을 클릭합니다.
1. 이 연결을 사용하는 활성 시나리오를 보려면 연결 옆에 있는 확인란을 선택한 다음 **활성 시나리오 가져오기**&#x200B;를 클릭합니다. 그런 다음 활성 시나리오 목록에서 시나리오를 클릭하여 해당 시나리오로 이동할 수 있습니다.

## 연결 갱신

Workfront Fusion은 일반적으로 특정 서비스에 대한 액세스 권한을 무제한으로 부여받습니다. 일부 애플리케이션은 일정 기간 후에 액세스 권한을 갱신해야 합니다. 이러한 경우 Workfront Fusion은 액세스 권한이 만료되기 직전에 이메일을 통해 사용자에게 알립니다.

연결을 갱신하려면:

1. 연결 영역을 열려면 왼쪽 탐색에서 **연결** ![연결 아이콘](assets/connections-icon.png)을 클릭합니다.
1. 갱신할 연결을 찾습니다.
1. 해당 연결의 행에서 연결 옆에 있는 확인란을 선택한 다음 화면 하단 근처에 있는 **재인증**&#x200B;을 클릭합니다.

## 리소스

* 환경 및 형식 등의 연결 메타데이터에 대한 자세한 내용은 [연결 메타데이터](/help/workfront-fusion/references/connections/connection-metadata.md)를 참조하십시오.
