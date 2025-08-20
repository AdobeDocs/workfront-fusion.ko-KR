---
title: Jira 모듈
description: Adobe Workfront Fusion 시나리오에서는 Jira 소프트웨어를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
source-git-commit: 9865101fe57c2668ecb5ad743b3d6963833feb4a
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 6%

---

# Jira 모듈

>[!NOTE]
>
>이러한 지침은 간단히 Jira라는 레이블이 지정된 Jira 커넥터의 새 버전에 적용됩니다. 레거시 Jira Cloud 및 Jira Server 커넥터에 대한 지침은 [Jira 소프트웨어 모듈](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md)을 참조하십시오.

Adobe Workfront Fusion 시나리오에서는 Jira를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

Jira 커넥터는 Jira Cloud와 Jira Data Server 모두에 사용할 수 있습니다.

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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

Jira 모듈을 사용하려면 Jira 계정이 있어야 합니다.

## Jira를 Workfront Fusion에 연결

### 필요한 자격 증명 만들기

Jira에 대한 연결을 만들려면 다음이 필요합니다.

| 연결 유형 | 계정 유형 | 자격 증명 필요 |
|---|---|---|
| OAuth 2 | 임의 | 클라이언트 ID 및 클라이언트 암호 |
| 기본 | Jira 클라우드 | Jira API 토큰 |
| 기본 | Jira 데이터 센터 | Jira 개인 액세스 토큰(PAT) |

이러한 항목을 만드는 방법에 대한 지침은 Jira 설명서를 참조하십시오.

이러한 자격 증명을 만들 때 다음 정보가 필요합니다.

* OAuth 2의 경우:

  | Fusion 데이터 센터 | 리디렉션 URL |
  |---|---|
  | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira2` |
  | EU | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira2` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira2` |



* PAT(개인 액세스 토큰)의 경우:

  | Fusion 데이터 센터 | 리디렉션 URL |
  |---|---|
  | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira` |
  | EU | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira` |

  >[!IMPORTANT]
  >
  >PAT를 사용하려면 `jira/bin/WEB-INF/classes` 파일의 `jira-config.properties` 파일에서 다음을 사용하도록 설정해야 합니다.
  >
  >* `jira.rest.auth.allow.basic = true`
  >* `jira.rest.csrf.disabled = true`
  >
  >이 파일이 없으면 직접 만들어야 합니다.

### Workfront Fusion에서 Jira에 대한 연결 만들기

Workfront Fusion에서 연결을 만들려면 다음 작업을 수행하십시오.

1. Jira 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>연결 유형</p> </td> 
      <td> <p>기본 연결을 만드는지 OAuth 2 연결을 만드는지 선택합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>연결 이름</p> </td> 
      <td> <p>새 연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">서비스 URL</td>
      <td>Jira 인스턴스 URL을 입력합니다. Jira에 액세스하는 데 사용하는 URL입니다.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira 계정 유형</td>
       <td>Jira Cloud에 연결할지 또는 Jira 데이터 센터에 연결할지 선택합니다.</td>
     </tr>
     <tr> 
      <td role="rowheader">클라이언트 ID</td> 
      <td> <p>OAuth 2 연결을 만드는 경우 Jira 클라이언트 ID를 입력합니다</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">클라이언트 암호</td> 
      <td> <p>OAuth 2 연결을 만드는 경우 Jira 클라이언트 암호를 입력합니다</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">이메일</td> 
      <td>Jira Cloud에 대한 기본 연결을 만드는 경우 이메일 주소를 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API 토큰</td> 
      <td>Jira Cloud에 대한 기본 연결을 만드는 경우 API 토큰을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">개인 액세스 토큰</td> 
      <td>Jira 데이터 센터에 대한 기본 연결을 만드는 경우 개인 액세스 토큰을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API 버전</td> 
      <td>이 연결을 연결할 Jira API 버전을 선택합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.


## Jira 모듈 및 해당 필드

Jira 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱 또는 서비스의 액세스 수준 등의 요소에 따라 추가 Jira 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

#### 레코드 시청

이 트리거 모듈은 레코드가 추가, 업데이트 또는 삭제될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhook</td> 
   <td> <p>레코드를 감시하는 데 사용할 웹후크를 선택하거나 새 웹후크를 만듭니다. </p> <p>새 웹후크를 생성하려면</p> 
    <ol> 
     <li><strong>추가</strong> 클릭</li> 
     <li>Webhook의 이름을 입력합니다.</li> 
     <li> Webhook에 사용할 연결을 선택합니다. <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </li> 
     <li> <p>소프트웨어에서 감시할 레코드 유형을 선택합니다.</p> 
      <ul> 
       <li>문제</li> 
       <li>댓글 </li> 
       <li>작업 로그 </li> 
       <li>프로젝트 </li> 
       <li>Sprint</li> 
       <li>첨부 파일 </li> 
      </ul> </li> 
     <li>이 시나리오를 트리거할 이벤트 유형을 하나 이상 선택하십시오.</li> 
     <li>이 모듈에 대한 Jira 쿼리 언어 필터를 입력합니다.<p>JQL에 대한 자세한 내용은 Atlassian 도움말 사이트에서 <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a>을(를) 참조하십시오. </p></li>
     <li>웹후크를 저장하려면 <b>저장</b>을 클릭하세요. 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [스프린트에 문제 추가](#add-issue-to-sprint)
* [레코드 만들기](#create-a-record)
* [사용자 정의 API 호출](#custom-api-call)
* [레코드 삭제](#delete-a-record)
* [첨부 파일 다운로드](#download-an-attachment)
* [레코드 읽기](#read-a-record)
* [레코드 업데이트](#update-a-record)

#### 스프린트에 문제 추가

이 작업 모듈은 스프린트에 하나 이상의 문제를 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">스프린트 ID</td> 
   <td>문제를 추가하려는 스프린트의 스프린트 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">문제 ID 또는 키</td> 
   <td>스프린트에 추가할 각 문제 또는 키에 대해 <b>항목 추가</b>를 클릭하고 문제 ID 또는 키를 입력합니다. 한 모듈에 최대 50개를 입력할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 만들기

이 작업 모듈은 Jira에 새 레코드를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>모듈에서 만들 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li>첨부 파일</li> 
     <li>댓글</li> 
     <li>문제</li> 
     <li>프로젝트</li> 
     <li>Sprint </li> 
     <li>작업 로그</li> 
     <li>사용자</li> 
     <li>보드</li> 
     <li>카테고리</li> 
     <li>필터</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td> 다른 필드에 내용을 입력합니다. 필드는 선택한 레코드 유형에 따라 사용할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 정의 API 호출

이 작업 모듈을 사용하면 Jira API에 대해 사용자 지정 인증된 호출을 할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>상대 경로 입력<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">메서드</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">헤더</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">쿼리 문자열</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">본문</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 삭제

이 작업 모듈은 지정된 레코드를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>모듈에서 삭제할 레코드 유형을 선택합니다. </p> 
    <ul> 
     <li>댓글</li> 
     <li>문제</li> 
     <li>프로젝트</li> 
     <li>Sprint </li> 
     <li>작업 로그</li> 
     <li>첨부 파일</li> 
     <li>보드</li> 
     <li>카테고리</li> 
     <li>필터</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">(레코드 유형)ID</td> 
   <td>삭제하려는 레코드의 ID 또는 키를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 첨부 파일 다운로드

이 작업 모듈은 지정된 첨부 파일을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>다운로드하려는 첨부 파일의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 읽기

이 작업 모듈은 Jira의 지정된 레코드에서 데이터를 읽습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>모듈에서 읽을 Jira 레코드의 유형을 선택합니다.</p> 
    <ul> 
     <li>첨부 파일</li> 
     <li>댓글</li> 
     <li>문제</li> 
     <li>프로젝트</li> 
     <li>Sprint </li> 
     <li>작업 로그</li> 
     <li>사용자</li> 
     <li>보드</li> 
     <li>카테고리</li> 
     <li>필터</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력</td> 
   <td>수신하려는 출력을 선택합니다. 출력 옵션은 "레코드 유형" 필드에서 선택한 레코드 유형에 따라 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">(레코드 유형) ID</td> 
   <td> <p>모듈에서 읽을 레코드의 고유 Jira ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 업데이트

이 작업 모듈은 문제 또는 프로젝트와 같은 기존 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>모듈을 업데이트할 레코드 유형을 선택합니다. 레코드 유형을 선택하면 해당 레코드 유형과 관련된 다른 필드가 모듈에 나타납니다.</p> 
    <ul> 
     <li>댓글</li> 
     <li>문제</li> 
     <li>프로젝트</li> 
     <li>Sprint </li> 
     <li>전환 문제</li> 
     <li>카테고리 </li> 
     <li>필터 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID 또는 키</td> 
   <td>업데이트하려는 레코드의 ID 또는 키를 입력하거나 매핑합니다.</td> 
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td> 다른 필드에 내용을 입력합니다. 필드는 선택한 레코드 유형에 따라 사용할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

#### 레코드 검색

이 검색 모듈은 지정한 검색 쿼리와 일치하는 Jira의 객체에서 레코드를 찾습니다.

이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Jira 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Workfront Fusion에 Jira 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>모듈에서 검색할 레코드 유형을 선택합니다. 레코드 유형을 선택하면 해당 레코드 유형과 관련된 다른 필드가 모듈에 나타납니다.</p> 
    <ul> 
     <li>문제</li> 
     <li>프로젝트</li> 
     <li>사용자</li> 
     <li>Sprint</li> 
     <li>보드</li> 
     <li>작업 로그</li> 
     <li>댓글</li> 
     <li>전환 문제</li> 
     <li>카테고리</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>최대 결과</p> </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 검색할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">오프셋</td> 
    <td> 세부 정보를 검색할 첫 번째 항목의 ID를 입력하거나 매핑합니다. 이것은 레코드에 페이지를 매기는 방법입니다. 5000번째 항목을 오프셋으로 입력하면 모듈은 항목 5000-9999를 반환합니다.</td> 
   </tr>
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td> 다른 필드에 내용을 입력합니다. 필드는 선택한 레코드 유형에 따라 사용할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>
