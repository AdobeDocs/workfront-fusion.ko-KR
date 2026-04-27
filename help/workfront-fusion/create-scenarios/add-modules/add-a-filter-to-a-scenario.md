---
title: 시나리오에 필터 추가
description: In some scenarios, you need to work only with bundles that meet specific criteria. Filters allow you to select those bundles.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: 8de3e365ff7ff91f4b29fb8a298f3b846de0a980
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 19%

---

# 시나리오에 필터 추가

In some scenarios, you need to work only with bundles that meet specific criteria. Filters allow you to select those bundles.

For example, you could create a scenario with the [!UICONTROL Watch records] trigger for Workfront to capture only tasks assigned to a specific user.

You can add a filter between two modules and check whether bundles received from the preceding modules fulfill specific filter conditions:

* If they do, the bundles pass on to the next module in the scenario.
* If they don&#39;t, processing for the bundles terminates.

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
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 전제 조건

You must add both modules to a scenario before you can add a filter between them.

## Add a filter between two modules:

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Click the wrench icon ![Wrench icon](assets/wrench-icon.png) between the modules where you want to add a filter and select **Set up a filter**.
1. In the box that displays, enter a **[!UICONTROL Label]** for the filter.
1. Define the filter **[!UICONTROL Condition]**.

   Enter the field that you want to filter by in the first field, the operator, and (if necessary) the value that you want to compare the field to.

   >[!TIP]
   >
   >You can enter values into filter fields from the mapping panel
   >For more information on mapping, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   For example, if you wanted the filter to pass files in Adobe Workfront ending with XML, you would enter **[!UICONTROL File name]** in the first box and .**[!UICONTROL xml]** in the second box. In the drop-down menu between them, you would select **[!UICONTROL Ends with (case insensitive)]**. This filter would apply to incoming bundles from the first module (Workfront). Only bundles containing XML files would pass on to the next module.

   ![Set up a filter](assets/set-up-filter-box.png)

1. **[!DNL OK]**&#x200B;을(를) 클릭합니다.

## Copy a filter

You can copy an existing filter and paste it elsewhere in the scenario.

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Right-click on the connecting dots between modules where the filter is located.
1. Select **Copy filter**.
1. Right-click on the connecting dots between modules where you want to paste the filter.
1. Select **Paste** filter
1. (Optional) To adjust the filter, click the filter icon or label, and enter values as described in [Add a filter between two modules](#add-a-filter-between-two-modules) in this article.




<!--

Currently, the scenario editor does include a feature for copying a filter.

>[!NOTE]
>
>If you copy the modules on either side of the filter, the filter is also copied.
>
>For more information on copying modules, see [Copy modules or scenarios in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

To copy a filter without copying modules, you can use the Fusion DevTool

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Open the Fusion DevTool by clicking on the DevTool icon ![DevTool icon](assets/debugger-icon.png) near the bottom of the screen.
   
   If you do not see the DevTool icon, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) for instructions on opening the DevTool.
   
1. Click the **[!UICONTROL Tools]** icon ![DevTool tools](assets/devtools-tools-icon.png) in the left side bar.

1. Click **[!UICONTROL Copy Filter]**, then configure the **[!UICONTROL Copy Filter]** tool in the right side panel:

   1. Set the **[!UICONTROL Source Module]** as the module directly after the filter you want to copy.
   1. Set the **[!UICONTROL Target Module]** as the module that you want to place the filter directly after.

1. Click **[!UICONTROL Run]**.

-->
