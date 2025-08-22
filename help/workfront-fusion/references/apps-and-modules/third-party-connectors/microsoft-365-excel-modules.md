---
title: Microsoft Office 365 Excel 모듈
description: Adobe Workfront Fusion 시나리오에서는 Microsoft 365 Excel을 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 059bc82b-f1bc-4b92-a44b-51c1daf14f08
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2693'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Excel]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Microsoft 365 Excel]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Microsoft office 365 Excel]을(를) 사용하려면 Microsoft 계정이 있어야 합니다.

## Microsoft Office 365 Excel API 정보

Microsoft Office 365 Excel 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v2.0.16</td> 
  </tr>
 </tbody> 
 </table>



## Workfront Fusion에 [!DNL Office 365 Excel] 서비스 연결

[!DNL Office 365 Excel] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion에 연결 만들기] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.

## [!DNL Microsoft Office 365 Excel]개 모듈 및 해당 필드

[!DNL Microsoft 365 Excel] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Microsoft 365 Excel] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [워크북](#workbook)
* [워크시트](#worksheet)
* [테이블](#table)
* [기타](#other)

### 워크북

* [통합 문서 다운로드](#download-a-workbook)
* [통합 문서 검색](#search-workbooks)
* [통합 문서 보기](#watch-workbooks)

#### [!UICONTROL 통합 문서 다운로드]

이 작업 모듈은 지정된 Excel 통합 문서의 콘텐츠를 다운로드합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 통합 문서 다운로드]</td> 
   <td> <p>모듈이 다운로드할 통합 문서를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL ID를 수동으로 입력하여]</strong> </p> <p>[!UICONTROL 통합 문서 ID] 필드에 모듈을 다운로드할 특정 통합 문서의 ID를 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 경로]</strong>에서 선택 </p> <p>[!UICONTROL Workbook] 필드에서 루트 폴더에 없는 경우 경로를 포함하여 모듈이 다운로드할 통합 문서를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 통합 문서 검색]

이 작업 모듈은 [!DNL Excel]개의 통합 문서를 검색합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더]</td> 
   <td> <p>통합 문서를 검색할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>선택한 기준을 충족하는 통합 문서만 검색하도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터를 평가할 필드, 연산자 및 필터를 허용할 값을 입력합니다. AND 또는 OR 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 워크시트 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL 통합 문서 보기]

이 트리거 모듈은 통합 문서가 만들어질 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더]</td> 
   <td> <p>새 통합 문서에 대해 감시할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>선택한 기준을 충족하는 통합 문서만 보도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터를 평가할 필드, 연산자 및 필터를 허용할 값을 입력합니다. AND 또는 OR 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 통합 문서 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 워크시트

* [[!UICONTROL 워크시트 추가]](#add-a-worksheet)
* [[!UICONTROL 워크시트 행 추가]](#add-a-worksheet-row)
* [[!UICONTROL 워크시트 행 삭제]](#delete-a-worksheet-row)
* [[!UICONTROL 워크시트 행 나열]](#list-worksheet-rows)
* [[!UICONTROL 워크시트 나열]](#list-worksheets)
* [[!UICONTROL 워크시트 행 업데이트]](#update-a-worksheet-row)
* [[!UICONTROL 워크시트 행 보기]](#watch-worksheet-rows)

#### [!UICONTROL 워크시트 추가]

이 작업 모듈은 선택한 통합 문서 내에 새 워크시트를 만듭니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>통합 문서가 루트 디렉터리에 없는 경우 경로를 포함하여 워크시트를 추가할 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 이름] </td>
   <td> <p>새 워크시트의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 워크시트 행 추가]

이 작업 모듈은 선택한 워크시트에 새 행을 추가합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>통합 문서가 루트 디렉터리에 없는 경우 경로를 포함하여 행을 추가할 워크시트가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p>행을 추가할 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 입력 중인 값의 유형]</p> </td> 
   <td> <p>워크시트에 입력할 값 유형을 선택합니다. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 수식]</strong> </p> <p> Excel에서는 지정된 식을 평가하려고 합니다. 수식의 함수 이름은 영어로 되어 있다. 예: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formula local]</strong> </p> <p>Excel에서는 지정된 식을 평가하려고 합니다. 함수 이름은 Excel 응용 프로그램의 언어로 되어 있습니다. 예: <code>=SUM(A1, 1.5)</code> 및 <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL 값]</strong> </p> <p>Excel에서는 값이 평가되지 않습니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 행]</td>
    <td>각 열에 대해 열에 지정할 값을 새 행에 입력합니다.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 워크시트 행 삭제]

이 작업 모듈은 워크시트에서 행을 삭제합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>삭제할 행이 포함된 워크시트가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트]</td>
   <td> <p> 삭제할 행이 포함된 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 행 ID]</td>
   <td>삭제할 행의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 워크시트 행 나열]

이 작업 모듈은 지정된 워크시트의 행 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>통합 문서가 루트 디렉터리에 없는 경우 경로를 포함하여 나열할 행이 포함된 워크시트가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p>나열할 행이 포함된 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 제한]</td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 워크시트 행 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 워크시트 나열]

이 작업 모듈은 지정된 통합 문서의 워크시트 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>모듈에 나열할 워크시트가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 제한]</td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 워크시트 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 워크시트 행 업데이트]

이 작업 모듈은 기존 워크시트 행을 갱신합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>갱신할 행이 포함된 워크시트가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p>갱신할 행이 포함된 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 입력 중인 값의 유형]</p> </td> 
   <td> <p>워크시트에 입력할 값 유형을 선택합니다. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 수식]</strong> </p> <p> Excel에서는 지정된 식을 평가하려고 합니다. 수식의 함수 이름은 영어로 되어 있다. 예: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formula local]</strong> </p> <p>Excel에서는 지정된 식을 평가하려고 합니다. 함수 이름은 Excel 응용 프로그램의 언어로 되어 있습니다. 예: <code>=SUM(A1, 1.5)</code> 및 <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL 값]</strong> </p> <p>Excel에서는 값이 평가되지 않습니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 행 ID]</td> 
   <td>업데이트할 행의 번호를 선택합니다.</td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 행]</td>
    <td>각 열에 대해 열에 지정할 값을 새 행에 입력합니다.</td>
    </tr> 
 </tbody> 
</table>

#### [!UICONTROL 워크시트 행 보기]

이 트리거 모듈은 새 행이 시트에 추가될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>새 행을 조사할 워크시트가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p>새 행에 대해 조사할 Excel 시트를 선택합니다.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL 빈 행 건너뛰기] </td>
   <td> <p>워크시트에서 빈 행에 대한 번들을 반환하지 않으려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 제한]</td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 워크시트 행 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 테이블

* [[!UICONTROL 테이블 추가]](#add-a-table)
* [[!UICONTROL 테이블 행 추가]](#add-a-table-row)
* [[!UICONTROL 테이블 삭제]](#delete-a-table)
* [[!UICONTROL 테이블 가져오기]](#get-a-table)
* [[!UICONTROL 테이블 행 나열]](#list-table-rows)
* [[!UICONTROL 목록 테이블]](#list-tables)
* [[!UICONTROL 테이블 업데이트]](#update-a-table)
* [[!UICONTROL 테이블 행 보기]](#watch-table-rows)

#### [!UICONTROL 테이블 추가]

이 작업 모듈은 Excel 워크시트 내에 테이블 요소를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 통합 문서] </td> 
   <td> <p>표를 추가할 워크시트가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 워크시트] </td> 
   <td> <p>테이블을 추가할 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Has headers]</td> 
   <td> <p>첫 번째 행을 테이블 머리글로 정의하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 주소]</p> </td> 
   <td> <p>왼쪽 위 셀과 오른쪽 아래 셀을 표시하여 표의 크기를 설정합니다. 예: <code>A1:C10</code>은(는) 3개의 열과 10개의 행으로 테이블을 만듭니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 테이블 행 추가]

이 작업 모듈은 기존 테이블을 수정합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>행을 추가할 표가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p>행을 추가할 테이블이 포함된 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 테이블]</td>
   <td>행을 추가할 테이블을 선택합니다.</td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL 행]</td>
    <td>각 열에 대해 열에 지정할 값을 새 행에 입력합니다.</td>
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 행 ID]</p> </td> 
   <td> <p>테이블의 특정 위치에 행을 추가하려면 행 번호를 입력하거나 매핑합니다. 이 행 뒤에 새 행이 삽입됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 테이블 삭제]

이 작업 모듈은 [!DNL Excel] 워크시트에서 지정된 테이블을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 삭제]</td> 
   <td> <p>삭제할 테이블을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>삭제할 테이블이 포함된 통합 문서의 ID를 입력하거나 매핑한 다음 테이블이 포함된 워크시트의 ID를 입력하거나 매핑합니다.</p> <p>[!UICONTROL Table Name] 필드에 삭제할 테이블의 이름을 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>삭제할 테이블이 포함된 통합 문서와 워크시트를 선택한 다음 테이블을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 테이블 가져오기]

이 작업 모듈은 지정된 테이블에 대한 메타데이터를 검색합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> 
     <p >[!UICONTROL Connection]</p>
   </td> 
   <td> 
     <p>Office 365 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p>
    —&gt; </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 가져오기]</td> 
   <td> <p>검색할 테이블을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>검색할 테이블이 포함된 통합 문서의 ID를 입력하거나 매핑한 다음 테이블이 포함된 워크시트의 ID를 입력하거나 매핑합니다.</p> <p>[!UICONTROL Table Name] 필드에 검색할 테이블의 이름을 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>검색할 테이블이 포함된 통합 문서와 워크시트를 선택한 다음 테이블을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 테이블 행 나열]

이 검색 모듈은 통합 문서의 모든 표 행 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>나열할 행이 포함된 표가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p>나열할 행이 포함된 테이블이 포함된 워크시트를 선택합니다</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 테이블] </td>
   <td> <p>나열할 행이 포함된 테이블을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 제한]</td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 테이블 행 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 목록 테이블]

이 검색 모듈은 모든 테이블 객체의 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL 통합 문서] </td>
   <td> <p>나열할 표가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p>나열할 테이블이 포함된 워크시트를 선택합니다</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 제한]</td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 테이블 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 테이블 업데이트]

이 작업 모듈은 기존 테이블을 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 업데이트]</td> 
   <td> <p>갱신할 테이블을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>수동으로 입력</strong> </p> <p>[!UICONTROL 통합 문서 ID] 필드에 업데이트할 테이블이 포함된 통합 문서의 ID를 입력하거나 매핑합니다.</p> <p>[!UICONTROL Table Name] 필드에 업데이트할 테이블 이름을 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>업데이트할 테이블이 포함된 통합 문서와 워크시트를 선택한 다음 테이블을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이름]</td> 
   <td> <p>표의 이름을 바꾸려면 표의 새 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 머리글 표시]</td> 
   <td> <p>업데이트된 테이블의 헤더를 표시하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 합계 표시]</td> 
   <td>이 옵션을 활성화하면 표의 총 값이 표시됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스타일]</td> 
   <td>새 테이블의 스타일을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 테이블 행 보기]

이 트리거는 새 행이 테이블에 추가될 때 시나리오를 시작합니다.

>[!NOTE]
>
>여기에서 표는 통합 문서에 포함된 표 요소를 나타냅니다. 전체 표가 아닙니다(통합 문서/시트).

![포함된 테이블](/help/workfront-fusion/references/apps-and-modules/assets/embedded-table-350x420.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 통합 문서]</p> </td> 
   <td> <p>보려는 테이블이 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 워크시트] </td>
   <td> <p> 보려는 테이블이 포함된 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 테이블]</p> </td> 
   <td> <p>보려는 테이블을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 제한]</td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 행 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [[!UICONTROL API 호출 만들기]](#make-an-api-call)
* [[!UICONTROL 데이터 검색]](#retrieve-data)

#### [!UICONTROL API 호출 만들기]

이 작업 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://graph.microsoft.com</code>과(와) 관련된 경로를 입력하십시오. 예:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
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
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:   <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 데이터 검색]

이 작업은 정의된 워크시트 범위에서 데이터를 검색하고 각 행에 대한 번들을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 통합 문서] </td> 
   <td> <p>검색할 데이터가 포함된 통합 문서를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 워크시트] </td> 
   <td> <p>검색할 데이터가 포함된 워크시트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 범위] </td> 
   <td> <p>왼쪽 상단 및 오른쪽 하단 셀을 표시하여 데이터를 검색할 시트의 영역을 지정합니다. 예: <code>A1:D10</code></p> </td> 
  </tr> 
 </tbody> 
</table>
