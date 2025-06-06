---
title: Google Sheets 모듈
description: ' [!DNL Google Sheets] with [!DNL Adobe Workfront Fusion],you need the [!UICONTROL Workfront Fusion Google Sheets] extension을 사용하려면(선택 사항이지만 인스턴트 트리거에는 필요).'
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 80965570-2937-4ac8-97c0-54f7a813ec50
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3957'
ht-degree: 0%

---

# [!DNL Google Sheets]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Google Sheets]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 [연결 만들기 [!DNL Adobe Workfront Fusion] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하세요.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>또는</p>
   <p>레거시: 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 전제 조건

[!UICONTROL Google 시트] 모듈을 사용하려면 [!UICONTROL Google] 계정이 있어야 합니다.

## Google Sheets API 정보

Google Sheets 커넥터에서는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://sheets.googleapis.com/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v2.5.7</td> 
  </tr>
 </tbody> 
 </table>

## Google Sheets 모듈 및 필드

[!DNL Google Forms] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Sheets] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 트리거

#### [!UICONTROL 행 보기]

스프레드시트에서 새로 추가된 행에서 값을 검색합니다.

모듈은 이전에 채워지지 않은 새 행만 검색합니다. 트리거는 덮어쓴 행을 처리하지 않습니다.

>[!IMPORTANT]
>
>워크시트에 빈 행이 있으면 빈 행 뒤에 행이 처리되지 않습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet] </td> 
   <td> <p>보려는 시트가 포함된 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet] </td> 
   <td> <p>새 행에 대해 조사할 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table contains headers]</td> 
   <td> <p> 스프레드시트에 머리글 행이 포함되어 있는지 여부를 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>모듈은 헤더 행을 출력 데이터로 검색하지 않습니다. </p> <p>출력에서 변수 이름은 헤더에 의해 호출됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 번호]</strong> </p> <p>모듈은 첫 번째 테이블 행도 검색합니다</p> <p>출력의 변수 이름은 A, B, C, D 등입니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">헤더가 있는 [!UICONTROL 행] </td> 
   <td> <p>머리글 행의 범위를 입력합니다. 예: <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 첫 번째 테이블 행]</td> 
   <td> <p>테이블의 첫 번째 행 범위를 입력합니다. 예: <code>A1:F1</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 값 렌더링 옵션]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL 형식의 값]</p> <p>셀의 서식에 따라 회신에서 값이 계산되고 서식이 지정됩니다. 서식은 요청한 사용자의 로케일이 아니라 스프레드시트의 로케일을 기반으로 합니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"$1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 형식이 지정되지 않은 값]</p> <p>값이 계산되지만 회신에서 형식이 지정되지 않습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) 숫자 <code>"1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 공식]</p> <p>값이 계산되지 않습니다. 답변에는 수식이 포함되어 있습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"=A1"</code>을(를) 반환합니다.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 날짜 및 시간 렌더링 옵션]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL 일련 번호]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 Lotus 1-2-3에서 대중화된 "일련 번호" 형식의 두 배로 출력됩니다. 값의 전체 숫자 부분(소수점 왼쪽)은 1899년 12월 30일 이후의 일을 계산합니다. 분수 부분(소수점의 오른쪽)은 시간을 하루의 분수로 계산합니다. 예를 들어, 1900년 1월 1일 정오가 2.5이고, 1899년 12월 30일 이후 2일이므로 2이고, 정오가 반나절이므로 .5입니다. 1900년 2월 1일 오후 3시 는 33.625가 됩니다. 이는 1900년을 윤년이 아닌 해로 올바르게 취급한다.</p> </li><li><p style="font-weight: bold;">[!UICONTROL 서식 있는 문자열]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 스프레드시트의 로케일에 따라 지정된 숫자 형식으로 문자열로 출력됩니다.</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 사용할 최대 결과 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 행 추가]](#add-a-row)
* [[!UICONTROL 시트 추가]](#add-a-sheet)
* [[!UICONTROL 셀 지우기]](#clear-a-cell)
* [[!UICONTROL 행 지우기]](#clear-a-row)
* [[!UICONTROL 스프레드시트 만들기]](#create-a-spreadsheet)
* [[!UICONTROL 행 삭제]](#delete-a-row)
* [[!UICONTROL 시트 삭제]](#delete-a-sheet)
* [[!UICONTROL 셀 가져오기]](#get-a-cell)
* [[!UICONTROL API 호출 만들기]](#make-an-api-call)
* [[!UICONTROL 셀 업데이트]](#update-a-cell)
* [[!UICONTROL 행 업데이트]](#update-a-row)

#### [!UICONTROL 행 추가]

이 모듈은 시트에 행을 추가합니다.

[!DNL Google Sheets] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Sheets] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 모드]</td> 
   <td> <p>스프레드시트와 시트를 수동으로 선택할지 아니면 매핑으로 선택할지를 선택합니다.</p> <p>참고: 수동 매핑은 [!DNL Workfront Fusion] 시나리오에서 새 스프레드시트가 만들어지고 시나리오에서 직접 새로 생성된 스프레드시트에 데이터를 추가하려는 경우 유용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>[!DNL Google] 스프레드시트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>행을 추가할 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 열 범위]</td> 
   <td>작업할 열 범위를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> 스프레드시트에 머리글 행이 포함되어 있는지 여부를 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>모듈은 헤더 행을 출력 데이터로 검색하지 않습니다. </p> <p>출력에서 변수 이름은 헤더에 의해 호출됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 번호]</strong> </p> <p>모듈은 첫 번째 테이블 행도 검색합니다</p> <p>출력의 변수 이름은 A, B, C, D 등입니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값] </td> 
   <td> <p>추가할 행의 원하는 셀을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값 입력 옵션]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL 사용자가 입력됨]</strong></p> <p>값은 사용자가 UI에 입력한 것처럼 구문 분석됩니다. 숫자는 그대로 유지되지만 문자열은 [!DNL Google Sheets] UI를 통해 셀에 텍스트를 입력할 때 적용되는 규칙과 동일한 규칙에 따라 숫자, 날짜 또는 다른 형식으로 변환될 수 있습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 사용자가 입력하는 값은 구문 분석되지 않고 입력된 대로 저장됩니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 데이터 삽입 옵션]</td> 
   <td> <p>새 데이터를 입력할 때 기존 데이터가 변경되는 방법을 지정합니다. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 행 삽입]</strong></p> <p>새 데이터에 대한 행이 삽입됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 덮어쓰기]</strong> </p> <p>새 데이터는 작성된 영역의 기존 데이터를 덮어씁니다. 시트 끝에 데이터를 추가하면 데이터를 쓸 수 있도록 새 행이나 열이 삽입됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 시트 추가]

선택한 스프레드시트에 새 시트를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>시트를 추가하려는 Google 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 속성]</td> 
   <td> 
    <ul> 
     <li> <p style="font-weight: bold;">[!UICONTROL Title]</p> <p>새 시트의 이름을 입력합니다.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Index]</p> <p>시트 위치를 입력합니다. 기본값은 0(시트를 첫 번째 위치에 배치함)입니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 셀 지우기]

지정된 셀에서 값을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>셀을 지우려는 시트가 포함된 Google 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>셀을 지울 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 셀] </td> 
   <td> <p>지우려는 셀의 ID를 입력하거나 매핑합니다. 예: <code>A5</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 행 지우기]

지정된 행에서 값을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>행을 지우려는 시트가 포함된 [!DNL Google] 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p> 데이터를 지우려는 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 행 번호]</td> 
   <td> <p>데이터를 지우려는 행의 번호를 입력합니다. 예: <code> 23</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 스프레드시트 만들기]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>새 스프레드시트의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Locale]</td> 
   <td> <p>다음 형식 중 하나로 스프레드시트의 로케일을 입력합니다.</p> 
    <ul> 
     <li>다음과 같은 ISO 639-1 언어 코드 <code>en</code></li> 
     <li>639-1 코드가 없는 경우 <code>haw</code>과(와) 같은 ISO 639-2 언어 코드</li> 
     <li>다음과 같은 ISO 언어 코드와 국가 코드의 조합 <code>en_US</code></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 재계산 간격]</td> 
   <td> <p>휘발성 함수가 다시 계산되기 전까지 대기할 시간:</p> <ul><li><p style="font-weight: bold;">변경 시 </p> <p>변동성 함수는 변경 시마다 업데이트됩니다.</p></li><li> <p style="font-weight: bold;">변경 시 및 매분 </p> <p>변동성 함수는 변경 시마다 매 분마다 업데이트됩니다.</p></li> <li><p style="font-weight: bold;">변경 시 및 시간별 </p> <p>변동성 함수는 변경 시마다 업데이트됩니다.</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 시간대]</td> 
   <td> <p> 스프레드시트의 시간대를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Number format]</td> 
   <td> <p>스프레드시트에 있는 모든 셀의 기본 형식을 선택합니다.</p> <p><strong>[!UICONTROL Text]</strong>: 텍스트 서식. 예: <code>1000. 12</code></p> <p><strong>[!UICONTROL Number]</strong>: 숫자 서식. 예: <code>1,000.12</code></p> <p><strong>[!UICONTROL Percent]</strong>: 서식 적용 비율입니다. 예: <code>10. 12%</code></p> <p><strong>[!UICONTROL Currency]</strong>: 통화 형식입니다. 예: <code>$1,000.12</code></p> <p><strong>[!UICONTROL Date]</strong>: 날짜 형식입니다. 예: <code>9/26/2008</code></p> <p><strong>[!UICONTROL 시간]</strong>: 시간 서식. 예: <code>3:59:00 PM</code></p> <p><strong>[!UICONTROL 날짜 시간]</strong>: 날짜 및 시간 서식. 예: <code>9/26/08 15:59:00</code> </p> <p><strong>[!UICONTROL Scientific]</strong>: 과학 숫자 서식. 예: <code>1. 01E+03</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheets] </td> 
   <td> <p>스프레드시트에 추가할 각 시트에 대해 <strong>[!UICONTROL 항목 추가]</strong>를 클릭하고 시트 제목 및 시트 색인을 입력하거나 매핑합니다. 색인 0은 첫 번째 시트를 나타냅니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 행 삭제]

지정된 행을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>행을 삭제할 시트가 포함된 Google 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>시트 </td> 
   <td> <p>행을 삭제할 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>행 번호</td> 
   <td> <p>삭제할 행의 번호를 입력합니다. 예: <code>23</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 시트 삭제]

특정 시트를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>[!DNL Google] 스프레드시트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>삭제할 시트를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 셀 가져오기]

선택한 셀에서 값을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>[!DNL Google] 스프레드시트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>데이터를 검색할 셀이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 셀] </td> 
   <td> <p>데이터를 검색할 셀의 ID를 입력합니다. 예: <code>A6</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값 렌더링 옵션]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL 형식의 값]</p> <p>셀의 서식에 따라 회신에서 값이 계산되고 서식이 지정됩니다. 서식은 요청한 사용자의 로케일이 아니라 스프레드시트의 로케일을 기반으로 합니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"$1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 형식이 지정되지 않은 값]</p> <p>값이 계산되지만 회신에서 형식이 지정되지 않습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) 숫자 <code>"1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 공식]</p> <p>값이 계산되지 않습니다. 답변에는 수식이 포함되어 있습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"=A1"</code>을(를) 반환합니다.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!DNL Date and time render option]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!DNL Serial number]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 Lotus 1-2-3에서 대중화된 "일련 번호" 형식의 두 배로 출력됩니다. 값의 전체 숫자 부분(소수점 왼쪽)은 1899년 12월 30일 이후의 일을 계산합니다. 분수 부분(소수점의 오른쪽)은 시간을 하루의 분수로 계산합니다. 예를 들어, 1900년 1월 1일 정오가 2.5이고, 1899년 12월 30일 이후 2일이므로 2이고, 정오가 반나절이므로 .5입니다. 1900년 2월 1일 오후 3시 는 33.625가 됩니다. 이는 1900년을 윤년이 아닌 해로 올바르게 취급한다.</p></li><li> <p style="font-weight: bold;">[!DNL Formatted string]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 스프레드시트의 로케일에 따라 지정된 숫자 형식으로 문자열로 출력됩니다.</p> </li><ul></td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL API 호출 만들기]

이 작업 모듈을 사용하면 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Google Sheets 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td><code>https://sheets.googleapis.com/v4/</code>과(와) 관련된 경로를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메서드]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 예: <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion]이(가) 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p> 표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:   <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 셀 업데이트]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>[!DNL Google] 스프레드시트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>셀을 업데이트할 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 셀] </td> 
   <td> <p>업데이트할 셀의 ID를 입력합니다. 예: <code>A5</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값]</td> 
   <td> <p>셀의 새 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값 입력 옵션]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL 사용자가 입력됨]</strong></p> <p>값은 사용자가 UI에 입력한 것처럼 구문 분석됩니다. 숫자는 그대로 유지되지만 문자열은 [!DNL Google Sheets] UI를 통해 셀에 텍스트를 입력할 때 적용되는 규칙과 동일한 규칙에 따라 숫자, 날짜 또는 다른 형식으로 변환될 수 있습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 사용자가 입력하는 값은 구문 분석되지 않고 입력된 대로 저장됩니다. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 행 업데이트]

이 모듈에서는 선택한 행의 셀 내용을 변경할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 모드]</td> 
   <td> <p>스프레드시트와 시트를 수동으로 선택할지 아니면 매핑으로 선택할지를 선택합니다.</p> <p>참고: 수동 매핑은 [!UICONTROL Workfront Fusion] 시나리오에서 새 스프레드시트가 생성되고 시나리오에서 직접 새로 생성된 스프레드시트에 데이터를 추가하려는 경우 유용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>[!DNL Google] 스프레드시트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>행을 갱신할 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 행 번호]</td> 
   <td> <p> 갱신할 행의 번호를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> 스프레드시트에 머리글 행이 포함되어 있는지 여부를 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>모듈은 헤더 행을 출력 데이터로 검색하지 않습니다. </p> <p>출력에서 변수 이름은 헤더에 의해 호출됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 번호]</strong> </p> <p>모듈은 첫 번째 테이블 행도 검색합니다</p> <p>출력의 변수 이름은 A, B, C, D 등입니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값] </td> 
   <td> <p>변경(업데이트)하려는 행의 원하는 셀에 값을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값 입력 옵션]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL 사용자가 입력됨]</strong></p> <p>값은 사용자가 UI에 입력한 것처럼 구문 분석됩니다. 숫자는 그대로 유지되지만 문자열은 [!DNL Google Sheets] UI를 통해 셀에 텍스트를 입력할 때 적용되는 규칙과 동일한 규칙에 따라 숫자, 날짜 또는 다른 형식으로 변환될 수 있습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 사용자가 입력하는 값은 구문 분석되지 않고 입력된 대로 저장됩니다. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL 범위 값 가져오기]](#get-range-values)
* [[!UICONTROL 목록 시트]](#list-sheets)
* [[!UICONTROL 행 검색]](#search-rows)
* [[!UICONTROL 행 검색(고급)]](#search-rows-advanced)

#### [!UICONTROL 범위 값 가져오기]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>[!DNL Google] 스프레드시트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>범위 컨텐츠를 가져올 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 범위] </td> 
   <td> <p>가져올 범위를 입력하십시오. 예: <code>A1:D25</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p>시트에 머리글 행이 있는 경우 이 상자를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>헤더가 있는 [!UICONTROL 행]</td> 
   <td>테이블 머리글의 범위를 입력합니다. 예 <code>A1:F1</code>. 필드를 비워 두면 [!DNL Workfront Fusion]에서 지정한 범위의 첫 행을 헤더로 처리합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값 렌더링 옵션]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL 형식의 값]</p> <p>셀의 서식에 따라 회신에서 값이 계산되고 서식이 지정됩니다. 서식은 요청한 사용자의 로케일이 아니라 스프레드시트의 로케일을 기반으로 합니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"$1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 형식이 지정되지 않은 값]</p> <p>값이 계산되지만 회신에서 형식이 지정되지 않습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) 숫자 <code>"1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 공식]</p> <p>값이 계산되지 않습니다. 답변에는 수식이 포함되어 있습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"=A1"</code>을(를) 반환합니다.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 날짜 및 시간 렌더링 옵션]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL 일련 번호]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 Lotus 1-2-3에서 대중화된 "일련 번호" 형식의 두 배로 출력됩니다. 값의 전체 숫자 부분(소수점 왼쪽)은 1899년 12월 30일 이후의 일을 계산합니다. 분수 부분(소수점의 오른쪽)은 시간을 하루의 분수로 계산합니다. 예를 들어, 1900년 1월 1일 정오가 2.5이고, 1899년 12월 30일 이후 2일이므로 2이고, 정오가 반나절이므로 .5입니다. 1900년 2월 1일 오후 3시 는 33.625가 됩니다. 이는 1900년을 윤년이 아닌 해로 올바르게 취급한다.</p> </li><li><p style="font-weight: bold;">[!UICONTROL 서식 있는 문자열]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 스프레드시트의 로케일에 따라 지정된 숫자 형식으로 문자열로 출력됩니다.</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 목록 시트]

이 모듈은 스프레드시트에 있는 모든 시트 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>나열할 시트가 포함된 [!DNL Google] 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 행 검색]

필터 옵션을 사용하여 행을 검색합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Google Sheets 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>[!DNL Google] 스프레드시트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>행을 검색할 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> 스프레드시트에 머리글 행이 포함되어 있는지 여부를 선택합니다. [!UICONTROL Yes] 옵션을 선택하면 출력 데이터와 출력의 변수 이름이 헤더에 의해 호출되므로 모듈은 헤더 행을 검색하지 않습니다. [!UICONTROL No] 옵션이 선택된 경우 모듈은 또한 첫 번째 테이블 행을 검색하고 출력의 변수 이름을 A, B, C, D 등으로만 호출합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 열 범위]</td> 
   <td>작업할 열 범위를 선택하십시오. 예: <code>A-F</code></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter]</td> 
   <td> <p>행을 검색하는 데 사용할 필터를 설정합니다.</p> <!--<p>For more information about filters, see <a href="/help/workfront-fusion/create-scenarios/add-modules/" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 정렬 순서]</td> 
   <td>오름차순 또는 내림차순 정렬 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td>정렬 기준으로 사용할 열을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 값 렌더링 옵션]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL 형식의 값]</p> <p>셀의 서식에 따라 회신에서 값이 계산되고 서식이 지정됩니다. 서식은 요청한 사용자의 로케일이 아니라 스프레드시트의 로케일을 기반으로 합니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"$1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 형식이 지정되지 않은 값]</p> <p>값이 계산되지만 회신에서 형식이 지정되지 않습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) 숫자 <code>"1.23"</code>을(를) 반환합니다.</p></li><li> <p style="font-weight: bold;">[!UICONTROL 공식]</p> <p>값이 계산되지 않습니다. 답변에는 수식이 포함되어 있습니다. 예를 들어 <code>A1</code>이(가) <code>1.23</code>이고 <code>A2</code>이(가) <code>=A1</code>이고 통화 형식인 경우 <code>A2</code>은(는) <code>"=A1"</code>을(를) 반환합니다.</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 날짜 및 시간 렌더링 옵션]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!UICONTROL 일련 번호]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 Lotus 1-2-3에서 대중화된 "일련 번호" 형식의 두 배로 출력됩니다. 값의 전체 숫자 부분(소수점 왼쪽)은 1899년 12월 30일 이후의 일을 계산합니다. 분수 부분(소수점의 오른쪽)은 시간을 하루의 분수로 계산합니다. 예를 들어, 1900년 1월 1일 정오가 2.5이고, 1899년 12월 30일 이후 2일이므로 2이고, 정오가 반나절이므로 .5입니다. 1900년 2월 1일 오후 3시 는 33.625가 됩니다. 이는 1900년을 윤년이 아닌 해로 올바르게 취급한다.</p> </li><li><p style="font-weight: bold;">[!UICONTROL 서식 있는 문자열]</p> <p>날짜, 시간, 날짜/시간 및 기간 필드는 스프레드시트의 로케일에 따라 지정된 숫자 형식으로 문자열로 출력됩니다.</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 행 수]</td> 
   <td>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 행 수를 설정하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 행 검색(고급)]

지정된 기준과 일치하는 결과를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Sheets] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>검색할 시트가 포함된 Google 스프레드시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>검색할 행이 포함된 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>[!DNL Google Charts Query Language] 사용. 예: <code>select * where B = "John"</code></p> <p>[!DNL Google Charts Query Language]에 대한 자세한 내용은 [!DNL Google] 설명서의 <a href="https://developers.google.com/chart/interactive/docs/querylanguage">쿼리 언어 참조</a>를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용 제한

오류 `429: RESOURCE_EXHAUSTED`이(가) 발생하면 API 속도 제한을 초과했습니다.

[!DNL Google Sheets] API의 제한은 프로젝트당 100초당 500개 요청 및 사용자당 100초당 100개 요청입니다. 읽기 및 쓰기 제한은 별도로 추적됩니다. 일일 사용 제한은 없습니다.

자세한 내용은 [developers.google.com/sheets/api/limits](https://developers.google.com/sheets/api/limits)을 참조하세요.

## 팁 및 요령

* [ [!DNL Google] 시트에서 빈 셀 가져오기](#get-empty-cells-from-a-google-sheet)
* [시트에 단추를 추가하여 시나리오 실행](#add-a-button-in-a-sheet-to-run-a-scenario)

### [!DNL Google Sheet]에서 빈 셀 가져오기

빈 셀을 가져오려면 [!UICONTROL 행 검색(고급)] 모듈을 사용합니다. 이 수식을 사용하여 빈 열을 가져옵니다.

```
select * where E is null
```

여기서 &quot;E&quot;는 열이고 &quot;is null&quot;은 조건입니다. Google 쿼리 언어를 사용하여 고급 쿼리를 만들 수 있습니다. 자세한 내용은 Google 설명서의 [Google 쿼리 언어](https://developers.google.com/chart/interactive/docs/querylanguage)를 참조하십시오.

### 시트에 단추를 추가하여 시나리오 실행

1. [!DNL Workfront Fusion]에서 시나리오에 **[!UICONTROL Webhook]** > **[!UICONTROL 사용자 지정 Webhooks]** 모듈을 삽입하고 구성합니다. 자세한 내용은 [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)을(를) 참조하십시오.

1. 웹후크의 URL을 복사합니다.
1. 시나리오를 실행합니다.
1. Google Sheets의 메인 메뉴 모음에서 **[!UICONTROL 삽입]** > **[!UICONTROL 그리기]**...을 선택합니다.

1. [!UICONTROL 그리기] 창에서 창 위쪽에 있는 **[!UICONTROL 텍스트 상자]** 아이콘 ![텍스트 상자](/help/workfront-fusion/references/apps-and-modules/assets/text-box.png)을 클릭합니다.
1. 단추를 디자인하고 오른쪽 상단의 **[!UICONTROL 저장 및 닫기]** 단추를 클릭합니다.
1. 단추가 워크시트에 있습니다. 단추의 오른쪽 위 모서리에 있는 세 개의 세로 점을 클릭합니다.
1. **[!UICONTROL 스크립트 할당 선택..].메뉴에서**.
1. 스크립트(함수)의 이름(예: `runScenario`)을 입력하고 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.
1. 메인 메뉴 모음에서 **[!UICONTROL 도구]** > **[!UICONTROL 스크립트 편집기]**&#x200B;를 선택합니다.

1. 다음 코드를 삽입합니다.

   * 함수 이름은 9단계에서 지정한 이름과 일치해야 합니다.
   * URL을 2단계에서 복사한 웹후크의 URL로 바꿉니다.

     ```
     function runScenario() {
     UrlFetchApp.fetch("&lt;webhook you copied>");
     }
     ```

1. 스크립트 파일을 저장하려면 **[!UICONTROL Ctrl+S]**&#x200B;를 누르고 프로젝트 이름을 입력한 다음 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

1. [!DNL Google Sheets]&#x200B;(으)로 다시 전환하고 새 단추를 클릭하세요.
1. 스크립트에 필요한 권한 부여:
1. [!DNL Workfront Fusion]에서 시나리오가 성공적으로 실행되었는지 확인합니다.

## 스프레드시트에 날짜 저장

날짜 값을 포맷하지 않고 스프레드시트에 저장하면 ISO 8601 형식의 텍스트로 스프레드시트에 나타납니다. 그러나 이 텍스트를 이해하지 못하는 날짜에 작동하는 [!DNL Google Sheets]개의 수식 또는 함수(예: 수식 `=A1+10`)에 다음 오류가 표시됩니다.

![오류](/help/workfront-fusion/references/apps-and-modules/assets/mceclip6-350x87.png)

[!DNL Google Sheets]이(가) 날짜를 이해할 수 있도록 하려면 `formatDate` 함수로 형식을 지정하십시오. 두 번째 인수로 함수에 전달되는 올바른 형식은 스프레드시트의 로케일 설정에 따라 다릅니다.

이 함수에 대한 자세한 내용은 문서 날짜 및 시간 함수에서 [[!UICONTROL formatDate] (date; format; [timezone])](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md#formatdate-date-format-timezone)을(를) 참조하십시오.

올바른 형식을 확인하려면 다음을 수행하십시오.

1. Google Sheets의 기본 메뉴에서 **[!UICONTROL 파일]** > **[!UICONTROL 스프레드시트]** 설정을 선택하여 로케일을 확인하고 설정합니다.

1. 올바른 로케일을 확인하거나 설정한 후 기본 메뉴에서 **[!UICONTROL 형식]** > **[!UICONTROL 숫자]**&#x200B;을(를) 선택하여 해당 날짜 및 시간 형식을 결정합니다. 형식은 날짜 시간 메뉴 항목 옆에 표시됩니다.

1. [!UICONTROL formatDate()] 함수에 전달해야 하는 올바른 형식을 작성하려면 [날짜 및 시간 형식에 대한 토큰 목록](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md)을 참조하세요.

>[!BEGINSHADEBOX]

**예:**

`MM/DD/YYYY HH:mm:ss` 형식(미국 로케일)의 경우:

![로케일 시간 수식](/help/workfront-fusion/references/apps-and-modules/assets/locale-time-350x83.png)

>[!ENDSHADEBOX]

## [!DNL Google Sheets]개 함수 활용 중

Google Sheets에서 기본 제공 함수를 사용하려면 이를 활용할 수 있습니다. 자세한 내용은 함수를 사용하여 항목 매핑 문서에서 [함수 사용 [!DNL Google Sheets] 을 참조하십시오](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md#use-google-sheets-functions).

## [!DNL Google Sheets]이(가) 숫자를 날짜로 변경하지 못하도록 방지

텍스트로 사용하는 숫자 문자열이 [!DNL Google] 워크시트에서 날짜로 해석되는 경우 이를 방지하기 위해 숫자를 일반 텍스트로 미리 서식을 지정할 수 있습니다. 예를 들어, 1-2019를 텍스트로 입력한다면, Google은 날짜로 해석할 수 있다.

1. [!DNL Google Sheets]에서 숫자가 들어 있는 열 또는 셀을 강조 표시합니다.
1. **[!UICONTROL 서식]** > **[!UICONTROL 숫자]** > **[!UICONTROL 일반 텍스트]**&#x200B;를 클릭합니다.

[!DNL Workfront Fusion]의 또 다른 해결 방법은 숫자 앞에 아포스트로피(&#39;)를 입력하는 것입니다(예: &#39;1-2019 또는 &#39;1/47). [!DNL Workfront Fusion]에서 데이터를 보낸 후에는 아포스트로피가 셀에 표시되지 않습니다.
