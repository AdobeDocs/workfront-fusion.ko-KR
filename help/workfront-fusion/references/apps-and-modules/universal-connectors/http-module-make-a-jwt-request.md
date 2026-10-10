---
title: HTTP > JWT 요청 모듈 만들기
description: Adobe Workfront Fusion HTTP > JWT 요청 만들기 모듈은 URL에 HTTP(S) 요청을 보내고 Fusion이 자동으로 서명하는 JSON 웹 토큰으로 승인합니다.
author: Becky
feature: Workfront Fusion
exl-id: 2f8c0b0d-085a-4b49-b350-4fd4cca1d0a7
TQID: 'https://experienceleague.adobe.com/ko'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 5e6403abee4e5767da9134529b9e88070bad5f44
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 11%
---
# [!UICONTROL HTTP] > [!UICONTROL JWT 요청 만들기] 모듈

Adobe Workfront Fusion [!UICONTROL HTTP] > [!UICONTROL JWT 요청 만들기] 모듈은 URL에 HTTP(S) 요청을 보내고 모든 호출 시 모듈이 서명하는 JSON 웹 토큰(JWT)을 사용하여 이를 승인합니다. 그런 다음 표준 [!UICONTROL HTTP] > [!UICONTROL 요청 만들기] 모듈과 같은 방식으로 응답이 처리됩니다.

이 모듈은 표준 [!UICONTROL 요청 만들기] 모듈처럼 동작하며, 한 가지 주요 차이점은 사용자가 제공한 클레임에서 JWT에 자동으로 서명하고 요청에 기본적으로 `Authorization: Bearer <token>`으로 추가하는 것입니다.

이 모듈을 사용하여 서명된 JWT가 인증에 필요한 모든 API(예: 별도의 단계에서 토큰을 만들지 않고, HMAC(공유 암호) 또는 RSA/ECDSA(개인 키)로 서명된 단기 전달자 토큰이 필요한 서비스)를 호출합니다.

API에서 OAuth 2.0, 기본 인증, API 키 또는 클라이언트 인증서를 사용하는 경우 일치하는 전용 HTTP 모듈을 대신 사용하십시오.

>[!NOTE]
>
>현재 전용 커넥터가 없는 Adobe 제품에 연결하는 경우 Adobe Authenticator 모듈을 사용하는 것이 좋습니다.
>
>자세한 내용은 [Adobe Authenticator 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)을 참조하세요.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## JWT 연결 만들기

모듈에는 JWT 연결이 필요합니다. 비밀 또는 개인 키가 시나리오에 표시되지 않아도 되도록 연결이 서명 자료를 저장합니다.

### Fusion에서 JWT 연결 만들기

1. 시나리오에 [!UICONTROL HTTP] > [!UICONTROL JWT 요청 만들기] 모듈을 추가합니다.
1. **[!UICONTROL 연결]** 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 연결 필드를 구성합니다.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader"><p>연결 이름</p></td>
      <td><p>연결의 이름을 입력합니다.</p></td>
     </tr>
     <tr>
      <td role="rowheader"><p>알고리즘</p></td>
      <td>
       <p>연결에 대한 서명 알고리즘을 선택합니다.</p>
       <ul>
        <li><code>HS256</code></li>
        <li><code>HS384</code></li>
        <li><code>HS512</code></li>
        <li><code>RS256</code></li>
        <li><code>RS384</code></li>
        <li><code>RS512</code></li>
        <li><code>PS256</code></li>
        <li><code>PS384</code></li>
        <li><code>PS512</code></li>
        <li><code>ES256</code></li>
        <li><code>ES384</code></li>
        <li><code>ES512</code></li>
       </ul>
      </td>
     </tr>
     <tr>
      <td role="rowheader"><p>Secret</p></td>
      <td>
       <p>서명 키를 입력합니다.</p>
       <ul>
        <li><code>HS*</code> 알고리즘의 경우 공유 암호 문자열을 사용하십시오.</li>
        <li><code>RS*</code>, <code>PS*</code> 및 <code>ES*</code> 알고리즘의 경우 PEM으로 인코딩된 개인 키를 사용하십시오.</li>
       </ul>
      </td>
     </tr>
    </tbody>
   </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

>[!IMPORTANT]
>
>JWT 연결은 하나의 알고리즘으로만 서명합니다. 시나리오에 둘 이상의 서명 알고리즘이 필요한 경우 각 알고리즘에 대해 별도의 연결을 만듭니다. 이는 기존의 독립형 JWT 앱 동작과 일치합니다.

## [!UICONTROL HTTP] > [!UICONTROL JWT 요청 만들기] 모듈과 해당 필드

[!UICONTROL HTTP] > [!UICONTROL JWT 요청 만들기] 모듈을 구성할 때 Adobe Workfront Fusion은 아래 나열된 필드를 모듈 UI에 표시되는 순서와 동일한 순서로 표시합니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다. 고급으로 표시된 필드는 **[!UICONTROL 고급 설정 표시]**&#x200B;를 선택하지 않으면 숨겨집니다.

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 연결]</p></td>
   <td><p>기존 JWT 연결을 선택하거나 새 연결을 만듭니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL URL]</p></td>
   <td><p>요청에 대한 대상 URL입니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 메서드]</p></td>
   <td><p>GET, POST, PUT, PATCH 또는 DELETE과 같은 HTTP 메서드입니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 헤더]</p></td>
   <td><p>키/값 형식의 사용자 지정 요청 헤더입니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 쿼리 문자열]</p></td>
   <td><p>키/값 형식의 쿼리-문자열 매개 변수.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Body type]</p></td>
   <td><p>요청 본문을 인코딩하는 방법입니다. 옵션에는 Raw, application/x-www-form-urlencoded 및 multipart/form-data가 포함됩니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 구문 분석 응답]</p></td>
   <td><p>활성화된 경우 Fusion은 응답 콘텐츠 유형을 기반으로 응답 본문을 구문 분석합니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL JWT 페이로드(클레임)]</p></td>
   <td><p>JWT 페이로드에 클레임으로 포함된 키/값 쌍입니다. 예약된 클레임 <code>exp</code>, <code>iat</code> 및 <code>nbf</code>은(는) Unix Epoch 이후 초 단위의 NumericDate여야 합니다. 클레임 값은 JSON 유형을 유지하므로 숫자는 숫자를 유지하고 부울은 부울을 유지합니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 시간 초과] (고급)</p></td>
   <td><p>요청 시간 제한(초)을 지정합니다(1-300). 기본값은 40초입니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 재시도 횟수] (고급)</p></td>
   <td><p>재시도 가능한 오류로 인해 요청이 실패할 경우 요청을 재시도해야 하는 횟수를 지정합니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 추가 재시도 상태 코드] (고급)</p></td>
   <td><p>다시 시도 가능한 것으로 처리되어야 하는 추가 HTTP 상태 코드를 지정합니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 다른 HTTP 모듈과 쿠키 공유] (고급)</p></td>
   <td><p>이 옵션을 활성화하면 시나리오의 모든 HTTP 모듈과 서버의 쿠키를 공유할 수 있습니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 자체 서명된 인증서] (고급)</p></td>
   <td><p>자체 서명된 인증서를 사용하여 TLS를 사용하려면 인증서를 업로드하십시오.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 확인되지 않은(자체 서명된) 인증서를 사용하는 연결을 거부합니다.] (고급)</p></td>
   <td><p>확인되지 않은 TLS 인증서를 사용하는 연결을 거부하려면 이 옵션을 활성화합니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Follow redirect] (고급)</p></td>
   <td><p>3xx 응답이 있는 URL 리디렉션을 따르려면 이 옵션을 활성화하십시오.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 배열과 동일한 쿼리 문자열 키를 여러 개 직렬화할 수 없음] (고급)</p></td>
   <td><p>기본적으로 Workfront Fusion은 배열과 동일한 URL 쿼리 문자열 매개 변수 키에 대해 여러 값을 처리합니다. 예를 들어 <code>www.test.com?foo=bar&amp;foo=baz</code>은(는) <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>(으)로 변환됩니다. 이 기능을 비활성화하려면 이 옵션을 활성화합니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Request compressed content] (고급)</p></td>
   <td><p>웹 사이트의 압축된 버전을 요청하려면 이 옵션을 활성화하십시오. 압축된 콘텐츠를 요청하기 위해 <code>[!UICONTROL Accept-Encoding]</code> 헤더를 추가합니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Use Mutual TLS] (고급)</p></td>
   <td><p>HTTP 요청에서 상호 TLS를 사용하려면 이 옵션을 활성화하십시오.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Sign Options] (고급)</p></td>
   <td><p>요청에 추가하려는 각 서명 옵션에 대해 <b>항목 추가</b>를 클릭하고 매개 변수의 이름과 값을 입력하십시오.</p><p>JWT 서명자에게 전달된 추가 옵션(예: <code>expiresIn</code>, <code>issuer</code>, <code>audience</code>, <code>subject</code> 및 <code>keyid</code>). <code>expiresIn</code>과(와) 같은 기간 값은 <code>jsonwebtoken</code> 라이브러리에서 해석됩니다. 일반 숫자는 밀리초로 처리되므로 <code>"1h"</code> 또는 <code>"3600s"</code>과(와) 같은 단위 문자열을 명시적으로 사용하십시오. 알고리즘은 연결에서 가져오며 여기에서 재정의할 수 없습니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Header Name] (고급)</p></td>
   <td><p>서명된 JWT를 받는 요청 헤더의 이름을 입력하거나 매핑합니다. 기본값: <code>Authorization</code>. 점선 이름은 거부되고 요청 로그에서 마스킹할 수 없으므로 헤더 이름에는 점(<code>.</code>)을 사용할 수 없습니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 토큰 유형] (고급)</p></td>
   <td><p>토큰 앞에 배치된 인증 체계를 입력하거나 매핑합니다(예: <code>Bearer</code>). 접두사 없이 원시 토큰을 전송하려면 이 항목을 비워 둡니다.</p></td>
  </tr>
 </tbody>
</table>

## 토큰 빌드 방법

1. 모듈은 [!UICONTROL JWT 페이로드(클레임)] 필드에 있는 클레임을 수집합니다.
1. <code>exp와 같은 예약된 클레임</code>, <code>iat</code>, 및 <code>nbf</code> NumericDate 값으로 변환됩니다.
1. 모듈은 [!UICONTROL 서명 옵션]을 적용하고 연결의 알고리즘을 사용하여 토큰에 서명합니다.
1. 서명된 토큰이 [!UICONTROL 헤더 이름]에 정의된 요청 헤더에 배치되었습니다.
1. [!UICONTROL 토큰 형식]이 설정되면 모듈은 토큰 앞에 접두사를 추가합니다. 예: <code>전달자 키...</code>.
1. 요청이 전송되며 응답은 표준 [!UICONTROL HTTP] > [!UICONTROL 요청 만들기] 모듈과 동일한 방식으로 처리됩니다.

서명된 토큰은 디버그 및 오류 로그에 자동으로 마스킹되어 노출되지 않습니다.

## 예

### 연결

- 알고리즘: `HS256`
- 암호: `my-shared-secret`

### 모듈 설정

- URL: `https://api.example.com/v1/orders`
- 메서드: `GET`
- JWT 페이로드(클레임):
  - `sub` = `service-account-42`
  - `iss` = `make-integration`
- 서명 옵션:
  - `expiresIn` = `1h`
- 헤더 이름: `Authorization`
- 토큰 형식: `Bearer`

### 결과

모듈은 다음과 유사한 헤더가 있는 요청을 전송합니다.

```text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

## FAQ / 과제

### 왜 내 토큰이 그렇게 빨리 만료되었습니까?

`expiresIn`에 대해 `3600`과(와) 같은 기본 번호를 입력했을 수 있습니다. `jsonwebtoken` 라이브러리는 일반 숫자를 밀리초로 해석합니다. 대신 `"1h"` 또는 `"3600s"`과(와) 같은 단위 문자열을 사용하십시오.

### 토큰은 언제 생성됩니까?

모듈은 연결을 만들 때가 아니라 모듈이 실행될 때마다 새로운 JWT에 서명합니다. 연결에서 서명 자료와 알고리즘만 저장하므로 `iat` 및 `exp`과(와) 같은 클레임은 해당 모듈 실행 순간을 반영합니다.

요청이 동일한 모듈 실행 내에서 다시 시도하는 경우, Fusion은 각 시도에 대해 새 토큰에 서명하는 대신 해당 재시도에 대해 서명된 동일한 토큰을 다시 사용합니다. 이 때문에 `expiresIn` 값이 너무 짧으면 다시 시도하기 전에 만료되어 이미 만료된 토큰을 다시 보낼 수 있습니다. 이를 방지하려면 `"1h"` 또는 `"3600s"`과(와) 같은 명확한 단위 문자열을 사용하고 토큰 수명이 지나치게 짧지 않도록 하십시오.

### 요청에 따라 알고리즘을 변경할 수 있습니까?

아니요. 알고리즘은 연결에 의해 수정됩니다. 다른 알고리즘이 필요한 경우 다른 JWT 연결을 만듭니다.

### 사용자 지정 헤더로 토큰을 보낼 수 있습니까?

예. [!UICONTROL 헤더 이름] 필드를 사용자 지정 이름으로 설정하되 점(`.`)을 포함할 수 없습니다.

### `Bearer` 없이 원시 토큰을 보낼 수 있습니까?

예. [!UICONTROL 토큰 형식]을 비워 둡니다.

### 토큰이 로그에 표시됩니까?

아니요. 서명된 토큰은 디버그 및 오류 로그에 자동으로 마스킹됩니다.


>[!NOTE]
>
>기술 참고: 서명은 `jsonwebtoken` 라이브러리를 사용하고 독립 실행형 JWT 앱의 서명 동작을 미러링하므로 동일한 입력이 독립 실행형 JWT 앱과 동일한 토큰을 생성합니다.
