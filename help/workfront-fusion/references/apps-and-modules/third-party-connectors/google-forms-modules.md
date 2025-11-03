---
title: Google Forms 모듈
description: ' [!DNL Adobe Workfront Fusion Google Forms] 모듈을 사용하면 Google Forms에서 응답을 모니터링, 선택, 추가, 업데이트 또는 삭제할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%

---

# [!DNL Google Forms]개 모듈

Adobe Workfront Fusion [!DNL Google Forms] 모듈을 사용하면 [!DNL Google Forms]에서 응답을 모니터링, 선택, 추가, 업데이트 또는 삭제할 수 있습니다.

Adobe Workfront Fusion에서 [!DNL Google Docs]을(를) 사용하려면 [!DNL Google] 계정이 있어야 합니다. 아직 [!DNL Google] 계정이 없는 경우 [!DNL Google] 계정 도움말 페이지에서 계정을 만들 수 있습니다.

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

[!DNL Google Forms] 모듈을 사용하려면 [!DNL Google] 계정이 있어야 합니다.

## Google Forms API 정보

Google Forms 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## 양식에서 스프레드시트 만들기

양식 응답 작업을 수행하려면 먼저 응답 스프레드시트를 만들어야 합니다.

1. 양식을 엽니다.
1. **[!UICONTROL 응답]** 탭으로 이동합니다.
1. **[!UICONTROL 스프레드시트 만들기]** 아이콘 ![스프레드시트 아이콘](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png)을 클릭합니다.

1. 새 스프레드시트를 만들지 기존 스프레드시트를 만들지 선택합니다.
1. Click **[!UICONTROL Create]**.

## [!DNL Google Forms]개 모듈 및 해당 필드

[!DNL Google Forms] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Forms] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

#### [!UICONTROL 응답 보기]

양식에 새 응답이 있는지 확인합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>새 응답을 확인할 양식의 응답이 들어 있는 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 양식 응답이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">헤더가 있는 [!UICONTROL 행]</td> 
   <td>테이블의 머리글 행을 지정합니다. 기본 행은 <code>A1:Z1</code>입니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 값 렌더링 옵션]</td> 
   <td> <p>출력에서 값을 렌더링할 방법을 지정합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 형식의 값]</strong> </p> <p>값은 셀의 형식에 따라 응답에서 계산되고 형식이 지정됩니다. 서식은 요청한 사용자의 로케일이 아니라 스프레드시트의 로케일을 기반으로 합니다. 예를 들어 <code>A1</code>이(가) <code>1. 23</code>이고 <code>A2 </code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>$1. 23</code> 을(를) 반환합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 형식이 지정되지 않은 값]</strong> </p> <p>값은 계산되지만 회신에서 포맷되지 않습니다. 예를 들어 <code>A1</code>이(가) <code>1. 23</code>이고 <code>A2 </code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) 숫자 <code>1. 23</code>을(를) 반환합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 수식]</strong> </p> <p>값이 계산되지 않습니다. 답변에는 수식이 포함되어 있습니다. 예를 들어 <code>A1</code>이(가) <code>1. 23</code>이고 <code>A2 </code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>=A1</code>을(를) 반환합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 날짜 및 시간 렌더링 옵션]</td> 
   <td>날짜, 시간 및 기간을 출력에 표시할 방법을 선택합니다. [!UICONTROL Value Render Option]이 [!UICONTROL Formatted Value]로 설정된 경우 이 필드가 무시됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p> 한 주기 동안 Workfront Fusion이 작동하는 최대 응답 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 응답 추가]](#add-a-response)
* [[!UICONTROL 응답 삭제]](#delete-a-response)
* [[!UICONTROL 응답 업데이트]](#update-a-response)

#### [!UICONTROL 응답 추가]

이 모듈은 양식의 스프레드시트 하단에 새 응답을 추가합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>응답을 추가할 시트가 포함된 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 양식 응답이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL 값]</p> </td> 
   <td> <p>시트 열에 원하는 값을 입력합니다. 열은 시트를 기준으로 사용할 수 있습니다.</p> <p>[!UICONTROL Timestamp] 열의 경우 다음 값을 사용합니다.</p><pre>formatDate(now;DD/MM/YYYY HH:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 값 입력 옵션]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 사용자가 입력하는 값은 구문 분석되지 않고 그대로 저장됩니다. </p> </li> 
     <li> <p><strong>[!UICONTROL 사용자가 입력됨]</strong></p> <p>값은 사용자가 UI에 입력한 것처럼 구문 분석됩니다. 숫자는 그대로 유지되지만 문자열은 [!DNL Google Sheets] UI를 통해 셀에 텍스트를 입력할 때 적용되는 규칙과 동일한 규칙에 따라 숫자, 날짜 또는 다른 형식으로 변환될 수 있습니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 데이터 삽입 옵션]</td> 
   <td> <p>새 데이터를 입력할 때 기존 데이터가 변경되는 방법을 지정합니다. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 덮어쓰기]</strong> </p> <p>새 데이터는 작성된 영역의 기존 데이터를 덮어씁니다. 시트 끝에 데이터를 추가하면 데이터를 쓸 수 있도록 새 행이나 열이 삽입됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 행 삽입]</strong></p> <p>새 데이터에 대한 행이 삽입됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 응답 삭제]

이 모듈은 선택한 응답을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>응답을 삭제할 시트가 포함된 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 양식 응답이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 행 번호]</p> </td> 
   <td> <p>삭제할 행 번호를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 응답 업데이트]

이 모듈은 선택한 응답을 업데이트합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>응답을 갱신할 시트가 포함된 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 양식 응답이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 행 번호]</p> </td> 
   <td> <p>갱신할 행 번호를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 값]</p> </td> 
   <td> <p>원하는 열에 대한 새 값을 입력합니다. 열은 시트를 기준으로 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 값 입력 옵션]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 사용자가 입력하는 값은 구문 분석되지 않고 그대로 저장됩니다. </p> </li> 
     <li> <p><strong>[!UICONTROL 사용자가 입력됨]</strong></p> <p>값은 사용자가 UI에 입력한 것처럼 구문 분석됩니다. 숫자는 그대로 유지되지만 문자열은 [!DNL Google Sheets] UI를 통해 셀에 텍스트를 입력할 때 적용되는 규칙과 동일한 규칙에 따라 숫자, 날짜 또는 다른 형식으로 변환될 수 있습니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL 응답 검색]](#search-responses)
* [[!UICONTROL 검색 응답(고급])](#search-responses-advanced)

#### [!UICONTROL 응답 검색]

이 모듈은 지정된 기준과 일치하는 응답을 반환합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>연결</td>
   <td> <p>[!DNL Google] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>검색할 양식을 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>양식 응답이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL 열 범위]</td>
   <td> <p> 검색할 열 범위를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>응답 검색 기준으로 사용할 필터를 정의합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL 정렬 순서] </td>
   <td> <p>반환된 응답을 오름차순으로 정렬할지 아니면 내림차순으로 정렬할지 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> 반환된 응답 순서를 지정할 열을 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 값 렌더링 옵션]</td> 
   <td> <p>출력에서 값을 렌더링할 방법을 지정합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 형식의 값]</strong></p> <p>값은 셀의 형식에 따라 응답에서 계산되고 형식이 지정됩니다. 서식은 요청한 사용자의 로케일이 아니라 스프레드시트의 로케일을 기반으로 합니다. 예를 들어 <code>A1</code>이(가) <code>1. 23</code>이고 <code>A2 </code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>$1. 23</code> 을(를) 반환합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 형식이 지정되지 않은 값]</strong> </p> <p>값은 계산되지만 회신에서 포맷되지 않습니다. 예를 들어 <code>A1</code>이(가) <code>1. 23</code>이고 <code>A2 </code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) 숫자 <code>1. 23</code>을(를) 반환합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 수식]</strong> </p> <p>값이 계산되지 않습니다. 답변에는 수식이 포함되어 있습니다. 예를 들어 <code>A1</code>이(가) <code>1. 23</code>이고 <code>A2 </code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>=A1</code>을(를) 반환합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL 날짜 및 시간 렌더링 옵션]</td>
    <td>날짜, 시간 및 기간을 출력에 표시할 방법을 선택합니다. [!UICONTROL Value Render] 옵션이 Formatted Value로 설정되어 있으면 이 필드가 무시됩니다. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL 반환되는 최대 응답 수]</td>
   <td> <p> Workfront Fusion이 한 주기 동안 반환하는 최대 응답 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 검색 응답(고급)]

이 모듈은 [[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage)을 사용하여 검색을 수행합니다. 이 모듈은 행 번호를 반환하지 않습니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>[!DNL Google] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>검색할 시트가 포함된 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> 양식 응답이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p><a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>을(를) 사용하여 검색 쿼리를 정의합니다.</p> <p>예: <code>select * where C = "John"</code>은(는) C 열이 "John"인 행의 모든 값을 검색합니다.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL 반환되는 최대 행 수]</td>
   <td> <p> Workfront Fusion이 한 주기 동안 반환하는 최대 응답 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
