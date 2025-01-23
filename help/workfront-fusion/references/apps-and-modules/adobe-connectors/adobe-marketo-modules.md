---
title: Marketo 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는  [!DNL Marketo]을(를) 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1814'
ht-degree: 0%

---

# [!DNL Marketo]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Marketo]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

Marketo 커넥터에 대한 비디오 소개는 다음을 참조하십시오.

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

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

[!DNL Marketo] 모듈을 사용하려면 [!DNL Marketo] 계정이 있어야 합니다.

## Marketo API 정보

Marketo 커넥터는 다음을 사용합니다.

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
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL Marketo] 연결 {#connect-marketo-to-workfront-fusion}

[!DNL Marketo] 모듈 내에서 직접 [!DNL Marketo] 계정에 연결할 수 있습니다.

1. 모든 Marketo 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>새 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Account / Munchkin ID]</td>
        <td>
          <p>[!DNL Marketo] 계정 또는 [!DNL Marketo] [!UICONTROL Munchkin] ID를 입력하십시오. 계정에 할당된 기본 URL 또는 끝점의 고유한 부분이며, 해당 [!UICONTROL REST] API를 통해 [!DNL Marketo]에 액세스하는 데 사용합니다. 찾는 방법에 대한 지침은 [!DNL Marketo] 설명서의 [기본 URL](https://developers.marketo.com/rest-api/base-url/)을 참조하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Marketo 클라이언트 ID를 입력합니다. 찾는 방법에 대한 지침은 [!DNL Marketo] 설명서의 [Authentication](https://developers.marketo.com/rest-api/authentication/)을 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Marketo 클라이언트 암호를 입력합니다. 찾는 방법에 대한 지침은 [!DNL Marketo] 설명서의 [Authentication](https://developers.marketo.com/rest-api/authentication/)을 참조하십시오.</td>
      </tr>
     </tbody>
    </table>
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## [!DNL Marketo] 모듈 및 해당 필드

[!DNL Marketo] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Marketo] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

* [[!UICONTROL Watch events (Instant)]](#watch-events-instant)
* [[!UICONTROL Watch records]](#watch-records)

#### [!UICONTROL Watch events (Instant)]

이 트리거 모듈은 레코드가 생성되거나 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>모듈에서 사용할 웹후크를 입력합니다.</p> <p>웹후크에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">웹후크</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch records]

이 트리거 모듈은 레코드가 생성되거나 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>보려는 활동 유형을 선택합니다. </p> <p>모듈은 새 활동만 감시합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p><b>이벤트 유형</b> 필드에서 새 레코드, 업데이트된 레코드, 새 레코드와 업데이트된 레코드 모두 또는 특정 필드 업데이트를 감시할지 여부를 선택합니다. 특정 필드 업데이트를 시청하도록 선택하는 경우 모듈에서 시청하려는 필드를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p><b>이벤트 유형</b> 필드에서 새 레코드, 업데이트된 레코드 또는 새 레코드와 업데이트된 레코드를 모두 감시할지 여부를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL Add Leads to a List]](#add-leads-to-a-list)
* [[!UICONTROL Clone a Program]](#clone-a-program)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API call]](#custom-api-call)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Remove Leads from a List]](#remove-leads-from-a-list)
* [[!UICONTROL Schedule a Campaign]](#schedule-a-campaign)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a File]](#upload-a-file)

#### [!UICONTROL Add Leads to a List]

이 작업 모듈은 리드 ID를 사용하여 하나 이상의 리드를 목록에 추가합니다. 한 번에 최대 300개의 리드를 추가할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>리드를 추가할 목록의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>목록에 추가할 각 잠재 고객에 대해 <b>[!UICONTROL Add]</b>을(를) 클릭한 다음 추가할 잠재 고객의 ID를 입력하거나 매핑합니다. 목록에 추가할 모듈에 대해 최대 300개의 리드를 추가할 수 있습니다.</p> <p>맵 토글을 클릭하여 목록에 추가하려는 기존 리드 컬렉션을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clone a Program]

이 작업 모듈은 기존 프로그램의 ID를 사용하여 프로그램의 복사본을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Existing Program ID]</td> 
   <td>복사할 프로그램의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Program Name]</p> </td> 
   <td> <p>새 프로그램의 이름 입력 또는 매핑</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>새 프로그램을 배치할 폴더의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a record]

이 작업 모듈은 [!DNL Marketo]에 새 레코드를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>회사 또는 가망 고객을 생성하는 경우 신규 레코드 생성 시 값을 설정할 필드를 선택한 다음 해당 필드에 대한 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Type]</td> 
   <td>프로그램을 만드는 경우 만들려는 프로그램 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Channel] </td> 
   <td>프로그램을 만드는 경우 프로그램을 만들려는 프로그램 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Program Name]</td> 
   <td>폴더 또는 프로그램을 생성하는 경우 새 레코드의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>폴더 또는 프로그램을 생성하는 경우 새 레코드에 대한 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID]</td> 
   <td>폴더 또는 프로그램을 만드는 경우 새 레코드를 만들 상위 폴더의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>프로그램을 생성하는 경우 비용을 추가합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>프로그램을 만드는 경우 태그를 추가합니다</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API call]

이 작업 모듈을 사용하면 [!DNL Marketo] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Marketo] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://{your-base-url}.mktorest.com/</code>과(와) 관련된 경로를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] 인증 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>API 호출에 추가할 각 필드에 대해 <b>항목 추가</b>를 클릭하고 필드의 키와 값을 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

이 작업 모듈은 파일 ID를 사용하여 파일을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>다운로드할 파일의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

이 작업 모듈은 해당 ID를 사용하여 레코드에 대한 정보를 읽습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL List]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다. 필드는 선택한 [!UICONTROL Record Type]을(를) 기반으로 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Object> ID]</td> 
   <td>정보를 검색할 개체의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Leads from a List]

이 작업 모듈은 리드 ID를 사용하여 목록에서 하나 이상의 리드를 제거합니다. 한 번에 최대 300개의 리드를 제거할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>리드를 제거할 목록의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>목록에서 제거할 각 잠재 고객에 대해 <b>[!UICONTROL Add item]</b>을(를) 클릭한 다음 제거할 잠재 고객의 ID를 입력하거나 매핑합니다. 목록에서 제거할 모듈에 대해 최대 300개의 리드를 추가할 수 있습니다. </p> <p>맵 토글을 클릭하여 목록에서 제거할 기존 리드 컬렉션을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Schedule a Campaign]

이 작업 모듈은 특정 날짜에 대한 기존 캠페인을 예약합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>예약하려는 캠페인의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>캠페인을 실행할 날짜를 선택합니다. 이 필드를 비워 두면 시나리오가 시작된 후 5분 후에 캠페인이 실행됩니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

이 작업 모듈은 해당 ID를 사용하여 기존 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Company] / [!UICONTROL Lead] / [!UICONTROL Program ID]</td> 
   <td>업데이트할 레코드의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>회사 또는 가망 고객을 갱신하는 경우 값을 갱신할 필드를 선택한 다음 해당 필드에 대한 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>프로그램을 업데이트하는 경우 프로그램의 새 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>프로그램을 갱신하는 경우 프로그램에 대한 새 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>프로그램을 갱신하는 경우 프로그램의 신규 시작 일자를 입력하거나 맵핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>프로그램을 갱신하는 경우 프로그램의 신규 종료 일자를 입력하거나 맵핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>프로그램을 업데이트하는 경우 비용을 추가합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>프로그램을 업데이트하는 경우 태그를 추가합니다</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

이 작업 모듈은 새 파일을 [!UICONTROL Marketo]에 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>새 파일을 저장할 폴더의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>업로드한 파일에 대한 설명을 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search Records]](#update-a-record)

#### [!UICONTROL List records]

이 작업 모듈은 특정 유형의 모든 레코드를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>나열할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Read all campaigns]</p> </li> 
     <li> <p>[!UICONTROL Read all programs]</p> </li> 
     <li> <p>[!UICONTROL Read all leads] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>가망 고객 검색을 선택한 경우 목록에서 가망 고객을 검색할지 프로그램에서 가망 고객을 검색할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다. 필드는 선택한 [!UICONTROL Record Type]을(를) 기반으로 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Records]

이 검색 모듈은 특정 검색 기준과 일치하는 레코드 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">[!DNL Marketo]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>검색할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaigns]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programs]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>검색할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value / values]</td> 
   <td>검색할 필드의 값을 입력합니다. 필드에서 여러 값을 검색할 수 있는 경우 검색할 각 값에 대해 <b>[!UICONTROL Add item]</b>을(를) 클릭하고 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
