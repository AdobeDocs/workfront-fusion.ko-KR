---
title: HTTP > 요청 모듈 만들기
description: Adobe Workfront Fusion HTTP > 요청 만들기 모듈은 HTTP 요청을 구성하고 서버에 제출할 수 있는 범용 모듈입니다. 그러면 수신된 HTTP 응답이 출력 번들에 포함됩니다.
author: Becky
feature: Workfront Fusion
exl-id: 42f6176e-86e0-489e-868b-66823a932daf
source-git-commit: a7ee3e751b75523c4da62cea71e59a63f98b95e0
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 1%

---

# [!UICONTROL HTTP] > [!UICONTROL Make a request] 모듈

[!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] > [!UICONTROL Make a request module]은(는) HTTP 요청을 구성하고 서버에 제출할 수 있는 범용 모듈입니다. 그러면 수신된 HTTP 응답이 출력 번들에 포함됩니다.

>[!NOTE]
>
>현재 전용 커넥터가 없는 Adobe 제품에 연결하는 경우 Adobe Authenticator 모듈을 사용하는 것이 좋습니다.
>
>자세한 내용은 [Adobe Authenticator 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)을 참조하세요.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## [!UICONTROL HTTP] > [!UICONTROL Make a request] 모듈 구성

[!UICONTROL HTTP] > [!UICONTROL Make a request] 모듈을 구성할 때 [!DNL Adobe Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx)] </td> 
   <td> <p>이 옵션을 사용하여 오류 처리를 설정합니다.</p> <p>자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">오류 처리 추가</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>API 엔드포인트 또는 웹 사이트와 같이 요청을 보낼 URL을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
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
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>이 본문 형식은 <code>[!UICONTROL application/x-www-form-urlencoded]</code>을(를) 사용하여 [!UICONTROL POST] 데이터에 사용됩니다.</p> <p><code>application/x-www-form-urlencoded</code>의 경우 서버로 전송된 HTTP 메시지의 본문은 기본적으로 하나의 쿼리 문자열입니다. 키와 값은 키와 값 사이에 <code>=</code>이(가) 있고 <code>&amp;</code>(으)로 구분된 키-값 쌍으로 인코딩됩니다. </p> <p>이진 데이터의 경우 대신 <code>[!UICONTROL multipart/form-data]</code>을(를) 사용합니다.</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>예: </b></span></span> 
       <p>결과 HTTP 요청 형식의 예:</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL  Multipart/form-data]은(는) 파일 및 데이터를 전송하는 데 사용되는 HTTP 다중 파트 요청입니다. 일반적으로 서버에 파일을 업로드하는 데 사용됩니다.</p> <p>요청에 전송할 필드를 추가합니다. 각 필드에는 키-값 쌍이 포함되어야 합니다.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>요청 본문 내에 보낼 키와 값을 입력합니다.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>키를 입력하고 요청 본문에 보낼 소스 파일을 지정합니다.</p> <p>이전 모듈에서 업로드할 파일을 매핑하거나([!UICONTROL HTTP] &gt; [!UICONTROL Get a File] 또는 [!UICONTROL Google Drive] &gt; 파일 다운로드) 파일 이름과 파일 데이터를 수동으로 입력합니다.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>응답을 자동으로 구문 분석하고 JSON 및 XML 응답을 변환하려면 이 옵션을 활성화합니다.</p> <p>구문 분석된 JSON 또는 XML 컨텐츠를 사용하기 전에 모듈에서 응답 컨텐츠를 인식하고 이를 후속 모듈에 매핑할 수 있도록 모듈을 한 번 수동으로 실행하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL User name]</p> </td> 
   <td> <p> 기본 인증을 사용하여 요청을 전송하려면 사용자 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password] </td> 
   <td> <p>기본 인증을 사용하여 요청을 보내려면 암호를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>요청 시간 제한(초)을 지정합니다(1-300). 기본값은 40초입니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> 이 옵션을 활성화하면 시나리오의 모든 HTTP 모듈과 서버의 쿠키를 공유할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>자체 서명된 인증서를 추가하려면 다음을 수행하십시오.</p>
          <ol>
            <li value="1">
              <p><b>[!UICONTROL Extract]</b>을(를) 클릭합니다.</p>
            </li>
            <li value="2">
              <p>추출 중인 파일 유형을 선택합니다.</p>
            </li>
            <li value="3">
              <p>또는 인증서가 포함된 파일을 선택합니다.</p>
            </li>
            <li value="4">
              <p>파일의 암호를 입력합니다.</p>
            </li>
            <li value="5">
              <p><b>[!UICONTROL Save]</b>을(를) 클릭하여 파일을 추출하고 모듈 설정으로 돌아갑니다.</p>
            </li>
          </ol>
</p> </td> 
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
   <td> <p>HTTP 요청에서 상호 TLS를 사용하려면 이 옵션을 활성화하십시오.</p> <p>상호 TLS에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">HTTP 모듈에서 상호 TLS 사용</a>을 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**예:** 이 예제는 JSON 페이로드가 있는 [!UICONTROL POST] 요청을 제출하도록 모듈을 설정하는 방법을 보여 줍니다.

![요청 예제 만들기](/help/workfront-fusion/references/apps-and-modules/assets/make-a-request-example-350x522.png)

[!UICONTROL Request content] 필드에서 JSON 조각을 표현식 및 항목과 직접 혼합하지 않는 것이 좋습니다. 잘못된 JSON이 발생할 수 있기 때문입니다.

>[!ENDSHADEBOX]
