---
title: cURL을 사용하여 HTTP 모듈 추가
description: cURL 요청을 시나리오에 붙여 넣을 수 있으며, Fusion은 cURL 요청에서 구성된 HTTP 모듈을 만듭니다.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 2%

---

# cURL을 사용하여 HTTP 모듈 추가

cURL 요청을 시나리오에 붙여 넣을 수 있으며, Fusion은 cURL 요청에서 구성된 HTTP 모듈을 만듭니다.

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

## cURL 요청에서 HTTP 모듈 만들기


cURL을 사용하여 HTTP 모듈을 만들려면 다음을 수행하십시오.

1. 텍스트 편집기에서와 같이 Fusion 외부에 cURL 요청 텍스트를 만듭니다.
1. cURL 요청을 클립보드에 복사합니다.
1. 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 모듈을 만들 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 시나리오 편집기에서 공백을 마우스 오른쪽 단추로 클릭하고 **붙여넣기**&#x200B;를 선택합니다.

   또는

   Ctrl + V (Windows) 또는 Cmd + V (Mac)를 누릅니다.


   HTML 모듈이 만들어집니다.
1. 모듈을 드래그하여 시나리오에 연결합니다.

## 문제 해결

cURL을 시나리오에 붙여 넣을 수 없는 경우 브라우저 설정을 확인하여 클립보드에서 붙여 넣기가 활성화되어 있는지 확인하십시오.
