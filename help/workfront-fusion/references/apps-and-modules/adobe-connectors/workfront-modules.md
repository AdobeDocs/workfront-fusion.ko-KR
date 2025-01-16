---
title: Adobe Workfront 모듈
description: Adobe Workfront Fusion Adobe Workfront 커넥터를 사용하여 Workfront 내에서 프로세스를 자동화할 수 있습니다. 작업 자동화 및 통합을 위한 Workfront Fusion 라이선스가 있는 경우 이 라이선스를 사용하여 타사 앱 및 서비스에 연결할 수도 있습니다.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '6208'
ht-degree: 3%

---

# Adobe Workfront 모듈

Adobe Workfront Fusion Adobe Workfront 커넥터를 사용하여 Workfront 내에서 프로세스를 자동화할 수 있습니다. Workfront을 다른 애플리케이션 및 서비스에 연결할 수도 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오. 모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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
   <p>레거시: 모두 </p>
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


>[!NOTE]
>
>* 귀사에서 기존 라이선스 패키지(커넥터 기반)를 사용하는 경우 서드파티 앱 및 서비스에 연결하려면 Work Automation 및 Integration용 Workfront Fusion 라이선스가 있어야 합니다. Workfront 커넥터는 조직에서 사용할 수 있는 활성 앱 수에 포함되지 않습니다. 모든 시나리오는 Workfront 앱만 사용하더라도 조직의 총 시나리오 수에 대해 계산됩니다.

+++

## Workfront을 Workfront Fusion에 연결

Workfront 커넥터는 OAuth 2.0을 사용하여 Workfront에 연결합니다.

Workfront Fusion 모듈 내에서 직접 Workfront 계정에 대한 연결을 만들 수 있습니다.

1. 모든 Adobe Workfront 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
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
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Workfront 클라이언트 ID를 입력합니다. 이 정보는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. 연결할 특정 애플리케이션을 열어 클라이언트 ID를 확인합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Workfront 클라이언트 ID를 입력합니다. 이 정보는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. Workfront에 OAuth2 애플리케이션용 클라이언트 암호가 없는 경우 다른 클라이언트 암호를 생성할 수 있습니다. 자세한 내용은 Workfront 설명서를 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>이 값은 기본값으로 유지되거나 Workfront 인스턴스의 URL을 입력한 후 <code>/integrations/oauth2</code>을(를) 입력할 수 있습니다. <p>예: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>대부분의 경우 이 값은 <code>origin</code>이어야 합니다.
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

   Workfront에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인 후 연결을 허용할 수 있습니다.

>[!NOTE]
>
>* Workfront API에 대한 OAuth 2.0 연결은 더 이상 API 키를 사용하지 않습니다.
>* Workfront 샌드박스 환경에 대한 연결을 만들려면 해당 환경에서 OAuth2 애플리케이션을 만든 다음 해당 애플리케이션에서 생성된 클라이언트 ID 및 클라이언트 암호를 연결에서 사용해야 합니다.

## Workfront 모듈 및 해당 필드

Workfront 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Workfront 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.


![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Workfront 모듈에 최신 필드가 표시되지 않는 경우 캐싱 문제 때문일 수 있습니다. 1시간 기다린 후 다시 시도하십시오.
>* Adobe Workfront의 HTTP 429 상태 코드는 비활성화가 아니라 시나리오에서 짧은 실행 일시 중지를 트리거해야 합니다.

* [트리거](#triggers)
* [작업](#actions)
* [검색 결과](#searches)

### 트리거

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Watch Events]**

이 트리거 모듈은 Workfront에서 특정 유형의 개체가 추가, 업데이트 또는 삭제될 때 시나리오를 실시간으로 실행합니다

모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

1. **Webhook** 상자 오른쪽에 있는 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

1. 표시되는 **[!UICONTROL Add a hook]** 상자에서 웹후크를 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook name]</td> 
      <td>Webhook의 이름 입력</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Type]</td> 
      <td>모듈에서 볼 Workfront 레코드의 유형을 선택합니다.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL State]</td> 
      <td>이전 상태를 볼 것인지 새 상태를 볼 것인지 선택합니다.<ul><li><p><b>[!UICONTROL New state]</b></p><p>레코드가 지정된 값으로 <b>에서 </b>(으)로 변경되면 시나리오를 트리거합니다.</p><p>예를 들어 상태가 [!UICONTROL New State](으)로 설정되고 필터가 [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress](으)로 설정된 경우 웹후크는 이전 상태와 관계없이 [!UICONTROL Status]이(가) [!UICONTROL In Progress](으)로 변경되면 시나리오를 트리거합니다. </p></li><li><p><b>[!UICONTROL Old state]</b></p><p>레코드가 지정된 값에서 <b>부터</b>까지 변경되는 경우 시나리오를 트리거합니다.</p><p>예를 들어 상태가 [!UICONTROL Old State](으)로 설정되고 필터가 [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress](으)로 설정된 경우 웹후크는 현재 [!UICONTROL In Progress]인 [!UICONTROL Status]이(가) 다른 상태로 변경되면 시나리오를 트리거합니다. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>선택한 기준을 충족하는 레코드만 보도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터를 평가할 필드, 연산자 및 필터를 허용할 값을 입력합니다. AND 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> <p><b>참고</b>: 기존 Workfront 웹후크에서 필터를 편집할 수 없습니다. Workfront 이벤트 구독에 대해 서로 다른 필터를 설정하려면 현재 웹후크를 제거하고 새 필터를 만드십시오.</p> <p>이벤트 필터에 대한 자세한 내용은 이 문서의 <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Workfront &gt; [!UICONTROL Watch Events] 모듈에서 이벤트 구독 필터</a>를 참조하십시오.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>이 연결에 의해 만들어진 이벤트 제외</td> 
      <td>이 트리거 모듈에서 사용하는 것과 동일한 커넥터를 사용하여 생성되거나 업데이트된 이벤트를 제외하려면 이 옵션을 활성화합니다. 이렇게 하면 시나리오가 자체적으로 트리거되어 무한 반복에서 반복될 수 있는 상황을 방지할 수 있습니다.<p><b>참고</b>: 할당 레코드 형식에 이 옵션이 포함되어 있지 않습니다.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Origin]</td> 
      <td>
       <p>시나리오가 [!UICONTROL New Records Only], [!UICONTROL Updated Records Only], [!UICONTROL New and Updated Records] 또는 [!DNL Deleted Records Only]을(를) 시청할지 여부를 선택합니다.</p>
       <p><b>참고</b>: [!UICONTROL New and Updated Records]을(를) 선택하면 웹후크 만들기에서 동일한 웹후크 주소에 대해 2개의 이벤트 구독을 만듭니다.</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

웹후크가 생성되면 이벤트를 전송할 엔드포인트의 주소를 볼 수 있습니다.

자세한 내용은 Workfront 설명서의 이벤트 구독 API 문서에서 [이벤트 페이로드의 예](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) 섹션을 참조하십시오.

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++

+++ **[!UICONTROL Watch Field]**

이 트리거 모듈은 지정한 필드가 업데이트될 때 시나리오를 실행합니다. 모듈은 지정된 필드의 이전 값과 새 값을 모두 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>모듈에서 볼 Workfront 레코드의 유형을 선택합니다.</p> <p>예를 들어 작업에서 레코드 필드가 업데이트될 때마다 시나리오 실행을 시작하려면 [!UICONTROL Task]을(를) 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td>모듈에서 업데이트를 감시할 필드를 선택합니다. 이러한 필드는 Workfront 관리자가 추적을 위해 설정한 필드를 반영합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td>이 모듈의 출력 번들에 포함할 객체 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++

+++ **[!UICONTROL Watch Record]**

이 트리거 모듈은 특정 유형의 객체가 추가, 업데이트 또는 둘 다 될 때 시나리오를 실행합니다. 모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드 또는 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

출력에서 모듈은 각 레코드가 새로 추가되었는지 또는 업데이트되었는지 여부를 나타냅니다.

시나리오가 마지막으로 실행된 이후 추가 및 업데이트된 레코드는 새 레코드로 반환됩니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>시나리오가 [!UICONTROL New Records Only], [!UICONTROL Updated Records Only] 또는 [!UICONTROL New and Updated Records]을(를) 시청할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>모듈에서 볼 Workfront 레코드의 유형을 선택합니다.</p> <p>예를 들어 새 프로젝트가 생성될 때마다 시나리오를 시작하려면 다음을 선택합니다. [!UICONTROL Project]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reference]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 참조 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈에 대한 출력 번들에 포함할 컬렉션 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optional Filter]</td> 
   <td> <p>(고급) 기준을 세분화할 추가 매개 변수 또는 코드를 정의하려면 API 코드 문자열을 입력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++


### 액션

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL Convert object]**

이 작업 모듈은 다음 전환 중 하나를 수행합니다.

* 문제를 프로젝트로 전환
* 문제를 작업으로 전환
* 작업을 프로젝트로 전환

>[!NOTE]
>
>2024년 7월부터 개체를 변환할 때 사용자 정의 양식을 포함할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Object type]</td> 
   <td> <p>변환할 개체 유형을 선택합니다. 이는 전환 전에 개체가 가지고 있는 유형입니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Convert to]</td> 
   <td>변환할 개체를 선택합니다. 전환 후 개체가 갖는 형식입니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL <Object> ID]</td> 
   <td> <p>개체의 ID를 입력합니다. </p> <p>참고: 개체의 ID를 입력할 때 개체의 이름을 입력한 다음 목록에서 해당 개체를 선택할 수 있습니다. 그런 다음 모듈은 해당 ID를 필드에 입력합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Template ID]</td> 
   <td> <p>프로젝트로 변환하는 경우 프로젝트에 사용할 템플릿 ID를 선택합니다.</p> <p>참고: 개체의 ID를 입력할 때 개체의 이름을 입력한 다음 목록에서 해당 개체를 선택할 수 있습니다. 그런 다음 모듈은 해당 ID를 필드에 입력합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Custom forms]</td> 
   <td>새로 변환된 오브젝트에 추가할 사용자 정의 양식을 선택한 다음 사용자 정의 양식의 필드에 대한 값을 입력합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Options]</td> 
   <td> <p>개체를 변환할 때 원하는 옵션을 활성화합니다. 변환 중인 개체 또는 변환 중인 개체에 따라 옵션을 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy native fields]</td> 
   <td> <p>원본 개체에서 새 개체로 네이티브 필드를 복사하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy custom forms]</td> 
   <td> <p>원본 개체에서 새 개체로 네이티브 필드를 복사하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a record (attaching custom forms)]**

이 작업 모듈은 Workfront의 프로젝트, 작업 또는 문제와 같은 개체를 만들며, 이를 통해 사용자 정의 양식을 새 개체에 추가할 수 있습니다. 모듈을 사용하면 모듈에서 사용할 수 있는 개체 필드를 선택할 수 있습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

최소 입력 필드 수를 입력해야 합니다. 예를 들어, 문제를 만들려면 프로젝트 ID 필드에 유효한 상위 프로젝트 ID를 제공하여 문제가 Workfront에서 발생해야 하는 위치를 나타내야 합니다. 매핑 패널을 사용하여 시나리오의 다른 모듈에서 가져온 이 정보를 매핑하거나 이름을 입력한 다음 목록에서 선택하여 수동으로 입력할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>모듈에서 만들 Workfront 레코드 유형을 선택합니다.</p> <p>예를 들어 프로젝트를 만들려면 드롭다운 목록에서 [!UICONTROL Project]을(를) 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>데이터 입력에 사용할 수 있는 필드를 선택합니다. 따라서 필요하지 않은 필드를 스크롤하지 않고도 이러한 필드를 사용할 수 있습니다. 그런 다음 이러한 필드에 데이터를 입력하거나 매핑할 수 있습니다.</p> <p>사용자 정의 양식의 필드에는 <b>[!UICONTROL Attach Custom Form]</b> 필드를 사용하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Attach Custom Form]</td> 
   <td>새 오브젝트에 추가할 사용자 정의 양식을 선택한 다음 해당 필드에 값을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

>[!NOTE]
>
>* 개체의 ID를 입력할 때 개체의 이름을 입력한 다음 목록에서 해당 개체를 선택할 수 있습니다. 그런 다음 모듈은 해당 ID를 필드에 입력합니다.
>* 사용자 지정 필드 또는 [!UICONTROL Note] 개체(댓글 또는 답글)의 텍스트를 입력할 때 [!UICONTROL Note Text] 필드의 HTML 태그를 사용하여 굵게 또는 기울임꼴 텍스트와 같은 서식 있는 텍스트를 만들 수 있습니다.
>

+++

+++ **[!UICONTROL Create Record]**

이 작업 모듈은 Workfront의 프로젝트, 작업 또는 문제와 같은 개체를 만듭니다. 모듈을 사용하면 모듈에서 사용할 수 있는 개체 필드를 선택할 수 있습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

최소 입력 필드 수를 입력해야 합니다. 예를 들어, 문제를 만들려면 프로젝트 ID 필드에 유효한 상위 프로젝트 ID를 제공하여 문제가 Workfront에서 발생해야 하는 위치를 나타내야 합니다. 매핑 패널을 사용하여 시나리오의 다른 모듈에서 가져온 이 정보를 매핑하거나 이름을 입력한 다음 목록에서 선택하여 수동으로 입력할 수 있습니다.

이 모듈은 개체를 만들 때 사용자 정의 양식을 첨부하지 않습니다. 개체를 만드는 동안 사용자 정의 양식을 첨부하려면 [!UICONTROL Create a record (attaching custom forms)] 모듈을 사용하십시오.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>모듈에서 만들 Workfront 레코드 유형을 선택합니다.</p> <p>예를 들어 프로젝트를 만들려면 드롭다운 목록에서 [!UICONTROL Project]을(를) 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>데이터 입력에 사용할 수 있는 필드를 선택합니다. 따라서 필요하지 않은 필드를 스크롤하지 않고도 이러한 필드를 사용할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

>[!NOTE]
>
>* 개체의 ID를 입력할 때 개체의 이름을 입력한 다음 목록에서 해당 개체를 선택할 수 있습니다. 그런 다음 모듈은 해당 ID를 필드에 입력합니다.
>* 사용자 지정 필드 또는 [!UICONTROL Note] 개체(댓글 또는 답글)의 텍스트를 입력할 때 [!UICONTROL Note Text] 필드의 HTML 태그를 사용하여 굵게 또는 기울임꼴 텍스트와 같은 서식 있는 텍스트를 만들 수 있습니다.

+++

+++ **[!UICONTROL Custom API Call]**

이 작업 모듈을 사용하면 Workfront API에 대해 사용자 지정 인증 호출을 할 수 있습니다. 이렇게 하면 다른 Workfront 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

모듈은 다음 정보를 반환합니다.

* **[!UICONTROL Status Code]**(숫자): HTTP 요청의 성공 또는 실패를 나타냅니다. 이것은 인터넷에서 찾아볼 수 있는 표준 코드입니다.
* **[!UICONTROL Headers]**(개체): 출력 본문과 관련이 없는 응답/상태 코드에 대한 자세한 컨텍스트입니다. 응답 헤더에 표시되는 일부 헤더가 응답 헤더는 아니므로 유용하지 않을 수 있습니다.

  응답 헤더는 모듈을 구성할 때 선택한 HTTP 요청에 따라 다릅니다.

* **[!UICONTROL Body]**(개체): 모듈을 구성할 때 선택한 HTTP 요청에 따라 일부 데이터를 다시 받을 수 있습니다. 이 개체에는 GET 요청의 데이터와 같은 데이터가 포함됩니다.

이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p><code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>에 상대적인 경로를 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>모듈에서 사용할 Workfront API 버전을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 Adobe Workfront Fusion의 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 요청의 콘텐츠 유형을 결정합니다.</p> <p>For example,<code> {"Content-type":"application/json"}</code></p> <p>참고: 오류가 발생하여 원래 위치를 확인하기 어려운 경우 Workfront 설명서를 기반으로 헤더를 수정하는 것이 좋습니다. 사용자 지정 API 호출이 422 HTTP 요청 오류를 반환하는 경우 <code>"Content-Type":"text/plain"</code> 헤더를 사용해 보십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> <p>팁: 쿼리 매개 변수보다는 JSON 본문을 통해 정보를 전송하는 것이 좋습니다.</p> </td> 
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

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++

+++ **[!UICONTROL Delete Record]**

이 작업 모듈은 Workfront의 프로젝트, 작업 또는 문제와 같은 개체를 삭제합니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Force delete]</td> 
   <td>Workfront UI에서 삭제 확인을 요청하는 경우에도 레코드가 삭제되도록 하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Async delete]</td> 
   <td>이 옵션을 활성화하면 모듈이 비동기적으로 삭제될 수 있습니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>모듈이 삭제하려는 레코드의 고유 Workfront ID를 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 개체를 열고 "ID=" 뒤에 있는 URL 끝에 있는 텍스트를 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>모듈에서 삭제할 Workfront 레코드의 유형을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

>[!NOTE]
>
>비동기 작업으로 인해 레코드가 삭제되지 않도록 다음 시나리오 구성을 권장합니다.
>
>1. 동기적으로 레코드를 삭제합니다.
>1. 기록 삭제 모듈에 오류 처리를 추가하여 40초 시간 초과로 인해 발생한 오류를 무시합니다.


+++

+++ **[!UICONTROL Download Document]**

이 작업 모듈은 Workfront에서 문서를 다운로드합니다.

레코드의 ID를 지정합니다.

이 모듈은 문서의 컨텐트, 파일 이름, 파일 확장자 및 파일 크기를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Document ID]</td> 
   <td> <p>모듈에서 다운로드할 문서의 고유 Workfront ID를 매핑하거나 수동으로 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 개체를 열고 "ID=" 뒤에 있는 URL 끝에 있는 텍스트를 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++

+++ **[!UICONTROL Misc Action]**

이 작업 모듈을 사용하면 API에 대해 작업을 수행할 수 있습니다.

>[!NOTE]
>
>2024년 7월부터 `convertToProject` 작업에 `copyCategories` 필드가 포함됩니다. `TRUE`(으)로 설정하면 문제가 전환된 프로젝트에 모든 사용자 정의 양식이 포함됩니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>모듈이 상호 작용할 Workfront 레코드 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Action]</td> 
   <td> <p>모듈에서 수행할 작업을 선택합니다.</p> <p>선택한 [!UICONTROL Record Type] 및 [!UICONTROL Action]에 따라 추가 필드를 작성해야 할 수 있습니다. 이 두 설정을 조합하는 경우 레코드 ID만 필요하지만, 다른 설정(예: <strong>[!UICONTROL Record Type]</strong>의 경우 Project, <strong>[!UICONTROL Action]</strong>의 경우 [!UICONTROL Attach Template])에는 추가 정보(예: 개체 ID 및 템플릿 ID)가 필요합니다.</p><p>일부 작업에 사용할 수 있는 옵션은 이 문서에서 <a href="#misc-action-options" class="MCXref xref">기타 작업 옵션</a>을 참조하십시오.</p> <p>개별 필드에 대한 자세한 내용은 <a href="http://developer.workfront.com/">Workfront 개발자 설명서</a>를 참조하세요. <p><strong>참고</strong>: 개발자 설명서 사이트에는 API 버전 14를 통해서만 정보가 포함되지만 API 호출에 대한 중요한 정보가 포함되어 있습니다. </p> 
    <ol> 
     <li value="1"> <p>Workfront 개발자 설명서 페이지의 왼쪽 탐색에서 레코드 유형을 선택합니다. 다음 유형에는 자체 페이지가 있습니다.</p> 
      <ul> 
       <li> <p>[!UICONTROL Projects]</p> </li> 
       <li> <p>[!UICONTROL Tasks]</p> </li> 
       <li> <p>[!UICONTROL Issues]</p> </li> 
       <li> <p>[!UICONTROL Users]</p> </li> 
       <li> <p>[!UICONTROL Documents]</p> </li> 
      </ul> <p>다른 모든 레코드 종류의 경우 <b>[!UICONTROL Other objects and endpoints]</b>을(를) 선택하고 알파벳순으로 정렬된 페이지에서 레코드 종류를 찾습니다.</p> </li> 
     <li value="2"> <p>적절한 레코드 종류의 페이지에서 작업을 검색(Ctrl-F 또는 Cmd-F)합니다.</p> </li> 
     <li value="3"> <p>선택한 작업 아래의 사용 가능한 필드에 대한 설명을 봅니다.</p> </li> 
    </ol> <p>참고:  <p>Workfront [!UICONTROL Misc Action] 모듈을 통해 증명을 만들 때 가장 좋은 방법은 고급 옵션 없이 증명을 만든 다음 [!DNL Workfront Proof] SOAP API를 사용하여 증명을 업데이트하는 것입니다.</p><p>이 모듈에서 사용하는 Workfront API를 사용하여 증명을 만드는 방법에 대한 자세한 내용은 <a href="https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Adobe Workfront API를 통해 증명을 만들 때 고급 증명 옵션 추가</a>를 참조하십시오.</p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>모듈이 상호 작용할 레코드의 고유 Workfront ID를 입력하거나 매핑합니다.<p>ID를 가져오려면 브라우저에서 Workfront 개체를 열고 "ID=" 뒤에 있는 URL 끝에 있는 텍스트를 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

#### 기타 작업 옵션

##### 작업

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>액션</th> 
   <th>옵션</th> 
  </tr> 
  <tr> 
   <td>복사</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssets</li>
   <li>clearConstrains</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>이동</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssets</li>
   <li>clearDocuments</li>
   <li>clearConstrains</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### 문제

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>액션</th> 
   <th>옵션</th> 
  </tr> 
  <tr> 
   <td>복사</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssets</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>작업으로 전환</td> 
   <td>
   <ul>
   <li>preserveIssue<p>원래 문제를 유지하고 해결 방법을 이 작업에 연결</p></li>
   <li>preservePrimaryContact<p>이 작업에 대한 문제의 기본 담당자 액세스 허용</p></li>
   <li>preserveCompletionDate<p>문제의 계획된 완료 일자 유지</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>프로젝트로 전환</td> 
   <td>
   <ul>
   <li>preserveIssue<p>원래 문제를 유지하고 해결 방법을 이 작업에 연결</p></li>
   <li>preservePrimaryContact<p>이 작업에 대한 문제의 기본 담당자 액세스 허용</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### 프로젝트

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>액션</th> 
   <th>옵션</th> 
  </tr> 
  <tr> 
   <td>복사</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssets</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>템플릿 첨부 / 템플릿으로 저장</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssets</li>
   <li>clearBillingRates</li>
   <li>clearConstrains</li>
   <li>clearDeliverables<p>목표 지우기</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>대기열 속성 및 문제 설정 지우기</p></li>
   <li>clearPredecessors</li>
   <li>clearRisk</li>
   <li>지우기 공유 옵션</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Read a Record]**

이 작업 모듈은 단일 레코드에서 데이터를 검색합니다.

레코드의 ID를 지정합니다. 모듈에서 읽을 관련 레코드를 지정할 수도 있습니다.

예를 들어 모듈이 읽고 있는 레코드가 프로젝트인 경우 프로젝트의 작업을 읽도록 지정할 수 있습니다.

모듈은 지정한 출력 필드에서 데이터 배열을 반환합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>

<td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>

<td>모듈에서 읽을 Workfront 개체 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>

<td> <p>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>출력에 포함할 참조 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>출력에 포함할 참조 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>모듈에서 읽을 레코드의 고유 Workfront ID를 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 개체를 열고 "ID=" 뒤에 있는 URL 끝에 있는 텍스트를 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++

+++ **[!UICONTROL Update Record]**

이 작업 모듈은 프로젝트, 작업 또는 문제와 같은 개체를 업데이트합니다. 모듈을 사용하면 모듈에서 사용할 수 있는 개체 필드를 선택할 수 있습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 개체의 ID와 연결된 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>모듈에서 업데이트할 레코드의 고유 Workfront ID를 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 개체를 열고 "ID=" 뒤에 있는 URL 끝에 있는 텍스트를 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>모듈에서 업데이트할 Workfront 레코드의 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>데이터 입력에 사용할 수 있는 필드를 선택합니다. 따라서 필요하지 않은 필드를 스크롤하지 않고도 이러한 필드를 사용할 수 있습니다. 그런 다음 이러한 필드에 데이터를 입력하거나 매핑할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

>[!NOTE]
>
>* 개체의 ID를 입력할 때 개체의 이름을 입력한 다음 목록에서 해당 개체를 선택할 수 있습니다. 그런 다음 모듈은 해당 ID를 필드에 입력합니다.
>* 사용자 지정 필드 또는 [!UICONTROL Note] 개체(댓글 또는 답글)의 텍스트를 입력할 때 [!UICONTROL Note Text] 필드의 HTML 태그를 사용하여 굵게 또는 기울임꼴 텍스트와 같은 서식 있는 텍스트를 만들 수 있습니다.

+++

+++ **[!UICONTROL Upload Document]**

이 작업 모듈은 프로젝트, 작업 또는 문제와 같은 Workfront 개체에 문서를 업로드합니다. 이 모듈은 청크로 문서를 업로드하므로 Workfront의 업로드 프로세스가 더 원활해집니다.

이 모듈은 기존 모듈보다 큰 파일을 처리할 수 있으며 Ultimate Workfront 패키지를 사용하는 조직에 대한 단계별 롤아웃의 일부입니다.

문서의 위치, 업로드할 파일 및 파일의 새 이름(선택 사항)을 지정합니다.

모듈은 연결이 액세스하는 사용자 지정 필드 및 값과 함께 문서의 ID 및 관련 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>문서를 업로드할 레코드의 고유 Workfront ID를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>모듈이 문서를 업로드할 Workfront 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>관련 레코드 유형에 따라 폴더 ID를 입력하거나 매핑해야 할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++

+++ **[!UICONTROL Upload Document (Legacy)]**

이 작업 모듈은 프로젝트, 작업 또는 문제와 같은 Workfront 개체에 문서를 업로드합니다. 전체 문서를 한 번에 업로드합니다.

문서의 위치, 업로드할 파일 및 파일의 새 이름(선택 사항)을 지정합니다.

모듈은 연결이 액세스하는 사용자 지정 필드 및 값과 함께 문서의 ID 및 관련 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>문서를 업로드할 레코드의 고유 Workfront ID를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>모듈이 문서를 업로드할 Workfront 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>관련 레코드 유형에 따라 폴더 ID를 입력하거나 매핑해야 할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

각 Workfront 모듈에 사용할 수 있는 [Workfront 개체 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.

+++

### 검색 결과

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Read Related Records]**

이 검색 모듈은 특정 상위 객체에서 지정한 검색 쿼리와 일치하는 레코드를 읽습니다.

출력에 포함할 필드를 지정합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>연결된 레코드를 읽을 상위 레코드(Workfront 개체)의 유형을 선택합니다.</p> <p>이 문서에서 각 Workfront 모듈에 사용할 수 있는 <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">Workfront 개체 유형</a>에서 이 모듈을 사용할 수 있는 Workfront 개체 유형 목록을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Parent Record ID]</td> 
   <td> <p>읽고자 하는 관련 레코드의 상위 레코드 ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 개체를 열고 "ID=" 뒤에 있는 URL 끝에 있는 텍스트를 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>모듈에서 읽을 하위 레코드 유형을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search]**

이 검색 모듈은 Workfront의 객체에서 지정한 검색 쿼리와 일치하는 레코드를 찾습니다.

이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>모듈에서 검색할 Workfront 레코드 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>옵션을 선택하여 모듈이 검색 기준과 일치하는 첫 번째 결과를 가져오는지 또는 일치하는 모든 결과를 가져오는지 여부를 지정합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria fields]</td> 
   <td> <p>검색 기준에 사용할 필드를 선택합니다. 그런 다음 검색 기준 드롭다운에서 이러한 필드를 사용할 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>검색할 필드, 쿼리에 사용할 연산자 및 검색할 값을 필드에 입력합니다.</p> <p>참고: 검색 기준에 <code>username </code>을(를) 사용하지 마십시오. Workfront에 대한 API 쿼리에 <code>username </code>을(를) 포함하면 사용자가 Workfront에 로그인되므로 검색에 실패하게 됩니다.</p> <p>참고: <code>In</code> 및 <code>NotIn</code>은(는) 배열을 사용하여 작업합니다. 입력은 배열 형식이어야 합니다.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈의 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>검색에 포함할 참조 필드를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>검색에 추가할 컬렉션을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## 각 Workfront 모듈에서 사용할 수 있는 Workfront 개체 유형

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**각 Workfront 트리거 모듈에 사용할 수 있는 개체 형식**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Watch Record]</th> 
   <th>[!UICONTROL Watch Field]</th> 
   <th>[!UICONTROL Watch Events]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>승인 진행</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>할당</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>기준선</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 청구 기록 </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>청구 요금</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>회사</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>대시보드</td> 
   <td> </td> 
   <td> </td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서 폴더</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문서 요청</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문서 버전</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>경비 유형</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>그룹</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>시간</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>시간 유형</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문제</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>반복</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업 역할</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>저널 항목</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤 경로</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>참고</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>메모 태그</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>포트폴리오</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로그램</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로젝트</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로젝트 사용자</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>교정쇄 승인</td> 
   <td> </td> 
   <td> </td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>예약 시간* </td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>보고서</td> 
   <td> </td> 
   <td> </td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>위험</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험 유형</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>단계 승인자</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>팀</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>템플릿 작업</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>타임시트</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>사용자</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>업데이트</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**각 Workfront 작업 모듈에 사용할 수 있는 개체 형식**

>[!NOTE]
>
>Workfront 개체 유형이 해당 구성에 속하지 않으므로 [!UICONTROL Download Document] 모듈이 이 표에 포함되지 않습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Create a record]</th> 
   <th>[!UICONTROL Update a record]</th> 
   <th>[!UICONTROL Delete a record]</th> 
   <th>[!UICONTROL Upload Document]</th> 
   <th>[!UICONTROL Read a record]</th> 
   <th>[!UICONTROL Custom API Call]</th> 
   <th>[!UICONTROL Misc Action]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>승인 진행</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>할당</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>기준선</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>청구 기록</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>청구 요금</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>회사</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서 폴더</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서 버전</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>환율</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>경비 유형</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>외부 문서</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>그룹</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>시간</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>시간 유형</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문제</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>반복</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업 역할</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>저널 항목</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>마일스톤</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤 경로</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>참고</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>메모 태그</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>포트폴리오</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로그램</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로젝트</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로젝트 사용자</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>예약 시간* </td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험 유형</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>단계 승인자</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>팀</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿 작업</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>타임시트</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>사용자</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>업데이트</td> 
   <td> </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**각 Workfront 검색 모듈에 사용할 수 있는 개체 형식**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Search]</th> 
   <th>[!UICONTROL Read Related Records]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>승인 진행</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>할당</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>청구 기록</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>청구 요금</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>회사</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서 폴더</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>문서 버전</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비 유형</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>그룹</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>시간</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>시간 유형</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문제</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>반복</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업 역할</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>저널 항목</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤 경로</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>참고</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>메모 태그</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>포트폴리오</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로그램</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>프로젝트</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>프로젝트 사용자</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>예약 시간* </td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험 유형</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>단계 승인자</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>팀</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿 작업</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>타임시트</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>사용자</td> 
   <td>✓ 덧신</td> 
   <td>✓ 덧신</td> 
  </tr> 
  <tr> 
   <td>사용자 위임</td> 
   <td>✓ 덧신</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

예상대로 작동하는지 다시 확인하는 것이 좋습니다.

+++

## Workfront > [!UICONTROL Watch Events] 모듈의 이벤트 구독 필터

>[!NOTE]
>
>[!UICONTROL Watch Events] 모듈에서 이벤트 구독 필터를 사용하는 것이 좋습니다.

Workfront [!UICONTROL Watch Events] 모듈은 Workfront API에서 이벤트 구독을 만드는 웹후크를 기반으로 시나리오를 트리거합니다. 이벤트 구독은 웹후크로 전송되는 이벤트를 결정하는 데이터 세트입니다. 예를 들어 문제를 감시하는 [!UICONTROL Watch Events] 모듈을 설정하는 경우 이벤트 구독은 문제와 관련된 이벤트만 전송합니다.

Fusion 사용자는 이벤트 구독 필터를 사용하여 자신의 사용 사례에 더 적합한 이벤트 구독을 만들 수 있습니다. 예를 들어, 특정 프로젝트에 있는 문제만 웹후크로 보내도록 Workfront API에서 이벤트 구독을 설정하여 [!UICONTROL Watch Events] 모듈이 해당 프로젝트의 문제에만 트리거되도록 할 수 있습니다. 더 좁은 트리거를 생성하는 기능은 관련이 없는 트리거의 수를 줄임으로써 시나리오 설계를 향상시킨다.

이는 Workfront Fusion 시나리오에서 필터를 설정하는 것과 다릅니다. 이벤트 구독 필터가 없으면 웹후크는 사용자가 선택한 개체 유형과 관련된 모든 이벤트를 수신합니다. 이러한 이벤트의 대부분은 시나리오와 무관하며, 시나리오를 계속하려면 먼저 필터링해야 합니다.

Workfront > 이벤트 보기 필터에서 다음 연산자를 사용할 수 있습니다.

* 다음과 같음
* 같지 않음
* 보다 큼
* 보다 작음
* 크거나 같음
* 작거나 같음
* 포함
* 있음
   * 이 연산자에는 값이 필요하지 않으며 값 필드가 없습니다.
* 존재하지 않음
   * 이 연산자에는 값이 필요하지 않으며 값 필드가 없습니다.
* 변경됨
   * 이 연산자에는 값이 필요하지 않으며 값 필드가 없습니다.
   * 이 연산자는 상태 필드를 무시합니다.
   * `Changed`을(를) 사용하는 경우 **원본 기록** 필드에서 **업데이트된 이벤트만**&#x200B;을(를) 선택하십시오.

>[!IMPORTANT]
>
>기존 Workfront 웹후크에서 필터를 편집할 수 없습니다. Workfront 이벤트 구독에 대해 서로 다른 필터를 설정하려면 현재 웹후크를 제거하고 새 필터를 만드십시오.

>[!INFO]
>
>**예:** 특정 사용자 Ana에 할당된 새 문제를 처리하는 시나리오를 생각해 보십시오.
>
>### 이벤트 구독 필터를 사용하여 이벤트 필터링(권장)
>
>이벤트 필터를 사용하여 문제가 생성될 때 문제가 Ana에 할당될 때 시나리오를 트리거하도록 웹후크를 설정할 수 있습니다. Ana에 userID b378489d8f7cd3cee0539260720a84b7이 있습니다.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>하루에 100개의 문제가 만들어지지만 이 중 두 개의 문제만 Ana에 할당되면 시나리오는 두 번 실행됩니다.
>
>### 시나리오 내의 이벤트 필터링(권장되지 않음)
>
>Ana에 할당된 문제만 처리되도록 이벤트를 필터링하려면 [!UICONTROL Watch Events] 모듈 뒤에 필터를 만들 수 있습니다.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>하루에 100개의 문제가 만들어지지만 이 중 두 개의 문제만 Ana에 할당되면 시나리오는 100번 실행됩니다. 98개의 실행이 필터에서 중지되지만 트리거 모듈은 여전히 데이터를 소비하고 모든 실행에서 작업을 수행합니다.

Workfront 이벤트 구독에 대한 자세한 내용은 [FAQ - 이벤트 구독](https://experienceleague.adobe.com/en/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq)을 참조하십시오.

웹후크에 대한 자세한 내용은 Adobe Workfront Fusion의 [인스턴트 트리거(웹후크)](/help/workfront-fusion/references/modules/webhooks-reference.md)를 참조하십시오.

시나리오의 필터에 대한 자세한 내용은 [시나리오에 필터 추가](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md)를 참조하십시오.
