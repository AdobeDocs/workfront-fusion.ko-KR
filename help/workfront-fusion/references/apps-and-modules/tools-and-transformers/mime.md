---
title: MIME 모듈
description: Adobe Workfront Fusion에서 MIME 유형을 사용할 수 있습니다. MIME(Multipurpose Internet Mail Extension) 유형은 소프트웨어가 인터넷에서 공유되는 다른 유형의 데이터를 식별할 수 있도록 하는 레이블입니다. 웹 서버 및 브라우저는 MIME 유형을 사용하여 파일로 수행할 작업을 결정합니다. 예를 들어 MIME 유형 text/html이 있는 파일은 MIME 유형 image/jpeg가 있는 파일과 다르게 브라우저에서 처리됩니다. MIME 유형은 운영 체제 및 하드웨어에 관계없이 작동합니다.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# [!UICONTROL MIME]개 모듈

Adobe Workfront Fusion에서 MIME 유형을 사용할 수 있습니다. MIME(Multipurpose Internet Mail Extension) 유형은 소프트웨어가 인터넷에서 공유되는 다른 유형의 데이터를 식별할 수 있도록 하는 레이블입니다. 웹 서버 및 브라우저는 MIME 유형을 사용하여 파일로 수행할 작업을 결정합니다. 예를 들어 MIME 형식이 `text/html`인 파일은 MIME 형식이 `image/jpeg`인 파일과 다르게 브라우저에서 처리됩니다. MIME 유형은 운영 체제 및 하드웨어에 관계없이 작동합니다.

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

## [!UICONTROL MIME]개 모듈 및 해당 필드

### [!UICONTROL Get a MIME type]

이 변환기 모듈은 지정된 이름, 경로 또는 확장과 연결된 MIME 유형을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL File]</td> 
   <td> <p>MIME 유형을 결정할 파일을 입력하거나 매핑합니다. </p> <p>다음을 사용하여 파일을 입력할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File path]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File name]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File extension]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a file extension]

이 변환기 모듈은 지정된 MIME 유형에 대한 원본 파일 확장명을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td> <p>파일 확장자를 결정할 MIME 유형을 입력하거나 매핑합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
