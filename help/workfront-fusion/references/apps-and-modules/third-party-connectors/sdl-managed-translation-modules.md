---
title: SDL 관리 번역 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 SDL Managed Translation 계정을 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# [!DNL SDL Managed Translation]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL SDL Managed Translation] 계정을 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

## SDL Managed Translation API 정보

SDL Managed Translation 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>https://languagecloud.sdl.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.4.26</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL SDL Managed Translation]개 모듈

>[!NOTE]
>
>[!DNL SDL Managed Translation] 호출에 대한 작업 시간 제한은 **120초**&#x200B;입니다.

### 파일

#### [!UICONTROL Download Translated File]

이 모듈은 지정된 프로젝트 내에 포함된 번역된 단일 파일의 콘텐츠를 검색합니다. 요청된 파일이 아직 다운로드 상태가 아닌 경우 파일의 콘텐츠가 아직 완전히 번역되지 않았을 수 있습니다. 파일이 다운로드 상태이고 성공적으로 검색한 경우 `Cancel or Complete File` 메서드를 사용하여 파일을 완료된 것으로 표시해야 합니다.

#### [!UICONTROL Upload a File]

이 모듈에서는 번역용 또는 번역 프로젝트에 참조 자료로 포함할 파일을 업로드할 수 있습니다. 업로드는 다중 파트/양식 데이터를 사용하여 제출해야 하며 둘 이상의 파일을 포함할 수 있습니다. 업로드된 파일을 평가하는 데 사용해야 하는 `ProjectOptionId`을(를) 지정합니다. 이렇게 하면 업로드하는 각 파일이 번역을 위해 가능한 후보인지 또는 참조 자료로 처리해야 하는지 여부를 결정합니다. 아카이브(`zip `, `rar`, `7z`, `tar` 파일)의 경우 앱은 아카이브 내용을 검사하고 아카이브를 전체적으로 번역할 수 있는지 여부 또는 번역 가능한 파일과 번역할 수 없는 파일이 혼합되어 있는지 여부를 나타냅니다.

>[!NOTE]
>
>한 번에 두 개 이상의 파일을 업로드하면 실패의 영향을 높일 수 있으므로 권장되지 않습니다.

#### [!UICONTROL Add a Reference File]

이 모듈은 참조 파일을 추가합니다.

### 프로젝트

#### [!UICONTROL Create a project]

이 모듈은 지정된 프로젝트를 만듭니다.

#### 프로젝트 취소 또는 완료

이 모듈은 지정된 프로젝트를 취소하거나 완료합니다. 프로젝트가 다운로드 대기 중인 경우 워크플로의 마지막 단계를 통해 프로젝트가 전환되고 결국 완료로 이동합니다. 프로젝트가 승인 대기 중이거나 공급업체 선택이 취소된 경우. 프로젝트가 다른 상태에 있으면 요청이 실패합니다.

#### [!UICONTROL Download Project Zip]

이 모듈은 지정된 프로젝트에 대해 번역된 파일의 `zip` 파일을 가져옵니다.

#### [!UICONTROL Read a Project]

이 모듈은 지정된 프로젝트를 가져옵니다.

#### [!UICONTROL Get Projects at Status]

이 모듈은 지정된 상태에서 사용 가능한 모든 프로젝트를 가져옵니다. 이 메서드를 사용하면 `$top`, `$skip` 및 `$orderby` 쿼리 매개 변수를 지정하여 결과를 페이징할 수 있습니다.

#### [!UICONTROL Get Projects List]

각 프로젝트에 대한 일반 정보를 제공하여 모든 프로젝트의 간단한 목록을 가져옵니다. 이 메서드를 사용하면 `$top`, `$skip` 및 `$orderby` 쿼리 매개 변수를 지정하여 결과를 페이지로 만들 수 있습니다.

#### [!UICONTROL Search Project Creation Options]

이 모듈에서는 프로젝트 만들기 옵션을 가져옵니다.

### 기타

#### [!UICONTROL Make an API Call]

이 모듈은 임의의 승인된 API 호출을 수행합니다.
