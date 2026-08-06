---
title: Adobe Content Tagger 모듈
description: Adobe Workfront Fusion 시나리오에서는 Adobe Content Tagger를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: 801e8cb1a4c807aaa4275382c2d6211cf3cd6d1f
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 20%

---

# Adobe Content Tagger 모듈

Adobe Workfront Fusion 시나리오에서는 Adobe Content Tagger를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

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
   <p>운영 기반: 운영 기반 라이센스가 있는 조직에서 사용 가능</p>
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

## Adobe Content Tagger에 대한 연결 만들기

Adobe Content Tagger 모듈에 대한 연결을 만들려면 다음 작업을 수행하십시오.

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


## Adobe 컨텐츠 태그 모듈 및 해당 필드

Adobe Content Tagger 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Adobe 콘텐츠 태거 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 액션

* [태그 색상](#tag-colors)
* [태그 키워드](#tag-keywords)
* [이미지의 텍스트에 태그 지정](#tag-text-in-an-image)

#### 태그 색상

이 모듈은 40개의 색상 카테고리로 분류된 다양한 픽셀 색상으로 가려진 이미지의 비율을 반환합니다.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Content Tagger에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Adobe Content Tagger에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 파일 이름</td> 
   <td>색상에 태그를 지정할 이미지의 파일 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 데이터</td> 
   <td>색상에 태그를 지정할 이미지의 파일 데이터를 입력하거나 매핑합니다.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">이미지 형식</td> 
    <td>색상에 태그를 지정할 이미지의 이미지 유형을 선택합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">색상 수</td> 
    <td>반환할 색상 수를 입력하거나 매핑합니다. 모든 결과를 반환하려면 0을 입력합니다.</p></td> 
  </tr> 
 <tr> 
   <td role="rowheader">최소 범위</td> 
   <td>색상에 태깅할 최소 범위를 입력하거나 매핑합니다. 적어도 이 이미지 양을 포함하는 색상만 반환됩니다. 값 1은 이미지의 100%이고, 값 .5는 이미지의 50%를 나타냅니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">추출하기 전에 이미지 크기를 조정합니다.</td> 
   <td>색상을 추출하기 전에 이미지 크기를 320x320으로 조정하려면 [예]를 선택합니다. 전체 크기 이미지에서 색상을 추출하려면 [아니요]를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">전경/배경 마스크 활성화</td> 
   <td>전체 이미지, 전경 및 배경에 대해 색상을 별도로 보고하려면 [예]를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">색조 검색</td> 
   <td>색상 외에 따뜻한 색조, 중간 색조 및 차가운 색조에 대한 데이터를 검색하려면 [예]를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환되는 최대 색상 수</td> 
   <td>모듈이 한 실행 주기에 대해 반환하는 최대 색상 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>



#### 태그 키워드

이 모듈은 문서의 주제를 가장 잘 설명하는 키워드 또는 주요 구를 추출합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Content Tagger에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Adobe Content Tagger에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">문서 파일 이름</td> 
   <td>키워드를 추출할 문서의 파일 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 데이터</td> 
   <td>키워드를 추출할 문서의 파일 데이터를 입력하거나 매핑합니다.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">이미지 형식</td> 
    <td>키워드를 추출할 문서의 형식을 선택합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">애플리케이션 ID</td> 
   <td>문서에 대한 응용 프로그램 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">주요 구 수</td> 
   <td>모듈이 반환할 주요 구 수를 입력하거나 매핑합니다. 모든 결과를 반환하려면 0을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">최소 관련성</td> 
   <td>결과가 반환되지 않는 점수 임계값을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">최소 키 구 길이(단어)</td> 
   <td>주요 구문에 필요한 최소 단어 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">최대 키 구 길이(단어)</td> 
   <td>주요 구문에 필요한 최대 단어 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">의미 단위 깊이</td> 
   <td>계층 응답을 보낼 깊이를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">엔티티 유형</td> 
   <td>키 구문을 제한할 각 엔터티 형식에 대해 <b>항목 추가</b>를 클릭하고 엔터티 형식에 대한 정보를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### 이미지의 텍스트에 태그 지정

이 모듈은 이미지에 텍스트가 있는지 여부를 나타내고, 있는 경우 텍스트를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Content Tagger에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Adobe Content Tagger에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 파일 이름</td> 
   <td>텍스트를 추출할 문서의 파일 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 데이터</td> 
   <td>텍스트를 추출할 문서의 파일 데이터를 입력하거나 매핑합니다.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">이미지 형식</td> 
    <td>텍스트를 추출할 문서의 형식을 선택합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">사전을 사용하여 필터링</td> 
   <td>영어 사전에 있는 단어만 반환할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">최소 확률</td> 
   <td>최소 확률을 입력하거나 매핑합니다. 그러면 모듈에서 적어도 이 정도의 확률로 인식된 단어만 반환합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">최소 관련성</td> 
   <td>반환된 텍스트가 포함해야 하는 이미지의 최소 백분율을 입력합니다. 관련성은 전체 이미지와 비교하여 추출된 텍스트의 테두리 상자 영역의 분수로 계산됩니다. 0.01은 이미지의 최소 1%를 차지하는 텍스트로 변환됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>모듈이 한 실행 주기 동안 반환할 최대 결과 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>
