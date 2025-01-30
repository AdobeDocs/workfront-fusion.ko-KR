---
content-type: reference
title: 템플릿 편집
description: 이 문서에서는 Fusion 템플릿을 편집하는 방법에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# 템플릿 편집

Adobe Workfront Fusion 템플릿은 다양한 워크플로를 자동화하고 간소화하기 위해 설계된 사전 빌드된 시나리오입니다. 이러한 템플릿을 사용하면 처음부터 모든 것을 빌드할 필요 없이 통합 및 자동화를 빠르게 설정할 수 있습니다.

관리자는 다른 사용자가 만든 템플릿을 보고, 수정하고, 이름을 바꾸고, 게시하고, 승인하고, 삭제할 수 있는 권한이 있습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 플랜</td>
      <td><p>임의</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] 라이센스</td>
      <td><p>신규: [!UICONTROL Standard]</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td>
      <td>
        <p>현재: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
        <p>또는</p>
        <p>레거시: 모두</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">제품</td>
      <td>
        <p>신규:</p>
        <ul>
          <li>[!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Workfront] 플랜: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] 플랜 [!DNL Workfront Fusion]이(가) 포함되어 있습니다.</li>
        </ul>
        <p>또는</p>
        <p>현재: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## 관리자로 [!DNL Workfront Fusion] 템플릿 편집

1. 왼쪽 탐색 패널에서 **[!UICONTROL Administration]**&#x200B;을(를) 클릭하여 [!UICONTROL Administration] 영역을 엽니다.
1. 왼쪽 탐색 패널에서 **[!UICONTROL All Templates]**&#x200B;을(를) 클릭합니다.
1. 편집할 템플릿의 오른쪽에 있는 **[!UICONTROL Detail]**&#x200B;을(를) 클릭합니다.
1. (선택 사항) 오른쪽 상단의 **옵션**&#x200B;을 클릭하고 **이름 바꾸기**&#x200B;를 선택하여 템플릿의 이름을 변경합니다.
1. (선택 사항) 템플릿의 언어를 변경하려면 **[!UICONTROL Create a new template]** ![시나리오 설정 아이콘](assets/fusion-scenario-settings-icon.png)을 클릭하고 언어 드롭다운에서 언어를 선택합니다.

   >[!IMPORTANT]
   >
   >언어 선택은 시스템 설정에서 사용할 수 있는 언어에 해당하며 공개 템플릿의 이름과 설명만 고려합니다. 템플릿이 저장되면 템플릿 언어를 변경할 수 없습니다.

1. (선택 사항) 템플릿 설명을 편집하려면 **[!UICONTROL Set up a template]** ![시나리오 설정 아이콘](assets/fusion-scenario-settings-icon.png)을 클릭하고 설명을 입력하십시오.
1. 표준 시나리오를 만들 때와 동일한 방식으로 앱, 모듈 및 도구를 추가하거나 편집합니다.

   모듈에 상황별 도움말을 추가하려면 이 문서에서 [[!UICONTROL Wizard] 기능 설정](#set-up-wizard-functionality)을(를) 참조하십시오.

   <!--For more information on building a scenario, see [Create a scenario in [!DNL Adobe Workfront Fusion]](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >템플릿에 연결, 자격 증명 또는 기타 개인 정보에 민감한 정보를 추가해야 하는 모듈이 포함된 경우 이 정보는 템플릿 사용자와 공유되지 않습니다.

1. (선택 사항) 템플릿을 테스트하려면 **[!UICONTROL Run once]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Save]** 아이콘 ![저장 아이콘](assets/save-icon.png)을 클릭합니다.


## [!UICONTROL Wizard] 기능 설정

[!DNL Workfront Fusion template] [!UICONTROL Wizard]을(를) 사용하면 향후 템플릿 사용자에게 모듈에 사용되는 특정 필드와 관련된 지침이나 정보를 제공할 수 있습니다.

1. 템플릿에 추가된 모듈을 클릭하여 모듈의 필드를 확인합니다.
1. [!UICONTROL Wizard] 정보를 추가할 필드를 찾은 다음 해당 필드 아래에서 **[!UICONTROL Use in Wizard]**&#x200B;을(를) 사용하도록 설정하십시오.
1. [!UICONTROL Help] 필드에 사용자에게 표시할 정보를 입력하십시오.
1. (선택 사항) 템플릿을 사용할 때 사용자가 이 텍스트를 볼 수 있도록 하려면 **[!UICONTROL Use as default value]**&#x200B;을(를) 활성화합니다.
1. 정보를 제공하려는 각 필드에 대해 2~4단계를 반복합니다.
1. 변경 내용을 저장하고 모듈을 닫으려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하십시오.

게시 프로세스는 표준 사용자의 경우와 동일합니다. 자세한 내용은 [Publish 및 템플릿 공유](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md) 섹션을 참조하십시오.

## 템플릿 상태

템플릿 페이지의 템플릿 이름 아래에서 상태를 확인할 수 있습니다.

다음 상태를 사용할 수 있습니다.

* **[!UICONTROL Private]**: 이 템플릿은 템플릿 작성자와 해당 팀에만 표시됩니다.
* **[!UICONTROL Published]**: 이 템플릿은 템플릿 작성자와 해당 팀에만 표시됩니다. 게시되면 원하는 경우 승인을 위해 템플릿을 전송할 수 있습니다. 공유 가능한 링크를 복사할 수도 있습니다.
* **[!UICONTROL Approved]**: 이 템플릿은 모든 Workfront Fusion 사용자가 [!UICONTROL Public templates] 탭에 볼 수 있습니다. 화면 오른쪽 상단의 [!UICONTROL Options]을(를) 클릭하여 공유 가능한 링크를 복사할 수도 있습니다.

[!UICONTROL Team templates] 탭에서 상태를 확인할 수도 있습니다. 템플릿이 게시되면 템플릿 이름 오른쪽에 아이콘이 표시됩니다.

* **눈 모양 아이콘**: 템플릿이 게시되었습니다. 팀에 표시됩니다.
* **노란색 확인 표시 아이콘**: 템플릿이 게시되었으며 팀에만 표시되며 공개 템플릿 탭에 추가하는 승인을 보류 중입니다.
* **녹색 확인 표시 아이콘**: 템플릿은 공개 템플릿 탭에서 사용할 수 있으며 모든 Workfront Fusion 사용자에게 표시됩니다. 또한 [!UICONTROL Team templates] 탭에도 표시됩니다. 템플릿 작성자 또는 팀원은 여전히 템플릿을 편집할 수 있습니다.

아이콘이 없는 서식 파일의 상태는 [!UICONTROL Private]입니다. 이 지표는 게시되지 않으며 팀에게만 표시됩니다.

## 템플릿의 SVG 정보 찾기

1. 왼쪽 탐색 패널에서 **[!UICONTROL Administration]**&#x200B;을(를) 클릭하여 [!UICONTROL Administration] 영역을 엽니다.
1. 왼쪽 탐색 패널에서 **[!UICONTROL Templates]**&#x200B;을(를) 클릭합니다.
1. 정보를 찾을 템플릿을 클릭합니다.
1. 오른쪽 상단 모서리에서 **옵션**&#x200B;을 클릭합니다.
1. *SVG 다이어그램*&#x200B;을 선택하세요.

여기에서 SVG 다이어그램과 SVG 코드를 볼 수 있습니다.
