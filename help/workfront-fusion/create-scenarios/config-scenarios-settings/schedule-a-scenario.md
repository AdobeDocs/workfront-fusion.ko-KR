---
content-type: reference
title: 시나리오 예약
description: 기본적으로 시나리오는 15분마다 실행됩니다. 활성화된 시나리오가 실행되는 시기와 빈도를 정의하여 이를 변경할 수 있습니다. Fusion 시나리오는 5분마다 실행되도록 예약할 수 있습니다.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# 시나리오 예약

기본적으로 시나리오는 15분마다 실행됩니다. 활성화된 시나리오가 실행되는 시기와 빈도를 정의하여 이를 변경할 수 있습니다. Fusion 시나리오는 5분마다 실행되도록 예약할 수 있습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 시나리오 예약

1. 왼쪽 패널의 **시나리오** 탭을 클릭합니다.
1. 예약하려는 시나리오를 선택합니다.
1. 시나리오 세부 정보 페이지의 오른쪽 상단 모서리에서 **[!UICONTROL 옵션]** > **[!UICONTROL 예약]**&#x200B;을 클릭합니다.

   또는

   시나리오의 트리거 모듈에서 **[!UICONTROL 예약]** 아이콘(시계)을 클릭합니다.

1. 다음 필드에 정보를 입력합니다.

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL 실행 시나리오]</td> 
      <td> <p>시나리오를 실행할 빈도를 선택한 다음 간격을 선택합니다.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL At regular interval]</strong> </p> <p>실행 간격(분)을 입력합니다. 기본값은 15분입니다.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>시나리오를 실행할 날짜 및 시간을 입력합니다. <code>MM/DD/YYYY h:mm A</code> 형식을 사용합니다. 예: <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>시나리오를 실행할 시간을 입력합니다. <code>h:mm A</code> 형식을 사용합니다. 예: <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL 요일]</strong> </p> <p>일: 시나리오를 실행할 요일을 선택합니다. 하나 이상의 요일을 선택할 수 있습니다.</p> <p>시간: 선택한 일자에 시나리오를 실행할 시간을 입력합니다. <code>h:mm A</code> 형식을 사용합니다. 예: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL 해당 월의 일]</strong> </p> <p>일: 시나리오를 실행할 월을 선택합니다. 하나 이상의 요일을 선택할 수 있습니다.</p> <p>시간: 선택한 일자에 시나리오를 실행할 시간을 입력합니다. <code>h:mm A</code> 형식을 사용합니다. 예: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL 지정 날짜]</strong> </p> <p>월: 시나리오를 실행할 월을 선택합니다. 하나 이상의 월을 선택할 수 있습니다.</p> <p>일: 시나리오를 실행할 월을 선택합니다. 하나 이상의 요일을 선택할 수 있습니다.</p> <p>시간: 선택한 일자에 시나리오를 실행할 시간을 입력합니다. <code>h:mm A</code> 형식을 사용합니다. 예: <code>11:00 PM</code></p> </li> 
       </ul> <p>주: 시나리오가 해당 일자에 실행되려면 일자가 있어야 합니다. 예를 들어, 해당 달에는 31번째 날이 없으므로 해당 달의 31일에만 예약된 시나리오는 2월, 4월, 6월, 9월 또는 11월에 실행되지 않습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 고급 예약]</td> 
      <td>시나리오를 실행할 특정 시간 간격을 정의할 수 있습니다. 주중 또는 월 단위 시간 간격을 지정할 수 있습니다. 각 간격에 대해 <strong>[!UICONTROL 추가]</strong>를 클릭하고 [!UICONTROL 실행 시나리오] 필드에 설명된 대로 필드를 채웁니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 시작]</td> 
      <td>시나리오를 실행할 날짜 및 시간을 입력합니다. <code>MM/DD/YYYY h:mm A</code> 형식을 사용합니다. 예: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL End]</td> 
      <td>시나리오를 실행할 날짜 및 시간을 입력합니다. <code>MM/DD/YYYY h:mm A</code> 형식을 사용합니다. 예: <code>06/25/2019 11:00 PM</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. 예약 설정을 저장하고 시나리오로 돌아가려면 **[!UICONTROL 확인]**&#x200B;을 클릭하세요.
