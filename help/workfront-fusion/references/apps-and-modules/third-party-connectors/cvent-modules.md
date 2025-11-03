---
title: 이벤트 모듈
description: Adobe Workfront Fusion 시나리오에서는 Cvent를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 1%

---

# [!DNL Cvent]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Cvent]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

## Adobe Workfront Fusion에 [!DNL Cvent] 연결 {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>[!DNL Cvent] 모듈은 [!UICONTROL SOAP] API를 통해 작동합니다. [!DNL Cvent]에 대한 연결을 만들려면 다음을 확인해야 합니다.
>
>* [!UICONTROL  API에 대한 ]SOAP[!DNL Cvent] 액세스 권한이 있습니다.
>* Workfront Fusion IP 주소가 조직의 허용 목록에 추가하다에 추가되었습니다.
>
>  Workfront 허용 목록에 추가하다 Fusion IP 주소 목록을 보려면 [조직의 Fusion에 대한 IP 주소 구성](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)을 참조하십시오.


[!DNL Cvent] 모듈 내에서 직접 [!DNL Cvent] 계정에 연결할 수 있습니다.

1. [!DNL Cvent] 모듈에서 **[!UICONTROL 연결]** 필드 옆에 있는 [!UICONTROL 추가]를 클릭합니다.
1. 연결할 지역을 선택합니다.

   * [!UICONTROL 북미]
   * [!UICONTROL 유럽]
   * [!UICONTROL 샌드박스]

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## [!DNL Cvent]개 모듈 및 해당 필드

[!DNL Cvent] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Cvent] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [검색 결과](#searches)

### 액션

* [[!UICONTROL 사용자 지정 API 호출]](#create-meeting-request)
* [[!UICONTROL 레코드 읽기]](#read-a-record)
* [[!UICONTROL 초대 대상자 등록]](#register-invitee)
* [[!UICONTROL 초대 대상자 추가]](#add-invitee)
* [[!UICONTROL 연락처 삭제]](#delete-contact)
* [[!UICONTROL 연락처 업데이트]](#update-contact)
* [[!UICONTROL 모임 요청 만들기]](#create-meeting-request)

#### [!UICONTROL 사용자 지정 API 호출]

이 작업 모듈을 사용하면 [!DNL Cvent] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Cvent] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

이 모듈은 API 호출의 헤더 및 본문과 함께 상태 코드를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
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

#### [!UICONTROL 레코드 읽기]

이 작업 모듈은 특정 레코드에 대한 정보를 읽습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 레코드 유형]</p> </td> 
   <td>읽으려는 레코드의 항목 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact] / [!UICONTROL Event] / [!UICONTROL 초대 ID]</td> 
   <td> <p>읽으려는 항목의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다. 필드는 선택한 항목 유형에 따라 사용할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 초대 대상자 등록]

이 작업 모듈은 이벤트에 대한 초대장을 등록합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
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

#### [!UICONTROL 초대 대상자 추가]

이 작업 모듈은 이벤트에 연락처를 초대합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연락처 ID]</p> </td> 
   <td> <p>이벤트에 추가하려는 연락처의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이벤트 ID]</td> 
   <td> <p>연락처를 추가할 이벤트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 연락처 삭제]

이 작업 모듈은 Cvent의 단일 연락처를 삭제합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연락처 ID]</td> 
   <td> <p>삭제하려는 연락처의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 연락처 업데이트]

이 작업 모듈은 해당 ID를 사용하여 기존 연락처를 업데이트합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연락처 ID]</p> </td> 
   <td> <p>업데이트하려는 연락처의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td> <p>정보를 입력할 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사용자 정의 필드]</td> 
   <td> <p>정보를 입력할 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 모임 요청 만들기]

이 작업 모듈은 귀하의 계정에 모임 요청을 추가합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 양식 ID]</p> </td> 
   <td> <p>새 모임 요청을 만드는 데 사용할 양식의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모임 요청 필드]</td> 
   <td> <p>정보를 입력할 모임 요청 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이벤트 요청 필드]</td> 
   <td> <p>정보를 입력할 이벤트 요청 필드를 선택한 다음 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL RFP 요청 필드]</td> 
   <td> <p>정보를 입력할 제안 필드에 대한 요청을 선택한 다음, 해당 필드에 대해 원하는 값을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

#### [!UICONTROL 레코드 나열]

이 검색 모듈은 특정 유형의 모든 레코드에 대한 정보를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Cvent] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Cvent] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 레코드 유형]</p> </td> 
   <td> <p>나열할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!DNL Cvent] 계정의 모든 이벤트</p> </li> 
     <li> <p>이벤트에 대한 모든 세션</p> </li> 
     <li> <p>이벤트에 대한 모든 초대됨</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이벤트 ID]</td> 
   <td> <p>초대받은 사람이나 세션을 나열하는 경우 초대받은 사람이나 세션이 연결된 이벤트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
