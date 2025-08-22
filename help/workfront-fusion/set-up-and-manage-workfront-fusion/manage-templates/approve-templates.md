---
content-type: reference
title: 템플릿 승인 또는 비승인
description: 이 문서에서는 Fusion 템플릿을 승인하거나 승인하지 않는 방법에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# 공개 탭에 대한 템플릿 승인 또는 승인 취소

Adobe Workfront Fusion 템플릿은 다양한 워크플로를 자동화하고 간소화하기 위해 설계된 사전 빌드된 시나리오입니다. 이러한 템플릿은 사용자가 모든 것을 처음부터 빌드할 필요 없이 신속하게 통합 및 자동화를 설정하는 데 도움이 됩니다.

관리자는 공개 템플릿 탭에서 특정 템플릿을 전체 조직과 공유할지 여부를 선택할 수 있습니다.

사용자는 공용 템플릿 페이지에서 공유할 승인을 위해 만든 템플릿을 전송할 수 있습니다. <!--do the have to be requested or can an admin just choose to approve?-->

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">Adobe Workfront 플랜</td>
      <td><p>임의</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">Adobe Workfront 라이선스</td>
      <td><p>새로운 기능: 표준</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p></td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront Fusion 라이센스**</td>
      <td>
        <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
        <p>또는</p>
        <p>레거시: 모두</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">제품</td>
      <td>
        <p>신규:</p>
        <ul>
          <li>[!UICONTROL Select] 또는 [!UICONTROL Prime] Workfront 플랜: 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li>
          <li>[!UICONTROL Ultimate] Workfront 계획: Workfront Fusion이 포함됩니다.</li>
        </ul>
        <p>또는</p>
        <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## Workfront Fusion 템플릿 승인 또는 승인 취소

템플릿을 승인하면 [!UICONTROL 공개 템플릿] 탭에 표시되고 모든 사용자가 사용할 수 있습니다.

템플릿을 승인하지 않으면 [!UICONTROL 공개 템플릿] 탭에서 템플릿이 제거되고 템플릿을 만든 팀만 사용할 수 있게 됩니다.

1. 왼쪽 탐색 패널에서 **[!UICONTROL 관리]**&#x200B;를 클릭하여 [!UICONTROL 관리] 영역을 엽니다.
1. 왼쪽 탐색 패널에서 **[!UICONTROL 템플릿]**&#x200B;을 클릭합니다.
1. 템플릿을 승인하려면 템플릿 오른쪽에 있는 **[!UICONTROL 승인]**&#x200B;을 클릭합니다.
1. 템플릿을 승인하지 않으려면 템플릿 오른쪽에 있는 **[!UICONTROL 비승인]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>이전에 승인된 후 편집한 템플릿을 승인하는 경우 두 번째 승인이 원래 템플릿을 덮어씁니다.


## 템플릿 상태

템플릿 페이지의 템플릿 이름 아래에서 상태를 확인할 수 있습니다.

다음 상태를 사용할 수 있습니다.

* **[!UICONTROL 개인]**: 이 템플릿은 템플릿 작성자와 해당 팀에만 표시됩니다.
* **[!UICONTROL 게시됨]**: 이 템플릿은 템플릿 작성자와 해당 팀에만 표시됩니다. 게시되면 원하는 경우 승인을 위해 템플릿을 전송할 수 있습니다. 공유 가능한 링크를 복사할 수도 있습니다.
* **[!UICONTROL 승인됨]**: 이 템플릿은 모든 Workfront Fusion 사용자가 [!UICONTROL 공용 템플릿] 탭에서 볼 수 있습니다. 화면 오른쪽 상단의 [!UICONTROL 옵션]을 클릭하여 공유 가능한 링크를 복사할 수도 있습니다.

[!UICONTROL 팀 템플릿] 탭에서 상태를 확인할 수도 있습니다. 템플릿이 게시되면 템플릿 이름 오른쪽에 아이콘이 표시됩니다.

* **눈 모양 아이콘**: 템플릿이 게시되었으며, 팀에서만 볼 수 있고 승인 요청이 전송되지 않았습니다.
* **노란색 확인 표시 아이콘**: 템플릿이 게시되었으며 팀에만 표시되며 공개 템플릿 탭에 추가하는 승인을 보류 중입니다.
* **녹색 확인 표시 아이콘**: 템플릿은 공개 템플릿 탭에서 사용할 수 있으며 모든 Workfront Fusion 사용자에게 표시됩니다. 또한 [!UICONTROL 팀 템플릿] 탭에도 표시됩니다. 템플릿 작성자 또는 팀원은 여전히 템플릿을 편집할 수 있습니다.

아이콘이 없는 서식 파일의 상태는 [!UICONTROL 개인]입니다. 이 지표는 게시되지 않으며 팀에게만 표시됩니다.


<!--

## Questions about how this works

Editing

1. If an admin edits a template, do they have to publish again? ... Do they have to approve again?
1. What does publishing actually do?
1. Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
1. What is the admin approving? Does a user have to submit it for approval? 



What does "Publishing" mean?
What does "Approving" mean?
If an admin edits a template, do they have to publish again? ... Do they have to approve again?
Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
What is the admin approving? Does a user have to submit it for approval?

-->
