---
title: Adobe Firefly 오디오 및 비디오 모듈
description: Adobe Workfront Fusion 시나리오에서는 Adobe Firefly 오디오 및 비디오를 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수도 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: f54338aa35b8453ac991c9e16974f2b61fd30168
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 14%

---

# Adobe Firefly 오디오 및 비디오 모듈

Adobe Workfront Fusion 시나리오에서는 Adobe Firefly 오디오 및 비디오를 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수도 있습니다.

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

Adobe Firefly 오디오 및 비디오 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 Adobe Firefly 오디오 및 비디오 계정이 있어야 합니다.

## Adobe Firefly 오디오 및 비디오에 대한 연결 만들기

Adobe Firefly 오디오 및 비디오 모듈에 대한 연결을 만들려면 다음 작업을 수행하십시오.

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


## Adobe Firefly 오디오 및 비디오 모듈과 해당 필드

Adobe Firefly 오디오 및 비디오 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 추가 Adobe Firefly 오디오 및 비디오 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 액션

* [템플릿 설명](#describe-template)
* [오디오 또는 비디오 더브](#dub-audio-or-video)
* [텍스트 또는 오디오에서 아바타 비디오 생성](#generate-avatar-video-from-text-or-audio)
* [텍스트에서 음성 생성](#generate-speech-from-text)
* [프레임 비디오](#reframe-video)
* [템플릿 렌더링](#render-template)
* [기록 매체](#transcribe-media)

#### 템플릿 설명

이 작업 모듈은 MOGRT(비디오 템플릿) 파일을 분석하고 편집 가능한 컨트롤, 글꼴, 이미지, 오디오, 비디오 및 기타 지원되는 값의 매니페스트를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Adobe Firefly에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>입력 템플릿 파일을 가리키는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr>
 </tbody> 
</table>

#### 오디오 또는 비디오 더브

이 작업 모듈은 더빙된 오디오 또는 비디오를 생성합니다. 생성된 비디오에 립 싱크(lip sync)를 포함할 수도 있다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Adobe Firefly에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dub 유형</td> 
   <td>오디오 또는 비디오 더브를 생성할지 여부를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">사전 서명된 URL</td> 
   <td>모듈에서 입력에 사용할 사전 서명된 URL을 입력하거나 매핑합니다.<p>Firefly 오디오 및 비디오에서는 다음 미디어 스토리지 도메인을 허용합니다</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">미디어 유형</td> 
   <td>입력 파일의 미디어 유형 선택</td> 
  </tr>
  <tr> 
   <td role="rowheader">립 싱크</td> 
   <td>비디오 출력에 대해 고품질 합성 립 동기화를 생성할지 여부를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">대상 로케일 코드</td> 
   <td>추가할 각 로케일 코드에 대해 <b>항목 추가</b>를 클릭하고 로케일 코드를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">성적 증명서</td> 
   <td>추가할 각 성적 증명서에 대해 <b>항목 추가</b>를 클릭하고 성적 증명서의 사전 서명된 URL을 입력하거나 매핑하십시오.</td> 
  </tr>
 </tbody> 
</table>

#### 텍스트 또는 오디오에서 아바타 비디오 생성

이 작업 모듈은 사용자가 제공한 트랜스크립트 또는 오디오 파일에서 아바타 비디오를 생성합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Adobe Firefly에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>모듈에서 입력에 사용할 사전 서명된 URL을 입력하거나 매핑합니다.   </td> 
  </tr>
  <tr> 
  <tr> 
   <td role="rowheader">로케일 코드</td> 
   <td>결과에 사용할 언어를 나타내는 로케일 코드를 선택합니다.</td> 
  </tr>
   <td role="rowheader">미디어 유형(Source)</td> 
   <td>입력 파일의 미디어 유형 선택</td> 
  </tr>
  <tr> 
   <td role="rowheader">아바타</td> 
   <td>생성된 비디오에 사용할 아바타를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">미디어 유형</td> 
   <td>생성된 비디오의 출력 미디어 유형을 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">폭</td> 
   <td>생성된 비디오의 너비를 입력하거나 매핑합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">높이</td> 
   <td>생성된 비디오의 높이를 입력하거나 매핑합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">배경</td> 
   <td>생성된 비디오에 사용할 배경 유형을 선택합니다.
   <ul>
   <li><b>비디오</b>: 배경 비디오의 URL을 입력하거나 매핑합니다.</li> 
   <li><b>이미지</b>: 배경 이미지의 URL을 입력하거나 매핑합니다.</li>
   <li><b>색상</b>: 비디오 배경에 사용할 색상의 16진수 값을 입력하거나 매핑합니다.</li> 
   </ul>
   </td>
  </tr>
 </tbody> 
</table>

#### 텍스트에서 음성 생성

이 작업 모듈은 트랜스크립트에서 음성을 생성합니다. 일반 텍스트 트랜스크립션이나 사전 서명된 URL을 제공할 수 있습니다. 응답에는 작업 ID 및 작업 추적을 위한 상태 URL이 포함됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Adobe Firefly에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스크립트</td> 
   <td>제공할 스크립트 유형을 선택합니다.
   <ul>
   <li><b>텍스트</b>: 원본 텍스트를 텍스트 필드에 입력하거나 매핑합니다.</li>
   <li><b>텍스트 파일</b>: URL 필드에 텍스트 파일의 URL을 입력하거나 매핑합니다.</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">로케일 코드</td> 
   <td>결과에 사용할 언어를 나타내는 로케일 코드를 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">미디어 유형</td> 
   <td><code>text/plain</code>이어야 합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">음성</td> 
   <td>사용할 음성을 선택합니다. 사용 가능한 목소리는 Adobe Firefly 음성 카탈로그에서 확인할 수 있습니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">출력</td> 
   <td><code>audio/wav</code>이어야 합니다.</td> 
  </tr>
 </tbody> 
</table>

#### 프레임 비디오

이 모듈은 사용자가 제공하는 미디어의 이름을 바꿉니다. 미디어는 사전 서명된 URL을 통해 제공됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Adobe Firefly에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사전 서명된 URL</td> 
   <td>모듈에서 입력에 사용할 사전 서명된 URL을 입력하거나 매핑합니다.<p>Firefly 오디오 및 비디오에서는 다음 미디어 스토리지 도메인을 허용합니다</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">장면 편집 감지</td> 
   <td>프레임 전에 장면 편집 감지 를 적용할지 여부를 선택합니다. </td> 
  </tr>
  <tr> 
   <td role="rowheader">초점</td> 
   <td>추가할 각 초점에 대해 <b>항목 추가</b>를 클릭하고 초점의 키워드 식별자를 입력합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">오버레이</td> 
   <td>추가할 각 오버레이에 대해 <b>항목 추가</b>를 클릭하고 오버레이 정보를 입력하십시오.
   <ul>
   <li><b>Source</b>: 소스 미디어를 가리키는 URL을 입력하거나 매핑합니다.</li> 
   <li><b>시작 시간</b>: 시작 시간을 입력하거나 매핑합니다.</li>
   <li><b>기간</b>: 오버레이의 기간을 입력하거나 매핑합니다.</li> 
   <li><b>너비</b>: 크기가 조정된 오버레이의 너비를 입력하거나 매핑합니다.</li> 
   <li><b>높이</b>: 크기가 조정된 오버레이의 높이를 입력하거나 매핑합니다.</li> 
   <li><b>고정점</b>: 오버레이의 고정점을 선택합니다.</li> 
   <li><b>오프셋 X</b>: 오버레이의 가로 오프셋을 입력하거나 매핑합니다.</li> 
   <li><b>오프셋 Y</b>: 오버레이에 대한 세로 오프셋을 입력하거나 매핑합니다.</li> 
   <li><b>반복</b>: <code>loop</code>을(를) 입력하여 GIF이 반복되도록 합니다.</li> 
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">미디어 형식</td> 
   <td>재구성된 비디오의 형식을 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">사이드카 형식</td> 
   <td>추가 메타데이터의 형식을 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">표현물</td> 
   <td>렌디션을 추가하려면 <b>항목 추가</b>를 클릭하고 렌디션 정보를 입력하십시오.<!--add additional info--></td> 
  </tr>
 </tbody> 
</table>

#### 템플릿 렌더링

이 모듈은 무시 및 내보내기 사전 설정을 적용하여 하나 이상의 비디오 변형을 렌더링합니다.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Adobe Firefly에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">템플릿 파일 URL 입력</td> 
   <td>렌더링할 템플릿을 나타내는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">글꼴</td> 
   <td>추가할 각 글꼴에 대해 <b>항목 추가</b>를 클릭하고 글꼴의 포스트스크립트 이름과 글꼴 파일 URL을 입력합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">글꼴이 누락된 경우</td> 
   <td>렌더링에 실패할지 또는 글꼴이 누락된 경우 기본 글꼴을 사용할지 선택합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">미디어 자산</td> 
   <td>추가할 각 미디어 에셋에 대해 <b>항목 추가</b>를 클릭하고 에셋을 나타내는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr>
  <tr> 
   <td role="rowheader">사전 설정 내보내기</td> 
   <td>추가할 각 내보내기 사전 설정에 대해 <b>항목 추가</b>를 클릭하고 비디오 사전 설정을 선택한 다음 사전 설정을 나타내는 사전 서명된 URL을 입력하거나 매핑하십시오.</td> 
  </tr>
  <tr> 
   <td role="rowheader">변형</td> 
   <td>추가할 각 변형에 대해 <b>항목 추가</b>를 클릭하고 변형에 대한 세부 정보를 입력하십시오. 하나 이상의 변형에 대한 세부 정보를 입력해야 합니다.<!--add data here--></td> 
  </tr>
  <tr> 
   <td role="rowheader">출력 정의</td> 
   <td><b>항목 추가</b>를 클릭하고 추가된 변형 및 사전 설정 중 사용할 항목을 선택하고 파일 이름을 추가하여 출력을 정의합니다. 변형 및 사전 설정은 0으로 색인화됩니다(변형 목록의 첫 번째 항목은 0이고 그 다음 항목은 1임).</td> 
  </tr>
 </tbody> 
</table>

#### 기록 매체

이 모듈은 오디오 또는 비디오를 복사합니다.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly에 대한 연결 만들기에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Adobe Firefly에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">트랜스크립션 유형</td> 
   <td>오디오 또는 비디오 복사 여부를 선택합니다.   </td> 
  </tr>
  <tr> 
   <td role="rowheader">사전 서명된 URL</td> 
   <td>모듈에서 입력에 사용할 사전 서명된 URL을 입력하거나 매핑합니다.   </td> 
  </tr>
  <tr> 
  </tr>
   <td role="rowheader">미디어 유형 </td> 
   <td>입력 파일의 미디어 유형 선택</td> 
  </tr>
  <tr> 
   <td role="rowheader">대상 로케일 코드</td> 
   <td>추가할 각 로케일 코드에 대해 <b>항목 추가</b>를 클릭하고 결과에 사용할 언어를 나타내는 로케일 코드를 선택합니다.</td> 
  <tr> 
   <td role="rowheader">캡션 형식</td> 
   <td>캡션을 포함하려면 <code>SRT</code>을(를) 입력하거나, 캡션을 사용하지 않으려면 비워 두십시오.</td> 
  </tr>
 </tbody> 
</table>



