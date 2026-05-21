---
title: Allocadia 모듈
description: Adobe Workfront Fusion 시나리오에서는 Allocadia를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
TQID: https://experienceleague.adobe.com/bCfkq5fzw21hmZWLrWztL27g2RAlBbyk9vPEQ-v6bBU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1467
ht-degree: 56%

---

# [!DNL Allocadia] 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Allocadia]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

시나리오 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 색인](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>작업 기반: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Allocadia] 모듈을 사용하려면 [!DNL Allocadia] 계정이 있어야 합니다.

## [!DNL Allocadia] API 정보

Allocadia 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.7.6</td> 
  </tr>
 </tbody> 
</table>

## [!DNL Allocadia]를 Workfront Fusion에 연결

[!DNL Allocadia] 모듈 내에서 직접 [!DNL Allocadia] 계정에 연결할 수 있습니다.

1. [!DNL Allocadia] 모듈에서 [!UICONTROL 연결] 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 북미 서버를 사용할지 유럽 서버를 사용할지 선택합니다.
1. 사용자 이름과 암호를 입력합니다.
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

## [!DNL Allocadia] 모듈 및 해당 필드

[!DNL Allocadia] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL Allocadia] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

#### [!UICONTROL 레코드 보기]

이 트리거 모듈은 특정 유형의 오브젝트가 추가되거나 업데이트되거나 둘 다 사용될 때 시나리오를 실행합니다. 모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>Allocadia 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect Allocadia]를 Workfront Fusion</a>에 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">필터</td> 
   <td> <p>시나리오가 새 레코드만 볼 것인지 업데이트된 레코드만 볼 것인지 새 레코드와 업데이트된 레코드를 볼 것인지를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">엔티티 유형</td> 
   <td>모듈에서 감시할 Allocadia 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다. 사용 가능한 필드는 선택한 엔티티 유형에 따라 다릅니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제한</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 지켜볼 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [사용자 정의 API 호출](#custom-api-call)
* [레코드 읽기](#read-record)
* [레코드 만들기](#create-record)
* [레코드 삭제](#delete-record)
* [레코드 업데이트](#update-record)

#### [!UICONTROL 사용자 정의 API 호출]

이 액션 모듈을 사용하면 [!DNL Allocadia] API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Allocadia] 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

작업은 지정한 엔티티 유형(Allocadia 객체 유형)을 기반으로 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Allocadia] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Allocadia] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://api-na.allocadia.com/{version}</code> 또는 <code>https://api-eu.allocadia.com/{version}</code>과(와) 관련된 경로를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>예: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 읽기]

이 작업 모듈은 [!DNL Allocadia]의 단일 레코드에서 데이터를 읽습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Allocadia] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Allocadia] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 엔티티 유형]</td> 
   <td>모듈에서 읽을 [!DNL Allocadia] 레코드의 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다. 사용 가능한 필드는 선택한 [!UICONTROL Entity Type]에 따라 다릅니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>모듈에서 읽을 레코드의 고유 [!DNL Allocadia] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 만들기]

이 작업 모듈은 레코드를 만듭니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Allocadia] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Allocadia] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 엔티티 유형]</td> 
   <td>라인 항목 또는 열 선택에 따라 새 레코드를 생성할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 예산]</td> 
   <td> <p>레코드를 생성할 예산을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Column choices]</td> 
   <td>새 레코드를 만드는 데 사용할 열을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Label]</td> 
   <td>새 레코드에 대한 레이블 입력 또는 매핑</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 삭제]

이 작업 모듈은 특정 레코드를 삭제합니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Allocadia] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Allocadia] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 엔티티 유형]</td> 
   <td> <p>삭제할 엔티티 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 라인 항목]</strong> </p> <p>라인 항목 ID 입력</p> </li> 
     <li> <p><strong>[!UICONTROL 열 선택]</strong> </p> <p>레코드를 삭제할 예산을 선택한 다음 열 ID와 선택 ID를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 예측 태그]</strong> </p> <p>레코드를 삭제할 예산을 선택한 다음 태그 ID를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 업데이트]

이 작업 모듈은 라인 항목, 사용자 또는 열 선택과 같은 레코드를 업데이트합니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!UICONTROL Allocadia] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Allocadia] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 엔티티 유형]</td> 
   <td>모듈을 업데이트할 [!DNL Allocadia] 레코드의 형식을 선택하십시오. 다른 필드는 선택한 엔티티 유형에 따라 나타납니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 예산]</td> 
   <td> <p>레코드를 갱신할 예산을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

#### [!UICONTROL 레코드 검색]

이 검색 모듈은 지정한 검색 쿼리와 일치하는 [!DNL Allocadia]의 개체에서 레코드를 찾습니다.

시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

원하는 레코드 유형을 지정합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Allocadia] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Allocadia] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 엔티티 유형]</td> 
   <td>모듈에서 검색할 [!DNL Allocadia] 레코드의 형식을 선택하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 예산]</td> 
   <td> <p>검색할 예산을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 결과 집합]</td> 
   <td>모듈이 모든 일치 레코드를 반환할지, 첫 번째 일치 레코드만 반환할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드의 최대 개수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 검색 기준]</td> 
   <td>검색할 필드를 선택하고 작업을 선택한 다음 검색할 값을 입력하거나 매핑합니다. [!DNL AND] 또는 [!DNL OR] 규칙을 추가하여 검색을 추가로 필터링할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다. 사용 가능한 필드는 선택한 엔티티 유형에 따라 다릅니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
