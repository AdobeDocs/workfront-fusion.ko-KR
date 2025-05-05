---
title: 흐름 제어
description: 시나리오를 만들거나 편집할 때 설정을 구성하여 데이터가 시나리오를 통과하는 방식을 제어할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# 흐름 제어

시나리오를 만들거나 편집할 때 설정을 구성하여 데이터가 시나리오를 통과하는 방식을 제어할 수 있습니다.

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
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>Workfront Fusion 라이센스 요구 사항 없음</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 반복

[!UICONTROL 반복] 모듈을 사용하여 지정된 횟수만큼 작업을 반복할 수 있습니다. [!UICONTROL Repeater] 모듈은 번들을 하나씩 생성합니다.


<table>
    <tr>
        <td>[!UICONTROL 초기 값]</td>
        <td>첫 번째 반복에서 모듈에 포함할 값을 입력하거나 매핑합니다. 기본값은 1입니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 반복]</td>
        <td>모듈이 반복될 횟수를 입력하거나 매핑합니다. 이 숫자는 0보다 크거나 같고, 10,000보다 작거나 같아야 합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 단계]</td>
        <td>모듈이 값을 증가시키는 횟수입니다. 기본값은 1입니다.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

예를 들어 [!UICONTROL Repeater] 모듈을 사용하여 **[!UICONTROL Email] >[!UICONTROL Email 보내기]** 모듈을 [!UICONTROL Repeater] 모듈에 연결하여 제목 &quot;Hello 1&quot;, &quot;Hello 2&quot; 등이 포함된 5개의 이메일을 보낼 수 있습니다.

1. 화면 하단의 [!UICONTROL 흐름 제어] 아이콘 ![흐름 제어 아이콘](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif)을 클릭한 다음 표시되는 메뉴에서 **[!UICONTROL 반복]**&#x200B;을 클릭합니다.
1. [!UICONTROL 반복] 모듈을 클릭한 다음 표시되는 상자에서 **[!UICONTROL 자동으로 연결]**&#x200B;을 클릭합니다.

   Repeater 모듈이 열립니다.

1. **[!UICONTROL 반복]** 필드에 모듈을 생성할 반복 횟수(출력 번들)를 입력합니다.

   이 예제에서는 5를 입력합니다.

   ![반복](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   항목의 값이 각 반복에서 **[!UICONTROL 단계]** 필드에 지정된 값만큼 증가합니다. 이 값은 **[!UICONTROL 고급 설정 표시]**&#x200B;를 선택하여 볼 수 있습니다. 이 숫자는 기본적으로 1입니다.

1. **[!UICONTROL 확인]**&#x200B;을 클릭하여 **[!UICONTROL 흐름 컨트롤]** 상자를 닫습니다.

1. [!UICONTROL 반복] 모듈에 연결된 앱 또는 서비스 모듈을 클릭합니다.
1. 나타나는 상자에 반복할 정보를 입력합니다.

   전자 메일 예제에서는 [!UICONTROL 제목] 상자에 Hello를 입력한 다음 반복 모듈에서 `i`을(를) 매핑합니다.

   ![반복](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>반복 횟수는 프로그래밍의 루프 안에 있으므로 `i` 값으로 결정되지 않습니다. 모듈은 [!UICONTROL 반복] 필드에 표시된 횟수를 반복합니다. `i` 값은 [!DNL repeater] 모듈의 각 반복에 따라 변경되며 이후 모듈에 매핑될 수 있습니다. 위의 예에서는 `i` 값을 Hello 메시지에 매핑하여 &quot;Hello 1&quot;, &quot;Hello 2&quot; 등을 읽는 메시지가 생성됩니다.

>[!ENDSHADEBOX]

## [!UICONTROL 반복자]

[!UICONTROL 반복자]은(는) 배열을 일련의 번들로 변환하는 특별한 유형의 모듈입니다. 각 배열 항목은 [!UICONTROL 반복자] 모듈 출력에서 별도의 번들입니다. 자세한 내용은 [반복자 모듈](/help/workfront-fusion/references/modules/iterator-module.md)을 참조하세요.

## 배열 집계

배열 집계기는 여러 번들을 하나의 번들로 병합할 수 있는 특별한 유형의 모듈입니다. 자세한 내용은 [집계 모듈](/help/workfront-fusion/references/modules/aggregator-module.md)을 참조하세요.

## [!UICONTROL 라우터]

[!UICONTROL 라우터] 모듈을 사용하면 흐름을 여러 경로로 분기하고 각 경로 내의 데이터를 다르게 처리할 수 있습니다. [!UICONTROL Router] 모듈이 번들을 받으면, [!UICONTROL Router] 모듈에 경로가 첨부된 순서대로 연결된 각 경로로 전달합니다. 자세한 내용은  [!DNL Adobe Workfront Fusion][&#128279;](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)의 라우터 모듈을 참조하십시오.

## 지시문

오류 처리 지시문을 사용하면 시나리오가 오류에 반응하는 방식을 제어할 수 있습니다.

오류 처리 지시문에 대한 자세한 내용은 [오류 처리에 대한 지시문](/help/workfront-fusion/references/errors/directives-for-error-handling.md)을 참조하십시오.

