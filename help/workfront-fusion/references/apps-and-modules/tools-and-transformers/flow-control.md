---
title: 흐름 제어
description: 시나리오를 만들거나 편집할 때 설정을 구성하여 데이터가 시나리오를 통과하는 방식을 제어할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: ce2f13866fef97b5687991dfcf5d9579a5e539e4
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# 흐름 제어

시나리오를 만들거나 편집할 때 설정을 구성하여 데이터가 시나리오를 통과하는 방식을 제어할 수 있습니다.

## 액세스 요구 사항

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
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합의 경우 [!UICONTROL [!DNL Workfront Fusion], 작업 자동화의 경우 [!UICONTROL [!DNL Workfront Fusion]]</p>
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
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

## 반복

[!UICONTROL Repeater] 모듈을 사용하여 지정된 횟수만큼 작업을 반복할 수 있습니다. [!UICONTROL Repeater] 모듈은 번들을 하나씩 생성합니다.

예를 들어 [!UICONTROL Repeater] 모듈을 사용하여 **[!UICONTROL Email]>[!UICONTROL Send me an email]** 모듈을 [!UICONTROL Repeater] 모듈에 연결하여 제목이 &quot;Hello 1&quot;, &quot;Hello 2&quot; 등인 5개의 전자 메일을 보낼 수 있습니다.

[!UICONTROL Repeater] 모듈을 사용하려면:

1. 화면 하단의 [!UICONTROL Flow Control] 아이콘 ![](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif)을(를) 클릭한 다음 표시되는 메뉴에서 **[!UICONTROL Repeater]**&#x200B;을(를) 클릭합니다.
1. [!UICONTROL Repeater] 번들을 클릭한 다음 표시되는 상자에서 **[!UICONTROL Connect automatically]**&#x200B;을(를) 클릭합니다.
1. 표시되는 [!UICONTROL Flow Control] 상자에 원하는 반복 횟수(출력 번들)를 **[!UICONTROL Repeats]** 상자에 입력합니다.

   이메일 예제에서 5를 입력합니다.

   ![](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   항목의 값이 각 반복에서 **[!UICONTROL Show advanced settings]**&#x200B;을(를) 선택하여 볼 수 있는 **[!UICONTROL Step]** 필드에 지정된 값만큼 증가합니다. 이 숫자는 기본적으로 1입니다.

1. **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 **[!UICONTROL Flow Control]** 상자를 닫습니다.

1. [!UICONTROL Repeater] 모듈에 연결된 앱 또는 서비스 모듈을 클릭합니다.
1. 나타나는 상자에 반복할 정보를 입력합니다.

   전자 메일 예제에서는 [!UICONTROL Subject] 상자에 Hello를 입력한 다음 반복 모듈에서 `i`을(를) 매핑합니다.

   ![](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)

| 항목 | 설명 |
|---|---|
| [!UICONTROL Initial value] | 첫 번째 반복에서 모듈이 `i`(으)로 설정하려는 번호를 입력하거나 매핑합니다. 기본값은 1입니다. |
| [!UICONTROL Repeats] | 모듈이 반복될 횟수를 입력하거나 매핑합니다. 이 숫자는 0보다 크거나 같고, 10,000보다 작거나 같아야 합니다. |
| [!UICONTROL Step] | 모듈이 `i`의 값을 증가시키는 횟수입니다. 기본값은 1입니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>반복 횟수는 프로그래밍의 루프 안에 있으므로 `i` 값으로 결정되지 않습니다. 모듈은 [!UICONTROL Repeats] 필드에 표시된 횟수를 반복합니다. `i` 값은 [!DNL repeater] 모듈의 각 반복에 따라 변경되며 이후 모듈에 매핑될 수 있습니다. 위의 예에서는 `i` 값을 Hello 메시지에 매핑하여 &quot;Hello 1&quot;, &quot;Hello 2&quot; 등을 읽는 메시지가 생성됩니다.

## [!UICONTROL Iterator]

[!UICONTROL Iterator]은(는) 배열을 일련의 번들로 변환하는 특별한 유형의 모듈입니다. 각 배열 항목은 [!UICONTROL Iterator] 모듈 출력에서 별도의 번들입니다. 자세한 내용은 [반복자 모듈](/help/workfront-fusion/references/modules/iterator-module.md)을 참조하세요.

## 배열 집계

배열 집계기는 여러 번들을 하나의 번들로 병합할 수 있는 특별한 유형의 모듈입니다. 자세한 내용은 [집계 모듈](/help/workfront-fusion/references/modules/aggregator-module.md)을 참조하세요.

## [!UICONTROL Router]

[!UICONTROL Router] 모듈을 사용하면 플로우를 여러 경로로 분기하고 각 경로 내의 데이터를 다르게 처리할 수 있습니다. [!UICONTROL Router] 모듈이 번들을 수신하면 경로가 [!UICONTROL Router] 모듈에 첨부된 순서대로 연결된 각 경로로 전달합니다. 자세한 내용은  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)의 [라우터 모듈을 참조하십시오.

<!--
<div>
<h2>Directives</h2>
<p>The error handling directives allow you to control how your scenario reacts to errors. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md" class="MCXref xref">Advanced error handling in Adobe Workfront Fusion</a> and <a href="/help/workfront-fusion/references/errors/directives-for-error-handling.md" class="MCXref xref">Directives for error handling in Adobe Workfront Fusion</a>.</p>
</div>
-->
