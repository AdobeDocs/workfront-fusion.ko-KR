---
title: Microsoft Office 365 달력
description: Adobe Workfront Fusion 시나리오에서는 Microsoft Office 365 Calendar를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
source-git-commit: 413736673426c1a77dac9f15defa43d4348638b5
workflow-type: tm+mt
source-wordcount: '2047'
ht-degree: 21%

---

# [!DNL Microsoft Office 365 Calendar]

Adobe Workfront Fusion 시나리오에서는 [!DNL Microsoft Office 365 Calendar]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

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

[!DNL Microsoft Office 365 Calendar] 모듈을 사용하려면 [!DNL Microsoft Office 365 Calendar] 계정이 있어야 합니다.

## Microsoft Office 365 Calendar API 정보

Microsoft Office 365 Calendar 커넥터는 다음을 사용합니다.

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
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL Office 365 Calendar] 서비스 연결

[!DNL Office 365 Calendar] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion에 연결 만들기] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 &quot;테이블 읽기&quot; 권한을 부여받은 다음 Outlook 커넥터에 연결을 만들어 전자 메일을 읽으면 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;전자 메일 쓰기&quot; 권한이 모두 표시됩니다.

## [!DNL Microsoft Office 365 Calendar] 모듈 및 해당 필드

[!DNL Microsoft Office 365 Calendar] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL Microsoft Office 365 Calendar] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [이벤트](#event)
* [캘린더](#calendar)
* [기타](#other)

### 이벤트

* [[!UICONTROL 이벤트 만들기]](#create-an-event)
* [[!UICONTROL 이벤트 삭제]](#delete-an-event)
* [[!UICONTROL 이벤트 가져오기]](#get-an-event)
* [[!UICONTROL 이벤트 검색]](#search-events)
* [[!UICONTROL 이벤트 업데이트]](#update-an-event)
* [[!UICONTROL 이벤트 보기]](#watch-events)

#### [!UICONTROL 이벤트 만들기]

이 작업 모듈은 새 이벤트를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>생성된 이벤트의 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작 날짜]</td> 
   <td> 결합된 날짜 및 시간 표현에서 이벤트가 시작되는 단일 시점을 입력합니다. <code>{date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">유형 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 종료 날짜]</td> 
   <td> 이벤트가 결합된 날짜 및 시간 표시로 끝나는 단일 시점을 입력합니다. <code>{date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">유형 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 미리 알림 설정]</td> 
   <td>이 이벤트에 대한 미리 알림을 활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 알림 메시지]</td> 
   <td>알림 메시지가 트리거되어야 하는 이벤트 시작 시간(분)을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 중요도]</td> 
   <td> <p>이 이벤트의 중요도를 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 낮음]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL 높음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 감도] </td> 
   <td> <p>이 이벤트의 민감도를 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL 표준]</strong> </li> 
     <li> <p><strong>[!UICONTROL 개인]</strong> </p> <p>수신자에게 "[!UICONTROL Please treat this as Personal]" 메시지가 표시됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>수신자에게 "[!UICONTROL Please treat this as Private]" 메시지가 표시됩니다. 이 이벤트는 수신자의 받은 편지함 규칙에 의해 전달되거나 리디렉션되지 않습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 기밀]</strong> </p> <p>수신자에게 "[!UICONTROL Please treat this as Confidential]" 메시지가 표시됩니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문 내용 유형]</td> 
   <td>본문 내용이 일반 텍스트인지 또는 HTML인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>이벤트와 연계된 메시지 본문을 입력하거나 매핑합니다. 위의 [!UICONTROL Body Content Type] 필드에 지정된 대로 HTML 또는 텍스트 형식일 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 위치]</td> 
   <td> <p>이벤트 위치 세부 정보를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 응답 요청됨]</td> 
   <td>초대자에게 이벤트 초대에 대한 응답을 보내도록 요청하려면 <strong>[!UICONTROL 예]</strong>를 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 다음으로 표시]</td> 
   <td> <p>캘린더를 보는 사람에게 이벤트를 표시할 방법을 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL 미정]</li> 
     <li>[!UICONTROL 사용 중]</li> 
     <li>[!UICONTROL 부재 중]</li> 
     <li>[!UICONTROL 다른 곳에서 작업]</li> 
     <li>[!UICONTROL 알 수 없음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 출석자]</p> </td> 
   <td> <p>초대하려는 각 참석자에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>참석자의 이름을 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>참석자의 이메일 주소를 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 범주]</td> 
   <td>이벤트를 캘린더에 표시할 각 범주에 대해 <b>항목 추가</b>를 클릭하고 범주를 입력하거나 매핑하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 이벤트 삭제]

이 작업 모듈은 기존 이벤트를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이벤트 ID]</td> 
   <td> <p>삭제할 이벤트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 이벤트 가져오기]

이 작업 모듈은 지정된 이벤트의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이벤트 ID]</td> 
   <td> <p>세부 정보를 검색할 이벤트 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 이벤트 검색]

이 검색 모듈은 선택한 달력에서 이벤트가 생성, 업데이트, 삭제, 시작 또는 종료될 때 이벤트의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 달력 그룹 ID]</td> 
   <td>이벤트를 보려는 캘린더가 포함된 [!UICONTROL 캘린더 그룹]을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>보려는 특정 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필터]</td> 
   <td> <p>결과를 필터링할 필터 조건을 설정합니다. 다음 속성을 기준으로 필터링할 수 있습니다.</p> 
    <ul> 
     <li>[!UICONTROL Subject]</li> 
     <li>[!UICONTROL 이벤트 ID]</li> 
     <li>[!UICONTROL 만든 날짜 시간]</li> 
     <li>[!UICONTROL 마지막 수정 날짜 시간]</li> 
     <li>[!UICONTROL Body Preview]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>결과 순서 지정 방법을 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Subject]</strong>, 오름차순 또는 내림차순</li> 
     <li><strong>[!UICONTROL 생성된 날짜 시간]</strong>, 오름차순 또는 내림차순</li> 
     <li><strong>[!UICONTROL 마지막 수정 날짜 시간]</strong>, 오름차순 또는 내림차순</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td>한 시나리오 실행 주기 동안 Workfront Fusion에서 반환해야 하는 최대 이벤트 수를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 이벤트 업데이트]

이 작업 모듈은 기존 이벤트를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 대한 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이벤트 ID]</td> 
   <td>업데이트하려는 이벤트의 ID를 입력하거나 매핑하거나 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>이벤트의 새 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작 날짜]</td> 
   <td> 결합된 날짜 및 시간 표현에서 이벤트가 시작되는 단일 시점을 입력합니다. <code>{date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">유형 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 종료 날짜]</td> 
   <td> 이벤트가 결합된 날짜 및 시간 표시로 끝나는 단일 시점을 입력합니다. <code>({date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">유형 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 미리 알림 설정]</td> 
   <td>이 이벤트에 대한 미리 알림을 활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 알림 메시지]</td> 
   <td>미리 알림이 트리거되어야 하는 이벤트 시작 전 시간(분)을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 중요도]</td> 
   <td> <p>이 이벤트의 중요도를 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 낮음]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL 높음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 감도] </td> 
   <td> <p>이 이벤트의 민감도를 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>수신자에게 "[!UICONTROL Please treat this as Personal]" 메시지가 표시됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>수신자에게 "[!UICONTROL Please treat this as Private]" 메시지가 표시됩니다. 이 이벤트는 수신자의 받은 편지함 규칙에 의해 전달되거나 리디렉션되지 않습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>수신자에게 "[!UICONTROL 기밀 정보로 취급하십시오]" 메시지가 표시됩니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문 컨텐츠 유형]</td> 
   <td>이벤트와 연결된 메시지의 본문 콘텐츠가 일반 텍스트인지 HTML인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>이벤트와 연계된 메시지 본문을 입력하거나 매핑합니다. 위의 [!UICONTROL Body Content Type] 필드에 지정된 대로 HTML 또는 텍스트 형식일 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 위치]</td> 
   <td> <p>이벤트 위치 세부 정보를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 응답 요청됨]</td> 
   <td>초대자에게 이벤트 초대에 대한 응답을 보내도록 요청하려면 <strong>[!UICONTROL 예]</strong>를 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 다음으로 표시]</td> 
   <td> <p>캘린더를 보는 사람에게 이벤트를 표시할 방법을 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL 미정]</li> 
     <li>[!UICONTROL 사용 중]</li> 
     <li>[!UICONTROL 부재 중]</li> 
     <li>[!UICONTROL 다른 곳에서 작업]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 출석자]</p> </td> 
   <td> <p>이벤트의 참석자를 추가합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>참석자의 이름을 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>참석자의 전자 메일 주소를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 범주]</td> 
   <td>이벤트를 캘린더에 표시할 범주를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 이벤트 보기]

이 트리거 모듈은 선택한 달력에서 이벤트가 생성, 업데이트, 삭제, 시작 또는 종료될 때 이벤트의 세부 정보를 검색합니다.

>[!NOTE]
>
>이벤트 시리즈가 삭제되었는지 확인하려면 [!UICONTROL 이벤트 보기] 필드에서 [!UICONTROL 업데이트된 시간별]을(를) 선택하십시오. 이 모듈은 삭제된 단일 이벤트나 삭제된 이벤트 시리즈를 감시하지 않습니다.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 감시 이벤트]</td> 
   <td> <p>이벤트 시청 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 작성일 기준]</strong> </p> <p>새로운 이벤트를 확인하십시오.</p> </li> 
     <li> <p>업데이트된 시간까지 <strong></strong> </p> <p>업데이트된 이벤트를 확인하십시오.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 달력 그룹 ID]</td> 
   <td>이벤트를 보려는 캘린더가 포함된 [!UICONTROL 캘린더 그룹]을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>보려는 특정 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필터]</td> 
   <td>필터 조건을 설정하여 결과를 주제, 이벤트 ID 또는 본문별로 필터링합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>한 시나리오 실행 주기 동안 Workfront Fusion이 반환해야 하는 최대 메시지 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 캘린더

* [[!UICONTROL 일정 만들기]](#create-a-calendar)
* [[!UICONTROL 일정 삭제]](#delete-a-calendar)
* [[!UICONTROL 일정 가져오기]](#get-a-calendar)
* [[!UICONTROL 일정 나열]](#list-calendars)
* [[!UICONTROL 일정 업데이트]](#update-a-calendar)



#### [!UICONTROL 일정 만들기]

이 작업 모듈은 Office 365 계정에 새 달력을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar name]</td> 
   <td> <p>새 캘린더의 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 일정 삭제]

이 작업 모듈은 기존 캘린더를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 달력 ID]</td> 
   <td>삭제할 달력의 [!UICONTROL Calendar] ID를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 일정 가져오기]

이 작업 모듈은 단일 캘린더에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 달력 ID]</td> 
   <td> <p>세부 정보를 검색할 달력의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 일정 나열]

이 검색 모듈은 인증된 사용자의 모든 캘린더 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 달력 그룹 ID]</td> 
   <td>나열할 캘린더가 포함된 [!UICONTROL 캘린더 그룹]을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td>한 시나리오 실행 주기 동안 Workfront Fusion에서 반환해야 하는 최대 달력 수를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 일정 업데이트]

이 작업 모듈은 기존 일정을 편집합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 대한 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 일정 ID]</td> 
   <td>업데이트할 캘린더의 [!UICONTROL Calendar ID]를 입력하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 새 일정 이름]</td> 
   <td> <p>캘린더의 새 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

#### [!UICONTROL API 호출]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 대한 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code>https://graph.microsoft.com</code>와 관련된 경로를 입력합니다. 예:<code> /v1.0/me/events</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메서드]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다. 예, <code>{"Content-type":"application/json"}</code>. Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p> 표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:   <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
