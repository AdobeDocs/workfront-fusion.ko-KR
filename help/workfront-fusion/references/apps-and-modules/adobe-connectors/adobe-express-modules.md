---
title: Adobe Express 모듈
description: Adobe Workfront Fusion 시나리오에서는 Adobe Express을 사용하는 워크플로를 자동화할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: eab04db9a38020ed973f98d7f8f290ccd183251c
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 17%

---

# Adobe Express 모듈

Adobe Workfront Fusion 시나리오에서는 Adobe Express을 사용하는 워크플로를 자동화할 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

Adobe Express 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 Adobe Express 계정이 있어야 합니다.

## Adobe Express에 대한 연결 만들기

Adobe Express 모듈에 대한 연결을 만들려면 다음 작업을 수행하십시오.

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

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
          <p>이 연결의 이름을 입력합니다.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">환경</td>
        <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">유형</td>
        <td>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">클라이언트 ID</td>
        <td>Adobe 클라이언트 ID를 입력합니다. 이 정보는 Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
        <tr>
        <td role="rowheader">클라이언트 암호</td>
        <td>Adobe 클라이언트 암호를 입력합니다. 이 정보는 Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.


## Adobe Express 모듈 및 해당 필드

Adobe Express 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Adobe Express 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 액션

#### 렌디션 내보내기

이 모듈은 문서를 JPG 또는 PNG 형식으로 내보냅니다. 페이지 표현물에 대해 사전 서명된 URL을 제공할 수 있으며, 이 URL은 4시간 동안 유효합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Express에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Adobe Express에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">문서</td> 
   <td>렌디션을 내보낼 문서를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">페이지 번호</td> 
   <td>렌디션에 포함할 페이지 번호를 입력하거나 매핑합니다. 렌디션 요청이 수행될 페이지 번호를 쉼표로 구분한 문자열입니다. 예를 들어 "1,2,3". 페이지 범위를 지정할 수도 있습니다. 예를 들어 "1-3"은 1, 2, 3페이지를 포함합니다. 또 다른 예는 1, 3, 4, 5페이지를 포함하는 "1,3-5"입니다. "1-"는 모든 페이지를 지정하는 데 사용할 수 있으며, "5-"는 5페이지에서 마지막 페이지까지를 나타냅니다. 제공되지 않으면 기본적으로 첫 번째 페이지가 고려됩니다. 페이지 번호는 1부터 시작합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">렌디션 유형</td> 
   <td>내보낼 렌디션 유형(이미지, 비디오 또는 PDF)을 선택합니다</td> 
  </tr>
  <tr> 
   <td role="rowheader">형식</td> 
   <td>렌디션의 파일 형식을 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">PDF 유형</td> 
   <td>PDF을 내보내는 경우 표준 PDF을 내보내거나 를 인쇄할지 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">크기</td> 
   <td>이미지 또는 비디오를 내보내는 경우 가장 긴 변의 크기를 픽셀 단위로 입력하거나 매핑합니다. 종횡비는 그대로 유지됩니다. 이미지의 경우 지원되는 최소 크기는 1px이고 지원되는 최대 크기는 8192px입니다. 제공하지 않으면 페이지의 기본 크기가 고려됩니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">개별 PDF 파일 다운로드</td> 
   <td>PDF을 내보내는 경우 페이지가 별도의 PDF 파일로 다운로드되는지 여부를 선택합니다. true인 경우 각 페이지는 자체 PDF 파일로 다운로드됩니다. false인 경우 모든 페이지가 단일 PDF 파일로 결합됩니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">구성</td> 
   <td>PDF을 내보내는 경우 PDF을 표준 구성으로 할지 또는 인쇄 구성으로 할지를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">접근성 단계</td> 
   <td>표준 PDF을 내보내는 경우 PDF에 액세서빌러티 태그를 포함할지 여부를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">도련</td> 
   <td>인쇄 PDF을 내보내는 경우 내보내기에 도련 설정을 포함할지 여부를 선택합니다</td> 
  </tr>
  <tr> 
   <td role="rowheader">도련 설정 &gt; 양</td> 
   <td>도련 여백의 양을 입력합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">도련 설정 &gt; 단위</td> 
   <td>양이 인치를 나타내는지 아니면 밀리미터를 나타내는지 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">자르기</td> 
   <td>인쇄 PDF을 내보내는 경우 내보내기에 자르기 설정을 포함할지 여부를 선택합니다</td> 
  </tr>
  <tr> 
   <td role="rowheader">자르기 설정 &gt; 금액</td> 
   <td>자르기 여백의 양을 입력합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">자르기 설정 &gt; 단위</td> 
   <td>양이 인치를 나타내는지 아니면 밀리미터를 나타내는지 선택합니다.</td> 
  </tr>
 </tbody> 
</table>

#### 변형 생성

이 모듈은 제공된 입력 매개 변수를 기반으로 문서 변형을 만듭니다. 처리 후 생성된 문서를 임시 저장하고 지정된 폴더 내에서 사용자가 사용할 수 있도록 합니다. 30일 동안 문서에 액세스할 수 있는 상태가 유지되며, 이후 시스템에서 자동으로 해당 문서를 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Express에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Adobe Express에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">문서</td> 
   <td>변형을 생성할 문서를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">페이지 번호</td> 
   <td>렌디션에 포함할 페이지 번호를 입력하거나 매핑합니다. 변형 요청이 수행될 페이지 번호를 쉼표로 구분한 문자열입니다. 예를 들어 "1,2,3". 페이지 범위를 지정할 수도 있습니다. 예를 들어 "1-3"은 1, 2, 3페이지를 포함합니다. 또 다른 예는 1, 3, 4, 5페이지를 포함하는 "1,3-5"입니다. "1-"는 모든 페이지를 지정하는 데 사용할 수 있으며, "5-"는 5페이지에서 마지막 페이지까지를 나타냅니다. 제공되지 않으면 기본적으로 첫 번째 페이지가 고려됩니다. 페이지 번호는 1부터 시작합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">기본 문서 이름.</td> 
   <td>새 문서의 이름을 입력하거나 매핑합니다. 이름을 제공하지 않거나 이름이 이미 사용 중이면 시스템에서 고유한 이름을 생성합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">프로젝트 ID</td> 
   <td>변형이 저장될 프로젝트의 ID를 입력합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td>다른 필드에 대한 값을 입력합니다. 사용 가능한 필드는 선택한 문서를 기반으로 합니다.</td> 
  </tr>
 </tbody> 
</table>


### 검색 결과

#### 태그가 지정된 문서 검색

이 모듈은 관련 메타데이터와 함께 태그가 지정된 문서 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Express에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Adobe Express에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">색인 시작</td> 
   <td>페이지 매김 시작 인덱스를 입력하거나 매핑합니다. 다른 결과 목록을 검색한 후 해당 목록을 계속하려는 경우 사용합니다. 기본 색인은 0입니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 실행 주기에 대해 모듈이 반환할 최대 결과 수를 입력하거나 매핑합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">정렬 기준</td> 
   <td>결과를 정렬할 속성을 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">방향</td> 
   <td>결과를 오름차순으로 정렬할지 아니면 내림차순으로 정렬할지 선택합니다.</td> 
  </tr>
 </tbody> 
</table>

#### 문서 세부 정보 가져오기

이 모듈은 지정된 문서 내에서 페이지 및 태그가 지정된 요소의 세부 정보를 검색합니다. 문서 페이지의 페이지 매김된 목록과 각 페이지에 대한 메타데이터를 반환합니다. 문서에 태그가 지정된 요소가 있는 경우 API에는 크기 및 위치와 같은 해당 세부 정보가 포함됩니다. 문서에 태그가 지정된 요소가 없으면 빈 배열을 반환합니다. 응답에는 사용자가 문서의 페이지를 탐색하는 데 도움이 되는 페이지 매김 정보가 포함됩니다. 한 번의 주기로 최대 10개의 페이지를 반환할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Express에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Adobe Express에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">문서</td> 
   <td>페이지 및 세부 정보를 반환할 문서를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">시작 페이지</td> 
   <td>세부 정보를 검색할 첫 번째 페이지의 페이지 번호를 입력하거나 매핑합니다.</td>

#### 작업 상태 검색

이 모듈은 작업 ID로 작업 상태를 검색합니다. 작업 유형에 따라 응답에는 작업별 세부 정보가 포함될 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Express에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Adobe Express에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">작업 ID</td> 
   <td>세부 정보를 검색할 작업의 ID를 입력하거나 매핑합니다.</td> 
  </tr>

