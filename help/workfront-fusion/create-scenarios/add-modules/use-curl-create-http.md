---
title: cURL을 사용하여 HTTP 모듈 추가
description: cURL 요청을 시나리오에 붙여 넣을 수 있으며, Fusion은 cURL 요청에서 구성된 HTTP 모듈을 만듭니다.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# cURL을 사용하여 HTTP 모듈 추가

cURL 요청을 시나리오에 붙여 넣을 수 있으며, Fusion은 cURL 요청에서 구성된 HTTP 모듈을 만듭니다.

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

## cURL 요청에서 HTTP 모듈 만들기


cURL을 사용하여 HTTP 모듈을 만들려면 다음을 수행하십시오.

1. 텍스트 편집기에서와 같이 Fusion 외부에 cURL 요청 텍스트를 만듭니다.
1. cURL 요청을 클립보드에 복사합니다.
1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 모듈을 만들 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 시나리오 편집기에서 공백을 마우스 오른쪽 단추로 클릭하고 **붙여넣기**&#x200B;를 선택합니다.

   또는

   Ctrl + V (Windows) 또는 Cmd + V (Mac)를 누릅니다.


   HTML 모듈이 만들어집니다.
1. 모듈을 드래그하여 시나리오에 연결합니다.

## 문제 해결

cURL을 시나리오에 붙여 넣을 수 없는 경우 브라우저 설정을 확인하여 클립보드에서 붙여 넣기가 활성화되어 있는지 확인하십시오.
