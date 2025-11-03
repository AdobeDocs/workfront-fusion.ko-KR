---
title: MIME 모듈
description: Adobe Workfront Fusion에서 MIME 유형을 사용할 수 있습니다. MIME(Multipurpose Internet Mail Extension) 유형은 소프트웨어가 인터넷에서 공유되는 다른 유형의 데이터를 식별할 수 있도록 하는 레이블입니다. 웹 서버 및 브라우저는 MIME 유형을 사용하여 파일로 수행할 작업을 결정합니다. 예를 들어 MIME 유형 text/html이 있는 파일은 MIME 유형 image/jpeg가 있는 파일과 다르게 브라우저에서 처리됩니다. MIME 유형은 운영 체제 및 하드웨어에 관계없이 작동합니다.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# [!UICONTROL MIME] 모듈

Adobe Workfront Fusion에서 MIME 유형을 사용할 수 있습니다. MIME(Multipurpose Internet Mail Extension) 유형은 소프트웨어가 인터넷에서 공유되는 다른 유형의 데이터를 식별할 수 있도록 하는 레이블입니다. 웹 서버 및 브라우저는 MIME 유형을 사용하여 파일로 수행할 작업을 결정합니다. 예를 들어 MIME 형식이 `text/html`인 파일은 MIME 형식이 `image/jpeg`인 파일과 다르게 브라우저에서 처리됩니다. MIME 유형은 운영 체제 및 하드웨어에 관계없이 작동합니다.

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



## [!UICONTROL MIME] 모듈 및 해당 필드

* [파일 확장명 가져오기](#get-a-file-extension)
* [MIME 유형 가져오기](#get-a-mime-type)

### [!UICONTROL 파일 확장명 가져오기]

이 변환기 모듈은 지정된 MIME 유형에 대한 원본 파일 확장명을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td> <p>파일 확장자를 결정할 MIME 유형을 입력하거나 매핑합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL MIME 유형 가져오기]

이 변환기 모듈은 지정된 파일 이름, 경로 또는 확장명과 연결된 MIME 유형을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일]</td> 
   <td> <p>MIME 유형을 결정할 파일을 입력하거나 매핑합니다. </p> <p>다음을 사용하여 파일을 입력할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 파일 경로]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL 파일 이름]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL 파일 확장명]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
