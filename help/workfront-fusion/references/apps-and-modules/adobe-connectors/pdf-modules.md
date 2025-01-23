---
title: Adobe PDF 서비스
description: Adobe PDF 서비스
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 757580687ff5d1617f83432952d9870bd697925e
workflow-type: tm+mt
source-wordcount: '3623'
ht-degree: 0%

---

# [!DNL Adobe PDF Services]

[!DNL Adobe Workfront Fusion] [!DNL Adobe PDF Services]을(를) 사용하면 PDF 파일에서 데이터를 추출하거나 제공한 데이터에서 새 PDF 파일을 생성할 수 있습니다. 또한 다양한 파일 유형을 PDF으로 변환하거나 PDF을 다른 파일 유형으로 변환할 수 있습니다. 또한 PDF 서비스를 사용하여 PDF 파일에 대한 메타데이터를 결합, 압축 또는 읽거나 파일에 대한 암호 보호를 제어할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

PDF 서비스에 사용되는 API에 대한 자세한 내용은 [Adobe 문서 생성 API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html)를 참조하십시오.

## [!DNL Adobe PDF Services]을(를) 사용할 때의 보안 고려 사항

[!DNL Adobe PDF Services]은(는) 파일을 읽거나 변환하거나 수정할 수 있지만 [!DNL Adobe]과(와) [!DNL Workfront Fusion]은(는) 파일이나 데이터를 저장하지 않습니다. 이것은 다음을 의미합니다.

* 보안을 포함하여 파일에 대한 제어 유지
* PDF 서비스를 사용하기 위해 [!UICONTROL Adobe] 저장소 또는 클라우드 저장소 계정이 필요하지 않습니다.

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
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 작업 자동화 및 통합을 위한 Workfront Fusion </p>
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

## 전제 조건

OAuth 서버 간 연결을 만들려면 Adobe 개발자 콘솔에서 Adobe PDF 서비스 API를 추가해야 합니다. API를 추가할 때 OAuth 서버 간 옵션을 선택합니다.

지침은 Adobe 개발자 설명서에서 [OAuth를 사용하여 프로젝트에 API 추가](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/)를 참조하십시오.

## Adobe PDF 서비스 API 정보

Adobe PDF 서비스 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Adobe PDF Services]에 연결 만들기

[!DNL Adobe PDF Services] 모듈에 대한 연결을 만들려면:

1. [!DNL Adobe PDF Services] 모듈에서 연결 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>서버 간 연결을 만들지 JWT 연결을 만들지 선택합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>이 연결의 이름을 입력하십시오.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>[!DNL Adobe] [!UICONTROL Client ID]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>[!DNL Adobe] [!UICONTROL Client Secret]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Technical account ID] (JWT만 해당)</td>
          <td>[!DNL Adobe] [!UICONTROL Technical account ID]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Organization ID] (JWT만 해당)</td>
          <td>[!DNL Adobe] [!UICONTROL Organization ID]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Meta scopes] (JWT만 해당)</td>
          <td>
            연결에 필요한 메타 범위를 입력합니다.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>JWT 연결을 선택한 경우 [!DNL Adobe Developer Console]에서 자격 증명을 만들 때 생성된 개인 키를 입력하십시오. </p>
          <p>개인 키 또는 인증서를 추출하려면 다음을 수행하십시오.</p>
          <ol>
            <li value="1">
              <p><b>[!UICONTROL Extract]</b>을(를) 클릭합니다.</p>
            </li>
            <li value="2">
              <p>추출 중인 파일 유형을 선택합니다.</p>
            </li>
            <li value="3">
              <p>개인 키 또는 인증서가 포함된 파일을 선택합니다.</p>
            </li>
            <li value="4">
              <p>파일의 암호를 입력합니다.</p>
            </li>
            <li value="5">
              <p><b>[!UICONTROL Save]</b>을(를) 클릭하여 파일을 추출하고 연결 설정으로 돌아갑니다.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.


## [!DNL Adobe PDF Services]개 모듈 및 해당 필드

[!DNL PDF Services]을(를) 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준과 같은 요소에 따라 추가 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Combine PDF files]](#combine-pdf-files)
* [[!UICONTROL Compress PDF files]](#compress-pdf-files)
* [[!UICONTROL Convert document to PDF file]](#convert-document-to-pdf-file)
* [[!UICONTROL Convert HTML to PDF file]](#convert-html-to-pdf-file)
* [[!UICONTROL Convert image to PDF file]](#convert-image-to-pdf-file)
* [[!UICONTROL Convert PDF to document]](#convert-pdf-to-document)
* [[!UICONTROL Convert PDF to image]](#convert-pdf-to-image)
* [[!UICONTROL Extract Text / Table]](#extract-text--table)
* [[!UICONTROL Generate document]](#generate-document)
* [[!UICONTROL Linearize a PDF file]](#linearize-a-pdf-file)
* [사용자 지정 API 호출 만들기](#make-a-custom-api-call)
* [[!UICONTROL OCR for PDF file]](#ocr-for-pdf-file)
* [[!UICONTROL Page manipulation]](#page-manipulation)
* [[!UICONTROL PDF accessibility auto-tag]](#pdf-accessibility-auto-tag)
* [[!UICONTROL PDF file properties]](#pdf-file-properties)
* [[!UICONTROL Protect PDF file]](#protect-pdf-file)
* [[!UICONTROL Remove protection of a PDF file]](#remove-protection-of-a-pdf-file)
* [PDF 파일 분할](#split-a-pdf-file)

### [!UICONTROL Combine PDF files]

이 작업 모듈은 여러 PDF 파일을 가져와 단일 PDF 파일로 결합합니다. 예를 들어 이 모듈은 프로젝트가 완료되면 [!UICONTROL Workfront] 프로젝트의 모든 문서를 단일 PDF으로 결합할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents]</td> 
   <td> <p>집계 모듈을 사용하여 문서를 수집하여 PDF에 결합하거나 문서를 수동으로 추가할 수 있습니다. </p> <p>[!UICONTROL Array Aggregator] 모듈을 사용하여 이전 모듈의 출력을 집계하는 것이 좋습니다. 취합기를 사용하면 결합할 파일의 이름, 위치 또는 번호를 알 필요가 없습니다. 따라서 취합자를 사용하면 결합할 문서를 수동으로 입력하는 것보다 훨씬 유연하고 확장 가능합니다.</p> <p>집계기에 [!UICONTROL Combine PDF] 파일 모듈을 사용하려면 [!UICONTROL Documents] 필드에 매핑을 사용하도록 설정해야 합니다. </p> <p>이 예제에서 [!UICONTROL Read Related Records] 모듈은 프로젝트와 관련된 문서를 식별하고 [!UICONTROL Download Documents] 모듈은 각 문서를 다운로드합니다. 모든 PDF은 배열로 집계되어 [!UICONTROL Combine PDF] 파일 모듈로 전달됩니다.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>문서를 수동으로 입력할 수도 있습니다.</p> <p>결합된 PDF에 포함할 각 문서의 경우:</p> 
    <ol> 
     <li value="1"> <p>클릭 [!UICONTROL Add a Document]</p> </li> 
     <li value="2"> <p>[!UICONTROL Source file] 필드에서 포함할 문서를 출력하는 모듈을 선택하거나 원본 파일의 이름과 데이터를 매핑합니다. </p> </li> 
     <li value="3"> <p>(선택 사항) 소스 파일의 특정 페이지만 포함하려면 추가할 각 페이지 범위에 대해 [!UICONTROL Pages] 필드에서 <strong>[!UICONTROL Add item]</strong>을(를) 클릭한 다음 포함할 페이지 범위의 첫 번째 페이지와 마지막 페이지를 입력하고 <strong>[!UICONTROL Add]</strong>을(를) 클릭합니다. 단일 문서에서 두 개 이상의 페이지 범위를 포함할 수 있습니다.</p> </li> 
     <li value="4"> <p><strong>[!UICONTROL Add]</strong>을(를) 클릭합니다. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Compress PDF files]

이 작업 모듈은 PDF 파일을 가져와 압축합니다. 이는 대역폭 또는 메모리를 절약하는 데 유용할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compression level]</td> 
   <td>사용할 압축 수준을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert document to PDF file]

이 도구는 문서를 PDF 파일로 변환합니다. 소스 파일은 다음 문서 형식 중 하나여야 합니다.

* DOC
* XLS
* PPT
* TXT
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 다음 형식 중 하나여야 합니다.</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>소스 문서의 기본 언어를 선택합니다. 이렇게 하면 소스 파일에 글꼴이 포함되지 않은 경우 모듈에서 적절한 글꼴을 선택할 수 있습니다.</p> <p>다음 언어 중에서 선택합니다.</p> 
    <ul> 
     <li> <p>en-US (기본값): 영어 (미국)</p> </li> 
     <li> <p>ca-ES: 카탈로니아어(스페인)</p> </li> 
     <li> <p>cs-CZ: 체코어(체코)</p> </li> 
     <li> <p>da-DK: 덴마크어(덴마크)</p> </li> 
     <li> <p>de-DE: 독일어(독일)</p> </li> 
     <li> <p>en-AE: 영어(아랍에미리트)</p> </li> 
     <li> <p>en-GB: 영어(영국)</p> </li> 
     <li> <p>en-IL: 영어 (이스라엘)</p> </li> 
     <li> <p>en-US: 영어(미국)</p> </li> 
     <li> <p>es-ES: 스페인어(스페인)</p> </li> 
     <li> <p>es-MX: 스페인어(멕시코)</p> </li> 
     <li> <p>eu-ES: 바스크(스페인)</p> </li> 
     <li> <p>fi-FI: 핀란드어(핀란드)</p> </li> 
     <li> <p>fr-CA: 프랑스어(캐나다)</p> </li> 
     <li> <p>fr-FR: 프랑스어(프랑스)</p> </li> 
     <li> <p>fr-MA: 프랑스어(모로코)</p> </li> 
     <li> <p>hr-HR: 크로아티아어(크로아티아)</p> </li> 
     <li> <p>hu-HU: 헝가리어(헝가리)</p> </li> 
     <li> <p>it-IT: 이탈리아어(이탈리아)</p> </li> 
     <li> <p>ja-JP: 일본어(일본)</p> </li> 
     <li> <p>kr-KR: 한국어(대한민국)</p> </li> 
     <li> <p>nb-NO: 노르웨이어 부크몰 (노르웨이)</p> </li> 
     <li> <p>nl-NL: 네덜란드어(네덜란드)</p> </li> 
     <li> <p>pl-PL: 폴란드어(폴란드)</p> </li> 
     <li> <p>pt-BR: 포르투갈어(브라질)</p> </li> 
     <li> <p>pt-PT: 포르투갈어(포르투갈)</p> </li> 
     <li> <p>ro-RO: 루마니아어(루마니아)</p> </li> 
     <li> <p>ru-RU: 러시아어(러시아)</p> </li> 
     <li> <p>sk-SK: 슬로바키아어(슬로바키아)</p> </li> 
     <li> <p>sl-SI: 슬로베니아어(슬로베니아)</p> </li> 
     <li> <p>sv-SE: 스웨덴어(스웨덴)</p> </li> 
     <li> <p>tr-TR: 터키어(터키)</p> </li> 
     <li> <p>uk-UA: 우크라이나어(우크라이나)</p> </li> 
     <li> <p>zh-CN: 중국어(중국 본토)</p> </li> 
     <li> <p>zh-TW: 중국어(대만)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert HTML to PDF file]

이 도구는 HTML 파일을 PDF 파일로 변환합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>중요: Source 파일은 HTML 또는 ZIP 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>HTML이 JavaScript 변수를 참조하는 경우 여기에 해당 변수를 포함할 수 있습니다. </p> <p>각 변수에 대해 <strong>[!UICONTROL Add item]</strong>을(를) 클릭하고 변수의 키와 값을 포함합니다.</p> <p>참고:   
     <ul> 
      <li> <p>ZIP 파일에서 PDF을 만들 때 원본 자료에 <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code>과(와) 같은 스크립트 요소가 포함되어야 합니다. </p> </li> 
      <li> <p>URL에서 PDF을 만들 때 페이지가 렌더링되기 전에 이 JSON 개체의 콘텐츠가 브라우저 VM에 삽입됩니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include header and footer]</td> 
   <td> <p>PDF 문서의 머리글과 바닥글을 만들려면 이 옵션을 활성화합니다.</p> 
    <ul> 
     <li> <p>머리글에는 날짜와 문서 제목이 포함됩니다.</p> </li> 
     <li> <p>바닥글에는 파일 이름과 페이지 번호가 포함되어 있습니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page width]</td> 
   <td>용지의 너비를 인치 단위로 입력합니다. 모듈은 이 정보를 사용하여 생성된 PDF 파일의 페이지 서식을 지정합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page height]</td> 
   <td>용지의 높이를 인치 단위로 입력합니다. 모듈은 이 정보를 사용하여 생성된 PDF 파일의 페이지 서식을 지정합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert image to PDF file]

이 도구는 이미지를 PDF 파일로 변환합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 이미지 파일을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert PDF to document]

이 도구는 PDF 파일을 문서로 변환합니다. 출력 파일에 대해 다음 형식 중 하나를 선택할 수 있습니다.

* DOC
* DOCX
* PPTX
* XLSX
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>파일을 다음과 같이 출력할 형식을 선택합니다.</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>소스 문서의 기본 언어를 선택합니다. 이렇게 하면 소스 파일에 글꼴이 포함되지 않은 경우 모듈에서 적절한 글꼴을 선택할 수 있습니다.</p> <p>다음 언어 중에서 선택합니다.</p> 
    <ul> 
     <li> <p>en-US (기본값): 영어 (미국)</p> </li> 
     <li> <p>ca-ES: 카탈로니아어(스페인)</p> </li> 
     <li> <p>cs-CZ: 체코어(체코)</p> </li> 
     <li> <p>da-DK: 덴마크어(덴마크)</p> </li> 
     <li> <p>de-DE: 독일어(독일)</p> </li> 
     <li> <p>en-AE: 영어(아랍에미리트)</p> </li> 
     <li> <p>en-GB: 영어(영국)</p> </li> 
     <li> <p>en-IL: 영어 (이스라엘)</p> </li> 
     <li> <p>en-US: 영어(미국)</p> </li> 
     <li> <p>es-ES: 스페인어(스페인)</p> </li> 
     <li> <p>es-MX: 스페인어(멕시코)</p> </li> 
     <li> <p>eu-ES: 바스크(스페인)</p> </li> 
     <li> <p>fi-FI: 핀란드어(핀란드)</p> </li> 
     <li> <p>fr-CA: 프랑스어(캐나다)</p> </li> 
     <li> <p>fr-FR: 프랑스어(프랑스)</p> </li> 
     <li> <p>fr-MA: 프랑스어(모로코)</p> </li> 
     <li> <p>hr-HR: 크로아티아어(크로아티아)</p> </li> 
     <li> <p>hu-HU: 헝가리어(헝가리)</p> </li> 
     <li> <p>it-IT: 이탈리아어(이탈리아)</p> </li> 
     <li> <p>ja-JP: 일본어(일본)</p> </li> 
     <li> <p>kr-KR: 한국어(대한민국)</p> </li> 
     <li> <p>nb-NO: 노르웨이어 부크몰 (노르웨이)</p> </li> 
     <li> <p>nl-NL: 네덜란드어(네덜란드)</p> </li> 
     <li> <p>pl-PL: 폴란드어(폴란드)</p> </li> 
     <li> <p>pt-BR: 포르투갈어(브라질)</p> </li> 
     <li> <p>pt-PT: 포르투갈어(포르투갈)</p> </li> 
     <li> <p>ro-RO: 루마니아어(루마니아)</p> </li> 
     <li> <p>ru-RU: 러시아어(러시아)</p> </li> 
     <li> <p>sk-SK: 슬로바키아어(슬로바키아)</p> </li> 
     <li> <p>sl-SI: 슬로베니아어(슬로베니아)</p> </li> 
     <li> <p>sv-SE: 스웨덴어(스웨덴)</p> </li> 
     <li> <p>tr-TR: 터키어(터키)</p> </li> 
     <li> <p>uk-UA: 우크라이나어(우크라이나)</p> </li> 
     <li> <p>zh-CN: 중국어(중국 본토)</p> </li> 
     <li> <p>zh-TW: 중국어(대만)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert PDF to image]

이 도구는 PDF을 PNG 또는 JPEG 형식의 이미지로 변환한 다음 목록으로 출력하거나 ZIP으로 결합합니다.

ZIP으로 출력하는 경우 PDF은 페이지당 하나의 이미지로 변환되고 각 이미지는 페이지 번호로 종료됩니다. 그런 다음 이미지 파일이 ZIP 파일로 결합됩니다.

예를 들어, 페이지가 8개인 &quot;TestFile&quot;이라는 파일은 &quot;TestFile_1&quot;에서 &quot;TestFile_8&quot;까지의 8개의 이미지를 생성합니다. 모듈의 출력은 8개의 이미지가 포함된 ZIP 파일입니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>파일을 다음과 같이 출력할 형식을 선택합니다.</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output type]</td> 
   <td> <p>파일을 파일 목록으로 출력할지 ZIP 파일로 출력할지 선택합니다.</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL Extract Text / Table]

이 작업 모듈에서는 PDF 파일에서 데이터를 추출할 수 있습니다. 모듈은 단락 또는 표의 단일 셀에 있는 텍스트와 같은 개별 텍스트 요소를 출력합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elements that should be extracted as JSON]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Text]</p> </li> 
     <li> <p>[!UICONTROL Tables]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Extract Bounding boxes?]</td> 
   <td>텍스트의 테두리 상자에 대한 데이터를 추출하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include styling information for output?]</td> 
   <td>이 옵션을 활성화하여 출력 JSON에 스타일 정보를 추가합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Generate document]

[!UICONTROL Generate document] 모듈은 선택한 데이터가 포함된 PDF을 만드는 강력한 방법입니다. [!DNL Microsoft Word] 템플릿을 사용하거나 JSON 형식의 데이터를 제공하여 형식을 지정할 수 있습니다.

[!UICONTROL [!DNL Adobe PDF Services] Generate document] 기능에 대한 자세한 내용은 [!DNL Adobe Document Services] 설명서의 [문서 생성 개요](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html)를 참조하십시오.

* [ [!DNL Microsoft Word] 템플릿](#use-the-generate-document-module-with-a-microsoft-word-template)에 [!UICONTROL Generate document] 모듈 사용
* [JSON으로 [!UICONTROL Generate document] 모듈 사용](#use-the-generate-document-module-with-json)

#### [!DNL Microsoft Word] 템플릿으로 [!UICONTROL Generate document] 모듈 사용


>[!NOTE]
>
>Microsoft Word 템플릿에 대한 설명은 [Microsoft Word 템플릿 모듈](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md)을 참조하십시오.
>
>Microsoft Word 템플릿을 PDF 서비스 생성 문서 모듈과 함께 사용하기 위해 Microsoft Word 템플릿 모듈을 사용할 필요는 없습니다.


[!UICONTROL Microsoft Word] 템플릿으로 [!UICONTROL Generate document] 모듈을 사용하려면 먼저 템플릿을 만들어야 합니다. 지침은 [!DNL Microsoft Office] 설명서에서 &quot;템플릿 만들기&quot;를 검색하십시오.

다음과 같이 [!UICONTROL Generate document] 모듈 필드를 채웁니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>이 원본 파일은 모듈이 새 PDF을 생성하는 데 사용하는 [!DNL Microsoft Word] 템플릿입니다.</p> <p>[!DNL Workfront Fusion]에서 사용하는 [!DNL Microsoft Word] 템플릿에 대해 [!DNL Workfront]에서 프로젝트를 만드는 것이 좋습니다. 그런 다음 [!DNL Workfront] &gt; [!UICONTROL Download document] 모듈을 사용하여 적절한 템플릿을 시나리오로 가져올 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>생성된 문서의 형식을 선택합니다.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>텍스트로 바꿀 템플릿의 각 값 태그에 대해 다음을 입력합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Key]</p> <p>키를 입력합니다. 템플릿에서 키는 값 태그에 표시되는 텍스트입니다. 예를 들어 값 태그 <code>&#123;&#123;name&#125;&#125;</code>에 텍스트를 삽입하려면 키 필드에 <code>name </code>을(를) 입력합니다.</p> </li> 
     <li> <p>값 유형</p> <p>값 필드의 데이터가 값, 개체 또는 개체 배열인지 선택합니다.</p> </li> 
     <li> <p>[!UICONTROL Value]</p> <p>값 태그 대신 생성된 문서에 표시할 텍스트를 입력하거나 매핑합니다.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### JSON으로 [!UICONTROL Generate document] 모듈 사용

JSON이 있는 [!UICONTROL Generate document] 모듈을 사용하려면 다음과 같이 필드를 채웁니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>생성된 문서의 형식을 선택합니다.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>이 모듈에서 JSON을 사용하려면 이 필드에서 매핑을 활성화해야 합니다.</p> <p>JSON을 입력하거나 매핑하여 문서를 생성합니다. </p> <p>이 필드에 JSON을 직접 입력하거나 JSON 모듈의 JSON 출력을 매핑할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Linearize a PDF file]

이 도구는 PDF 문서를 선형화하여 웹에 최적화된 PDF 문서를 만듭니다. 선형 PDF 문서는 전체 문서를 다운로드할 필요 없이 페이지별로 볼 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용자 지정 API 호출 만들기

이 작업 모듈은 PDF 서비스 API에 대한 사용자 지정 HTTP 요청을 처리합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> 상대 경로 또는 URL을 입력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 인증 헤더를 자동으로 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>API 호출에 추가할 각 필드에 대해 <b>항목 추가</b>를 클릭하고 필드의 키와 선택적 값을 입력하십시오.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR for PDF file]

이 도구는 파일에서 OCR(광학 문자 인식)을 수행하고 PDF을 생성합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>이 문서의 언어를 선택합니다.<p>언어 옵션은 이 문서에서 <a href="#convert-document-to-pdf-file" class="MCXref xref" >문서를 PDF 파일로 변환</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR type]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Modified original image] type을 사용하면 텍스트를 검색하고 선택할 수 있지만, 보이지 않는 텍스트 레이어를 배치하기 전에 정리 프로세스(예: 축소판)를 진행하는 동안 원본 이미지가 수정됩니다. 이 유형은 원하지 않는 아티팩트를 제거하고 일부 시나리오에서 더 읽기 쉬운 문서를 생성할 수 있습니다. </p> </li> 
     <li> <p>[!UICONTROL Unchanged original image] 유형은 또한 원본 이미지 위에 검색 가능한 텍스트 레이어를 오버레이하지만, 이 경우 원본 이미지는 변경되지 않습니다. 이 유형은 원본 이미지에 최대 충실도를 생성합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Page manipulation]

이 모듈에서는 PDF 문서의 페이지를 선택적으로 회전하거나 삭제할 수 있습니다. 예를 들어 세로 보기를 가로 보기로 변경하거나 PDF 문서에서 특정 페이지를 제거할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> <p>파일에서 수행할 작업을 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Delete]</b> </p> <p>문서에서 페이지를 삭제하려면 이 옵션을 선택합니다.</p><p>삭제할 각 페이지 범위에 대해 <strong>[!UICONTROL Add]</strong>을(를) 클릭한 다음 페이지 범위의 첫 번째 페이지와 마지막 페이지를 입력합니다. </p> <p>참고:   
     <ul> 
      <li> <p>음수를 사용하여 문서 끝 부분부터 다시 계산할 수 있습니다. 문서의 마지막 페이지는 -1이고, 두 번째 페이지에서 마지막 페이지까지 -2입니다.</p> </li> 
      <li> <p>단일 페이지를 삭제하려면 동일한 페이지 번호를 범위의 시작 및 끝 둘 다로 설정합니다.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Rotate]</b> </p> <p>이 옵션을 선택하여 페이지를 회전한 다음 시작 방향을 기준으로 문서 페이지를 회전할 각도를 시계 방향으로 도 단위로 입력합니다.</p> <p>세로에서 가로로 또는 그 반대로 회전하려면 페이지를 90도 또는 270도로 회전합니다.</p> <p>페이지가 뒤집혀 있으면 180도 회전합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pages]</td> 
   <td> <p>삭제할 각 페이지 범위에 대해 <strong>[!UICONTROL Add]</strong>을(를) 클릭한 다음 페이지 범위의 첫 번째 페이지와 마지막 페이지를 입력합니다. </p> <p>참고:   
     <ul> 
      <li> <p>음수를 사용하여 문서 끝 부분부터 다시 계산할 수 있습니다. 문서의 마지막 페이지는 -1이고, 두 번째 페이지에서 마지막 페이지까지 -2입니다.</p> </li> 
      <li> <p>단일 페이지를 삭제하려면 동일한 페이지 번호를 범위의 시작 및 끝 둘 다로 설정합니다.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 사용할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF accessibility auto-tag]

이 작업 모듈은 접근성 사용 사례에 대해 태그가 지정된 PDF을 만듭니다. 또한 문제를 나열하고 수정 사항을 제안하는 선택적 Microsoft Excel 보고서를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shift Headings]</td> 
   <td> <p>문서의 제목을 이동하려면 이 옵션을 활성화합니다.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generate Report]</td> 
   <td> <p>이 옵션을 활성화하면 PDF의 접근성 문제를 위치와 함께 나열하고 이러한 문제를 해결하는 방법에 대한 제안을 제공하는 보고서를 생성할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF file properties]

이 도구는 다음과 같은 문서에 대한 기본 정보를 추출합니다.

* 페이지 수
* PDF 버전
* 파일이 암호화되었는지 여부
* 파일이 선형화되었는지 여부
* 파일에 포함된 파일이 포함되어 있는지 여부

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Protect a PDF file]

이 도구는 사용자 또는 소유자 암호로 PDF 문서를 보호합니다. 또한 PDF 문서의 인쇄, 편집 및 복사와 같은 특정 기능에 대한 제한 사항을 설정합니다. 암호화할 콘텐츠의 유형과 암호화 알고리즘을 선택합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password Protection Type]</td> 
   <td> <p>암호를 사용하여 입력 PDF 문서를 암호화하려면 이 옵션을 활성화합니다. 이 옵션을 사용하는 경우 다음 중 하나 또는 모두에 대한 값을 지정하고 입력해야 합니다. </p> 
    <ul> 
     <li> <p>[!UICONTROL User Password]</p> </li> 
     <li> <p>[!UICONTROL Owner Password] </p> </li> 
    </ul> <p>각 암호 길이는 최대 128자까지 가능합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encryption Algorithm]</td> 
   <td> <p>암호화 알고리즘을 선택합니다. </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128 encryption]</p> <p>암호는 LATIN-I 문자만 지원합니다. </p> </li> 
     <li> <p>[!UICONTROL AES-256 encryption]</p> <p>암호는 유니코드 문자 집합을 지원합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content to Encrypt]</td> 
   <td> <p>암호화할 콘텐츠의 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL All content]</p> </li> 
     <li> <p>[!UICONTROL All content except metadata]</p> </li> 
     <li> <p>[!UICONTROL Only embedded data] </p> </li> 
    </ul> <p>"[!UICONTROL Only embedded data]"을(를) 선택하면 제공된 모든 액세스 권한이 무효화됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permissions]</td> 
   <td> <p>인쇄, 편집 또는 콘텐츠 복사를 허용하도록 포함할 권한을 선택합니다.</p> <p>권한 설정은 [!UICONTROL Password Protection Type] 필드에 [!UICONTROL Owner Password]이(가) 설정된 경우에만 사용됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Remove protection of a PDF file]

이 도구는 PDF 문서에서 보안(암호 보호)을 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password]</td> 
   <td>현재 파일을 보호하는 암호를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Split a PDF file]

이 작업 모듈은 PDF 문서를 여러 개의 작은 문서로 분할합니다. 파일 수, 파일당 페이지 수 또는 페이지 범위별로 분할할지 여부를 지정합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택하십시오.</p> [!DNL Adobe PDF Services]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 대한 연결 만들기 를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split option]</td> 
   <td>파일을 분할할 방법을 선택합니다. 
   <ul>
   <li><p><b>페이지 범위</b></p><p>별도의 문서로 분할하려는 각 페이지 범위에 대해 <b>추가</b>를 클릭하고 시작할 페이지와 끝낼 페이지를 입력합니다.</p></li>
   <li><p><b>페이지 수</b></p><p>새 문서에 포함할 페이지 수를 입력합니다.</p></li>
   <li><p><b>파일 계정</b></p><p>문서를 분할할 파일 크기를 동일하게 입력합니다.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

