---
title: MS Graph REST API 호출
description: Adobe Workfront Fusion HTTP 및> OAuth 2.0 요청 모듈 만들기 를 통해 MS Graph REST API를 호출합니다.
author: Becky
feature: Workfront Fusion
exl-id: f411c807-955d-44fe-98b1-3ebba3fe0861
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 2%

---

# MS Graph REST API 호출

많은 Microsoft 웹 서비스는 Microsoft Graph API를 통해 액세스됩니다. Workfront Fusion HTTP > OAuth 2.0 요청 모듈 만들기를 사용하여 Microsoft Graph API에 대한 연결을 만들 수 있습니다.

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
   <p>현재: Workfront Fusion 라이선스 요구 사항 없음</p>
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

## Microsoft 애플리케이션 등록 포털에서 Workfront Fusion 등록

Microsoft Graph REST API에 대한 연결을 만들려면 먼저 Adobe Workfront Fusion을 등록해야 합니다.

1. Microsoft 설명서의 [Microsoft ID 플랫폼에 응용 프로그램 등록](https://docs.microsoft.com/en-us/graph/auth-register-app-v2)에 설명된 대로 새 응용 프로그램 등록을 시작합니다.

   등록의 일부로 Microsoft에는 다음 정보가 필요합니다.

   <table style="table-layout:auto">
      <tr>
        <td>애플리케이션 이름</td>
        <td>"내 Workfront Fusion 애플리케이션"과 같은 애플리케이션 이름을 입력합니다.</td>
      </tr>
      <tr>
        <td>리디렉션 URL</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. 앱 등록을 완료하면 애플리케이션 ID를 기록해 둡니다.

   >[!IMPORTANT]
   >
   >Workfront Fusion에서 연결을 설정하려면 애플리케이션 ID가 필요합니다.

1. 클라이언트 암호를 생성합니다. 이 비밀을 메모해 두십시오.

   자세한 내용은 Microsoft 설명서의 [Microsoft ID 플랫폼에 응용 프로그램 등록](https://docs.microsoft.com/en-us/graph/auth-register-app-v2)을 참조하십시오.

   >[!IMPORTANT]
   >
   >Workfront Fusion에서 연결을 설정하려면 클라이언트 암호가 필요합니다.

1. 애플리케이션에 대한 권한을 구성합니다.

   이러한 필드를 찾고 구성하는 방법에 대한 자세한 내용은 Microsoft 설명서의 [사용자 없이 액세스 받기](https://docs.microsoft.com/en-us/graph/auth-v2-service)에서 &quot;Microsoft 그래프에 대한 권한 구성&quot; 섹션을 참조하십시오.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">애플리케이션에 필요한 권한 유형은 무엇입니까?</td> 
      <td><code>Delegated permissions</code>을(를) 선택합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">권한 선택</td> 
      <td> <p>다음 권한을 선택합니다.</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>통합에 필요한 다른 모든 권한(예: <code>User.Read</code>)</p> </li> 
       </ul> <p><b>중요</b>: Workfront Fusion에서 연결을 설정하려면 선택한 권한이 필요합니다.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 계속해서 [Workfront Fusion에서 MS Graph API 연결을 구성](#configure-your-ms-graph-api-connection-in-workfront-fusion)합니다.

## Workfront Fusion에서 MS Graph API 연결 구성

[Workfront 애플리케이션 등록 포털에 Workfront Fusion 등록](#register-workfront-fusion-in-the-microsoft-application-registration-portal)에서 설명한 대로 Microsoft Fusion을 등록한 후 HTTP > Make an Oauth 2.0 request module에서 연결을 구성할 수 있습니다.

1. HTTP > OAuth 2.0 호출 모듈 만들기 를 시나리오에 추가합니다.
1. 연결 필드 옆의 **추가**&#x200B;를 클릭합니다.
1. 연결 필드를 다음과 같이 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">연결 이름</td> 
      <td>연결의 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">환경</p> </td> 
      <td>프로덕션 계정에 연결할지 아니면 비프로덕션 계정에 연결할지 선택합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">유형</p> </td> 
      <td>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">플로우 유형</p> </td> 
      <td><code>Authorization Code</code>을(를) 선택합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">URI 승인</td> 
      <td><code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code> 입력. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">토큰 URI</td> 
      <td><code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code> 입력. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">범위</td> 
      <td> <p>등록할 때 선택한 권한을 입력하십시오(예: <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Microsoft Application Registration Portal에서 Workfront Fusion 등록</a>).</p> <p>각 범위에 대해 <b>추가</b>를 클릭하고 권한을 입력하십시오.</p> <p>예: <code>offline_access</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">범위 구분 기호</td> 
      <td><code>SPACE</code>을(를) 선택합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">클라이언트 ID</td> 
      <td><a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Microsoft 응용 프로그램 등록 포털에서 Workfront Fusion 등록</a>의 2단계에서 응용 프로그램 ID를 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">클라이언트 암호</td> 
      <td><a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Microsoft 응용 프로그램 등록 포털에서 Workfront Fusion 등록</a>의 3단계에서 생성한 클라이언트 암호를 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">매개 변수 승인</td> 
      <td> <p>다음 승인 매개 변수를 추가합니다. 추가할 각 매개 변수에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오. </p> 
       <ul> 
        <li> <p>키:<code> response_mode</code> 값: <code>query</code></p> </li> 
        <li> <p>키: <code>prompt </code>값: <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">토큰 매개 변수 액세스</td> 
      <td>이 필드에는 아무 것도 입력할 필요가 없습니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">토큰 매개 변수 새로 고침</td> 
      <td> 
       <ol> 
        <li value="1"> <p><b>항목 추가</b>를 클릭합니다.</p> </li> 
        <li value="2"> <p><b>키</b> 필드에 <code>scope</code>을(를) 입력합니다.</p> </li> 
        <li value="3"> <p><b>값</b> 필드에 범위 필드에 입력한 모든 범위를 공백으로 구분하여 입력합니다.</p> <p>예: <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">사용자 지정 헤더</td> 
      <td>이 필드에는 아무 것도 입력할 필요가 없습니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">토큰 배치</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. **계속**&#x200B;을 클릭합니다.
1. 표시되는 창에서 **수락**&#x200B;을 클릭하여 연결을 완료하고 모듈로 돌아갑니다.
