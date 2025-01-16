---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Adobe Admin Console을 통해 Adobe Workfront Fusion에 사용자 추가
description: Adobe Admin Console에 사용자를 추가하고 Adobe Workfront Fusion에 할당하거나 Adobe Admin Console의 기존 사용자를 Workfront Fusion에 할당할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# Adobe Admin Console을 통해 Adobe Workfront Fusion에 사용자 추가

[!DNL Adobe Admin Console]에 사용자를 추가하고 [!DNL Adobe Workfront Fusion]에 할당하거나 [!DNL Adobe Admin Console]의 기존 사용자를 [!DNL Workfront Fusion]에 할당할 수 있습니다.

사용자를 추가하는 방법을 포함하여 [!DNL Adobe Admin Console]의 [!DNL Workfront Fusion]에 대해 설명하는 비디오는 Adobe IMS에서 [[!DNL Fusion] 을(를) 참조하십시오](https://video.tv.adobe.com/v/3412464/){target=_blank}.



이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 플랜*</td> 
   <td> <p>[!UICONTROL Pro] 이상</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재 라이선스 요구 사항: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합을 위한 [!UICONTROL [!DNL Workfront Fusion]] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>현재 제품 요구 사항: [!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Adobe Workfront] 플랜이 있는 경우 조직에서 이 문서에 설명된 기능을 사용하려면 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다. [!DNL Workfront Fusion]이(가) [!UICONTROL Ultimate] [!DNL Workfront] 계획에 포함되어 있습니다.</p>
   <p>또는</p>
   <p>레거시 제품 요구 사항: 이 문서에 설명된 기능을 사용하려면 조직에서 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] 관리자 권한</td> 
   <td>조직의 [!DNL Adobe] 제품 중 [!UICONTROL Product Configuration Administrator]개여야 합니다.</td> 
  </tr>
  </tbody> 
</table>

&#42;플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

&#42;&#42;라이선스 [!DNL Adobe Workfront Fusion]에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.



## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스</td> 
   <td> <p>신규: [!UICONTROL Standard]</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Workfront] 플랜: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 플랜: [!DNL Workfront Fusion]이(가) 포함되어 있습니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성*</td> 
   <td> 
     <p>조직의 [!DNL Workfront Fusion] 관리자여야 합니다.</p>
     <p>팀의 [!DNL Workfront Fusion] 관리자여야 합니다.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++


## 전제 조건

[!DNL Workfront]에 대해 [!DNL Admin Console]을(를) 사용하기 전에 콘솔로 초대하는 전자 메일을 받아야 합니다.

1. [!DNL Adobe]을(를) 처음 사용하는 경우 조직의 [!DNL Adobe] 소프트웨어 및 서비스를 관리할 수 있는 관리 권한이 있다는 전자 메일을 받은 경우 전자 메일의 버튼을 클릭하여 [!DNL Adobe] 계정을 만들고 [!DNL Admin Console]을(를) 여십시오.

   또는

   이미 Adobe 계정이 있는 경우 [[!DNL Adobe Admin Console] 페이지](https://adminconsole.adobe.com)(으)로 이동하십시오.


## [!DNL Adobe Admin Console] 및 [!DNL Workfront Fusion]에 새 사용자 추가

1. [[!DNL Adobe Admin Console] 페이지](https://adminconsole.adobe.com/)에서 위쪽 탐색 막대의 **[!UICONTROL Products]** 탭을 선택한 다음 **[!DNL Workfront Fusion]** 제품 타일을 선택합니다.

   ![Admin Console의 Fusion](assets/fusion-product-admin-console.png)

1. 표시되는 목록에서 사용자를 추가하려는 조직을 선택합니다.

   ![Admin Console의 Fusion 인스턴스](assets/fusion-instances-admin-console.png)

1. 표시되는 목록에서 **[!UICONTROL Product Profiles]** 탭을 선택하고 [!DNL Workfront Fusion] [!UICONTROL Product Profile] 링크의 이름을 클릭합니다.

   >[!IMPORTANT]
   >
   > [!UICONTROL Product Profile] 자체를 변경하지 마십시오.

1. 목록 위에 **[!UICONTROL Users]** 탭을 선택한 상태에서 **[!UICONTROL Add User]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Add users to this product profile]** 상자에 추가할 사용자의 전자 메일 주소 또는 이름을 입력한 다음 표시되는 목록에서 사용자를 선택합니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   사용자가 [!DNL Workfront Fusion]에서 만들어졌습니다.

1. (선택 사항) [계속  [!DNL Workfront Fusion]](#change-a-users-access-level-in-workfront-fusion)에서 사용자의 액세스 수준 변경

## Workfront Fusion에서 사용자의 액세스 수준 변경

* [사용자의 역할을 관리자로 변경](#change-a-users-role-to-admin)
* [사용자의 역할을 구성원, 회계사 또는 앱 개발자로 변경](#change-a-users-role-to-member-accountant-or-app-developer)

### 사용자의 역할을 관리자로 변경

사용자에게 관리자 역할을 부여하는 작업은 [!DNL Adobe Admin Console]에서 수행해야 합니다.

1. 사용자를 추가한 [!DNL Workfront Fusion] [!UICONTROL Product Profile] 페이지에서 **[!UICONTROL Admins]** 탭을 선택합니다.

1. **[!UICONTROL Add Admin]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Add product profile administrators]** 상자에 관리자가 될 사용자의 전자 메일 주소 또는 이름을 입력한 다음 표시되는 목록에서 사용자를 선택합니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   사용자가 [!DNL Workfront Fusion]의 관리자입니다.

### 사용자의 역할을 구성원, 회계사 또는 앱 개발자로 변경

멤버, 회계사 및 앱 개발자 역할은 Workfront Fusion 내에서 처리됩니다.

지침은 [사용자 역할 보기 또는 편집](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md)을 참조하세요.

## [!DNL Adobe Admin Console]의 기존 사용자를 [!DNL Workfront Fusion]에 할당

Fusion에서 기존 사용자를 팀에 추가할 수 있습니다. 이 작업은 Fusion 내에서 처리됩니다.

지침은 [팀에 사용자 추가](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md)를 참조하십시오.
