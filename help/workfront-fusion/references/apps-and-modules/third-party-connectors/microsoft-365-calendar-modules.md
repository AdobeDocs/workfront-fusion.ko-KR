---
title: Microsoft Office 365 달력
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Microsoft Office 365 캘린더를 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
source-git-commit: ddebec2d03d9d843c46182d92df6c8a871799999
workflow-type: tm+mt
source-wordcount: '1560'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Calendar]

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Microsoft Office 365 Calendar]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
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

## [!DNL Workfront Fusion]에 [!DNL Office 365 Calendar] 서비스를 연결하는 중

[!DNL Office 365 Calendar] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하세요.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.

## [!DNL Microsoft Office 365 Calendar]개 모듈 및 해당 필드

[!DNL Microsoft Office 365 Calendar] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Microsoft Office 365 Calendar] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [이벤트](#event)
* [캘린더](#calendar)
* [기타](#other)

### 이벤트

* [[!UICONTROL Create an Event]](#create-an-event)
* [[!UICONTROL Delete an Event]](#delete-an-event)
* [[!UICONTROL Get an Event]](#get-an-event)
* [[!UICONTROL Search Events]](#search-events)
* [[!UICONTROL Update an Event]](#update-an-event)
* [[!UICONTROL Watch Events]](#watch-events)

#### [!UICONTROL Create an Event]

이 작업 모듈은 새 이벤트를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>생성된 이벤트의 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> 결합된 날짜 및 시간 표현에서 이벤트가 시작되는 단일 시점을 입력합니다. <code>{date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> 이벤트가 결합된 날짜 및 시간 표시로 끝나는 단일 시점을 입력합니다. <code>{date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>이 이벤트에 대한 미리 알림을 활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>미리 알림이 트리거되어야 하는 이벤트 시작 전 시간(분)을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>이 이벤트의 중요도를 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>이 이벤트의 민감도를 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>받는 사람에게 "[!UICONTROL Please treat this as Personal]" 메시지가 표시됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>받는 사람에게 "[!UICONTROL Please treat this as Private]" 메시지가 표시됩니다. 이 이벤트는 수신자의 받은 편지함 규칙에 의해 전달되거나 리디렉션되지 않습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>받는 사람에게 "[!UICONTROL Please treat this as Confidential]" 메시지가 표시됩니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>본문 컨텐츠가 일반 텍스트인지 HTML인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>이벤트와 연계된 메시지 본문을 입력하거나 매핑합니다. HTML 또는 텍스트 형식일 수 있습니다(위의 [!UICONTROL Body Content Type] 필드에 지정된 형식).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>이벤트 위치 세부 정보를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>초대자에게 이벤트 초대에 대한 응답을 보내도록 요청하려면 <strong>[!UICONTROL Yes]</strong>을(를) 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>캘린더를 보는 사람에게 이벤트를 표시할 방법을 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!UICONTROL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>초대할 각 참석자에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>참석자의 이름을 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>참석자의 이메일 주소를 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Categories]</td> 
   <td>이벤트를 캘린더에 표시할 각 범주에 대해 <b>항목 추가</b>를 클릭하고 범주를 입력하거나 매핑하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Event]

이 작업 모듈은 기존 이벤트를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>삭제할 이벤트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Event]

이 작업 모듈은 지정된 이벤트의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>세부 정보를 검색할 이벤트 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Events]

이 검색 모듈은 선택한 달력에서 이벤트가 생성, 업데이트, 삭제, 시작 또는 종료될 때 이벤트의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>이벤트를 볼 캘린더가 포함된 [!UICONTROL calendar group]을(를) 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>보려는 특정 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>결과를 필터링하려면 필터 조건을 설정하십시오. 다음 속성을 기준으로 필터링할 수 있습니다.</p> 
    <ul> 
     <li>[!UICONTROL Subject]</li> 
     <li>[!UICONTROL Event ID]</li> 
     <li>[!UICONTROL Created Date Time]</li> 
     <li>[!UICONTROL Last Modified Date Time]</li> 
     <li>[!UICONTROL Body Preview]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>결과 정렬 방법을 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Subject]</strong>, 오름차순 또는 내림차순</li> 
     <li><strong>[!UICONTROL Created Date Time]</strong>, 오름차순 또는 내림차순</li> 
     <li><strong>[!UICONTROL Last Modified Date Time]</strong>, 오름차순 또는 내림차순</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>시나리오 실행 주기 동안 반환해야 하는 최대 이벤트 수 [!DNL Workfront Fusion]을(를) 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an Event]

이 작업 모듈은 기존 이벤트를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>업데이트하려는 이벤트의 ID를 입력하거나 매핑하거나 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>이벤트의 새 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> 결합된 날짜 및 시간 표현에서 이벤트가 시작되는 단일 시점을 입력합니다. <code>{date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록을 보려면 [!DNL Adobe Workfront Fusion]</a>의 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 변환을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> 이벤트가 결합된 날짜 및 시간 표시로 끝나는 단일 시점을 입력합니다. <code>({date}T{time}</code> 형식을 사용하십시오(예: <code>2017-08-29T04:00:00.0000000</code>). 지원되는 날짜 및 시간 형식 목록을 보려면 [!DNL Adobe Workfront Fusion]</a>의 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 변환을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>이 이벤트에 대한 미리 알림을 활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>미리 알림이 트리거되어야 하는 이벤트 시작 전 시간(분)을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>이 이벤트의 중요도를 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>이 이벤트의 민감도를 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>받는 사람에게 "[!UICONTROL Please treat this as Personal]" 메시지가 표시됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>받는 사람에게 "[!UICONTROL Please treat this as Private]" 메시지가 표시됩니다. 이 이벤트는 수신자의 받은 편지함 규칙에 의해 전달되거나 리디렉션되지 않습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>받는 사람에게 "[!UICONTROL Please treat this as Confidential]" 메시지가 표시됩니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>이벤트와 연결된 메시지의 본문 콘텐츠가 일반 텍스트인지 아니면 HTML인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>이벤트와 연계된 메시지 본문을 입력하거나 매핑합니다. HTML 또는 텍스트 형식일 수 있습니다(위의 [!UICONTROL Body Content Type] 필드에 지정된 형식).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>이벤트 위치 세부 정보를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>초대자에게 이벤트 초대에 대한 응답을 보내도록 요청하려면 <strong>[!UICONTROL Yes]</strong>을(를) 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>캘린더를 보는 사람에게 이벤트를 표시할 방법을 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>이벤트 참석자를 추가합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>참석자의 이름을 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>참석자의 이메일 주소를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>이벤트를 캘린더에 표시할 범주를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Events]

이 트리거 모듈은 선택한 달력에서 이벤트가 생성, 업데이트, 삭제, 시작 또는 종료될 때 이벤트의 세부 정보를 검색합니다.

>[!NOTE]
>
>이벤트 시리즈가 삭제되었는지 확인하려면 [!UICONTROL Watch events] 필드에서 [!UICONTROL By Updated Time]을(를) 선택합니다. 이 모듈은 삭제된 단일 이벤트 또는 삭제된 이벤트 시리즈를 감시하지 않습니다.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch events]</td> 
   <td> <p>이벤트 시청 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By Created Time]</strong> </p> <p>새로운 이벤트를 확인하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL By Updated Time]</strong> </p> <p>업데이트된 이벤트를 확인하십시오.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>이벤트를 볼 캘린더가 포함된 [!UICONTROL calendar group]을(를) 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>보려는 특정 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>필터 조건을 설정하여 결과를 주제, 이벤트 ID 또는 본문별로 필터링합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>시나리오 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환해야 하는 최대 메시지 수를 입력하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 캘린더

* [[!UICONTROL Create a Calendar]](#create-a-calendar)
* [[!UICONTROL Delete a Calendar]](#delete-a-calendar)
* [[!UICONTROL Get a Calendar]](#get-a-calendar)
* [[!UICONTROL List Calendars]](#list-calendars)
* [[!UICONTROL Update a Calendar]](#update-a-calendar)



#### [!UICONTROL Create a Calendar]

이 작업 모듈은 Office 365 계정에 새 달력을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar name]</td> 
   <td> <p>새 캘린더의 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Calendar]

이 작업 모듈은 기존 캘린더를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>삭제할 일정에 대한 [!UICONTROL Calendar] ID를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Calendar]

이 작업 모듈은 단일 캘린더에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>세부 정보를 검색할 달력의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Calendars]

이 검색 모듈은 인증된 사용자의 모든 캘린더 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>나열할 일정이 포함된 [!UICONTROL calendar group]을(를) 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>시나리오 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환해야 하는 최대 캘린더 수를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Calendar]

이 작업 모듈은 기존 캘린더를 편집합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>업데이트할 일정에 대한 [!UICONTROL Calendar ID]을(를) 입력하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Calendar name]</td> 
   <td> <p>달력의 새 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

#### [!UICONTROL Make an API Call]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code>https://graph.microsoft.com</code>과(와) 관련된 경로를 입력하십시오. 예:<code> /v1.0/me/events</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 예: <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion]이(가) 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
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
