---
title: Publish 및 공유 템플릿
description: 템플릿을 만들면 모든 팀원이 템플릿을 사용할 수 있습니다. 템플릿을 팀 외부의 사용자와 공유하려면 먼저 게시해야 합니다.
author: Becky
feature: Workfront Fusion
exl-id: 99a1227d-bff9-479f-b8b9-efcf7cea3708
source-git-commit: 7acc27ab2ce80b964b7f9fbb302816aa75964ab5
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 1%

---

# Publish 및 공유 템플릿

템플릿을 만들면 모든 팀원이 템플릿을 사용할 수 있습니다. 템플릿을 팀 외부의 사용자와 공유하려면 먼저 게시해야 합니다.

템플릿 만들기에 대한 자세한 내용은 [새 템플릿 만들기](/help/workfront-fusion/create-and-manage-templates/create-new-fusion-templates.md)를 참조하십시오.

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
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 전제 조건

템플릿을 게시하거나 공유하려면 먼저 템플릿을 만들어야 합니다.

## 템플릿 Publish

1. 왼쪽 탐색 패널에서 **[!UICONTROL Templates]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Team templates]** 탭을 클릭합니다.
1. 게시할 템플릿의 행에서 **Publish**&#x200B;을 클릭합니다.

   또는


   게시할 템플릿 이름을 클릭한 다음 화면 오른쪽 상단의 **[!UICONTROL Publish]** 단추를 클릭합니다.

## [!DNL Workfront Fusion] 템플릿 공유

템플릿을 게시한 후에는 공유할 수 있습니다.

1. 왼쪽 탐색 패널에서 **[!UICONTROL Templates]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Team templates]** 탭을 클릭합니다.
1. 공유할 템플릿의 이름을 클릭하여 템플릿을 엽니다.
1. 해당 버전의 템플릿을 열려면 **게시됨** 탭을 클릭하십시오.
1. (조건부) 공유 가능한 링크를 원하는 경우 **[!UICONTROL Share public link]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >이 링크를 공유할 수 있지만 템플릿 자체는 [!UICONTROL Team templates] 탭에 있으며 공개되지 않습니다.

1. (조건부) 템플릿을 공개하려면 **[!UICONTROL Request Approval]**&#x200B;을(를) 클릭하여 승인을 받기 위해 관리자에게 보내십시오.

   >[!NOTE]
   >
   >* 템플릿이 승인되면 공개됩니다. [!UICONTROL Public templates]은(는) 조직 또는 팀에 관계없이 모든 [!DNL Workfront Fusion] 사용자의 [!UICONTROL Public templates] 탭에 표시됩니다.
   >* 관리자가 이메일로 검토할 템플릿을 받았다는 알림을 받지 못했습니다. 승인이 긴급한 경우에는 관리자에게 직접 문의하십시오.


## 템플릿 상태

Fusion은 템플릿 페이지의 서로 다른 탭에 서로 다른 버전(비공개, 게시됨 및 승인됨)을 저장합니다.

다음 상태를 사용할 수 있습니다.

* **[!UICONTROL Private]**: 이 템플릿은 템플릿 작성자와 해당 팀에만 표시됩니다.
* **[!UICONTROL Published]**: 이 템플릿은 템플릿 작성자와 해당 팀에만 표시됩니다. 승인을 위해 게시된 템플릿을 보내고 공유 가능한 링크를 복사할 수 있습니다.
* **[!UICONTROL Approved]**: 이 템플릿은 모든 Workfront Fusion 사용자가 [!UICONTROL Public templates] 탭에 볼 수 있습니다. 화면 오른쪽 상단의 [!UICONTROL Options]을(를) 클릭하여 공유 가능한 링크를 복사할 수 있습니다.

<!--You can also check the status from the [!UICONTROL Team templates] tab. If a template is published, it will have an icon to the right of the template name.

* **Eye icon**: The template is published, it is visible only for the team, and the approval request was not sent.
* **Yellow checkmark icon**: The template is published, it is visible only for the team, and the approval request was sent.
* **Green checkmark icon**: The template is published and public. It is visible for any Workfront Fusion user in the [!UICONTROL Public templates] tab. It is also still visible in the [!UICONTROL Team templates] tab, and the template author or their team member can still edit it.

Templates without icons have [!UICONTROL Private] status. They are not published and are visible only to the team.
-->
