---
title: Google 달력 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Google 캘린더를 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 160e503adeca5404e18fd0cba9f475fee8510a48
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# [!DNL Google Calendar]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!UICONTROL Google Calendar]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

## 전제 조건

[!DNL Google Calendar] 모듈을 사용하려면 [!DNL Google] 계정이 있어야 합니다.

## Google Calendar API 정보

Google Calendar 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Calendar]개 모듈 및 해당 필드

[!DNL Google Calendar] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Calendar] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [트리거](#triggers)
* [액션](#actions)
* [반복기](#iterators)

### 트리거

* [이벤트 보기](#watch-events)
* [이벤트 보기(인스턴트)](#watch-events-instant)

#### 이벤트 보기

이 트리거 모듈은 지정한 달력에서 새 이벤트가 추가, 업데이트, 삭제, 시작 또는 종료될 때 시나리오를 실행합니다. 모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드 또는 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Calendar] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe 연결 만들기 [!DNL Workfront Fusion] - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>모듈을 사용할 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>새 이벤트만 시청할지, 새 이벤트와 모든 변경 사항을 시청할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>삭제된 이벤트를 포함하려면 이 옵션을 활성화하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>결과를 반환할 텍스트를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 작동하는 최대 이벤트 수(시나리오 실행당 반복 수)를 설정합니다. 값이 너무 높게 설정되면 지정된 타사 서비스 측에서 연결이 중단될 수 있습니다(시간 초과). [!DNL Workfront Fusion]은(는) 이 작업에 영향을 주지 않습니다. 낮은 값을 설정하고 최대 주기 횟수에 대해 높은 값을 정의하거나 시나리오를 더 자주 실행하는 것이 좋습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 이벤트 보기(인스턴트)

이 트리거 모듈은 메일 후크를 사용하여 이벤트에 대한 초대로 사용할 수 있는 이메일 주소를 만듭니다. 모듈은 이메일 주소가 초대된 이벤트를 기반으로 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>이 모듈에 사용할 메일 후크를 선택합니다. 새 메일 후크를 만들려면 <b>추가</b>를 클릭하고 메일 후크에 사용할 연결을 입력하십시오.</p><p>[!DNL Google Calendar] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe 연결 만들기 [!DNL Workfront Fusion] - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 작동하는 최대 이벤트 수(시나리오 실행당 반복 수)를 설정합니다. 값이 너무 높게 설정되면 지정된 타사 서비스 측에서 연결이 중단될 수 있습니다(시간 초과). [!DNL Workfront Fusion]은(는) 이 작업에 영향을 주지 않습니다. 낮은 값을 설정하고 최대 주기 횟수에 대해 높은 값을 정의하거나 시나리오를 더 자주 실행하는 것이 좋습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [캘린더 만들기](#create-a-calendar)
* [이벤트 만들기](#create-an-event)
* [이벤트 삭제](#delete-an-event)
* [이벤트 가져오기](#get-events)
* [이벤트 업데이트](#update-an-event)

#### 캘린더 만들기

이 작업 모듈은 계정과 연결된 캘린더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Calendar] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe 연결 만들기 [!DNL Workfront Fusion] - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>캘린더와 연결할 색상을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>새 달력의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

이 작업 모듈은 이벤트를 만듭니다.

이벤트에 대한 달력과 매개 변수를 지정합니다.

모듈은 연결에 액세스하는 사용자 지정 필드 및 값과 함께 이벤트의 ID 및 연결된 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>[!DNL Google Calendar] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>이벤트를 표시할 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>캘린더에 이벤트가 표시되는 색상을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> 이벤트의 이름을 입력하거나 매핑합니다. </p> <p>참고: [!UICONTROL Create an event] 필드에서 [!UICONTROL Quick add]을(를) 선택한 경우 이벤트의 날짜 및 시간을 포함할 수 있으며 [!DNL Workfront Fusion]에서 해당 날짜 및 시간에 대한 이벤트를 만듭니다. 예: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code> [!UICONTROL Quick add]을(를) 선택했지만 이벤트 이름에 날짜 및 시간을 포함하지 않는 경우 현재 시간부터 이벤트가 만들어지고 1시간 동안 진행됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>이벤트가 종일 이벤트인 경우(시작 및 종료 시간이 필요하지 않음) 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>이벤트의 시작 날짜 및 시간을 입력하거나 매핑합니다. </p> <p>지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 이벤트의 종료 날짜 및 시간을 입력하거나 매핑합니다. </p> <p>지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>이벤트에 대한 설명을 입력하거나 매핑합니다. 이 필드는 HTML을 지원합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>텍스트 양식에서 이벤트의 위치를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>기본 미리 알림 설정을 사용하려면 이 옵션을 활성화하십시오. [!UICONTROL Reminder] 필드에 사용자 지정 미리 알림을 설정하면 이 값은 [아니요]로 설정됩니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>이벤트에 대한 알림 메시지를 추가합니다. 추가할 각 미리 알림에 대해 <b>항목 추가</b>를 클릭한 다음 미리 알림을 받을 방법을 선택하고 미리 알림을 받을 이벤트까지 남은 시간(분)을 정의합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>이벤트에 참석자를 추가합니다. 각 참석자에 대해 <b>참석자 추가</b>를 클릭한 다음 이름과 전자 메일 주소를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>이 이벤트 동안 캘린더를 보는 사람이 [사용 중]으로 표시할지 또는 [사용 가능]으로 표시할지를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>이 이벤트의 가시성을 선택합니다. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>이벤트에는 달력 설정에서 설정한 가시성이 있습니다.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>캘린더를 공유하는 모든 사용자는 이 이벤트를 볼 수 있습니다.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>참석자만 이 이벤트를 볼 수 있습니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>새 이벤트 만들기에 대한 알림을 모든 게스트에게 보낼지, [!DNL Google Calendar]명이 아닌 게스트에게 보낼지, 아무도 보내지 않을지 선택합니다.</p> <p>팁: 마이그레이션 사용 사례에만 [!UICONTROL None] 옵션을 사용하는 것이 좋습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>게스트가 이 이벤트를 수정할 수 있도록 하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>이 이벤트에 적용할 되풀이 규칙을 추가합니다. 각 규칙에는 되풀이되는 이벤트에 대해 [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] 및 [!UICONTROL EXDATE] 줄 목록이 필요합니다. 이 필드에는 [!UICONTROL DTSTART] 및 [!UICONTROL DTEND] 줄이 허용되지 않습니다. 이벤트 시작 및 종료 시간은 시작 및 종료 필드에 지정됩니다. 이 필드는 단일 이벤트 또는 반복 이벤트의 인스턴스에 대해서는 생략됩니다. 자세한 내용은 <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>을(를) 참조하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an event]

이 작업 모듈은 이벤트를 삭제합니다.

달력 및 이벤트 ID를 지정합니다.

모듈은 연결에 액세스하는 사용자 지정 필드 및 값과 함께 이벤트의 ID 및 연결된 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Calendar] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe 연결 만들기 [!DNL Workfront Fusion] - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>삭제할 이벤트가 포함된 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> 삭제하려는 이전에 만든 [!DNL Google Calendar] 이벤트의 이벤트 ID를 입력하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get events]

이 모듈은 지정한 기준에 따라 선택한 달력에서 이벤트에 대한 정보를 검색합니다.

검색의 달력과 매개 변수를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 이벤트 및 연결된 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>[!DNL Google Calendar] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>이벤트를 검색할 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> 이벤트가 시작되는 날짜를 입력하거나 매핑합니다. 또한 이 모듈은 이 날짜 이전에 시작된 이벤트로서 입력한 시작 날짜에 여전히 발생하는 이벤트도 검색합니다. </p> <p>지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 이벤트가 종료되는 날짜를 입력하거나 매핑합니다. </p> <p> 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> 반복 이벤트를 단일 인스턴스로 처리하려면 이 옵션을 활성화합니다. 예를 들어 주간 회의가 있고 이 옵션이 활성화된 경우 모듈은 각 주의 회의를 별도의 이벤트로 반환합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>검색할 검색어를 입력하거나 매핑합니다. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>결과에서 반환되는 이벤트의 순서를 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong>: 시작 날짜 및 시간별 순서(오름차순). 단일 이벤트를 쿼리할 때만 사용할 수 있습니다.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: 마지막 수정 시간별 정렬(오름차순)</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mazimum number of returned events]</td> 
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]에서 반환되는 최대 이벤트 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event]

이 작업 모듈은 기존 이벤트를 변경합니다.

달력 및 이벤트 ID를 지정합니다.

모듈은 연결에 액세스하는 사용자 지정 필드 및 값과 함께 이벤트의 ID 및 연결된 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Calendar] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe 연결 만들기 [!DNL Workfront Fusion] - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>작업할 달력을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>이전에 만든 [!DNL Google Calendar] 이벤트에서 업데이트할 이벤트 ID를 입력하십시오.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> 이벤트의 이름을 입력하거나 매핑합니다. </p> <p>참고: [!UICONTROL Create an event] 필드에서 [!UICONTROL Quick add]을(를) 선택한 경우 이벤트의 날짜 및 시간을 포함할 수 있으며 [!DNL Workfront Fusion]에서 해당 날짜 및 시간에 대한 이벤트를 만듭니다. 예: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code> [!UICONTROL Quick add]을(를) 선택했지만 이벤트 이름에 날짜 및 시간을 포함하지 않는 경우 현재 시간부터 이벤트가 만들어지고 1시간 동안 진행됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>이벤트가 종일 이벤트인 경우(시작 및 종료 시간이 필요하지 않음) 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>이벤트의 시작 날짜 및 시간을 입력하거나 매핑합니다. </p> <p>지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 이벤트의 종료 날짜 및 시간을 입력하거나 매핑합니다. </p> <p>지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>이벤트에 대한 설명을 입력하거나 매핑합니다. 이 필드는 HTML을 지원합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>텍스트 양식에서 이벤트의 위치를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>기본 미리 알림 설정을 사용하려면 이 옵션을 활성화하십시오. [!UICONTROL Reminder] 필드에 사용자 지정 미리 알림을 설정하면 이 값은 [아니요]로 설정됩니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>이벤트에 대한 알림 메시지를 추가합니다. 추가할 각 미리 알림에 대해 <b>항목 추가</b>를 클릭한 다음 미리 알림을 받을 방법을 선택하고 미리 알림을 받을 이벤트까지 남은 시간(분)을 정의합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>이벤트에 참석자를 추가합니다. 각 참석자에 대해 <b>참석자 추가</b>를 클릭한 다음 이름과 전자 메일 주소를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>이 이벤트 동안 캘린더를 보는 사람이 [사용 중]으로 표시할지 또는 [사용 가능]으로 표시할지를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>이 이벤트의 가시성을 선택합니다. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>이벤트에는 달력 설정에서 설정한 가시성이 있습니다.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>캘린더를 공유하는 모든 사용자는 이 이벤트를 볼 수 있습니다.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>참석자만 이 이벤트를 볼 수 있습니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>새 이벤트 만들기에 대한 알림을 모든 게스트에게 보낼지, [!DNL Google Calendar]명이 아닌 게스트에게 보낼지, 아무도 보내지 않을지 선택합니다.</p> <p>팁: 마이그레이션 사용 사례에만 [!UICONTROL None] 옵션을 사용하는 것이 좋습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>게스트가 이 이벤트를 수정할 수 있도록 하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>이 이벤트에 적용할 되풀이 규칙을 추가합니다. 각 규칙에는 되풀이되는 이벤트에 대해 [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] 및 [!UICONTROL EXDATE] 줄 목록이 필요합니다. 이 필드에는 [!UICONTROL DTSTART] 및 [!UICONTROL DTEND] 줄이 허용되지 않습니다. 이벤트 시작 및 종료 시간은 시작 및 종료 필드에 지정됩니다. 이 필드는 단일 이벤트 또는 반복 이벤트의 인스턴스에 대해서는 생략됩니다. 자세한 내용은 <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>을(를) 참조하십시오.</td> 
  </tr>

</tbody> 
</table>

### 반복기

#### 첨부 파일 반복

이 작업 모듈은 첨부 파일을 이벤트로 반복하고 각 첨부 파일을 별도의 번들로 출력합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> 반복하려는 첨부 파일이 포함된 이벤트를 출력하는 이 시나리오의 모듈을 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### 참석자 반복

이 작업 모듈은 이벤트의 참석자를 반복하며 각 참석자를 별도의 번들로 출력합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> 이 시나리오에서 반복할 참석자가 포함된 이벤트를 출력하는 모듈을 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>





## 이벤트 전에 시나리오 트리거

표준 [!DNL Google Calendar] 전자 메일 미리 알림 및 [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] 모듈을 통해 지정된 시간 전에 시나리오를 트리거할 수 있습니다.

1. [!UICONTROL Google Calendar] >[!UICONTROL Update an event] 모듈을 사용하여 전자 메일 미리 알림을 이벤트에 추가하십시오.

   ![이벤트 전에 시나리오 트리거](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] 모듈로 시작하는 새 시나리오를 만듭니다.

   1. 메일후크의 이메일 주소를 복사합니다.
   1. 시나리오를 저장하고 실행합니다.

1. [!DNL Gmail]에서 [!DNL Google Calendar] 전자 메일 미리 알림을 메일 후크의 전자 메일 주소로 리디렉션합니다.

   1. **[!UICONTROL [!DNL Gmail] settings]**&#x200B;을 엽니다.
   1. **[!UICONTROL Forwarding and POP/IMAP]** 탭을 엽니다.
   1. **[!UICONTROL Add a forwarding address].** 클릭
   1. 복사한 메일 후크의 전자 메일 주소를 붙여 넣고 {&#x200B;0}을(를) 클릭한 다음 팝업 창에서 **[!UICONTROL Proceed]**&#x200B;을(를) 눌러 확인한 다음 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.**[!UICONTROL Next]**

   1. [!DNL Workfront Fusion]에서 확인 이메일을 받아 실행을 완료해야 하는 새 시나리오로 전환합니다.
   1. 모듈 위의 버블을 클릭하여 모듈의 출력을 검사합니다.
   1. `Text` 항목을 확장하고 확인 코드를 복사합니다.

      ![확인 코드](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. Gmail에서 편집 상자에 확인 코드를 붙여 넣고 {0&#x200B;}을(를) 클릭합니다.**[!UICONTROL Verify]**

      ![코드 붙여넣기](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. **[!UICONTROL Filters and Blocked Addresses]** 탭을 엽니다.
   1. **[!UICONTROL Create a new filter]**&#x200B;을(를) 클릭합니다.
   1. `     calendar-notification@google.com`에서 보낸 모든 전자 메일에 대한 필터를 설정하고 **[!UICONTROL Create a filter]**&#x200B;을(&#x200B;을) 클릭합니다.
   1. **[!UICONTROL Forward it to]**&#x200B;을(를) 선택하고 목록에서 메일 후크 전자 메일 주소를 선택합니다.
   1. 필터를 만들려면 **[!UICONTROL Create filter]**&#x200B;을(를) 클릭합니다.

1. (선택 사항) [!DNL Workfront Fusion]에서 [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] 모듈 뒤에 [!UICONTROL Text parser] > [!UICONTROL Match pattern] 모듈을 추가하여 전자 메일의 HTML 코드를 구문 분석하여 필요한 정보를 얻습니다.

   예를 들어 이벤트의 ID를 가져오도록 다음과 같이 모듈을 구성할 수 있습니다.

   *패턴*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *텍스트*: [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] 모듈에서 출력되는 `HTML content` 항목입니다.
