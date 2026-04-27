---
content-type: reference
title: 'Set up and managing organizations and teams: article index'
description: This section contains articles related to setting up and managing organizations and teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: 6762806f17a0fc55531b647a84901b8ca572a997
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 21%

---

# Delete users through the [!DNL Adobe Admin Console]

You can remove a user from Adobe Workfront Fusion only, leaving access to any other [!DNL Adobe] product profiles, or you can remove the user from the [!DNL Adobe Admin Console] entirely.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성</td> 
   <td> 
     <p>You must be an Adobe Admin Console administrator for your organization.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## Remove a user from Adobe Workfront Fusion only

You can remove a user from Workfront Fusion while leaving their other Adobe product permissions intact.

For instructions, see &quot;Remove users and user groups from a product&quot; in the article [Manage products on Admin Console](https://helpx.adobe.com/kr/enterprise/using/manage-products.html).

## Deactivate a user in all products in the [!DNL Adobe Admin Console]

To delete a user, you must deactivate the user through the [!DNL Adobe Admin Console].

A user is deactivated from the [!DNL Adobe Admin Console] when one of the following applies:

* The user is moved out from a product or product profile, and are not assigned to any other product or product profile.
* The user is removed from a group that is linked to a product profile, and is not included in any other group linked to a product profile.
* The user is removed from a product profile and is not assigned to another product profile.
* The user is deleted or deactivated in the organization that includes Workfront Fusion.

  For instructions, see the section &quot;Remove users&quot; in [Manage users individually](https://helpx.adobe.com/kr/enterprise/using/manage-users-individually.html).

In Workfront Fusion, the deactivation affects the user in one of the following ways:

* If the user is in only one organization, the user is deactivated.
* If the user is in more than one organization, the user is removed from the organization that the user was modified in on the [!DNL Adobe Admin Console].

### Considerations when deleting a user in Workfront Fusion

Consider the following when deleting a user.

* When a user is deleted, the user&#39;s connections, keys, and webhooks are removed.
* Any scenarios belonging to the user are transferred to the organization Owner. The connections in these scenarios must be updated, because the connections belonging to the user are no longer valid.
* 삭제된 사용자가 응용 프로그램 또는 공용 템플릿을 소유하고 있으면 해당 응용 프로그램 또는 공용 템플릿이 조직 소유자에게 이전됩니다. 조직 소유자가 없는 경우 애플리케이션이나 공용 템플릿이 다른 사용자에게 전송됩니다.
