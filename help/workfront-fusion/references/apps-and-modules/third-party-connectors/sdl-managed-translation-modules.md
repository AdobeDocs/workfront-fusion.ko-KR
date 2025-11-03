---
title: SDL 관리 번역 모듈
description: Adobe Workfront Fusion 시나리오에서는 SDL Managed Translation 계정을 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 1%

---

# [!DNL SDL Managed Translation]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL SDL Managed Translation] 계정을 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>작업 기반: Workfront Fusion 라이센스 요구 사항 없음</p>
   <p>커넥터 기반(레거시): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

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

#### [!UICONTROL 번역된 파일 다운로드]

이 모듈은 지정된 프로젝트 내에 포함된 번역된 단일 파일의 콘텐츠를 검색합니다. 요청된 파일이 아직 다운로드 상태가 아닌 경우 파일의 콘텐츠가 아직 완전히 번역되지 않았을 수 있습니다. 파일이 다운로드 상태이고 성공적으로 검색한 경우 `Cancel or Complete File` 메서드를 사용하여 파일을 완료된 것으로 표시해야 합니다.

#### [!UICONTROL 파일 업로드]

이 모듈에서는 번역용 또는 번역 프로젝트에 참조 자료로 포함할 파일을 업로드할 수 있습니다. 업로드는 다중 파트/양식 데이터를 사용하여 제출해야 하며 둘 이상의 파일을 포함할 수 있습니다. 업로드된 파일을 평가하는 데 사용해야 하는 `ProjectOptionId`을(를) 지정합니다. 이렇게 하면 업로드하는 각 파일이 번역을 위해 가능한 후보인지 또는 참조 자료로 처리해야 하는지 여부를 결정합니다. 아카이브(`zip `, `rar`, `7z`, `tar` 파일)의 경우 앱은 아카이브 내용을 검사하고 아카이브를 전체적으로 번역할 수 있는지 여부 또는 번역 가능한 파일과 번역할 수 없는 파일이 혼합되어 있는지 여부를 나타냅니다.

>[!NOTE]
>
>한 번에 두 개 이상의 파일을 업로드하면 실패의 영향을 높일 수 있으므로 권장되지 않습니다.

#### [!UICONTROL 참조 파일 추가]

이 모듈은 참조 파일을 추가합니다.

### 프로젝트

#### [!UICONTROL 프로젝트 만들기]

이 모듈은 지정된 프로젝트를 만듭니다.

#### 프로젝트 취소 또는 완료

이 모듈은 지정된 프로젝트를 취소하거나 완료합니다. 프로젝트가 다운로드 대기 중인 경우 워크플로의 마지막 단계를 통해 프로젝트가 전환되고 결국 완료로 이동합니다. 프로젝트가 승인 대기 중이거나 공급업체 선택이 취소된 경우. 프로젝트가 다른 상태에 있으면 요청이 실패합니다.

#### [!UICONTROL 프로젝트 Zip 다운로드]

이 모듈은 지정된 프로젝트에 대해 번역된 파일의 `zip` 파일을 가져옵니다.

#### [!UICONTROL 프로젝트 읽기]

이 모듈은 지정된 프로젝트를 가져옵니다.

#### [!UICONTROL 상태에서 프로젝트 가져오기]

이 모듈은 지정된 상태에서 사용 가능한 모든 프로젝트를 가져옵니다. 이 메서드를 사용하면 `$top`, `$skip` 및 `$orderby` 쿼리 매개 변수를 지정하여 결과를 페이징할 수 있습니다.

#### [!UICONTROL 프로젝트 목록 가져오기]

각 프로젝트에 대한 일반 정보를 제공하여 모든 프로젝트의 간단한 목록을 가져옵니다. 이 메서드를 사용하면 `$top`, `$skip` 및 `$orderby` 쿼리 매개 변수를 지정하여 결과를 페이지로 만들 수 있습니다.

#### [!UICONTROL 프로젝트 만들기 옵션 검색]

이 모듈에서는 프로젝트 만들기 옵션을 가져옵니다.

### 기타

#### [!UICONTROL API 호출 만들기]

이 모듈은 임의의 승인된 API 호출을 수행합니다.
