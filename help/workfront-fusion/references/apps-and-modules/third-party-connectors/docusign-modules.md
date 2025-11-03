---
title: DocuSign 모듈
description: ' [!DNL Adobe Workfront Fusion DocuSign] 모듈을 사용하면 봉투 상태를 모니터링 및 검색하고 봉투를 검색 및 검색하거나  [!DNL DocuSign] 계정에 로그인할 문서를 다운로드하여 보낼 수 있습니다.'
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2250'
ht-degree: 0%

---

# DocuSign 모듈

Adobe Workfront Fusion [!DNL DocuSign] 모듈을 사용하면 봉투 상태를 모니터링 및 검색하고 봉투를 검색 및 검색하거나 문서를 다운로드하여 보내 [!DNL DocuSign] 계정에 로그인할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

[!DNL DocuSign] 모듈을 사용하려면 [!DNL DocuSign] 계정이 있어야 합니다.

## DocuSign API 정보

DocuSign 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL DocuSign] 연결 {#connect-docusign-to-workfront-fusion}

[!DNL DocuSign] 모듈에 대한 연결을 만들려면:

1. 첫 번째 **[!UICONTROL 모듈 구성을 시작할 때]**&#x200B;연결[!UICONTROL  상자 옆에 있는 ]추가[!DNL DocuSign]를 클릭합니다.
1. 다음을 입력하십시오.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 이름]</p> </td> 
      <td>새 [!DNL DocuSign] 연결의 이름을 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 환경]</p> </td> 
      <td>비프로덕션 환경에서 프로덕션에 연결할지 여부를 선택합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 이름]</p> </td> 
      <td>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 계정 유형]</td> 
      <td>연결할 계정이 프로덕션 계정인지 데모 계정인지 선택합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 저장하고 모듈로 돌아가려면 **계속**&#x200B;을 클릭하세요.

## [!DNL DocuSign]개 모듈 및 해당 필드

[!DNL DocuSign] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL DocuSign] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)

### 트리거

#### [!UICONTROL 봉투 보기]

이 트리거 모듈은 봉투가 전송, 전달, 서명, 완료 또는 거부될 때 시나리오를 시작합니다.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 Docusign 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정] </td> 
   <td> <p>보려는 레코드가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이벤트 유형]</td> 
   <td> <p> 보려는 이벤트 유형을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 문서 완료]</li> 
     <li>[!UICONTROL 문서 거부됨]</li> 
     <li>[!UICONTROL 문서 전송됨]</li> 
     <li>[!UICONTROL 문서 서명됨]</li> 
     <li>[!UICONTROL 받은 편지함의 새 문서]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 출력]</p> </td> 
   <td> <p>모듈 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 사용할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 사용자 지정 필드 추가]](#add-a-custom-field)
* [[!UICONTROL Envelope에 수신자 추가]](#add-recipient-to-envelope)
* [[!UICONTROL 새 봉투 만들기]](#create-a-new-envelope)
* [[!UICONTROL 사용자 지정 API 호출]](#custom-api-call)
* [[!UICONTROL 문서 다운로드]](#download-a-document)
* [[!UICONTROL 사용자 지정 필드 수정]](#modify-custom-field)
* [[!UICONTROL 봉투 읽기]](#read-an-envelope)
* [[!UICONTROL 봉투 보내기]](#send-envelope)
* [[!UICONTROL 봉투(envelope)에 파일 업로드]](#upload-a-file-to-an-envelope)

#### [!UICONTROL 사용자 지정 필드 추가]

이 작업 모듈은 문서에 사용자 정의 필드를 추가합니다

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL DocuSign] 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정] </td> 
   <td> <p>사용자 정의 필드를 추가할 문서가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 사용자 정의 필드를 추가할 문서가 포함된 봉투의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드 이름]</td> 
   <td>추가할 새 필드의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필수]</td> 
   <td>추가된 필드를 필수 필드로 설정하려면 이 옵션을 활성화하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드 표시]</td> 
   <td>필드를 표시하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 값]</td> 
   <td>추가된 필드의 값(내용)을 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Envelope에 수신자 추가]

이 작업 모듈은 기존 봉투에 한 명 이상의 수신자를 추가합니다. 봉투를 이미 보낸 경우 수신자에게 이메일이 전송됩니다. 이미 완료된 봉투에는 이 모듈을 사용할 수 없습니다.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>DocuSign 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL 계정] </td>
   <td> <p>수신자를 추가할 봉투가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>수신자를 추가하려는 봉투 ID를 선택하거나 매핑합니다.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL 수신자 유형]</td>
   <td> <p> 봉투에 추가할 수신자 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-Person 서명자]</p> </li> 
     <li> <p>[!UICONTROL Intermediator]</p> </li> 
     <li> <p>[!UICONTROL 서명자]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>봉투에 추가하려는 수신자의 이메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 이름]</td>
   <td>봉투에 추가할 수신자의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL 라우팅 순서]</td>
   <td> <p>수신자의 라우팅 번호를 입력하거나 매핑합니다. 라우팅 번호는 수신자가 문서를 받고 서명하는 순서를 결정합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 이메일 본문]</td>
   <td>수신자에게 보낼 이메일의 본문(콘텐츠)을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL 이메일 제목]</td>
   <td>수신자에게 보내는 전자 메일의 제목을 입력하거나 매핑합니다.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> 수신자에게 비공개 메시지를 보내려면 메시지 텍스트를 입력하거나 매핑합니다. <p>선택한 수신자만 일반 메시지와 함께 비공개 메시지를 볼 수 있습니다. 비공개 메시지는 1000자로 제한됩니다.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>수신자의 ID를 확인하는 데 사용할 인증 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 없음]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL 액세스 코드]</strong> </p> <p>액세스 코드를 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>전화 번호를 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>전화 번호를 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 새 봉투 만들기]

이 작업 모듈은 템플릿에서 새 Envelope을 생성합니다. 새 봉투 ID와 새 봉투의 상태가 반환됩니다.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>DocuSign 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>의 문서를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 계정] </td>
   <td> <p>파일을 업로드할 봉투(envelope)가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> 새 포락선을 생성할 템플릿을 선택합니다. 템플릿은 선택한 [!UICONTROL 계정]을 기반으로 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     생성 후 [!UICONTROL]
   </td> 
   <td> <p>봉투를 초안으로 저장할지 서명을 위해 전송할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 템플릿 수신자]</td>
    <td>이 봉투에 추가할 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음 세부 정보를 입력하십시오.
    <ul>
    <li><b>액세스 코드</b><p>수신자가 봉투에 액세스하는 데 사용하는 코드를 입력하거나 매핑합니다.<p></li>
    <li><b>이메일</b><p>수신자의 이메일 주소를 입력하거나 매핑합니다.<p></li>
    <li><b>이름</b><p>수신자의 이름을 입력하거나 매핑합니다.<p></li>
    <li><b>역할 이름</b><p>수신자의 역할 이름을 입력하거나 매핑합니다.<p></li>
    <li><b>라우팅 순서</b><p>수신자의 라우팅 번호를 입력하거나 매핑합니다. 라우팅 번호는 수신자가 문서를 받고 서명하는 순서를 결정합니다.<p></li>
    </ul>
    </td>
    </tr>
  <tr> 
   <td role="rowheader">
     [!UICONTROL Allow Print and Sign]
   </td> 
   <td> <p>수신자가 문서를 인쇄하고 용지에 서명할 수 있도록 하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL 재할당 허용]
   </td> 
   <td> <p>수신자가 문서를 다른 사용자에게 재할당할 수 있도록 하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL 수신자 재귀 허용]
   </td> 
   <td> <p>수신자 재귀를 허용하려면 이 옵션을 활성화하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Authoritative copy]
   </td> 
   <td> <p>이 봉투 안에 있는 문서를 신뢰할 수 있는 복사본으로 표시하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL 자동 탐색]
   </td> 
   <td> <p>수신자에 대한 자동 탐색을 설정하려면 이 옵션을 활성화하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Brand ID]
   </td> 
   <td> <p>브랜드 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Markup Enabled]
   </td> 
   <td> <p>문서 마크업을 활성화하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL 만료 활성화됨]
   </td> 
   <td> <p>이 봉투 만료를 설정하려면 이 옵션을 활성화하십시오. 이 옵션을 활성화하면 다음 필드를 채웁니다.<ul><li><b>다음 시기 이후에 만료</b><p>이 봉투가 만료되는 일 수를 입력하거나 매핑합니다.</p></li><li><b>만료 경고</b><p>수신자에게 미리 알림 이메일을 보내는 만료 전 일 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Body]
   </td> 
   <td> <p>이 봉투와 함께 제공되는 이메일의 본문(콘텐츠)을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Subject]
   </td> 
   <td> <p>이 봉투와 함께 제공되는 전자 메일의 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 지정 API 호출]

이 작업 모듈을 사용하면 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL DocuSign] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 계정]</td> 
   <td>[!DNL DocuSign] API에 액세스하는 데 사용할 계정을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>상대 경로 입력 또는 매핑 <code>https://&lt;BASE_URI>/v2/accounts/&lt;ACCOUNT_ID>.</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 요청의 콘텐츠 유형을 결정합니다.</p> <p>For example,<code> {"Content-type":"application/json"}</code></p> <p>참고: 오류가 발생하여 원래 위치를 확인하기 어려운 경우 Workfront 설명서를 기반으로 헤더를 수정하는 것이 좋습니다. 사용자 지정 API 호출이 422 HTTP 요청 오류를 반환하는 경우 "Content-Type":"text/plain" 헤더를 사용해 보십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 제한]</td> 
   <td>한 실행 주기 동안 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**예:** 목록 봉투

다음 API 호출은 [!DNL DocuSign] 계정의 지정된 날짜에서 봉투를 반환합니다.

**URL**: `/v2.1/accounts/{accountId}/envelopes/`

**메서드**: `GET`

**쿼리 문자열**:

* **키**: `from_date`

* **값**: `YYYY-MM-DD`

요청에서 계정의 봉투 상태 변경 확인을 시작하는 시기를 지정합니다.

![Docusign 설정 예](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)

결과는 번들 > 본문 > 봉투에 있는 모듈의 출력에서 찾을 수 있습니다.

이 예에서는 6개의 봉투가 반환되었습니다.

![문서 출력 예](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

>[!ENDSHADEBOX]

#### [!UICONTROL 문서 다운로드]

이 작업 모듈은 단일 문서를 다운로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL DocuSign] 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정] </td> 
   <td> <p>다운로드할 문서가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 다운로드할 봉투 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 문서 ID]</p> </td> 
   <td> <p>다운로드하려는 문서의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 인증서]</td> 
   <td>다운로드에 봉투 서명 인증서를 포함하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자 ID별 [!UICONTROL 문서]</td> 
   <td>수신자가 사용자 ID로 문서를 검색할 수 있도록 하려면 이 옵션을 활성화합니다. 예를 들어 사용자가 서로 다른 가시성을 가진 두 개의 서로 다른 공정순서 주문에 포함된 경우 이 옵션을 사용하면 두 공정순서의 모든 문서가 반환됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>응답에서 반환된 PDF 바이트를 [!DNL DocuSign] 계정에 구성된 모든 키 관리자에 대해 암호화하려면 이 옵션을 사용합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>언어를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변경 사항 표시]</td> 
   <td>반환된 PDF의 변경된 모든 필드를 노란색으로 강조 표시하고 선택적 서명 또는 이니셜을 빨간색으로 윤곽선화하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 워터마크]</td> 
   <td> <p>워터마크 기능을 활성화하려면 이 옵션을 활성화합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 지정 필드 수정]

이 작업 모듈은 필드 이름을 사용하여 사용자 정의 필드를 수정합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL DocuSign] 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정] </td> 
   <td> <p>사용자 정의 필드를 수정할 문서가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 사용자 정의 필드를 수정할 문서가 포함된 봉투의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드 ID]</td> 
   <td>수정할 필드의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드 이름]</td> 
   <td>수정할 필드의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필수]</td> 
   <td>수정된 필드를 필수 필드로 설정하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드 표시]</td> 
   <td>필드를 표시하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 값]</td> 
   <td>수정된 필드의 값(내용)을 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 봉투 읽기]

이 작업 모듈은 봉투 ID를 사용하여 [!DNL DocuSign]에 있는 봉투 정보를 읽습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL DocuSign] 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정] </td> 
   <td> <p>정보를 읽을 문서가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 정보를 읽을 문서가 포함된 봉투의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>모듈의 출력에 표시할 속성을 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 봉투 보내기]

이 작업 모듈은 초안 봉투를 수신자에게 보냅니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL DocuSign] 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정] </td> 
   <td> <p>수신자에게 보낼 초안 봉투가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 수신자에게 보낼 초안 봉투의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 봉투(envelope)에 파일 업로드]

이 모듈은 지정된 파일을 DocuSign의 기존 봉투에 업로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL DocuSign] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL DocuSign] 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정] </td> 
   <td> <p>파일을 업로드할 봉투(envelope)가 포함된 계정을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 파일을 업로드할 봉투 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 파일]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>
