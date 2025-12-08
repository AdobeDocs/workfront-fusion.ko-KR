---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe InDesign 모듈
description: Adobe Workfront Fusion 시나리오에서는 Adobe InDesign을 사용하는 워크플로를 자동화할 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
source-git-commit: 30ddefa8519e6f2052308482137d0fa018676902
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 20%

---


# Adobe InDesign 모듈

Adobe Workfront Fusion 시나리오에서는 Adobe InDesign을 사용하는 워크플로를 자동화할 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

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
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>작업 기반: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

Adobe InDesign 커넥터를 사용하려면 먼저 활성 Adobe InDesign 계정이 있어야 합니다.

## Adobe InDesign에 대한 연결 만들기

Adobe InDesign 모듈에 대한 연결을 만들려면 다음 작업을 수행하십시오.

1. 모든 Adobe InDesign 모듈에서 연결 상자 옆에 있는 **추가**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
      </col>
      <tbody>
        <tr>
          <td role="rowheader">연결 이름</td>
          <td>
            <p>이 연결의 이름을 입력합니다.</p>
          </td>
        </tr>
      <tr>
        <td role="rowheader">환경</td>
        <td>
          <p>프로덕션 환경에 연결할지 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">유형</td>
        <td>
          <p>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
        <tr>
          <td role="rowheader">클라이언트 ID</td>
          <td>Adobe 클라이언트 ID를 입력합니다. Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다</td>
        </tr>
        <tr>
          <td role="rowheader">클라이언트 암호</td>
          <td>Adobe 클라이언트 암호를 입력합니다. Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다</td>
        </tr>
        <tr>
          <td role="rowheader">IMS 조직 ID</td>
          <td>Adobe 조직 ID를 입력합니다. Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다</td>
        </tr>
      </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **계속**&#x200B;을 클릭합니다.

## InDesign 모듈 및 해당 필드

Adobe InDesign 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Adobe InDesign 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 액션

* [렌디션 만들기](#create-rendition)
* [사용자 지정 스크립트 삭제](#delete-a-custom-script)
* [데이터 병합](#merge-data)
* [링크 다시 매핑](#remap-links)
* [사용자 지정 스크립트 실행 요청 제출](#submit-a-custom-script-execution-request)

#### 렌디션 만들기

이 작업 모듈은 특정 InDesign 문서의 JPEG, PNG 또는 PDF 렌디션을 만들고 반환합니다. `StatusCompletedRespons/output/data`의 구조에 대해서는 `RenditionOutputData`을(를) 참조하십시오. `FailedEvent`에서 가능한 오류 코드 목록은 `RenditionFailedData`을(를) 참조하십시오.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>유형</p>
      </td>
      <td>만들려는 렌디션의 파일 유형을 선택합니다. 
      <ul><li>JPEG</li><li>PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>에셋</p>
      </td>
      <td>렌디션에 추가할 각 에셋에 대해 다음 작업을 수행하십시오.<ol><li><b>항목 추가</b>를 클릭합니다.</li><li>에셋의 소스를 선택하거나 매핑합니다.</li><li>대상을 입력합니다. 대상은 리소스가 다운로드되는 임시 기본 디렉터리(작업 디렉터리)에 상대적인 경로입니다. 이는 매개 변수 내의 에셋을 식별합니다. '..'를 사용하여 위로 이동할 수 없습니다. 또는 '/'입니다. 유효한 파일 이름이 있어야 합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">대상 문서</td>
      <td>처리 및 렌더링할 문서를 입력하거나 매핑합니다. 현재는 한 번에 한 문서만 지원됩니다.</td>
    </tr>
    <tr>
      <td role="rowheader">기타 필드</td>
   <td>다른 필드의 경우 모듈에 포함된 정보를 참조하십시오.</td>     </tr>
  </tbody>
</table>

#### 사용자 지정 스크립트 삭제

이 작업 모듈은 등록된 단일 사용자 지정 스크립트를 삭제합니다. 스크립트의 모든 버전이 영구적으로 제거됩니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>스크립트 이름</p>
      </td>
      <td>삭제할 스크립트의 이름을 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### 데이터 병합

이 모듈은 CSV 데이터를 InDesign 템플릿과 병합하여 InDesign 문서 또는 PDF를 만듭니다. 출력 형식에는 JPEG, PNG, PDF 및 InDesign 문서가 포함됩니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>에셋</p>
      </td>
      <td>데이터 병합에 추가할 각 자산에 대해 다음 작업을 수행하십시오.<ol><li><b>항목 추가</b>를 클릭합니다.</li><li>에셋의 소스를 선택하거나 매핑합니다.</li><li>대상을 입력합니다. 대상은 리소스가 다운로드되는 임시 기본 디렉터리(작업 디렉터리)에 상대적인 경로입니다. 이는 매개 변수 내의 에셋을 식별합니다. '..'를 사용하여 위로 이동할 수 없습니다. 또는 '/'입니다. 유효한 파일 이름이 있어야 합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">대상 문서</td>
      <td>병합을 위한 템플릿으로 사용할 문서를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">데이터 소스</td>
      <td>사용할 소스 파일을 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">기타 필드</td>
   <td>다른 필드의 경우 모듈에 포함된 정보를 참조하십시오.</td>     </tr>
  </tbody>
</table>

#### 링크 다시 매핑

이 모듈은 InDesign 문서의 파일 기반 링크를 Adobe Experience Manager(AEM) URL로 대체합니다. 이 기능은 Adobe Asset Link를 사용하여 Adobe Experience Manager 작업에 유용할 수 있습니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
      </tr>
    <tr>
      <td role="rowheader">AEM 토큰</td>
      <td>전달자 키워드 없이 AEM 기술 계정에 대해 생성된 전달자 토큰을 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>에셋</p>
      </td>
      <td>모듈에 추가할 각 에셋에 대해:<ol><li><b>항목 추가</b>를 클릭합니다.</li><li>에셋의 소스를 선택하거나 매핑합니다.</li><li>대상을 입력합니다. 대상은 리소스가 다운로드되는 임시 기본 디렉터리(작업 디렉터리)에 상대적인 경로입니다. 이는 매개 변수 내의 에셋을 식별합니다. '..'를 사용하여 위로 이동할 수 없습니다. 또는 '/'입니다. 유효한 파일 이름이 있어야 합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">대상 문서</td>
      <td>링크를 다시 매핑할 문서를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">데이터 소스</td>
      <td>태그를 추출하고 일치시키는 데 사용할 소스 파일을 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">기타 필드</td>
   <td>다른 필드의 경우 모듈에 포함된 정보를 참조하십시오.</td>     </tr>
  </tbody>
</table>

#### 사용자 지정 스크립트 실행 요청 제출

이 작업 모듈은 사용자 지정 스크립트에 대한 실행 요청을 제출합니다. 실행 중에 사용자 지정 스크립트에서 사용할 입력 에셋 및 매개 변수를 정의합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>스크립트 ID</p>
      </td>
      <td>사용자 지정 스크립트의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>에셋</p>
      </td>
      <td>실행 요청을 제출하려는 각 에셋에 대해 <ol><li><b>항목 추가</b>를 클릭합니다.</li><li>에셋의 소스를 선택하거나 매핑합니다.</li><li>대상을 입력합니다. 대상은 리소스가 다운로드되는 임시 기본 디렉터리(작업 디렉터리)에 상대적인 경로입니다. 이는 매개 변수 내의 에셋을 식별합니다. '..'를 사용하여 위로 이동할 수 없습니다. 또는 '/'입니다. 유효한 파일 이름이 있어야 합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">기타 필드</td>
   <td>다른 필드의 경우 모듈에 포함된 정보를 참조하십시오.</td>     </tr>
  </tbody>
</table>

### 검색 결과

* [사용자 지정 스크립트 세부 정보 가져오기](#get-custom-script-details)
* [데이터 병합 태그 가져오기](#get-data-merge-tags)
* [문서 정보 가져오기](#get-document-information)
* [사용자 지정 스크립트 나열](#list-custom-scripts)

#### 사용자 지정 스크립트 세부 정보 가져오기

이 검색 모듈은 버전, 다운로드 링크, 등록 날짜 및 스크립트 이름을 포함하여 등록된 단일 사용자 정의 스크립트의 세부 정보를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>스크립트 이름</p>
      </td>
      <td>세부 정보를 검색할 스크립트의 이름을 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### 데이터 병합 태그 가져오기

이 모듈은 문서에서 데이터 병합 태그를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>에셋</p>
      </td>
      <td>모듈에 추가할 각 에셋에 대해:<ol><li><b>항목 추가</b>를 클릭합니다.</li><li>에셋의 소스를 선택하거나 매핑합니다.</li><li>대상을 입력합니다. 대상은 리소스가 다운로드되는 임시 기본 디렉터리(작업 디렉터리)에 상대적인 경로입니다. 이는 매개 변수 내의 에셋을 식별합니다. '..'를 사용하여 위로 이동할 수 없습니다. 또는 '/'입니다. 유효한 파일 이름이 있어야 합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">대상 문서</td>
      <td>태그를 검색할 문서를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">데이터 소스</td>
      <td>태그를 추출하고 일치시키는 데 사용할 소스 파일을 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">기타 필드</td>
   <td>다른 필드의 경우 모듈에 포함된 정보를 참조하십시오.</td>     </tr>
  </tbody>
</table>

#### 문서 정보 가져오기

이 모듈은 INDD/IDML 문서에 대한 포괄적인 정보를 검색하고 요청에 지정된 활성화된 정보 유형을 기반으로 데이터를 반환합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>에셋</p>
      </td>
      <td>모듈에 추가할 각 에셋에 대해:<ol><li><b>항목 추가</b>를 클릭합니다.</li><li>에셋의 소스를 선택하거나 매핑합니다.</li><li>대상을 입력합니다. 대상은 리소스가 다운로드되는 임시 기본 디렉터리(작업 디렉터리)에 상대적인 경로입니다. 이는 매개 변수 내의 에셋을 식별합니다. '..'를 사용하여 위로 이동할 수 없습니다. 또는 '/'입니다. 유효한 파일 이름이 있어야 합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">대상 문서</td>
      <td>정보를 가져올 문서를 입력하거나 매핑합니다.</td>
    </tr>
     <tr>
      <td role="rowheader">기타 필드</td>
   <td>다른 필드의 경우 모듈에 포함된 정보를 참조하십시오.</td>     </tr>
  </tbody>
</table>

#### 사용자 지정 스크립트 나열

이 모듈은 버전, 다운로드 링크, 등록 날짜 및 스크립트 이름을 포함하여 등록된 모든 사용자 지정 스크립트의 최신 버전에 대한 세부 정보를 검색합니다. 결과는 목록 길이에 따라 페이지가 매겨집니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
      </tr>
    <tr>
      <td role="rowheader">페이지 번호</td>
      <td>시작하려는 페이지 번호를 입력하거나 매핑합니다.</td>
    </tr>
  <tr> 
   <td>반환된 최대 결과 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 팀 또는 그룹 수를 설정합니다.</td> 
  </tr> 
  </tbody>
</table>


### 기타

#### 사용자 정의 API 호출하기

이 모듈은 Adobe InDesign API에 대한 사용자 지정 API 호출을 생성합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe InDesign에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Adobe InDesign에 대한 연결 만들기</a>를 참조하십시오.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>경로</p>
      </td>
      <td>
        <p><code>https://indesign.adobe.io/v3</code>과 관련된 경로를 입력합니다.</p><p> 예: <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>메서드</p>
      </td>
      <td>
        <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [HTTP 요청 메서드](/help/workfront-fusion/references/modules/http-request-methods.md)를 참조하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">헤더</td>
      <td>
        <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p>
        <p>예: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">쿼리 문자열  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
      </td>
    </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  </tbody>
</table>
