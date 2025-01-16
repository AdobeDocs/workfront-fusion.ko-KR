---
title: 사용자 지정 OAuth 클라이언트를 사용하여 Adobe Workfront Fusion을 Google 서비스에 연결
description: Adobe Workfront Fusion을 사용하여 사용자 지정 OAuth 클라이언트를 사용하여 Google 서비스에 연결할 수 있습니다. 이 절차에는 기존 Google 계정이 필요합니다.
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
source-git-commit: 362952ec85b0df2306ba117ba530e95201330cca
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 1%

---

# 사용자 지정 OAuth 클라이언트를 사용하여 Adobe Workfront Fusion을 Google 서비스에 연결

Adobe Workfront Fusion을 사용하여 사용자 지정 OAuth 클라이언트를 사용하여 Google 서비스에 연결할 수 있습니다. 이 절차에는 기존 Google 계정이 필요합니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지 
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
   <p>신규:</p> <ul><li>또는 Prime Workfront 플랜 선택: 귀사는 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 플랜: Workfront Fusion이 포함됩니다.</li></ul>
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

이 연결을 만들려면 기존 Google 계정이 필요합니다.

## 사용자 지정 OAuth 클라이언트를 사용하여 Fusion을 Google 서비스에 연결

이 연결을 만들려면 Google Cloud 플랫폼에서 프로젝트를 만들고 구성한 다음 해당 프로젝트를 기반으로 Fusion에서 연결을 구성해야 합니다.

>[!NOTE]
>
>이 절차는 다음 용도로 사용됩니다.
>
>* 개인 사용(`@gmail.com` 및 `@googlemail.com`명의 사용자)
>* 내부 사용(사용자 정의 OAuth 클라이언트를 사용하는 Google Workspace 사용자)

* [Google Cloud Platform에서 프로젝트 만들기](#create-a-project-on-google-cloud-platform)
* [OAuth 동의 설정 구성](#configure-oauth-consent-settings)
* [OAuth 자격 증명 만들기](#create-oauth-credentials)
* [Workfront Fusion에서 Google에 연결](#connect-to-google-in-workfront-fusion)

### Google Cloud Platform에서 프로젝트 만들기

Google Cloud Platform에서 프로젝트를 생성하려면:

1. Google Cloud Platform에서 프로젝트 만들기를 시작합니다.

   지침은 Google 설명서에서 [Google Cloud 프로젝트 만들기](https://developers.google.com/workspace/guides/create-project)를 참조하십시오.
1. API를 활성화할 때, Google Drive API와 사용하려는 모든 Google 앱의 API(예: Google Sheets API)를 활성화해야 합니다.
1. 프로젝트 작성을 완료합니다.
1. 이 문서의 [OAuth 동의 설정 구성](#configure-oauth-consent-settings) 섹션을 계속합니다.

### OAuth 동의 설정 구성

1. 프로젝트에 대한 OAuth 구성 시작

   지침은 Google 설명서에서 [OAuth 동의 화면 구성 및 범위 선택](https://developers.google.com/workspace/guides/configure-oauth-consent)을 참조하십시오.
1. **외부**&#x200B;를 선택한 다음 **만들기**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >이 옵션을 선택하면 요금이 부과되지 않습니다. 자세한 내용은 확인 요구 사항 예외 항목에 대한 Google 정보를 참조하십시오.

1. 다음과 같이 필수 필드를 채웁니다.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>앱 이름</p> </td> 
      <td> <p>동의를 요청하는 앱의 이름을 입력합니다.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>Adobe Workfront Fusion </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">사용자 지원 이메일</td> 
      <td>사용자가 이 앱에 연결할 때 동의에 대한 질문이 있는 경우 연락할 수 있는 이메일 주소를 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">이메일 주소</td> 
      <td>Google에서 프로젝트 변경 사항에 대해 알리는 데 사용할 수 있는 이메일 주소를 하나 이상 입력합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 인증된 도메인에서 **도메인 추가**&#x200B;를 클릭하고 `workfrontfusion.com`을(를) 입력합니다.
1. 다음 범위를 추가합니다.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>서비스/API</th> 
      <th>필수 범위</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google 드라이브</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   목록을 확장하거나 목록의 다음 페이지로 이동하여 모두 표시해야 할 수 있습니다.

1. (선택 사항) 프로젝트에 테스트 사용자를 추가합니다.
1. 정보가 정확한지 검사한 다음 **대시보드로 돌아가기**&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >Google에서 본인 동의 화면과 본인 확인 신청서를 제출하지 않아도 됩니다.

1. [OAuth 자격 증명 만들기](#create-oauth-credentials)를 계속합니다.

### OAuth 자격 증명 만들기

1. OAuth 클라이언트 ID 자격 증명 만들기를 시작합니다.

   자세한 내용은 Google 설명서에서 [액세스 자격 증명 만들기](https://developers.google.com/workspace/guides/create-credentials)를 참조하십시오.

   >[!NOTE]
   >
   >활성화한 첫 번째 API 또는 서비스(Gmail 또는 Google 드라이브)가 아닌 경우 새 자격 증명을 만들 필요가 없습니다.

1. 다음과 같이 필수 필드를 채웁니다.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">애플리케이션 유형</td> 
      <td> <p> 웹 애플리케이션</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">이름</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. 승인된 리디렉션 URI에서 다음 중 **one**&#x200B;을(를) 입력하십시오.

   * Gmail 또는 Google 드라이브의 경우: `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * 다른 Google 앱의 경우: `https://app.workfrontfusion.com/oauth/cb/google`

1. Click **Create**.

   클라이언트 ID 및 클라이언트 암호가 표시됩니다.

1. 클라이언트 ID 및 클라이언트 암호를 안전한 위치에 복사합니다. 이 플러그인을 사용하여 Workfront Fusion에서 연결을 만듭니다.
1. [Workfront Fusion에서 Google에 연결](#connect-to-google-in-workfront-fusion)을 계속합니다.

### Workfront Fusion에서 Google에 연결

Google에 대한 연결 만들기 프로세스는 Google 서비스(예: Google Sheets 또는 Google Docs)에서 모듈을 사용하는지 또는 HTTP >OAuth2.0 요청 모듈 만들기를 통해 Google에 연결하는 경우에 따라 다릅니다.

* [Google 서비스에서 Google에 연결](#connect-to-google-in-a-google-service)
* [HTTP에서 Google에 연결 > OAuth2.0 요청 모듈 만들기](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### Google 서비스에서 Google에 연결

1. Workfront Fusion에서 연결을 만들어야 하는 Google 모듈을 찾습니다.
1. **연결 만들기**&#x200B;를 클릭한 다음 **고급 설정 표시**&#x200B;를 클릭합니다.
1. 해당하는 경우 연결 이름, 환경 및 유형 필드를 입력합니다.
1. 각 필드에 [OAuth 자격 증명 만들기](#create-oauth-credentials)에서 검색한 클라이언트 ID와 클라이언트 암호를 입력한 다음 **계속**&#x200B;을 클릭합니다.

1. Google 계정으로 로그인

   **이 앱이 확인되지 않음** 창이 표시됩니다. 창 제목에 언급된 &quot;앱&quot;은 위에서 만든 OAuth 클라이언트입니다.

1. 사용자 지정 OAuth 클라이언트를 사용한 액세스를 허용하려면 **고급**&#x200B;을 클릭한 다음 **Workfront Fusion(안전하지 않은)으로 이동**&#x200B;을 클릭하십시오.

1. Workfront Fusion 권한을 부여하려면 **허용**&#x200B;을 클릭하세요.
1. 표시되는 창에서 **허용**&#x200B;을 다시 클릭하여 선택 항목을 확인합니다.

   사용자 지정 OAuth 클라이언트를 사용하여 원하는 Google 서비스에 대한 연결이 설정됩니다.

#### HTTP에서 Google에 연결 > OAuth2.0 요청 모듈 만들기 {#connect-to-google-in-the-http--make-an-oauth20-request-module}

HTTP > OAuth2.0 요청 모듈 만들기에서 Google에 연결하는 방법에 대한 지침은 HTTP > OAuth 2.0 요청 모듈 만들기에서 [HTTP에서 Google 연결 만들기 > OAuth 2.0 요청 모듈 만들기](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)를 참조하십시오.

## 가능한 오류 메시지:[403 액세스가 구성되지 않음]

`403 Access Not Configured` 오류 메시지가 표시되면 Google Cloud Platform에서 해당 API를 활성화해야 합니다. API를 사용하려면 이 문서의 [Google Cloud Platform에서 프로젝트 만들기](#create-a-project-on-google-cloud-platform) 섹션에 있는 단계를 따르십시오.
