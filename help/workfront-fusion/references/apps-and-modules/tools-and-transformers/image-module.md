---
title: 이미지 모듈
description: Adobe Workfront Fusion 이미지 모듈을 사용하면 특정 이미지(치수, 유형 등)에 대한 정보를 얻고, 이미지를 다른 파일 형식으로 변환하고, 이미지 크기를 직접 변경할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# 이미지 모듈

[!DNL Adobe Workfront Fusion] [!UICONTROL Image] 모듈을 사용하면 특정 이미지(치수, 유형 등)에 대한 정보를 얻고, 이미지를 다른 파일 형식으로 변환하고, 이미지 크기를 직접 변경할 수 있습니다.

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

## [!UICONTROL Image]개 모듈 및 해당 필드

이 모듈을 구성할 때 다음 필드가 표시됩니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

* [[!UICONTROL Resize]](#resize)
* [[!UICONTROL Convert a format]](#convert-a-format)
* [[!UICONTROL Extract metadata]](#extract-metadata)

### [!UICONTROL Resize]

이 변환기 모듈은 지정한 기준에 따라 이미지의 높이와 너비를 변경합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>변환할 이미지의 소스를 선택합니다. 이전 모듈에서 출력을 선택하거나 데이터 파일과 파일 이름을 매핑할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>변환할 파일을 매핑합니다. [!UICONTROL Source file] 필드에서 [!UICONTROL Map]을(를) 선택한 경우 이 필드를 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>변환된 파일의 이름을 입력합니다. [!UICONTROL Source file] 필드에서 [!UICONTROL Map]을(를) 선택한 경우 이 필드를 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to]</td> 
   <td>높이-너비 비율을 유지할지 또는 치수를 지정된 높이 및 너비로 변경할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL According to]</td> 
   <td> <p>모듈에서 이미지의 새 크기를 결정하는 방법을 선택합니다. 이 필드는 I want(높이-폭) 필드에서 높이-폭 비율을 유지하도록 선택한 경우에 나타납니다. 다른 필드는 이 필드의 선택 사항을 기반으로 표시됩니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Maximum width]</p> <p>이미지를 지정한 너비로 줄입니다. 높이는 자동으로 계산됩니다.</p> </li> 
     <li> <p>[!UICONTROL Maximum height]</p> <p>이미지를 지정한 높이로 줄입니다. 너비는 자동으로 계산됩니다.</p> </li> 
     <li> <p>[!UICONTROL Maximum height or width]</p> <p>높이 및 너비가 지정한 값을 초과하지 않도록 이미지를 줄입니다. 이 옵션은 높이-폭 비율을 유지하므로 치수 중 하나가 지정된 것보다 작을 수 있습니다. 예를 들어 높이와 너비를 모두 40으로 지정하면 400x300 이미지가 40X30으로 줄어듭니다.</p> </li> 
     <li> <p>[!UICONTROL Minimum width]</p> <p>지정한 너비로 이미지를 확대합니다. 높이는 자동으로 계산됩니다.</p> </li> 
     <li> <p>[!UICONTROL Minimum height]</p> <p>지정한 높이까지 이미지를 확대합니다. 너비는 자동으로 계산됩니다.</p> </li> 
     <li> <p>[!UICONTROL Minimum height or width]</p> <p>높이 및 너비가 사용자가 지정한 값보다 작지 않도록 이미지를 확대합니다. 이 옵션은 높이-폭 비율을 유지하므로 치수 중 하나가 지정된 것보다 클 수 있습니다. 예를 들어 높이와 너비를 모두 300으로 지정하면 40x30 이미지가 400X300으로 확대됩니다.</p> </li> 
     <li> <p>[!UICONTROL Percent]</p> <p>지정한 값을 기준으로 이미지 크기를 백분율로 변경합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Width]</td> 
   <td>크기 조정된 이미지의 원하는 너비를 픽셀 단위로 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Height]</td> 
   <td>크기 조정된 이미지의 원하는 높이를 픽셀 단위로 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert a format]

이 변환기 모듈은 이미지 파일의 형식을 변경합니다. 이 모듈은 다음 형식과 호환됩니다.

* PNG
* JPG
* GIF
* BMP

소스 파일과 출력은 모두 다음 형식 중 하나여야 합니다. 예를 들어 [!UICONTROL Image] >[!UICONTROL Convert a format] 모듈은 PNG 파일을 BMP 파일로 변환하거나 BMP를 JPG으로 변환할 수 있습니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>변환할 이미지의 소스를 선택합니다. 이전 모듈에서 출력을 선택하거나 데이터 파일과 파일 이름을 매핑할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>변환할 파일을 매핑합니다. [!UICONTROL Source file] 필드에서 [!UICONTROL Map]을(를) 선택한 경우 이 필드를 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>변환된 파일의 이름을 입력합니다. [!UICONTROL Source file] 필드에서 [!UICONTROL Map]을(를) 선택한 경우 이 필드를 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output format]</td> 
   <td>모듈이 소스 파일을 변환할 형식을 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extract metadata]

이 변환기 모듈은 모듈에 대한 기본 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>변환할 이미지의 소스를 선택합니다. 이전 모듈에서 출력을 선택하거나 데이터 파일과 파일 이름을 매핑할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>변환할 파일을 매핑합니다. [!UICONTROL Source file] 필드에서 맵을 선택한 경우 이 필드를 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>변환된 파일의 이름을 입력합니다. [!UICONTROL Source file] 필드에서 맵을 선택한 경우 이 필드를 사용할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

## 가능한 문제

### 작업이 오류와 함께 종료됨

작업을 오류와 함께 종료할 수 있는 세 가지 경우가 있습니다.

* 받은 데이터가 JPG/GIF/PNG/BMP 형식이 아닙니다.
* 이미지 크기를 변경하는 동안 최대 너비/높이 제한을 초과했습니다. 이미지 크기는 너비 3840px, 높이 2160px를 초과할 수 없습니다.
* 이미지의 크기 또는 형식을 변경하는 동안 이미지의 최대 허용 크기를 초과했습니다.
