---
title: 새 템플릿 만들기
description: ' [!DNL Adobe] Workfront Fusion에서 새 시나리오 템플릿을 만들 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 0%

---

# 새 템플릿 만들기

[!DNL Adobe] Workfront Fusion에서 새 시나리오 템플릿을 만들 수 있습니다.

>[!TIP]
>
>새 템플릿을 만들기 전에 [!UICONTROL 공개 템플릿] 탭에서 만들 템플릿을 아직 사용할 수 있는지 확인할 수 있습니다.

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

## 새 템플릿 만들기

시나리오 작성과 유사한 프로세스에서 템플릿을 작성할 수 있습니다. Fusion 관리자는 기존 시나리오에서 템플릿을 만들 수도 있습니다.

* [템플릿 작성](#build-a-template)
* [시나리오에서 템플릿 만들기](#create-a-template-from-a-scenario)

### 템플릿 작성

1. 왼쪽 탐색 패널에서 **[!UICONTROL 템플릿]** ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 오른쪽 상단의 **[!UICONTROL 새 템플릿 만들기]**&#x200B;를 클릭합니다.
1. (선택 사항) 왼쪽 위 모서리에서 기본 **[!UICONTROL 새 템플릿 이름]**&#x200B;을(를) 바꾸어 템플릿 이름을 변경합니다.
1. (선택 사항) 템플릿의 언어를 변경하려면 **[!UICONTROL 템플릿 설정]** ![시나리오 설정 아이콘](assets/scenario-settings-icon.png)을 클릭하고 언어 드롭다운에서 언어를 선택합니다.

   >[!IMPORTANT]
   >
   >언어 선택은 시스템 설정에서 사용할 수 있는 언어에 해당하며 공개 템플릿의 이름과 설명만 고려합니다. 템플릿이 저장되면 템플릿 언어를 변경할 수 없습니다.

1. (선택 사항) 템플릿에 대한 설명을 입력하려면 **[!UICONTROL 템플릿 설정]** ![시나리오 설정 아이콘](assets/scenario-settings-icon.png)을 클릭하고 설명을 입력하십시오.
1. 시나리오에 모듈을 추가하는 것과 동일한 프로세스를 사용하여 앱, 모듈 및 도구를 추가합니다.

   자세한 내용은 [모듈 추가](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)의 문서를 참조하십시오.

   모듈에 상황별 도움말을 추가하려면 이 문서에서 [마법사 기능 설정](#set-up-wizard-functionality)을 참조하십시오.

   시나리오 작성에 대한 자세한 내용은 [시나리오 작성을 위한 워크플로](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md)를 참조하십시오.

   >[!NOTE]
   >
   >템플릿에 연결, 자격 증명 또는 기타 개인 정보에 민감한 정보를 추가해야 하는 모듈이 포함된 경우 이 정보는 템플릿 사용자와 공유되지 않습니다.

1. (선택 사항) 템플릿을 테스트하려면 **[!UICONTROL 한 번 실행]**&#x200B;을 클릭합니다.
1. 템플릿을 저장하려면 **[!UICONTROL 저장]** 아이콘 ![저장 아이콘](assets/save-icon.png)을 클릭합니다.

템플릿을 저장하면 팀 구성원이 볼 수 있게 됩니다. 팀 외부에서 템플릿에 액세스할 수 있게 하려면 요청을 제출하여 템플릿을 승인 및 게시해야 합니다. 승인을 위해 Adobe Workfront Fusion 팀으로 요청이 전송됩니다. 승인된 템플릿은 팀 외부의 다른 사용자가 액세스할 수 있습니다.

템플릿 게시에 대한 자세한 내용은 [Adobe Workfront Fusion 템플릿 게시 및 공유](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md)를 참조하십시오.

### 시나리오에서 템플릿 만들기

>[!NOTE]
>
>시나리오에서 템플릿을 만들려면 Fusion 관리자여야 합니다.

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 템플릿을 만들 시나리오를 선택합니다.
1. 페이지의 오른쪽 상단 근처에 있는 **관리자** 드롭다운을 클릭합니다.
1. **템플릿으로 복제**&#x200B;를 선택합니다.

   시나리오가 새 템플릿 페이지에 복사됩니다.
1. (선택 사항) 왼쪽 위 모서리에서 기본 **[!UICONTROL 새 템플릿 이름]**&#x200B;을(를) 바꾸어 템플릿 이름을 변경합니다.
1. (선택 사항) 템플릿의 언어를 변경하려면 **[!UICONTROL 템플릿 설정]** ![시나리오 설정 아이콘](assets/scenario-settings-icon.png)을 클릭하고 언어 드롭다운에서 언어를 선택합니다.

   >[!IMPORTANT]
   >
   >언어 선택은 시스템 설정에서 사용할 수 있는 언어에 해당하며 공개 템플릿의 이름과 설명만 고려합니다. 템플릿이 저장되면 템플릿 언어를 변경할 수 없습니다.

1. (선택 사항) 템플릿에 대한 설명을 입력하려면 **[!UICONTROL 템플릿 설정]** ![시나리오 설정 아이콘](assets/scenario-settings-icon.png)을 클릭하고 설명을 입력하십시오.
1. 시나리오에 모듈을 추가하는 것과 동일한 프로세스를 사용하여 앱, 모듈 및 도구를 원하는 대로 편집합니다.

   자세한 내용은 [모듈 추가](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)의 문서를 참조하십시오.

   모듈에 상황별 도움말을 추가하려면 이 문서에서 [[!UICONTROL 마법사] 기능 설정](#set-up-wizard-functionality)을 참조하십시오.

   >[!NOTE]
   >
   >템플릿에 연결, 자격 증명 또는 기타 개인 정보에 민감한 정보를 추가해야 하는 모듈이 포함된 경우 이 정보는 템플릿 사용자와 공유되지 않습니다.

1. (선택 사항) 템플릿을 테스트하려면 **[!UICONTROL 한 번 실행]**&#x200B;을 클릭합니다.
1. **[!UICONTROL 저장]** 아이콘 ![저장 아이콘](assets/save-icon.png)을 클릭합니다.

## [!UICONTROL 마법사] 기능 설정 {#set-up-wizard-functionality}

[!DNL Workfront Fusion template] [!UICONTROL 마법사]를 사용하면 향후 템플릿 사용자에게 모듈에서 사용되는 특정 필드와 관련된 지침이나 정보를 제공할 수 있습니다.

1. 템플릿을 만드는 동안 템플릿에 추가된 모듈을 클릭하여 모듈의 필드를 확인합니다.
1. [!UICONTROL 마법사] 정보를 추가할 필드를 찾은 다음 해당 필드에 대해 **[!UICONTROL 마법사에서 사용]**&#x200B;을 사용하도록 설정하십시오.
1. [!UICONTROL 도움말] 필드에 사용자에게 표시할 정보를 입력하십시오.
1. (선택 사항) 템플릿을 사용할 때 사용자가 이 텍스트를 볼 수 있도록 하려면 **[!UICONTROL 기본값으로 사용]**&#x200B;을 사용하도록 설정하십시오.
1. 정보를 제공하려는 각 필드에 대해 2~4단계를 반복합니다.
1. 변경 내용을 저장하고 모듈을 닫으려면 **[!UICONTROL 확인]**&#x200B;을 클릭하십시오.
