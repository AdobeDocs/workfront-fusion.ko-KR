---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: 템플릿 보기, 편집 및 삭제
description: Adobe Workfront Fusion에는 Adobe Workfront 라이센스 외에 Adobe Workfront Fusion 라이센스가 필요합니다.
author: Becky
feature: Workfront Fusion
exl-id: 97e3402c-d1d0-44f6-9752-11b0f5abee22
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 0%

---

# 템플릿 보기, 편집 및 삭제

[!DNL Workfront Fusion] 템플릿 기능을 사용하면 기존 템플릿을 만들어 Workfront Fusion 시나리오의 시작점으로 사용할 수 있습니다. 템플릿은 조직의 요구 사항과 특정 사용 사례를 충족하도록 구성하고 수정할 수 있는 일반적인 사용 사례를 나타냅니다.

현재 사용 가능한 Fusion 템플릿 목록은 [현재 사용 가능한 Adobe Workfront Fusion 템플릿](/help/workfront-fusion/create-and-manage-templates/currently-available-fusion-templates.md)을 참조하십시오.

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

## Fusion 템플릿 보기 및 선택

템플릿 영역에서 사용 가능한 템플릿, 템플릿에 포함된 애플리케이션 및 구조를 볼 수 있습니다. 특정 앱 또는 이름을 검색하고 사용 사례를 필터링할 수도 있습니다.

1. 왼쪽 탐색에서 **템플릿** ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 공개적으로 사용 가능한 템플릿을 보려면 공개 템플릿 탭을 클릭합니다.

   또는

   팀으로 제한된 템플릿을 보려면 팀 템플릿 탭을 클릭합니다.



   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Public templates]</td> 
      <td> <p> 게시된 후 관리자가 승인한 모든 템플릿. 템플릿 타일에서 템플릿 이름, 미리 보기 및 소켓 아이콘을 확인할 수 있습니다. 이 아이콘에는 지금까지 사용된 템플릿 횟수를 나타내는 숫자가 있습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Team templates]</td> 
      <td> <p>관리자가 이미 공개한 템플릿을 포함하여 팀 멤버가 만든 모든 템플릿. 템플릿 타일에서 템플릿 이름, 이 설명서의 템플릿 게시 및 공유 섹션에 자세히 설명된 상태 아이콘 및 삭제 버튼을 볼 수 있습니다.</p> <b>참고:</b>팀 템플릿 탭에서 필요한 템플릿이 표시되지 않으면 왼쪽 탐색 또는 머리글을 확인하여 현재 올바른 팀을 보고 있는지 확인하십시오.</td> 
     </tr> 
    </tbody> 
   </table>
1. (선택 사항) 특정 애플리케이션이나 이름을 검색하려면 앱 또는 이름 검색 상자에 입력을 시작한 다음 드롭다운에 표시될 때 용어를 선택합니다.
1. (선택 사항) 오른쪽의 범주별 섹션에서 범주를 클릭하여 특정 사용 사례 범주를 필터링합니다.
1. (선택 사항) 템플릿 카드 위로 마우스를 가져간 후 시나리오 템플릿의 구조를 확인합니다.
1. 시나리오를 만드는 데 사용할 템플릿을 클릭합니다.

   템플릿의 다이어그램이 표시됩니다.

1. 공개 템플릿에서 시나리오를 만들려면 왼쪽 하단의 **템플릿에서 새 시나리오 만들기**&#x200B;를 클릭합니다.

   또는


   팀 템플릿에서 시나리오 작성을 시작하려면 다이어그램을 클릭한 다음, 모듈을 클릭하여 구성을 시작합니다.

템플릿으로 시나리오를 만드는 방법에 대한 지침은 [템플릿을 사용하여 시나리오 만들기](/help/workfront-fusion/create-and-manage-templates/create-scenarios-with-fusion-templates.md)를 참조하십시오.



>[!NOTE]
>
>* 액세스하려는 템플릿이 귀하 또는 귀하의 팀 구성원이 만든 것이 아니고 아직 공개되지 않은 경우 템플릿을 만들고 게시한 사람에게 템플릿 링크를 공유하도록 요청할 수 있습니다.
>* 사용자가 만든 공개 템플릿을 찾을 수 없는 경우 관리자에게 문의하십시오. 관리자가 템플릿을 승인하기 전에 이름을 변경했을 수 있습니다.

## 템플릿 편집

[!UICONTROL Team templates] 탭에서 사용할 수 있는 모든 템플릿을 편집할 수 있습니다.

1. 측면 탐색 메뉴에서 **[!UICONTROL Templates]** 아이콘 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. **[!UICONTROL Team templates]** 탭을 클릭합니다.
1. **[!UICONTROL Private]** 탭을 클릭합니다.
1. 편집할 템플릿을 클릭합니다.
1. 오른쪽 상단 모서리에서 **[!UICONTROL Edit]** 클릭

   또는

   템플릿 다이어그램을 클릭합니다.

1. 템플릿을 변경합니다. 템플릿을 만들 때 사용할 수 있었던 모든 옵션에 액세스할 수 있습니다. 이러한 옵션을 보려면 [새 템플릿 만들기](/help/workfront-fusion/create-and-manage-templates/create-new-fusion-templates.md)를 참조하세요.
1. **[!UICONTROL Save]** 아이콘 ![저장 아이콘](assets/save-icon.png)을 클릭합니다.

>[!NOTE]
>
>[!UICONTROL Team templates] 탭에는 게시된 템플릿뿐만 아니라 관리자가 이미 공개한 템플릿의 사본도 포함됩니다. 즉, 모든 사용자가 이미 볼 수 있는 템플릿을 편집할 수 있습니다. 이러한 템플릿 중 하나를 수정하는 경우, 변경 사항이 공용 템플릿을 바로 덮어쓰지 않습니다. [!UICONTROL Public templates] 탭의 템플릿은 그대로 유지되지만 [!UICONTROL Team templates]에서 변경한 내용이 포함된 최신 버전은 게시 프로세스를 시작합니다. 수정된 버전이 게시되고 승인되면 원래 공개 템플릿을 덮어씁니다.

## 템플릿 삭제

아직 승인되지 않은 템플릿만 삭제할 수 있습니다. 공개 템플릿을 삭제하려면 관리자에게 문의하십시오.

템플릿을 삭제한 후에는 복원할 수 없습니다. 팀 템플릿은 팀의 모든 멤버가 사용할 수 있으므로 템플릿을 삭제하기 전에 팀에 확인하여 템플릿이 필요하지 않은지 확인하는 것이 좋습니다.

1. 측면 탐색 메뉴에서 **[!UICONTROL Templates]** 아이콘 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. **[!UICONTROL Team templates]** 탭을 클릭합니다.
1. 템플릿 이름 옆에 있는 **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다

   또는

   템플릿 이름을 클릭하여 템플릿으로 이동합니다. 오른쪽 상단 모서리에서 **[!UICONTROL Options]**&#x200B;을(를) 클릭하고 **[!UICONTROL Delete]**&#x200B;을(를) 선택합니다.

1. 삭제를 확인하려면 **[!UICONTROL Really?]**&#x200B;을(를) 클릭합니다.
