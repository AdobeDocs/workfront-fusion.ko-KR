---
title: Markdown 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Markdown 모듈을 사용하여 Markdown을 HTML으로, HTML을 Markdown으로 변환할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: f1134bbf-c244-4f52-8744-f97453b2ce8a
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# [!UICONTROL Markdown]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!UICONTROL Markdown] 모듈을 사용하여 Markdown을 HTML으로, HTML을 Markdown으로 변환할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합을 위한 [!UICONTROL [!DNL Workfront Fusion]] </p>
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

## [!UICONTROL Markdown to HTML]

이 모듈은 Markdown을 HTML으로 변환합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Markdown]</td> 
   <td> <p>Markdown 형식의 일반 텍스트를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL GitHub Flavored Markdown] </td> 
   <td> <p>HTML GitHub 버전의 Markdown을 Markdown으로 변환하려면 이 옵션을 활성화하십시오.</p> <p>자세한 내용은 [!DNL GitHub] 설명서의 3월[!DNL ]다운 치트시트를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sanitize]</td> 
   <td>옵션을 선택하여 텍스트에서 HTML 태그를 제거할지 또는 Esc HTML을 제거할지를 지정합니다.</td> 
  </tr> 
 </tbody> 
</table>

## [!UICONTROL HTML to Markdown]

이 모듈은 HTML 코드를 Markdown으로 변환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Markdown]</td> 
   <td> <p>Markdown으로 변환할 HTML 코드를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL GitHub Flavored Markdown] </td> 
   <td> <p>HTML을 [!DNL GitHub Flavored Markdown](으)로 변환하려면 이 옵션을 활성화하십시오.</p> <p>자세한 내용은 [!DNL GitHub] 설명서에서 Markdown 치트시트를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>
