---
title: 시나리오에 모듈 추가
description: 이 문서에서는 시나리오에 모듈을 추가하는 기본 프로세스에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
TQID: 'https://experienceleague.adobe.com/R2JCX7aaYzmYHgiLqj1WDlVFHI-s-qanltoOrycQ5JU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 8%
---
# 시나리오에 모듈 추가

시나리오는 앱 내에서 데이터를 변환하거나 앱과 웹 서비스 간에 전송하는 방법을 나타내는 일련의 모듈로 구성됩니다. 모듈을 추가하고 구성하여 모듈을 빌드합니다.

이 문서에서는 시나리오에 모듈을 추가하는 기본 프로세스에 대해 설명합니다. 시나리오를 추가하는 방법에 대한 자세한 지침은 [모듈 추가: 문서 인덱스](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)의 다른 문서를 참조하십시오.

>[!NOTE]
>
>Workfront Fusion에서 시나리오 편집기를 새 경험으로 전환합니다. 이 전환 중에 클래식 경험과 새 경험을 모두 사용할 수 있으며 언제든지 전환할 수 있습니다. 새 경험을 사용하는 것이 좋습니다. 자세한 내용은 문서 시나리오 편집기에서 [새 경험 및 클래식 경험](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)을 참조하십시오.

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 시나리오에 첫 번째 모듈 추가

시나리오의 첫 번째 모듈은 일반적으로 트리거 모듈입니다.

트리거 모듈에 대한 자세한 내용은 문서 모듈 개요에서 [트리거 모듈](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)을(를) 참조하십시오.

* [새 경험에서 첫 번째 모듈 추가(권장)](#add-the-first-module-in-the-new-experience-recommended)
* [클래식 경험의 첫 번째 모듈 추가](#add-the-first-module-in-the-classic-experience)

### 새 경험에서 첫 번째 모듈 추가(권장)

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 화면 오른쪽 상단의 **새 시나리오 만들기**&#x200B;를 클릭하여 시나리오 만들기를 시작합니다.

   자리 표시자 모듈과 사용 가능한 커넥터 목록이 있는 시나리오 편집기가 열립니다.

   ![자리 표시자 모듈](/help/workfront-fusion/build-practice-scenarios/assets/new-placeholder-module.png)

   ![앱 및 서비스 선택기](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. 이 시나리오를 시작할 커넥터 또는 웹후크 선택:

   * 왼쪽의 패널을 사용하여 카테고리별로 찾아보거나([!UICONTROL 즐겨찾기], [!UICONTROL 모든 앱], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative 및 콘텐츠], [!UICONTROL Adobe 클라우드 서비스], [!UICONTROL 생성 AI] 또는 [!UICONTROL 기본 제공])
   * 검색 상자에 용어를 입력합니다. 입력할 때 결과가 업데이트되고, 모듈 이름과 설명이 일치하기 전에 커넥터 일치가 나열됩니다.

1. 시나리오에 추가할 모듈을 클릭합니다.

1. 모듈을 구성합니다.

   모듈의 설정이 캔버스의 오른쪽에 있는 패널에서 열립니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>* 커넥터 목록에서 배지는 비공개, 프리미엄 및 베타 앱을 식별합니다.
>* 대형 앱용 모듈은 그룹으로 구성됩니다.
>* 오류 핸들러를 추가하면 지시문이 먼저 나열됩니다.
>* 커넥터의 버전이 두 개 이상인 경우 커넥터를 선택한 후 버전을 선택할 수 있습니다.

>[!NOTE]
>
>시나리오에서 첫 번째 모듈을 제거했으며 교체하려면 자리 표시자 모듈을 클릭하여 커넥터 목록을 엽니다.

### 클래식 경험의 첫 번째 모듈 추가

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 화면 오른쪽 상단의 **새 시나리오 만들기**&#x200B;를 클릭하여 시나리오 만들기를 시작합니다.

   자리 표시자(물음표) 모듈과 사용 가능한 커넥터 목록이 있는 시나리오 편집기가 열립니다.

   ![자리 표시자 모듈](assets/placeholder-module.png)

1. 이 시나리오를 시작할 커넥터 또는 웹후크를 선택합니다. 목록의 검색 창에 커넥터 이름을 입력하여 목록을 필터링할 수 있습니다.
1. 모듈을 구성합니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>시나리오에서 첫 번째 모듈을 제거했으며 교체하려면 자리 표시자(물음표) 모듈을 클릭하여 커넥터 목록을 엽니다.

## 시나리오에 다른 모듈 추가

* [새 경험에서 다른 모듈 추가(권장)](#add-another-module-in-the-new-experience-recommended)
* [클래식 경험에서 다른 모듈 추가](#add-another-module-in-the-classic-experience)

### 새 경험에서 다른 모듈 추가(권장)

1. 모듈을 추가할 시나리오의 시나리오 편집기에 없는 경우 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 다른 모듈 뒤에 모듈을 추가하려면 모듈을 추가할 모듈의 오른쪽 가장자리를 마우스로 가리킨 다음 모듈이 나타나면 **다른 모듈 추가**&#x200B;를 클릭합니다.

   커넥터 목록이 열리고 시나리오에 이미 사용된 커넥터가 표시됩니다.

1. (선택 사항) 다른 커넥터를 선택하려면 목록에서 **다른 모듈 추가**&#x200B;를 클릭한 다음 커넥터를 선택합니다.

   * 왼쪽의 패널을 사용하여 카테고리별로 찾아보거나([!UICONTROL 즐겨찾기], [!UICONTROL 모든 앱], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative 및 콘텐츠], [!UICONTROL Adobe 클라우드 서비스], [!UICONTROL 생성 AI] 또는 [!UICONTROL 기본 제공])
   * 검색 상자에 용어를 입력합니다. 입력할 때 결과가 업데이트되고, 모듈 이름과 설명이 일치하기 전에 커넥터 일치가 나열됩니다.

1. 시나리오에 추가할 모듈을 클릭합니다.

1. 모듈을 구성합니다.

   모듈의 설정이 캔버스의 오른쪽에 있는 패널에서 열립니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

### 클래식 경험에서 다른 모듈 추가

1. 모듈을 추가할 시나리오의 시나리오 편집기에 없는 경우 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 다른 모듈에 모듈을 추가하려면 모듈을 추가할 모듈의 오른쪽 핸들을 마우스로 가리킨 다음 모듈이 나타나면 **다른 모듈 추가**&#x200B;를 클릭합니다.

   커넥터 목록이 열리고 시나리오에 이미 사용된 커넥터가 표시됩니다.

1. (선택 사항) 다른 커넥터를 선택하려면 목록에서 **다른 모듈 추가**&#x200B;를 클릭한 다음 커넥터를 선택합니다. 목록의 검색 창에 커넥터 이름을 입력하여 목록을 필터링할 수 있습니다.
1. 모듈을 구성합니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## 시나리오의 기존 모듈 사이에 모듈 삽입

* [새 경험에 모듈 삽입(권장)](#insert-a-module-in-the-new-experience-recommended)
* [클래식 경험에 모듈 삽입](#insert-a-module-in-the-classic-experience)

### 새 경험에 모듈 삽입(권장)

1. 모듈을 추가할 시나리오의 시나리오 편집기에 없는 경우 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 모듈을 삽입할 모듈 사이의 경로를 마우스 오른쪽 단추로 클릭한 다음 **모듈 추가**&#x200B;를 선택합니다.

   ![기존 모듈 사이에 모듈 추가](assets/add-a-module-between-modules.png)

   커넥터 목록이 열리고 시나리오에 이미 사용된 커넥터가 표시됩니다.

1. (선택 사항) 다른 커넥터를 선택하려면 목록에서 **다른 모듈 추가**&#x200B;를 클릭한 다음 커넥터를 선택합니다.

   * 왼쪽의 패널을 사용하여 카테고리별로 찾아보거나([!UICONTROL 즐겨찾기], [!UICONTROL 모든 앱], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative 및 콘텐츠], [!UICONTROL Adobe 클라우드 서비스], [!UICONTROL 생성 AI] 또는 [!UICONTROL 기본 제공])
   * 검색 상자에 용어를 입력합니다. 입력할 때 결과가 업데이트되고, 모듈 이름과 설명이 일치하기 전에 커넥터 일치가 나열됩니다.

1. 시나리오에 추가할 모듈을 클릭합니다.

1. 모듈을 구성합니다.

   모듈의 설정이 캔버스의 오른쪽에 있는 패널에서 열립니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>특정 모듈에 대한 링크를 만들려면 다음 페이지를 볼 때 URL에 `?moduleId=<module-id>`을(를) 추가하십시오.
>
>* 시나리오 편집 페이지(URL이 `/edit`에 끝남)
>* 특정 시나리오 실행(URL이 `/logs/<log-id>`에 끝남)
>
>`<module-id>`은(는) 시나리오를 볼 때 모듈 레이블 옆에 있는 숫자를 참조합니다.
>
>이 기능은 시나리오를 디버깅하거나 모듈 구성을 복사할 때 유용합니다.

### 클래식 경험에 모듈 삽입

1. 모듈을 추가할 시나리오의 시나리오 편집기에 없는 경우 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 모듈을 삽입할 모듈 사이의 점선 경로를 클릭합니다.
1. 표시되는 메뉴에서 **모듈 추가**&#x200B;를 선택합니다.

커넥터 목록이 열리고 시나리오에 이미 사용된 커넥터가 표시됩니다.

1. (선택 사항) 다른 커넥터를 선택하려면 목록에서 **다른 모듈 추가**&#x200B;를 클릭한 다음 커넥터를 선택합니다. 목록의 검색 창에 커넥터 이름을 입력하여 목록을 필터링할 수 있습니다.
1. 모듈을 구성합니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>특정 모듈에 대한 링크를 만들려면 다음 페이지를 볼 때 URL에 `?moduleId=<module-id>`을(를) 추가하십시오.
>
>* 시나리오 편집 페이지(URL이 `/edit`에 끝남)
>* 특정 시나리오 실행(URL이 `/logs/<log-id>`에 끝남)
>
>`<module-id>`은(는) 시나리오를 볼 때 모듈 레이블 옆에 있는 숫자를 참조합니다.
>
>이 기능은 시나리오를 디버깅하거나 모듈 구성을 복사할 때 유용합니다.
