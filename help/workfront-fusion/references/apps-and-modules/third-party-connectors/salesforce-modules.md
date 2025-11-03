---
title: Salesforce 모듈
description: Adobe Workfront Fusion 시나리오에서는 Salesforce을 사용하는 워크플로를 자동화할 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2990'
ht-degree: 0%

---

# [!DNL Salesforce]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Salesforce]을(를) 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

Salesforce 커넥터에 대한 비디오 소개는 다음을 참조하십시오.

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

>[!NOTE]
>
>* [!DNL Salesforce]의 모든 버전에 API 액세스 권한이 있는 것은 아닙니다. 자세한 내용은 [!DNL Salesforce] 커뮤니티 사이트에서 API 액세스 권한이 있는 [!DNL Salesforce] 버전에 대한 정보를 참조하십시오.
>* [!DNL Salesforce] API에서 반환된 특정 오류에 대한 자세한 내용은 [!DNL Salesforce] API 문서를 참조하십시오. [!DNL Salesforce] API의 상태를 통해 가능한 서비스 중단을 확인할 수도 있습니다.
>

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

[!DNL Salesforce] 모듈을 사용하려면 [!DNL Salesforce] 계정이 있어야 합니다.

## Salesforce API 정보

Salesforce 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> {{connection.instanceUrl}}</td>
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v62.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Salesforce]개 개체 검색 정보

객체를 검색할 때 개별 검색어를 입력하거나 와일드카드 및 연산자를 사용하여 보다 복잡한 질의를 생성할 수 있습니다.

* 별표 와일드카드(\*)를 0개 이상의 문자 대용으로 사용합니다. 예를 들어 Ca\*를 검색하면 Ca로 시작하는 항목이 검색됩니다
* 물음표 와일드카드(?) 사용 단일 문자의 대용품입니다. 예를 들어 Jo?n을 검색하면 John 또는 Joan이라는 용어가 있지만 Jon은 아닌 항목이 검색됩니다
* 따옴표 연산자(&quot; &quot;)를 사용하여 정확한 구문 일치를 찾습니다. 예: &quot;Monday meeting&quot;

검색 가능성에 대한 자세한 내용은 SOQL 및 SOSL에 대한 [!DNL Salesforce] 개발자 설명서를 참조하십시오.

## [!DNL Salesforce]에 연결 만들기

[!DNL Salesforce] 모듈에 대한 연결을 만들려면:

1. [!DNL Salesforce] 모듈에서 [연결] 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>
          <p>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>
          <p>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>Salesforce 클라이언트 ID를 입력합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>Salesforce 클라이언트 암호를 입력합니다. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Sandbox]</td>
        <td>샌드박스 환경인 경우 이 옵션을 활성화합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL API Version]</td>
        <td>사용할 Salesforce API 버전을 입력합니다. 기본 버전은 62.0입니다.</td>
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.


## [!DNL Salesforce]개 모듈 및 해당 필드

* [트리거](#triggers)
* [작업](#actions)
* [검색 결과](#searches)

### 트리거

* [[!UICONTROL 필드 보기]](#watch-a-field)
* [[!UICONTROL 레코드 보기]](#watch-for-records)
* [[!UICONTROL 아웃바운드 메시지 보기]](#watch-outbound-messages)

#### [!UICONTROL 필드 보기]

이 트리거 모듈은 [!DNL Salesforce]에서 필드를 업데이트할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형] </td> 
   <td> <p>모듈에서 조사할 필드가 포함된 레코드 유형을 선택합니다. [!DNL Salesforce] 설정에서 [!UICONTROL 필드 기록]이 설정된 레코드 종류를 선택해야 합니다. 자세한 내용은 <a href="https://help.salesforce.com/s/articleView?id=xcloud.tracking_field_history.htm&type=5"> 설명서의 </a>필드 기록 추적[!DNL Salesforce]을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 필드]</td> 
   <td> <p>모듈에서 변경 사항을 감시할 필드를 선택합니다. 사용 가능한 필드는 선택한 레코드 유형에 따라 다릅니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 필드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 보기]

이 트리거 모듈은 오브젝트 내의 레코드가 생성되거나 업데이트될 때 시나리오를 실행한다. 모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드 또는 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 유형] </td> 
   <td> <p>모듈을 감시할 [!DNL Salesforce] 레코드 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 필드]</td> 
   <td>모듈에서 조사할 필드를 선택합니다. 사용 가능한 필드는 레코드 유형에 따라 다릅니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드의 최대 개수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>선택한 유형의 새 레코드만 시나리오에 표시할지, 선택한 유형의 새 레코드와 해당 유형의 다른 모든 레코드 변경 사항을 시나리오에 표시할지 여부를 결정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 아웃바운드 메시지 보기]

이 트리거 모듈은 누군가가 메시지를 보낼 때 시나리오를 실행합니다. 모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드 또는 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈에서는 추가 설정이 필요합니다. 아웃바운드 메시지에 대해 구성된 흐름이 있어야 합니다.

* Salesforce의 흐름에 대한 지침은 Salesforce 설명서에서 [흐름을 사용하여 작업 자동화](https://help.salesforce.com/s/articleView?id=platform.flow.htm)를 참조하십시오.
* Salesforce에서 아웃바운드 메시지를 구성하는 방법에 대한 자세한 내용은 Salesforce 설명서의 [레코드에서 트리거된 흐름에서 아웃바운드 메시지 보내기](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_outbound_message.htm)를 참조하십시오

<!--

1. Go to the [!DNL Salesforce] setup page.

   To access the setup page, locate and click the button labeled "[!UICONTROL Setup]" in the upper-right hand corner of the [!DNL Salesforce] account. From the [!DNL Salesforce] setup page, locate the "[!UICONTROL Quick Find / Search]" bar on the left hand side. Search for "[!UICONTROL Workflow Rules]." 

1. Click **[!UICONTROL Workflow Rules]**. 
1. On the the [!UICONTROL Workflow Rules] page that appears, click **[!UICONTROL New Rule]** and select the object type the rule will apply to (such as "[!UICONTROL Opportunity]" if you are monitoring updates to Opportunity records).
1. Click **[!UICONTROL Next]**.
1. Set a rule name, evaluation criteria, and rule criteria, then click **[!UICONTROL Save]** and **[!UICONTROL Next]**.

1. Click **[!UICONTROL Done]**.
1. From the newly created Workflow rule, click **[!UICONTROL Edit]**..
1. From the **[!UICONTROL Add Workflow Action]** drop-down list, select **[!UICONTROL New Outbound Message]**.

1. Specify name, description, Endpoint URL, and fields you want to include in the new outbound message, then click **[!UICONTROL Save]**.

   The **[!UICONTROL Endpoint URL]** field contains the URL provided on the [!DNL Salesforce] [!UICONTROL Outbound Message] in Workfront Fusion.

1. Configure a scenario beginning with the [!UICONTROL Outbound Message] event. 

1. Click the **</>** icon in the bottom right and copy the provided URL.
1. Return to the **[!UICONTROL Workflow Rules]** page, locate the newly created rule, then click **[!UICONTROL Activate]**.

-->

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>보내는 메시지를 보는 데 사용할 웹후크를 선택합니다. 웹후크를 추가하려면 <strong>[!UICONTROL 추가]</strong>를 클릭하고 웹후크의 이름과 연결을 입력하십시오.</p> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 대한 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형] </td> 
   <td> <p>모듈에서 보내는 메시지를 확인할 [!DNL Salesforce] 레코드 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 필드]</td> 
   <td> <p>모듈에서 보내는 메시지를 확인할 필드를 선택합니다. 사용 가능한 필드는 레코드 유형에 따라 다릅니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 레코드 만들기]](#create-a-record)
* [[!UICONTROL 사용자 지정 API 호출]](#custom-api-call)
* [[!UICONTROL 레코드 삭제]](#delete-a-record)
* [[!UICONTROL 첨부 파일/문서 다운로드]](#download-attachmentdocument)
* [[!UICONTROL 레코드 읽기]](#read-a-record)
* [[!UICONTROL 첨부 파일/문서 업로드]](#upload-attachmentdocument)
* [파일 업로드](#upload-file)

#### [!UICONTROL 레코드 만들기]

이 작업 모듈은 개체에 새 레코드를 만듭니다.

모듈을 사용하면 모듈에서 사용할 수 있는 개체 필드를 선택할 수 있습니다. 이렇게 하면 모듈을 설정할 때 스크롤해야 하는 필드의 수가 줄어듭니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 레코드 유형] </p> </td> 
   <td> <p>모듈을 만들 [!DNL Salesforce] 레코드 형식을 선택하십시오. 필드는 [!UICONTROL 레코드 유형] 필드에서 선택한 레코드 유형에 따라 사용할 수 있습니다. 이 필드는 [!DNL Salesforce] API를 기반으로 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 매핑할 필드 선택]</td> 
   <td> <p>새 레코드를 만들 때 모듈에서 구성할 필드를 선택합니다. 필수 필드는 목록의 맨 위에 있습니다. </p> <p>선택한 필드는 이 필드 아래에 열립니다. 이제 이러한 필드에 값을 입력할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 지정 API 호출]

이 작업 모듈을 사용하면 [!DNL Salesforce] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Salesforce] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

모듈은 다음을 반환합니다.

* **[!UICONTROL 상태 코드]**(숫자): HTTP 요청의 성공 또는 실패를 나타냅니다. 이것은 인터넷에서 찾아볼 수 있는 표준 코드입니다.
* **[!UICONTROL Headers]**(개체): 출력 본문과 관련이 없는 응답/상태 코드에 대한 자세한 컨텍스트입니다. 응답 헤더에 표시되는 일부 헤더가 응답 헤더는 아니므로 유용하지 않을 수 있습니다.

  응답 헤더는 모듈을 구성할 때 선택한 HTTP 요청에 따라 다릅니다.

* **[!UICONTROL Body]**(개체): 모듈을 구성할 때 선택한 HTTP 요청에 따라 일부 데이터를 다시 받을 수 있습니다. [!UICONTROL GET] 요청의 데이터와 같은 데이터가 이 개체에 포함되어 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code> &lt;Instance URL&gt;/services/data/v62.0/</code>에 상대적인 경로를 입력하십시오.</p> <p>사용 가능한 끝점 목록은 <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Salesforce REST API 개발자 안내서</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메서드]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 예, <code>{"Content-type":"application/json"}</code>. Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다. For example: <code>{"name":"something-urgent"}</code></p> </td> 
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

>[!BEGINSHADEBOX]

**예:** 다음 API 호출은 [!DNL Salesforce] 계정의 모든 사용자 목록을 반환합니다.

* **URL**: `query`

* **메서드**: [!UICONTROL GET]

* **쿼리 문자열**:

* **키**: `q`

* **값**: `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`

검색 일치 항목은 **[!UICONTROL 번들] > [!UICONTROL 본문] > [!UICONTROL 레코드]**&#x200B;의 모듈 출력에서 찾을 수 있습니다.

이 예에서는 6명의 사용자가 반환되었습니다.

![검색 일치](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)

>[!ENDSHADEBOX]

#### [!UICONTROL 레코드 삭제]

이 작업 모듈은 오브젝트의 기존 레코드를 삭제합니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형] </td> 
   <td> <p>모듈을 삭제할 [!DNL Salesforce] 레코드의 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>모듈에서 삭제할 레코드의 고유 [!DNL Salesforce] ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 [!DNL Salesforce] 개체를 열고 마지막 슬래시(/) 뒤의 URL 끝에 있는 텍스트를 복사합니다. For example: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 첨부 파일/문서 다운로드]

이 작업 모듈은 레코드에서 문서 또는 첨부 파일을 다운로드합니다.

레코드의 ID와 원하는 다운로드 유형을 지정합니다.

모듈은 연결이 액세스하는 사용자 지정 필드 및 값과 함께 첨부 파일 또는 문서의 ID와 관련 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL 다운로드 유형]</td>
    <td> <p>Salesforce에서 다운로드할 파일 유형을 지정합니다.</p> 
     <ul> 
      <li>[!UICONTROL 첨부 파일]</li> 
      <li>[!UICONTROL 문서]</li> 
      <li>[!UICONTROL ContentDocument] ([!DNL Saleforce CRM Content] 또는 [!DNL Salesforce Files]의 라이브러리에 업로드된 문서임)</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL 첨부 파일 ID] / </p> <p>[!UICONTROL ContentDocument ID]</p> </td>
    <td> <p>모듈을 다운로드할 레코드의 고유 [!DNL Salesforce] ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 [!DNL Salesforce] 개체를 열고 마지막 슬래시(/) 뒤의 URL 끝에 있는 텍스트를 복사합니다. For example: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 읽기]

이 작업 모듈은 [!DNL Salesforce]의 단일 개체에서 데이터를 읽습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL 레코드 유형]</td>
    <td>모듈에서 읽을 [!DNL Salesforce] 레코드의 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL 레코드 필드]</td>
    <td>모듈에서 읽을 필드를 선택합니다. 필드를 하나 이상 선택해야 합니다. 사용 가능한 필드는 레코드 유형에 따라 다릅니다.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>모듈에서 읽을 레코드의 고유 [!DNL Salesforce] ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 [!DNL Salesforce] 개체를 열고 마지막 슬래시(/) 뒤의 URL 끝에 있는 텍스트를 복사합니다. For example: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 레코드 업데이트]

이 작업 모듈은 오브젝트의 레코드를 편집합니다.

모듈을 사용하면 모듈에서 사용할 수 있는 개체 필드를 선택할 수 있습니다. 이렇게 하면 모듈을 설정할 때 스크롤해야 하는 필드의 수가 줄어듭니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>업데이트할 레코드의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 레코드 유형] </p> </td> 
   <td> <p>모듈을 업데이트할 [!DNL Salesforce] 레코드의 형식을 선택하십시오. 필드는 레코드 유형 필드에서 선택한 레코드 유형에 따라 사용할 수 있습니다. 이 필드는 [!DNL Salesforce] API를 기반으로 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 매핑할 필드 선택]</td> 
   <td> <p>새 레코드를 만들 때 모듈에서 구성할 필드를 선택합니다. 필수 필드는 목록의 맨 위에 있습니다. </p> <p>선택한 필드는 이 필드 아래에 열립니다. 이제 이러한 필드에 값을 입력할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 첨부 파일/문서 업로드]

이 작업 모듈은 파일을 업로드하여 지정한 레코드에 첨부하거나 문서를 업로드합니다.

모듈은 연결이 액세스하는 사용자 지정 필드 및 값과 함께 첨부 파일 또는 문서의 ID와 관련 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 업로드 유형]</td> 
   <td>모듈에서 첨부 파일을 업로드할지 문서를 업로드할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>첨부 파일을 업로드할 오브젝트의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더]</td> 
   <td>문서를 업로드할 폴더를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source 파일]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 파일 업로드

이 작업 모듈은 단일 파일을 Salesforce에 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">연결 만들기[!DNL &#x200B; Adobe Workfront Fusion] - 기본 지침</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 연결]</td> 
   <td>콘텐츠 문서 링크를 적용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL linkedEntityId]</td> 
   <td>문서 연결을 사용하는 경우 연결된 개체의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ShareType]</td> 
   <td>문서 연결을 사용하는 경우 파일에 대한 권한을 선택합니다.<ul><li><b>뷰어 권한</b><p>사용자는 파일을 볼 수 있습니다.</p></li><li><b>공동 작업자 권한</b><p>사용자는 파일을 보고 편집할 수 있습니다.</p></li><li><b>권한 유추</b><p>권한은 라이브러리와 같은 관련 레코드에 대한 사용자의 권한을 기반으로 합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 가시성]</td> 
   <td>문서 연결을 사용하는 경우 문서의 가시성을 입력하거나 매핑합니다.<ul><li><b>모든 사용자</b><p>권한이 있는 모든 사용자가 사용할 수 있습니다.</p></li><li><b>내부 사용자</b><p>권한이 있는 내부 사용자가 사용할 수 있습니다.</p></li><li><b>공유 사용자</b><p>파일이 게시된 피드를 볼 수 있는 사용자가 사용할 수 있습니다.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [검색](#search)
* [쿼리를 사용하여 검색](#search-with-query)

#### [!UICONTROL 검색]

이 작업 모듈은 지정된 조건을 충족하는 모든 레코드를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">연결 만들기[!DNL &#x200B; Adobe Workfront Fusion] - 기본 지침</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 유형]</td> 
   <td> <p>검색할 객체 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 검색 기준]</td> 
   <td>검색할 필드, 쿼리에 사용할 연산자 및 필드에서 검색할 값을 선택합니다. AND 또는 OR를 사용하여 쿼리를 연결할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>모듈의 출력에 포함할 필드를 선택합니다. 필드는 레코드 유형에 따라 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 결과 집합]</td> 
   <td>모듈이 모든 일치 레코드를 반환할지, 첫 번째 일치 레코드만 반환할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 검색할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 쿼리로 검색]

이 검색 모듈은 지정한 검색 쿼리와 일치하는 [!DNL Salesforce]의 개체에서 레코드를 찾습니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-salesforce">Salesforce에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 검색 유형]</td> 
   <td> <p>모듈에서 수행할 검색 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Simple]</p> </li> 
     <li> <p>[!UICONTROL Using SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Using SOQL(Salesforce 개체 쿼리 언어)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 유형] </p> </td> 
   <td> <p>단순 검색 유형을 선택한 경우 모듈에서 검색할 [!DNL Salesforce] 레코드의 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] / [!UICONTROL SOSL Query] / [!UICONTROL SOQL Query]</td> 
   <td> <p>검색할 쿼리를 입력합니다.</p> <p>SOSL에 대한 자세한 내용은 <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm"> 설명서의 </a>Salesforce SOSL(개체 검색 언어) [!DNL Salesforce]을 참조하십시오.</p> <p>SOQL에 대한 자세한 내용은 <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm"> 설명서에서 </a>Salesforce SOQL(개체 쿼리 언어) [!DNL Salesforce]을(를) 참조하십시오.</p> <p>참고: 매개 변수 <code>RETURNING </code>의 값은 모듈의 출력에 영향을 줍니다. <code>LIMIT</code>을(를) 사용하는 경우 [!DNL Fusion]은(는) [!UICONTROL 최대 레코드 수] 필드의 설정을 무시합니다. 제한을 설정하지 않으면 [!UICONTROL LIMIT = 최대 레코드 수] 값이 삽입됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드의 최대 개수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
