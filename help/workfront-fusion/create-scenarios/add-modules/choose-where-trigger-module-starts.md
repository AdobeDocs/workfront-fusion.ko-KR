---
title: 트리거 모듈의 시작 위치 선택
description: 일부 트리거 모듈을 사용하면 번들 검색을 시작할 첫 번째 번들을 선택할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 83628fa5-82e2-4f67-bfed-70a4c3c19f7f
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# 트리거 모듈의 시작 위치 선택

일부 트리거 모듈을 사용하면 번들 검색을 시작할 첫 번째 번들을 선택할 수 있습니다.

특정 날짜 이후에 모든 번들을 검색할지 아니면 번들만 검색할지 지정할 수도 있습니다.

트리거 모듈에 대한 자세한 내용은 문서 모듈 개요에서 [트리거 모듈](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) 섹션을 참조하십시오.

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

## 트리거 모듈의 시작 위치 선택

1. 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 트리거가 시작되는 위치를 선택할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 트리거 모듈을 구성하고 저장합니다.

   또는

   트리거 모듈의 아이콘을 마우스 오른쪽 단추로 클릭하고 **시작할 위치 선택**&#x200B;을 선택합니다.

   ![시작할 위치 선택](assets/choose-where-to-start.png)

1. 표시되는 **[!UICONTROL Choose where to start]** 상자에서 옵션을 선택하십시오.

   표시되는 옵션은 제공된 서비스의 가능성에 따라 다릅니다. 여기에는 다음이 포함될 수 있습니다.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody>
    <tr>
    <td>[!UICONTROL From now on] (기본)</td>
    <td>이 옵션을 선택한 후 설정에 따라 추가되거나 업데이트된 모든 번들을 검색합니다.</td>
    </tr>
     <tr>
    <td>[!UICONTROL Since specific date]</td>
    <td>지정된 날짜 및 시간 이후에 추가되거나 업데이트된 모든 번들(설정에 따라 다름)을 검색합니다.</td>
      </tr>
      <tr>
    <td>[!UICONTROL All]</td>
    <td>사용 가능한 모든 번들 검색</td>
     </tr>
      <tr>
    <td>[!UICONTROL Choose manually]</td>
    <td>번들 검색을 시작할 첫 번째 번들을 선택할 수 있습니다.</td>
     </tr>
     </tbody>
   </table>



   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>새 [!DNL DocuSign] 연결의 이름 입력</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>연결할 계정이 프로덕션 계정인지 데모 계정인지 선택합니다.</td> 
     </tr> 
    </tbody> 
   </table>


