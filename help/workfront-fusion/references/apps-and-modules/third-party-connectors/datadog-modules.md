---
title: Datadog 모듈
description: Adobe Workfront Fusion 시나리오에서는 Datadog를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 1%

---

# [!DNL Datadog]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Datadog]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

## 전제 조건

[!DNL Datadog] 모듈을 사용하려면 [!DNL Datadog] 계정이 있어야 합니다.

## Datadog API 정보

Datadog 커넥터에서는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>1.0.11</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL Datadog] 연결 {#connect-datadog-to-workfront-fusion}

### API 키 및 애플리케이션 키 검색 {#retrieve-your-api-key-and-application-key}

[!DNL Datadog] 계정을 Workfront Fusion에 연결하려면 [!DNL Datadog] 계정에서 API 키 및 응용 프로그램 키를 검색해야 합니다.

1. [!DNL Datadog] 계정에 로그인합니다.
1. 왼쪽 탐색 패널에서 **[!UICONTROL 통합]**&#x200B;을 클릭한 다음 **[!UICONTROL API]**&#x200B;를 클릭합니다.
1. 기본 화면에서 **[!UICONTROL API 키]**&#x200B;를 클릭합니다.
1. 보라색 막대 위로 마우스를 가져가 API 키를 표시합니다.
1. API 키를 보안 위치에 복사합니다.
1. 기본 화면에서 **[!UICONTROL 응용 프로그램 키]**&#x200B;를 클릭합니다.
1. 보라색 막대 위로 마우스를 가져가면 애플리케이션 키가 표시됩니다.
1. 응용 프로그램 키를 보안 위치에 복사합니다.

### Workfront Fusion에서 [!DNL Datadog]에 대한 연결 만들기

[!DNL Datadog]Datadog[!UICONTROL  모듈 내에서 직접 ] 계정에 연결할 수 있습니다.

1. [!UICONTROL Datadog] 모듈에서 **[!UICONTROL 연결]** 필드 옆에 있는 [!UICONTROL 추가]를 클릭합니다.
1. 다음과 같이 모듈의 필드를 채웁니다.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL 연결 이름]</td> 
      <td> <p> 연결의 이름을 입력합니다.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>이 연결이 프로덕션 환경용인지 아니면 비프로덕션 환경용인지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>연결할 도메인(미국 또는 유럽 연합)을 선택합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API 키 위치] </td> 
      <td> <p>헤더에 API 키를 포함할지 쿼리 문자열에 포함할지 선택합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API 키]</td> 
      <td> <p> [!DNL Datadog] API 키를 입력하십시오. </p> <p>API 키 검색에 대한 지침은 이 문서에서 <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">API 키 및 응용 프로그램 키 검색</a>을 참조하십시오.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## [!DNL Datadog]개 모듈 및 해당 필드

[!DNL Datadog] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Datadog] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 액션

* [[!UICONTROL API 호출 만들기]](#make-an-api-call)
* [[!UICONTROL 시계열 점수 게시]](#post-timeseries-points)

#### [!UICONTROL API 호출 만들기]

이 작업 모듈을 사용하면 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Datadog] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Datadog] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Dedicated Domain]</td> 
   <td>들어오는 트래픽이 많을 것으로 예상되는 일부 Datadog API 끝점이 전용 도메인에서 실행되고 있습니다. API 호출에 전용 도메인을 사용하려면 이 확인란을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://api.datadoghq.com/api/</code>과(와) 관련된 경로를 입력하십시오. 예: <code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

**예:** 다음 API 호출은 [!DNL Datadog] 계정의 모든 대시보드를 반환합니다.

URL: `/v1/dashboard`

메서드: `GET`

![Datadog API 호출 예](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

결과는 번들 > 본문 > 대시보드 아래에 있는 모듈의 출력에서 찾을 수 있습니다.

이 예에서는 3개의 대시보드가 반환되었습니다.

![Datadog API 응답](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)

#### [!UICONTROL 시계열 점수 게시]

모듈을 사용하면 [!DNL Datadog]의 대시보드에 그래프로 표시할 수 있는 시계열 데이터를 게시할 수 있습니다.

압축 페이로드의 제한은 압축 해제된 페이로드의 경우 3.2메가바이트(3200000) 및 62메가바이트(62914560)입니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Datadog] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Datadog] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 유형]</td> 
   <td> 사용할 지표 유형을 선택합니다. 
   <ul>
   <li>게이지</li>
   <li>요율</li>
   <li>계수</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Interval]</td> 
   <td> 지표 유형이 비율 또는 개수인 경우 해당 간격을 정의합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Points]</td> 
   <td><p>지표와 관련된 포인트를 추가합니다.</p> <p>포인트의 JSON 배열입니다. 각 점의 형식은 다음과 같습니다. <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>참고:  <p>타임스탬프는 초 단위여야 합니다.</p> <p>타임스탬프는 현재여야 합니다. 현재를 미래 10분 이하 또는 과거 1시간 이상으로 정의한다.</p> <p> 숫자 값 형식은 부동 소수로만 지정할 수 있습니다.</p> </p> <p>이 필드에는 최소 1개의 항목이 포함되어야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 호스트]</td> 
   <td>지표를 생성한 호스트의 이름을 입력합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 태그]</td> 
   <td> 지표에 추가할 각 태그에 대해 <b>항목 추가</b>를 클릭하고 태그의 값을 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>
