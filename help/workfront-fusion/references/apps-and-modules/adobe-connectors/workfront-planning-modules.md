---
title: Adobe Workfront Planning 모듈
description: ' [!DNL Adobe Workfront Planning] 모듈을 사용하면  [!DNL Adobe] Workfront Planning 계정의 이벤트를 기반으로 Adobe Workfront Fusion 시나리오를 시작하고, 계약 및 기타 레코드를 만들거나 읽거나 업데이트하고, 설정한 기준을 사용하여 레코드를 검색하고, 문서를 업로드할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: a58a6c25751eb10365508c06ab1571ce7652d0c8
workflow-type: tm+mt
source-wordcount: '1992'
ht-degree: 52%

---

# [!DNL Adobe Workfront Planning] 모듈

[!DNL Adobe Workfront Planning] 모듈을 사용하면 Workfront Planning에서 이벤트가 발생할 때 시나리오를 트리거할 수 있습니다. 레코드를 만들고, 읽고, 업데이트하고 삭제하거나 [!DNL Adobe Workfront Planning] 계정에 대한 사용자 지정 API 호출을 수행할 수도 있습니다.

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
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 전제 조건

Workfront Planning에 액세스하려면 다음 항목이 있어야 합니다.

* 새로운 Workfront 패키지 및 라이선스. 기존 Workfront 패키지 또는 라이선스에는 Workfront Planning을 사용할 수 없습니다.
* Workfront Planning 패키지
* 조직의 Workfront 인스턴스는 Adobe 통합 경험에 온보딩되어야 합니다.

## Adobe Workfront Planning API 정보

Adobe Workfront Planning 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>https://{{connection.host}}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Planning을 Workfront Fusion에 연결

Workfront Planning 커넥터는 OAuth 2.0을 사용하여 Workfront Planning에 연결합니다.

Workfront Planning Fusion 모듈 내에서 직접 Workfront Planning 계정에 대한 연결을 생성할 수 있습니다.

* [클라이언트 ID 및 클라이언트 암호를 사용하여 Workfront Planning에 연결](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [서버 간 연결을 사용하여 Workfront Planning에 연결](#connect-to-workfront--planning-using-a-server-to-server-connection)

### 클라이언트 ID 및 클라이언트 암호를 사용하여 Workfront Planning에 연결

1. Adobe Workfront Planning 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 유형]</td>
        <td>
          <p><b>Adobe Workfront 인증 연결</b>을 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새로운 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>Workfront 클라이언트 ID를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. 연결할 특정 애플리케이션을 열어 클라이언트 ID를 확인합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>Workfront 클라이언트 암호를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. Workfront에 OAuth2 애플리케이션에 대한 클라이언트 암호가 없는 경우 다른 애플리케이션을 생성할 수 있습니다. 자세한 내용은 Workfront 설명서를 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인증 URL]</td>
        <td>이 값은 기본값으로 유지되거나 Workfront 인스턴스의 URL을 입력한 다음 <code>/integrations/oauth2</code>를 입력할 수 있습니다. <p>예: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 호스트 접두사]</td>
        <td>대부분의 경우 이 값은 <code>origin</code>이어야 합니다.
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   Workfront Planning에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인한 후 연결을 허용할 수 있습니다.

>[!NOTE]
>
>* OAuth 2.0의 Workfront API에 대한 연결은 더 이상 API 키에 사용하지 않습니다.
>* Workfront 샌드박스 환경에 연결하려면 해당 환경에서 OAuth2 애플리케이션을 만든 다음 해당 애플리케이션에서 생성한 클라이언트 ID와 클라이언트 암호를 연결에 사용해야 합니다.

### 서버 간 연결을 사용하여 Workfront Planning에 연결

1. Adobe Workfront Planning 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 유형]</td>
        <td>
          <p><b>Adobe Workfront 서버 간 연결</b>을 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새로운 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인스턴스 이름]</td>
        <td>
          <p>인스턴스 이름(도메인이라고도 함)을 입력합니다.</p><p>예: URL이 <code>https://example.my.workfront.com</code>인 경우 <code>example</code>을(를) 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인스턴스 레인]</td>
        <td>
          <p>이 연결이 연결될 환경 유형을 입력합니다.</p><p>예: URL이 <code>https://example.my.workfront.com</code>인 경우 <code>my</code>을(를) 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>Workfront 클라이언트 ID를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. 연결할 특정 애플리케이션을 열어 클라이언트 ID를 확인합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>Workfront 클라이언트 암호를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. Workfront에 OAuth2 애플리케이션에 대한 클라이언트 암호가 없는 경우 다른 애플리케이션을 생성할 수 있습니다. 자세한 내용은 Workfront 설명서를 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 범위]</td>
        <td>이 연결에 적용할 수 있는 범위를 입력합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 호스트 접두사]</td>
        <td>대부분의 경우 이 값은 <code>origin</code>이어야 합니다.
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   Workfront Planning에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인한 후 연결을 허용할 수 있습니다.

>[!NOTE]
>
>* OAuth 2.0의 Workfront API에 대한 연결은 더 이상 API 키에 사용하지 않습니다.
>* Workfront 샌드박스 환경에 연결하려면 해당 환경에서 OAuth2 애플리케이션을 만든 다음 해당 애플리케이션에서 생성한 클라이언트 ID와 클라이언트 암호를 연결에 사용해야 합니다.


## [!DNL Adobe Workfront Planning] 모듈 및 해당 필드

Workfront 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 Workfront 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.


![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)
* [미분류](#uncategorized)

### 트리거

#### 이벤트 보기

이 트리거 모듈은 기록, 레코드 유형 또는 작업 영역이 Workfront Planning에서 생성, 업데이트 또는 삭제될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 웹후크]</td>
      <td>사용할 웹후크를 선택하거나 추가 를 클릭하여 새 웹후크를 만듭니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 오브젝트 유형]</td>
      <td>레코드, 레코드 종류 또는 작업 영역을 감시할지 여부를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 상태]</td>
      <td>이전 상태를 볼 것인지 새 상태를 볼 것인지 선택합니다.<ul><li><p><b>[!UICONTROL 새 상태]</b></p><p>레코드가 지정된 값<b>으로</b> 변경되면 시나리오를 트리거합니다.</p></li><li><p><b>[!UICONTROL 이전 상태]</b></p><p>레코드가 지정된 값<b>에서</b> 변경되면 시나리오를 트리거합니다.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>레코드를 보는 경우 레코드를 볼 Workspace을 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레코드 유형]</td>
      <td>레코드를 보는 경우 보려는 레코드 유형을 선택합니다.</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 이벤트 필터]</p> </td> 
      <td> <p>선택한 기준을 충족하는 레코드만 보도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터가 평가할 필드, 연산자, 필터를 허용하기 원하는 값을 입력합니다. AND 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> <p>참고: 기존 Workfront 웹후크에서는 필터를 편집할 수 없습니다. Workfront 이벤트 구독에 대해 서로 다른 필터를 설정하려면 현재 웹후크를 제거하고 새 웹후크를 만듭니다.</p> <p>이벤트 필터에 대한 자세한 내용은 Workfront 모듈 문서의 Workfront &gt; [!UICONTROL Watch Events] 모듈에서 <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">이벤트 구독 필터</a>를 참조하십시오.</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>새로운 항목을 감시할지 여부를 선택합니다. 업데이트, 새 레코드 및 업데이트 또는 삭제된 레코드.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 이 연결에 의해 수행된 업데이트 제외]</p>
      </td>
      <td>이 모듈에서 사용한 연결에 의해 변경이 있을 때 시나리오가 트리거되지 않도록 하려면 이 옵션을 활성화합니다. 이렇게 하면 이 시나리오가 트리거 작업을 수행하는 경우 시나리오의 다른 인스턴스가 트리거되지 않습니다.</td> 
      </tr>
  </tbody>
</table>

### 액션

* [레코드 유형 삭제](#delete-a-record-type)
* [사용자 정의 AI 호출 만들기](#make-a-custom-api-call)

#### 레코드 유형 삭제

이 작업 모듈은 해당 ID로 Workfront Planning에서 단일 레코드 유형을 삭제합니다.

>[!WARNING]
>
>Workfront Planning에서 레코드 유형을 삭제하면 레코드 유형 테이블의 모든 레코드도 삭제됩니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형 ID]</p>
      </td>
      <td>삭제하려는 레코드 유형의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 사용자 정의 API 호출하기

이 모듈은 [!DNL Adobe Workfront Planning] API에 대한 사용자 지정 API 호출을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>상대 경로 입력 <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
      </td>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 헤더]</td>
      <td>
        <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p>
        <p>예: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>쿼리 문자열에 추가할 각 키/값 쌍에 대해 <b>항목 추가</b>를 클릭하고 키와 값을 입력하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 본문]</td>
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>


### 검색 결과

#### 레코드 검색

이 작업 모듈은 지정한 조건에 따라 레코드 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>검색할 레코드가 포함된 Workspace을 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>검색할 레코드 유형을 선택합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 필드]</p>
      </td>
      <td>검색할 각 필드에 대해 해당 필드를 찾은 다음 연산자를 선택하고 검색할 값을 입력하거나 매핑합니다. 필드는 선택한 레코드 유형에 따라 사용할 수 있습니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Condition for filters]</p>
      </td>
      <td>필터 조건 선택:<ul><li><b>및</b><p>모듈이 사용자가 선택한 필드 값의 <b>모두</b>를 충족하는 레코드를 반환합니다.</p></li><li><b>또는</b><p>모듈은 선택한 필드 값의 <b>any</b>을(를) 충족하는 레코드를 반환합니다.</p></li></ul></td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 제한]</p>
      </td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
      </tr>
  </tbody>
</table>


### 미분류


#### 레코드 만들기

이 작업을 수행하면 Workfront Planning에 단일 레코드가 만들어집니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형 ID]</p>
      </td>
      <td>생성할 레코드 유형을 입력하거나 매핑합니다. 사용 가능한 레코드 유형은 Workfront Planning 계정을 기반으로 합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>기타 필드</p>
      </td>
      <td>새 레코드에 보유할 값을 입력합니다. 이 필드는 선택한 레코드 종류를 기반으로 합니다.</td> 
      </tr>
     <tr>
  </tbody>
</table>

### 레코드 삭제

이 작업 모듈은 Workfront Planning에서 지정된 레코드를 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 ID]</p>
      </td>
      <td>삭제할 레코드의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

### 레코드 가져오기

이 작업 모듈은 ID로 지정된 [!DNL Adobe Workfront Planning]에서 단일 레코드를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레코드 ID]</td>
      <td>검색할 레코드의 ID를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

### 레코드 유형별 레코드 가져오기

이 작업 모듈은 지정된 유형의 모든 레코드를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>검색할 레코드가 포함된 작업 영역을 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레코드 유형]</td>
      <td>검색할 레코드 유형을 선택합니다.</td>
    </tr>
     <!--<tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> -->
  </tbody>
</table>

### 레코드 유형 가져오기

이 작업 모듈은 [!DNL Adobe Workfront Planning] 계정의 레코드 종류 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>검색할 레코드 유형이 포함된 작업 영역을 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

### 레코드 업데이트

이 작업은 Workfront Planning의 단일 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 ID]</p>
      </td>
      <td>업데이트할 레코드 유형을 입력하거나 매핑합니다. 사용 가능한 레코드 유형은 Workfront Planning 계정을 기반으로 합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>기타 필드</p>
      </td>
      <td>레코드에 보유할 새 값을 입력합니다. 이 필드는 선택한 레코드 종류를 기반으로 합니다.</td> 
      </tr>
     <tr>
  </tbody>
</table>


## 읽을 수 있는 `record-types` 분류에 JSONata 사용

다음 JSONata 표현식은 레코드 유형 분류를 제공하는 Planning 쿼리의 사람이 읽을 수 있는 출력을 생성합니다. 이렇게 하면 레코드 유형 이름, 필드 이름 및 필드 옵션 이름(해당하는 경우)을 사람이 이름으로 읽을 수 있도록 하고 나머지 구조는 그대로 유지합니다.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

JSONata 모듈 사용에 대한 자세한 내용은 [JSONata 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md)을 참조하십시오.

