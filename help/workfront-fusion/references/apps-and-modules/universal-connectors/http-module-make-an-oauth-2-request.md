---
title: HTTP &gt; OAuth 2.0 요청 모듈 만들기
description: OAuth 2.0 인증이 필요한 서버에  [!DNL Adobe Workfront Fusion] HTTP(S) 요청을 하려면 먼저 OAuth 연결을 만들어야 합니다. [!DNL Adobe Workfront Fusion] 이 연결을 사용하여 만든 모든 호출에 적절한 인증 헤더가 있는지 확인하고 필요한 경우 관련 토큰을 자동으로 새로 고칩니다.
author: Becky
feature: Workfront Fusion
exl-id: a302a1d4-fddf-4a71-adda-6b87ff7dba4b
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1918'
ht-degree: 0%

---

# [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] 모듈

>[!NOTE]
>
>[!DNL Adobe Workfront Fusion]에는 [!DNL Adobe Workfront] 라이선스 외에 [!DNL Adobe Workfront Fusion] 라이선스가 필요합니다.

OAuth 2.0 인증이 필요한 서버에 [!DNL Adobe Workfront Fusion] HTTP(S) 요청을 하려면 먼저 OAuth 연결을 만들어야 합니다. [!DNL Adobe Workfront Fusion]은(는) 이 연결을 사용한 모든 호출에 적절한 인증 헤더가 있는지 확인하고 필요한 경우 관련 토큰을 자동으로 새로 고칩니다.

[!DNL Workfront Fusion]은(는) 다음 OAuth 2.0 인증 흐름을 지원합니다.

* 인증 코드 흐름
* 암시적 흐름

리소스 소유자 암호 자격 증명 흐름 및 클라이언트 자격 증명 흐름과 같은 다른 흐름은 이 모듈을 통해 자동으로 지원되지 않습니다.

OAuth 2.0 인증에 대한 자세한 내용은 [OAuth 2.0 권한 부여 프레임워크](https://tools.ietf.org/html/rfc6749)를 참조하십시오.

>[!NOTE]
>
>현재 전용 커넥터가 없는 Adobe 제품에 연결하는 경우 Adobe Authenticator 모듈을 사용하는 것이 좋습니다.
>
>자세한 내용은 [Adobe Authenticator 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)을 참조하세요.

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">  
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] 플랜*</td> 
   <td> <p>[!UICONTROL Pro] 이상</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재 라이선스 요구 사항: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합을 위한 [!UICONTROL [!DNL Workfront Fusion]] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>현재 제품 요구 사항: [!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Adobe Workfront] 플랜이 있는 경우 조직에서 이 문서에 설명된 기능을 사용하려면 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다. [!DNL Workfront Fusion]이(가) [!UICONTROL Ultimate] [!DNL Workfront] 계획에 포함되어 있습니다.</p>
   <p>또는</p>
   <p>레거시 제품 요구 사항: 이 문서에 설명된 기능을 사용하려면 조직에서 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

## [!DNL OAuth] 요청에 대한 연결을 만드는 중

* [HTTP > OAuth 2.0 요청 모듈 만들기에서 연결을 만드는 일반적인 지침](#general-instructions-for-creating-a-connection-in-the-http--make-an-oauth-20-request-module)
* [HTTP >[!UICONTROL Make] 및 OAuth 2.0 요청 모듈에서 Google에 대한 연결을 만들기 위한 지침](#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)
* [HTTP > OAuth 2.0 요청 모듈 만들기를 통해 Microsoft Graph API에 연결하기 위한 지침](#instructions-for-connecting-to-microsoft-graph-api-via-the-http--make-an-oauth-20-request-module)

### [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] 모듈에서 연결을 만들기 위한 일반적인 지침

1. [!DNL Adobe Workfront Fusion]과(와) 통신할 [!DNL target] 서비스에 OAuth 클라이언트를 만듭니다. 이 옵션은 지정된 서비스의 [!UICONTROL Developer] 섹션에서 찾을 수 있습니다.

   1. 클라이언트를 만들 때 `[!UICONTROL Redirect URL]` 또는 `[!UICONTROL Callback URL]` 필드에 적절한 URL을 입력하십시오.

      | 아메리카 / APAC | `https://app.workfrontfusion.com/oauth/cb/oauth2` |
      |---|---|
      | EMEA | `https://app-eu.workfrontfusion.com/oauth/cb/oauth2` |

   1. 클라이언트를 만든 후 해당 서비스에 `[!UICONTROL Client ID]` 및 `[!UICONTROL Client Secret]` 키 2개가 표시됩니다. 일부 서비스에서는 이러한 `[!UICONTROL App Key]` 및 `[!UICONTROL App Secret]`을(를) 호출합니다. Workfront Fusion에서 연결을 만들 때 키 및 암호를 제공할 수 있도록 안전한 위치에 저장합니다.

1. 제공된 서비스의 API 설명서에서 `[!UICONTROL Authorize URI]` 및 `[!UICONTROL Token URI]`을(를) 찾으십시오. [!DNL Workfront Fusion]이(가) [!DNL target] 서비스와 통신하는 URL 주소입니다. 주소는 OAuth 권한 부여에 사용됩니다.

   >[!NOTE]
   >
   >서비스에서 암시적 흐름을 사용하는 경우 `[!UICONTROL Authorize URI]`만 필요합니다.

   >[!INFO]
   >
   >**예:** Yahoo 주소:
   >
   >* URI 승인:
   >
   >`https://api.login.yahoo.com/oauth2/request_auth`
   >
   >* 토큰 URI:
   >
   >`https://api.login.yahoo.com/oauth2/get_token`

1. (조건부) 대상 서비스가 범위(액세스 권한)를 사용하는 경우, 서비스가 개별 범위를 분리하는 방법을 확인하고 고급 설정에서 구분 기호를 적절히 설정했는지 확인하십시오. 구분 기호가 올바르게 설정되지 않으면 [!DNL Workfront Fusion]에서 연결을 만들지 못하고 잘못된 범위 오류가 표시됩니다.
1. 위의 단계를 완료하면 [!DNL Workfront Fusion]에서 OAuth 연결을 만들 수 있습니다. OAuth 2.0 HTTP(S) 요청 및 응답 처리 모듈을 시나리오에 추가합니다.
1. 모듈의 연결 필드에서 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

1. 다음 필드를 입력하여 연결을 만듭니다.

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>토큰을 얻기 위한 플로우를 선택합니다.</p> 
       <ul> 
        <li><strong>[!UICONTROL Authorization Code]</strong>: 서비스의 API 설명서에서 <code>[!UICONTROL Authorize URI]</code> 및 <code>[!UICONTROL Token URI]</code>을(를) 입력합니다.</li> 
        <li><strong>[!UICONTROL Implicit]</strong>: 서비스의 API 설명서에서 <code>[!UICONTROL Authorize URI]</code>을(를) 입력합니다.</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>개별 범위를 추가합니다. 해당 서비스의 개발자(API) 설명서에서 이 정보를 찾을 수 있습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>위에 입력한 범위를 구분할 기준을 선택하십시오. 해당 서비스의 개발자(API) 설명서에서 이 정보를 찾을 수 있습니다.</p> <p>경고: 구분 기호가 올바르게 설정되지 않으면 [!DNL Workfront Fusion]에서 연결을 만들지 못하고 잘못된 범위 오류가 표시됩니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>클라이언트 ID를 입력합니다. 연결할 서비스에서 OAuth 클라이언트를 만들 때 클라이언트 ID를 얻었습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p> 클라이언트 암호를 입력합니다. 연결할 서비스에서 OAuth 클라이언트를 만들 때 클라이언트 암호를 받았습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>인증 호출에 포함할 매개 변수를 추가합니다. 다음 표준 매개 변수는 항상 자동으로 포함되며 추가할 필요가 없습니다.</p> <p>표준 매개 변수:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL response_type]</strong> </p> <p> <code>code </code>대상: [!UICONTROL Authorization Code flow] 및 <code>token </code> [!UICONTROL Implicit flow]</p> </li> 
        <li> <p><strong>[!UICONTROL redirect_uri]</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">아메리카 / APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong> </p> <p> 계정을 만들 때 받은 클라이언트 ID</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Access token parameters]</p> </td> 
      <td> <p>토큰 호출에 포함할 매개 변수를 추가합니다. 다음 표준 매개 변수는 항상 자동으로 포함되며 추가할 필요가 없습니다.</p> <p>표준 매개 변수:</p> 
       <ul> 
        <li><strong>[!UICONTROL grant_type]</strong>: <code>authorization_code</code></li> 
        <li> <p><strong>[!UICONTROL redirect_uri]:</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">아메리카 / APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li><strong>[!UICONTROL client_id]</strong>: 계정을 만들 때 받은 클라이언트 ID가 요청 본문에 자동으로 포함됩니다</li> 
        <li><strong>client_secret</strong>: 계정을 만들 때 받은 클라이언트 암호가 요청 본문에 자동으로 포함됩니다</li> 
        <li><strong>code</strong>: 인증 요청에서 반환된 코드입니다.</li> 
       </ul> <p>참고:  <p>OAuth 2.0 표준은 이 단계(<code>[!UICONTROL client_secret_basic]</code> 및 <code>[!UICONTROL client_secret_post]</code>) 동안 최소 두 가지 이상의 클라이언트 인증 방법을 지원합니다. [!DNL Workfront Fusion]은(는) <code>[!UICONTROL client_secret_post]</code> 메서드를 통해 지정된 클라이언트 ID와 암호를 자동으로 보냅니다. 따라서 이러한 매개 변수는 토큰 요청 본문의 일부로 자동으로 포함됩니다. </p> <p>OAuth 2.0 인증에 대한 자세한 내용은 <a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0 권한 부여 프레임워크</a>를 참조하십시오.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Refresh token parameters]</p> </td> 
      <td> <p>토큰 호출에 포함할 매개 변수를 추가합니다. 다음 표준 매개 변수는 항상 자동으로 포함되며 추가할 필요가 없습니다.</p> <p>표준 매개 변수:</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL grant_type]</strong>: <code>refresh_token</code></p> </li> 
        <li> <p><strong>[!UICONTROL refresh_token]</strong>: 연결 중인 서비스에서 얻은 가장 최근 새로 고침 토큰</p> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong>: 계정을 만들 때 받은 클라이언트 ID가 요청 본문에 자동으로 포함됩니다</p> </li> 
        <li> <p><strong>[!UICONTROL client_secret]</strong>: 계정을 만들 때 받은 클라이언트 암호가 요청 본문에 자동으로 포함됩니다</p> </li> 
       </ul> <p>참고:  <p>OAuth 2.0 표준은 이 단계(<code>[!UICONTROL client_secret_basic]</code> 및 <code>[!UICONTROL client_secret_post]</code>) 동안 최소 두 가지 이상의 클라이언트 인증 방법을 지원합니다. [!DNL Workfront Fusion]은(는) <code>[!UICONTROL client_secret_post]</code> 메서드를 통해 지정된 클라이언트 ID와 암호를 자동으로 보냅니다. 따라서 이러한 매개 변수는 토큰 요청 본문의 일부로 자동으로 포함됩니다. </p> <p>OAuth 2.0 인증에 대한 자세한 내용은 <a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0 권한 부여 프레임워크</a>를 참조하십시오.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Custom Headers]</p> </td> 
      <td> <p>[!UICONTROL Token] 및 R[!UICONTROL efresh Token] 단계의 헤더에 포함할 추가 키 및 값을 지정하십시오.</p> <p>참고:  <p>OAuth 2.0 표준은 이 단계(<code>[!UICONTROL client_secret_basic]</code> 및 <code>[!UICONTROL client_secret_post]</code>) 동안 최소 두 가지 이상의 클라이언트 인증 방법을 지원합니다. [!DNL Workfront Fusion]은(는) <code>[!UICONTROL client_secret_basic]</code> 메서드를 자동으로 지원하지 않습니다. 연결하는 서비스에서 클라이언트 ID와 클라이언트 암호가 단일 문자열로 결합된 다음 base64가 인증 헤더에 인코딩되어야 하는 경우 해당 헤더와 키 값을 여기에 추가해야 합니다.</p> <p> OAuth 2.0 인증에 대한 자세한 내용은 <a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0 권한 부여 프레임워크</a>를 참조하십시오.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Token placement]</p> </td> 
      <td> <p>지정된 URL에 연결할 때 토큰을 [!UICONTROL header], [!UICONTROL query string] 또는 둘 다에 전송할지 여부를 선택합니다.</p> <p>토큰은 요청 헤더에서 가장 일반적으로 전송됩니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Header token name] </td> 
      <td> <p>헤더에 인증 토큰의 이름을 입력합니다. 기본값: <code>[!UICONTROL Bearer]</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Query string parameter name] </td> 
      <td> <p>쿼리 문자열에 인증 토큰의 이름을 입력합니다. 기본값: <code>[!UICONTROL access_token]</code>.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 연결 설정을 저장하려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.
1. [OAuth 2.0 요청 모듈 설정](#oauth-20-request-module-setup)을 계속합니다.

### [!UICONTROL HTTP] >[!UICONTROL Make an OAuth 2.0 request module]에서 [!DNL Google]에 대한 연결을 만드는 방법

다음 예제에서는 [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0] 요청 모듈을 사용하여 [!DNL Google]에 연결하는 방법을 보여 줍니다.

1. [Connect [!DNL Adobe Workfront Fusion] to [!DNL Google Services] 사용자 지정 OAuth 클라이언트 사용](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)에 설명된 대로 프로젝트를 만들고, OAuth 설정을 구성하고, 자격 증명을 생성했는지 확인하십시오.
1. [!UICONTROL HTTP] >[!UICONTROL Make an OAuth 2.0 request] 모듈을 엽니다.
1. 연결 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 다음 값을 입력합니다.

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>[!UICONTROL Authorization Code]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Authorize URI]</td> 
      <td><code>https://accounts.google.com/o/oauth2/v2/auth</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Token URI]</td> 
      <td><code>https://www.googleapis.com/oauth2/v4/token</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>개별 범위를 추가합니다. 범위에 대한 자세한 내용은 [!DNL Google] 설명서의 [!DNL Google] API</a>에 대한 <a href="https://developers.google.com/identity/protocols/oauth2/scopes">OAuth 2.O 범위를 참조하십시오.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>[!UICONTROL SPACE]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>[!DNL Google] 클라이언트 ID를 입력하십시오. </p> <p>클라이언트 ID를 만들려면 사용자 지정 OAuth 클라이언트를 사용하여 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md" class="MCXref xref">[!DNL Connect Adobe Workfront Fusion]에서 [!DNL Google Services]에 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create2" class="MCXref xref">OAuth 자격 증명 만들기</a>를 참조하십시오</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p>[!DNL Google] 클라이언트 암호를 입력하십시오. </p> <p>클라이언트 암호를 만들려면 사용자 지정 OAuth 클라이언트를 사용하여 [!DNL Google] 서비스에 대해 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md" class="MCXref xref">[!DNL Connect Adobe Workfront Fusion]에서 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create2" class="MCXref xref">OAuth 자격 증명 만들기</a>를 참조하십시오</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p><code>[!UICONTROL access_type]</code> - <code>[!UICONTROL offline] </code>키-값 쌍을 추가합니다.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-authentication-http.png"> </p> <p>참고: 토큰 새로 고침 등의 인증 문제가 발생하면 <code>[!UICONTROL prompt] </code>- <code>[!UICONTROL consent] </code>키-값 쌍을 추가해 보십시오.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 연결 설정을 저장하려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.
1. [OAuth 2.0 요청 모듈 설정](#oauth-20-request-module-setup)을 계속합니다.

<!--### Instructions for connecting to [!DNL Microsoft Graph API] via the [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module 

For instructions regarding [!DNL Microsoft Graph API], see [Call the [!DNL MS Graph REST API] via the [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).-->

## OAuth 2.0 요청 모듈 설정

[요청에 대한 연결 만들기 [!DNL OAuth] 요청](#creating-a-connection-for-an-oauth-request)에 설명된 대로 [!DNL Oauth 2].0 연결을 설정했으면 원하는 대로 모듈을 계속 설정합니다. 모든 인증 토큰은 이 요청 및 동일한 연결을 사용하는 다른 모든 요청에 자동으로 포함됩니다.

[!UICONTROL HTTP] >[!UICONTROL Make an OAuth 2.0 request] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보를 매핑 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

<!--
<img src="" style="width: 350;height: 74;">
-->

<table style="table-layout:auto">  
 <col> 
 <col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>연결 설정에 대한 자세한 내용은 이 문서에서 <a href="#creating-a-connection-for-an-oauth-request" class="MCXref xref">OAuth 요청에 대한 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx]) </td> 
   <td> <p>이 옵션을 사용하여 오류 처리를 설정합니다.</p> <p>자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">오류 처리를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>API 끝점, 웹 사이트 등과 같이 요청을 보낼 URL을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. For example, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> 원하는 쿼리 키-값 쌍을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>HTTP Body는 사용할 데이터 바이트가 있는 경우 헤더 바로 다음에 오는 HTTP 트랜잭션 메시지로 전송됩니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>원시 본문 유형은 일반적으로 개발자 설명서에서 전송할 데이터를 지정하지 않는 경우에도 대부분의 HTTP 본문 요청에 적합합니다.</p> <p>[!UICONTROL Content type] 필드의 데이터를 구문 분석하는 형식을 지정하십시오.</p> <p>선택한 콘텐츠 유형에도 불구하고 데이터는 개발자 설명서에서 규정하거나 요구하는 모든 형식으로 입력됩니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>이 본문 형식은 <code>[!UICONTROL application/x-www-form-urlencoded]</code>을(를) 사용하여 데이터를 POST 하는 것입니다.</p> <p><code>[!UICONTROL application/x-www-form-urlencoded]</code>의 경우 서버로 전송된 HTTP 메시지의 본문은 기본적으로 하나의 쿼리 문자열입니다. 키와 값은 키와 값 사이에 <code>=</code>이(가) 있고 <code>&amp;</code>(으)로 구분된 키-값 쌍으로 인코딩됩니다. </p> <p>이진 데이터의 경우 대신 <code>use [!UICONTROL multipart/form-data]</code>을(를) 사용합니다.</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>예: </b></span></span> 
       <p>결과 HTTP 요청 형식의 예:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data]은(는) 파일 및 데이터를 보내는 데 사용되는 HTTP 다중 파트 요청입니다. 일반적으로 서버에 파일을 업로드하는 데 사용됩니다.</p> <p>요청에 전송할 필드를 추가합니다. 각 필드에는 키-값 쌍이 포함되어야 합니다.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>요청 본문 내에 보낼 키와 값을 입력합니다.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>키를 입력하고 요청 본문에 보낼 소스 파일을 지정합니다.</p> <p>이전 모듈에서 업로드할 파일을 매핑하거나([!UICONTROL HTTP] &gt;[!UICONTROL Get a File] 또는 [!UICONTROL Google Drive] &gt;[!UICONTROL Download a File)]) 파일 이름과 파일 데이터를 수동으로 입력합니다.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>[!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] 또는 [!UICONTROL XML] &gt; [!UICONTROL Parse XML] 모듈을 사용할 필요가 없도록 응답을 자동으로 구문 분석하고 JSON 및 XML 응답을 변환하려면 이 옵션을 활성화하십시오.</p> <p>구문 분석된 JSON 또는 XML 컨텐츠를 사용하기 전에 모듈에서 응답 컨텐츠를 인식하고 이를 후속 모듈에 매핑할 수 있도록 모듈을 한 번 수동으로 실행하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>요청 시간 제한(초)을 입력합니다(1-300). 기본값은 40초입니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> 이 옵션을 활성화하면 시나리오의 모든 HTTP 모듈과 서버의 쿠키를 공유할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p> 자체 서명된 인증서를 사용하여 TLS를 사용하려면 인증서를 업로드하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>확인되지 않은 TLS 인증서를 사용하는 연결을 거부하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> 3xx 응답이 있는 URL 리디렉션을 따르려면 이 옵션을 활성화하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>모든 응답 코드와 함께 URL 리디렉션을 따르려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>기본적으로 [!DNL Workfront Fusion]은(는) 배열과 동일한 URL 쿼리 문자열 매개 변수 키에 대해 여러 값을 처리합니다. 예를 들어 <code>www.test.com?foo=bar&amp;foo=baz</code>은(는) <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>(으)로 변환됩니다. 이 기능을 비활성화하려면 이 옵션을 활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> 웹 사이트의 압축된 버전을 요청하려면 이 옵션을 활성화하십시오.</p> <p>압축된 콘텐츠를 요청하기 위해 <code>[!UICONTROL Accept-Encoding]</code> 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>HTTP 요청에서 상호 TLS를 사용하려면 이 옵션을 활성화하십시오.</p> <p>상호 TLS에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">HTTP 모듈에서 상호 TLS 사용([!DNL Adobe Workfront Fusion]</a>)을 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>
