---
title: HTTP &gt; 기타 모듈
description: ' [!DNL Adobe Workfront Fusion] HTTP 앱은 HTTP(Hypertext Transfer Protocol) 프로토콜을 기반으로 통신을 위한 다양한 모듈을 제공합니다. HTTP는 World Wide Web을 위한 데이터 통신의 기초입니다. 모듈을 사용하여 웹 페이지 및 파일을 다운로드하고, 웹후크 및 API 엔드포인트를 호출하는 등의 작업을 수행할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# HTTP > 기타 모듈

>[!NOTE]
>
>[!UICONTROL Adobe Workfront Fusion]에는 [!UICONTROL Adobe Workfront] 라이선스 외에 [!UICONTROL Adobe Workfront Fusion] 라이선스가 필요합니다.

[!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] 앱은 HTTP(Hypertext Transfer Protocol) 프로토콜을 기반으로 통신을 위한 다양한 모듈을 제공합니다. HTTP는 World Wide Web을 위한 데이터 통신의 기초입니다. 모듈을 사용하여 웹 페이지 및 파일을 다운로드하고, 웹후크 및 API 엔드포인트를 호출하는 등의 작업을 수행할 수 있습니다.

모듈의 올바른 선택은 액세스하려는 리소스가 사용하는 인증/권한 부여 메커니즘에 따라 다릅니다. 다음은 모듈의 예입니다

* 요청:범용 모듈은 주로 인증/권한 부여를 사용하지 않는 리소스를 위한 것입니다.
* [!DNL HTTP] BA(기본 인증)를 사용하는 리소스에 대한 기본 인증 요청 만들기
* OAuth 2.0 인증 프로토콜을 사용하는 리소스에 대해 OAuth 2.0 요청:
* 클라이언트 인증서 인증 요청 만들기: 클라이언트측 인증서가 필요한 인증 프로토콜을 사용하는 리소스에 대해 입니다.
* API 키 인증 요청 만들기: 인증을 위해 API 키를 사용하는 리소스에 대해.

>[!NOTE]
>
>현재 전용 커넥터가 없는 Adobe 제품에 연결하는 경우 Adobe Authenticator 모듈을 사용하는 것이 좋습니다.
>
>자세한 내용은 [Adobe Authenticator 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)을 참조하세요.

## 모듈 요청

특정 요청 모듈 지침에 대해서는 다음 문서를 참조하십시오.

* [[!UICONTROL HTTP] > [!UICONTROL Make a request] 모듈](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Basic Authorization request] 모듈](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] 모듈](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request] 모듈](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## 기타 작업 모듈

* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Resolve a target URL]](#resolve-a-target-url)

### [!UICONTROL Get a File]

이 작업 모듈은 지정된 URL에서 파일을 다운로드합니다. 파일이 다운로드되면 시나리오의 다른 모듈을 사용하여 파일을 추가로 처리(파일 데이터 매핑)할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>다운로드할 파일의 URL을 입력하거나 매핑합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolve a target URL]

이 작업 모듈은 HTTP 리디렉션 체인을 해결하고 대상 URL을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>[!DNL bit.ly] URL과 같이 확인할 URL을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method] </td> 
   <td> <p>[!UICONTROL HEAD] 메서드를 사용할지 [!UICONTROL GET] 메서드를 사용할지 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

## 반복자 모듈

### [!UICONTROL Retrieve headers]

이 모듈은 지정된 HTTP 모듈의 각 헤더(이름 및 값)를 별도의 번들로 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> 헤더를 검색할 모듈을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

## JSON 웹 토큰(JWT) 생성

기본 제공 함수를 사용하여 JWT 토큰을 생성할 수 있습니다.

헤더:

![JWT 헤더](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

복사 및 붙여넣기용 코드:

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

페이로드:

![JWT 페이로드](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

복사 및 붙여넣기용 코드:

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

토큰:

![JWT 토큰](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

복사 및 붙여넣기용 코드:

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
