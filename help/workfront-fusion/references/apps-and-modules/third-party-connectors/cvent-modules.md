---
title: 이벤트 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Cvent를 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%

---

# [!DNL Cvent]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Cvent]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

[!DNL Cvent] 모듈을 사용하려면 [!DNL Cvent] 계정이 있어야 합니다.

## Cvent API 정보

Cvent 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> V200611.ASMX </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.7.14</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]에 연결 {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>[!DNL Cvent] 모듈은 [!UICONTROL SOAP] API를 통해 작동합니다. [!DNL Cvent]에 대한 연결을 만들려면 다음을 확인해야 합니다.
>
>* [!DNL Cvent] API에 대한 [!UICONTROL SOAP] 액세스 권한이 있습니다.
>* 조직의 [!DNL Workfront Fusion] IP 주소가 허용 목록에 추가하다에 추가되었습니다.
>
>  허용 목록에 추가하다 [!DNL Workfront Fusion]개의 IP 주소 목록을 보려면 [조직의 Fusion에 대한 IP 주소 구성](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)을 참조하십시오.


[!DNL Cvent] 모듈 내에서 직접 [!DNL Cvent] 계정에 연결할 수 있습니다.

1. [!DNL Cvent] 모듈에서 [!UICONTROL Connection] 필드 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 연결할 지역을 선택합니다.

   * [!UICONTROL North America]
   * [!UICONTROL Europe]
   * [!UICONTROL Sandbox]

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## [!DNL Cvent]개 모듈 및 해당 필드

[!DNL Cvent] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Cvent] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [검색 결과](#searches)

### 액션

* [[!UICONTROL Custom API Call]](#create-meeting-request)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Register Invitee]](#register-invitee)
* [[!UICONTROL Add Invitee]](#add-invitee)
* [[!UICONTROL Delete Contact]](#delete-contact)
* [[!UICONTROL Update Contact]](#update-contact)
* [[!UICONTROL Create meeting request]](#create-meeting-request)

#### [!UICONTROL Custom API Call]

이 작업 모듈을 사용하면 [!DNL Cvent] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Cvent] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

이 모듈은 API 호출의 헤더 및 본문과 함께 상태 코드를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">작업</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">본문(XML)</td> 
   <td> <p>API 호출 본문을 입력하거나 매핑합니다. XML만 포함해야 합니다. 모듈에 인증 헤더가 자동으로 포함됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

이 작업 모듈은 특정 레코드에 대한 정보를 읽습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td>읽으려는 레코드의 항목 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact] / [!UICONTROL Event] / [!UICONTROL Invitee ID]</td> 
   <td> <p>읽으려는 항목의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다. 필드는 선택한 항목 유형에 따라 사용할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Register Invitee]

이 작업 모듈은 이벤트에 대한 초대장을 등록합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>초대 ID</p> </td> 
   <td> <p>이벤트에 등록할 초대장의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">이벤트 ID</td> 
   <td> <p>초대를 등록할 이벤트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Invitee]

이 작업 모듈은 이벤트에 연락처를 초대합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>이벤트에 추가하려는 연락처의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>연락처를 추가할 이벤트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Contact]

이 작업 모듈은 Cvent의 단일 연락처를 삭제합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID]</td> 
   <td> <p>삭제하려는 연락처의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update Contact]

이 작업 모듈은 해당 ID를 사용하여 기존 연락처를 업데이트합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>업데이트하려는 연락처의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>정보를 입력할 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> <p>정보를 입력할 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create meeting request]

이 작업 모듈은 귀하의 계정에 모임 요청을 추가합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Form ID]</p> </td> 
   <td> <p>새 모임 요청을 만드는 데 사용할 양식의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Meeting Request Fields]</td> 
   <td> <p>정보를 입력할 모임 요청 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Request Fields]</td> 
   <td> <p>정보를 입력할 이벤트 요청 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL RFP Request Fields]</td> 
   <td> <p>정보를 입력할 제안 필드에 대한 요청을 선택한 다음, 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

#### [!UICONTROL List records]

이 검색 모듈은 특정 유형의 모든 레코드에 대한 정보를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Cvent]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td> <p>나열할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!DNL Cvent] 계정의 모든 이벤트</p> </li> 
     <li> <p>이벤트에 대한 모든 세션</p> </li> 
     <li> <p>이벤트에 대한 모든 초대됨</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>초대받은 사람이나 세션을 나열하는 경우 초대받은 사람이나 세션이 연결된 이벤트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
