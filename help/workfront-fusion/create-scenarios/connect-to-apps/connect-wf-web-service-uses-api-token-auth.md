---
title: API 토큰 인증을 사용하는 웹 서비스에 Adobe Workfront Fusion 연결
description: 일부 서비스에서는 Adobe Workfront Fusion과 같은 통합 솔루션으로 시나리오에서 쉽게 사용할 수 있는 앱을 만들 수 없습니다.
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 1%

---

# API 토큰 인증을 사용하는 웹 서비스에 Adobe Workfront Fusion 연결

일부 서비스에서는 Adobe Workfront Fusion과 같은 통합 솔루션으로 시나리오에서 쉽게 사용할 수 있는 앱을 만들 수 없습니다.

이 상황의 해결 방법은 HTTP > 요청 만들기 모듈을 사용하여 원하는 서비스(앱)를 Workfront Fusion에 연결하는 것입니다.

이 문서에서는 API 키/API 토큰을 사용하여 거의 모든 웹 서비스를 Workfront Fusion에 연결하는 방법을 설명합니다.

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

## API 토큰을 사용하는 웹 서비스에 연결

API 토큰을 통해 서비스를 연결하는 절차는 대부분의 웹 서비스에서 유사합니다.

1. [새 응용 프로그램을 만들고 API 토큰을 얻기](#create-a-new-application-and-obtain-the-api-token) 섹션에 설명된 대로 웹 서비스의 웹 사이트에서 응용 프로그램을 만듭니다.
1. API 키 또는 API 토큰을 가져옵니다.
1. Workfront Fusion의 HTTP > 요청 모듈 만들기 를 시나리오에 추가합니다.
1. 이 문서의 [HTTP 모듈 설정](#set-up-the-http-module) 섹션에 설명된 대로 웹 서비스의 API 설명서에 따라 모듈을 설정하고 시나리오를 실행합니다.

>[!NOTE]
>
>이 예에서는 Pushver 알림 서비스에 연결합니다.

## 새 애플리케이션 만들기 및 API 토큰 가져오기

>[!NOTE]
>
>웹 서비스가 API 키 또는 API 토큰을 만들고 배포하는 방법은 매우 다양합니다. 원하는 웹 서비스에 대한 API 키 및 토큰을 얻는 방법에 대한 지침은 서비스 웹 사이트에서 &quot;API 키&quot; 또는 &quot;API 토큰&quot;을 검색합니다.
>
>푸시 API 키를 얻는 방법에 대한 지침은 찾을 수 있는 예제의 경우에만 포함됩니다.

1. Pushover 계정에 로그인합니다.
1. 페이지 하단에서 **응용 프로그램/API 토큰 만들기**&#x200B;를 클릭합니다.
1. 응용 프로그램 정보를 입력하고 **응용 프로그램 만들기**&#x200B;를 클릭합니다.
1. 제공된 API 토큰을 안전한 장소에 저장합니다. 원하는 웹 서비스에 연결하려면 Workfront Fusion HTTP > 요청 만들기 모듈에 필요합니다(이 경우 푸시오버).

## HTTP 모듈 설정

웹 서비스를 Workfront Fusion 시나리오에 연결하려면 시나리오에서 HTTP > 요청 모듈 만들기 를 사용하고 웹 서비스의 API 설명서에 따라 모듈을 설정해야 합니다.

1. HTTP > 요청 만들기 모듈을 시나리오에 추가합니다.
1. Workfront Fusion을 사용하여 메시지를 푸시하려면 다음과 같이 HTTP 모듈을 설정합니다.

   >[!NOTE]
   >
   >이러한 모듈 설정은 Pushover 웹 서비스 API 설명서에 해당합니다. 설정은 다른 웹 서비스에 대해 다를 수 있습니다. 예를 들어 API 토큰은 Body 필드가 아닌 Header에 삽입될 수 있습니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>URL 필드에는 웹 서비스의 API 설명서에서 찾을 수 있는 끝점이 포함됩니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> 메서드</td> 
      <td> <p><code>POST</code> </p> <p>사용되는 메서드는 해당 끝점에 따라 다릅니다. 메시지 푸시를 위한 푸시 엔드포인트는 POST 메서드를 사용합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 헤더</p> </td> 
      <td> <p>일부 웹 서비스는 헤더를 사용하여 API 토큰 인증 또는 기타 매개 변수를 지정할 수 있습니다. 메시지 푸시에 대한 푸시 엔드포인트가 모든 요청 유형에 대해 본문(아래 참조)을 사용하므로 이 예에서는 그렇지 않습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 쿼리 문자열</p> </td> 
      <td> <p>일부 웹 서비스는 쿼리 문자열을 사용하여 다른 매개 변수를 지정할 수 있습니다. 이 예제에서는 Pushover 웹 서비스가 모든 요청 유형에 대해 Body(아래 참조)를 사용하므로 그렇지 않습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 본문 유형</p> </td> 
      <td> <p><code>Raw</code> </p> <p>이 설정을 사용하면 아래 콘텐츠 유형 필드에서 JSON 콘텐츠 유형을 선택할 수 있습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 콘텐츠 유형</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON은 푸시 앱의 필수 콘텐츠 유형입니다. 이는 다른 웹 서비스와 다를 수 있습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 콘텐츠 요청</p> </td> 
      <td> <p>JSON 형식으로 본문 요청 컨텐츠를 입력합니다. 이 문서의 <a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref">JSON을 사용하여 JSON 본문 매핑 &gt; JSON 모듈 만들기</a>에 설명된 대로 JSON &gt; JSON 모듈 만들기를 사용할 수 있습니다. 또는 이 문서의 <a href="#enter-the-json-body-manually" class="MCXref xref">JSON 본문을 수동으로 입력</a>에 설명된 대로 JSON 콘텐츠를 수동으로 입력할 수도 있습니다.</p> <p>해당 웹 서비스에 필요한 매개 변수에 대해서는 웹 서비스의 API 설명서 를 참조하십시오.</p> </td>

   </tr> 
    </tbody> 
   </table>

## JSON 본문을 수동으로 입력

매개 변수와 값을 JSON 형식으로 지정하십시오.

>[!BEGINSHADEBOX]

**예:**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

이 예에는 다음 정보가 포함됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> 사용자</p> </td> 
   <td> <p>사용자 키. 이 이름은 푸시오버 대시보드에서 찾을 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> 토큰 </td> 
   <td> <p>생성된 API 토큰/API 키 는 Pushver 앱을 만들었습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> 메시지 </td> 
   <td> <p>장치로 전송되는 푸시 알림의 텍스트 콘텐츠입니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> 제목 </td> 
   <td> <p>(선택 사항) 메시지 제목입니다. 값을 입력하지 않으면 앱 이름이 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## JSON > JSON 생성 모듈을 사용하여 JSON 본문 매핑

JSON 작성 모듈을 통해 JSON을 더 쉽게 지정할 수 있습니다. 또한 값을 동적으로 정의할 수 있습니다.

JSON 모듈에 대한 자세한 내용은 [JSON 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md)을 참조하세요.

1. JSON을 생성할 값을 입력하거나 매핑합니다.

   ![JSON 값](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png)

1. JSON > JSON 만들기 모듈을 HTTP > 요청 모듈에 연결합니다.
1. JSON 만들기 모듈의 JSON 문자열을 HTTP > 요청 모듈 만들기의 요청 콘텐츠 필드에 매핑합니다.

시나리오를 실행하면 푸시 알림이 푸시 계정에 등록된 장치로 전송됩니다.
