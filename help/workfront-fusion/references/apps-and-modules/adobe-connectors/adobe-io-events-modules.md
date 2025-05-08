---
title: Adobe I/O Events 모듈
description: Adobe I/O Events 모듈을 사용하면 Adobe 애플리케이션의 이벤트를 기반으로 Adobe Workfront Fusion 시나리오를 시작할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: ef55cc62a0e0de70662440bc38d3eabbfe5e3c13
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 1%

---

# Adobe I/O Events 모듈

Adobe I/O Events 모듈을 사용하면 전용 Adobe Workfront Fusion 커넥터가 없는 Adobe 계정 및 서비스의 이벤트를 기반으로 Workfront Fusion 시나리오를 시작할 수 있습니다.

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

Adobe I/O Events 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 Adobe 계정이 있어야 합니다.

## Adobe I/O Events API 정보

Adobe I/O Events 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## Adobe I/O Events에 대한 연결 만들기

Adobe I/O Events 모듈에 대한 연결을 만들려면 다음 작업을 수행하십시오.

1. 연결 상자 옆에 있는 추가 를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">연결 이름</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">환경</td>
        <td>
          <p>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">유형</td>
        <td>
          <p>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">추가 범위</td>
        <td>범위를 추가하려면 <b>항목 추가</b>를 클릭하고 범위를 입력하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">클라이언트 ID</td>
        <td>Adobe 클라이언트 ID를 입력합니다. Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다</td>
      </tr>
      <tr>
        <td role="rowheader">클라이언트 암호</td>
        <td>Adobe 클라이언트 암호를 입력합니다. Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다</td>
      </tr>
      </tr>
        <tr>
        <td role="rowheader">소비자 조직 ID</td>
        <td>소비자 조직 ID를 입력합니다. 프로젝트의 자격 증명 URL에서 찾을 수 있습니다. <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">자격 증명 ID</td>
        <td>자격 증명 ID를 입력합니다. 프로젝트의 자격 증명 URL에서 찾을 수 있습니다. <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">IMS 조직 ID</td>
        <td>Adobe 조직 ID를 입력합니다. Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다</td>
      </tr>
        <tr>
        <td role="rowheader">프로젝트 ID</td>
        <td>프로젝트 ID를 입력합니다. 프로젝트의 자격 증명 URL에서 찾을 수 있습니다. <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">WORKSPACE ID</td>
        <td>프로젝트의 Workspace ID를 보려면 Adobe Developer Console의 프로젝트 개요 페이지에서 프로젝트 세부 정보를 다운로드하십시오. </td>
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **계속**&#x200B;을 클릭하세요.

## Adobe I/O Events 모듈 및 해당 필드

[!DNL Adobe I/O Events] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Adobe I/O Events] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

<!--Becky start here-->

#### 이벤트 등록 만들기

이 작업 모듈은 웹후크를 사용하여 이벤트 설명을 만듭니다. 여기에서 Webhook을 구성할 수 있습니다. 기존 웹후크를 사용하는 경우 이 모듈의 필드는 읽기 전용입니다.

웹후크를 생성하려면 다음을 수행합니다.

1. Webhook 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Webhook name]</td>
        <td>이 웹후크의 이름을 입력하십시오.</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>[!DNL Adobe I/O Events]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >[!DNL Adobe I/O Events]</a>에 대한 연결 만들기 를 참조하십시오.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Webhook 설명]
         </td>
         <td>
           이 웹후크에 대한 설명을 입력하십시오.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL 이벤트 공급자]
         </td>
         <td>
           이벤트를 만들 제품 또는 계정을 선택합니다.
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL 이벤트 유형]
         </td>
         <td>
           웹후크에서 보려는 이벤트를 선택합니다. 이러한 이벤트가 발생하면 시나리오가 트리거됩니다.
         </td>
       </tr>
     </tbody>
   </table>

1. Save 를 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다.

### 액션

* [공급자 및 이벤트 ID 가져오기](#get-provider-and-event-ids)
* [사용자 지정 API 호출 만들기](#make-a-custom-api-call)

#### 공급자 및 이벤트 ID 가져오기

이 검색 모듈은 지정된 공급자 및 이벤트에 대한 Adobe I/O Events ID를 가져옵니다.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>[!DNL Adobe I/O Events]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >[!DNL Adobe I/O Events]</a>에 대한 연결 만들기 를 참조하십시오.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL 이벤트 공급자]
         </td>
         <td>
           ID를 검색할 공급자를 선택합니다.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL 이벤트 유형]
         </td>
         <td>
              ID를 제공할 이벤트를 선택합니다. 이벤트는 이벤트 공급자를 기반으로 사용할 수 있습니다. 
         </td>
       </tr>
     </tbody>
   </table>


#### 사용자 지정 API 호출 만들기

이 작업 모듈은 [!DNL Adobe I/O Events] API에 대한 사용자 지정 API 호출을 만듭니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
        <td>[!DNL Adobe I/O Events]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >[!DNL Adobe I/O Events]</a>에 대한 연결 만들기 를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 경로]</p>
      </td>
      <td>
        <p>상대 경로 입력 <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
      </td>
      <td>
  <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 인증 헤더와 x-api-key 헤더를 자동으로 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### 검색 결과

#### 저널에서 모든 이벤트 가져오기

이 검색 모듈은 저널에서 등록에 대한 모든 이벤트를 검색합니다.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>[!DNL Adobe I/O Events]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >[!DNL Adobe I/O Events]</a>에 대한 연결 만들기 를 참조하십시오.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL 등록 ID]
         </td>
         <td>
           이벤트를 검색할 등록을 선택합니다.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL 반환되는 최대 이벤트 수]
         </td>
         <td>
              각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다. 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL 다음 시간 이후에 발생하는 이벤트 반환]
         </td>
         <td>날짜를 입력하거나 매핑합니다. 이 모듈은 이 날짜 이후에 발생한 이벤트를 반환합니다.
         </td>
       </tr>
<!--       <tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>-->
       <tr>
         <td role="rowheader">
           [!UICONTROL 최신]
         </td>
         <td>
         최신 이벤트를 반환하려면 이 옵션을 활성화하십시오.
         </td>
       </tr>
     </tbody>
   </table>
&lt;!—

이벤트 보기

이 트리거 모듈은 선택한 Adobe 제품 또는 서비스에서 이벤트가 발생할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>Webhook 필드 옆에 있는 <b>추가</b>를 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>보려는 이벤트의 소스</li></ul></li><li>웹후크를 저장하고 모듈로 돌아가려면 <b>저장</b>을 클릭하십시오. </td> 
   </tr> 
   </tbody> 
</table>

—>
