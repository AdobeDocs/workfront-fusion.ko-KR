---
title: Adobe PDF Services
description: Adobe PDF Services
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '4151'
ht-degree: 100%

---

# [!DNL Adobe PDF Services]

Adobe Workfront Fusion [!DNL Adobe PDF Services]를 사용하면 PDF 파일에서 데이터를 추출하거나 제공한 데이터에서 새 PDF 파일을 생성할 수 있습니다. 또한 다양한 파일 유형을 PDF로 변환하거나 PDF를 다른 파일 유형으로 변환할 수 있습니다. PDF Services를 사용하면 PDF 파일의 메타데이터를 결합, 압축 또는 읽을 수 있을 뿐만 아니라 파일의 암호 보호도 제어할 수 있습니다.

시나리오 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 색인](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

PDF Services에 사용되는 API에 대한 자세한 내용은 [Adobe Document Generation API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html)를 참조하십시오.

## [!DNL Adobe PDF Services]를 사용할 때의 보안 고려 사항

[!DNL Adobe PDF Services]는 파일을 읽거나 변환하거나 수정할 수 있지만, [!DNL Adobe]나 Workfront Fusion은 파일이나 데이터를 저장하지 않습니다. 이것의 의미는 다음과 같습니다.

* 보안을 포함한 파일에 대한 통제권을 유지합니다.
* PDF Services를 사용하기 위해 [!UICONTROL Adobe] 스토리지 또는 클라우드 스토리지 계정이 필요하지 않습니다.

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

OAuth 서버 간 연결을 만들려면 Adobe Developers Console에 Adobe PDF Services API를 추가해야 합니다. API를 추가할 때, OAuth 서버 간 옵션을 선택합니다.

자세한 내용은 Adobe 개발자 설명서에서 [OAuth 사용자 인증 자격 증명을 사용하여 API를 프로젝트에 추가](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication)를 참조하십시오.

## Adobe PDF Services API 정보

Adobe PDF Services 커넥터는 다음을 사용합니다.

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

## [!DNL Adobe PDF Services]에 연결하기

사용자의 [!DNL Adobe PDF Services] 모듈에 연결하려면:

1. 모든 [!DNL Adobe PDF Services] 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 연결 유형]</td>
          <td>
            <p>서버 간 연결할지 JWT 연결할지 선택합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 연결 이름]</td>
          <td>
            <p>이 연결의 이름을 입력합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 기술 계정 ID] (JWT만 해당)</td>
          <td>[!DNL Adobe] [!UICONTROL 기술 계정 ID]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 조직 ID] (JWT만 해당)</td>
          <td>[!DNL Adobe] [!UICONTROL 조직 ID]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Meta 범위] (JWT만 해당)</td>
          <td>
            연결에 필요한 메타 범위를 입력합니다.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 비공개 키]</td>
        <td>
          <p>JWT 연결을 선택한 경우 [!DNL Adobe Developer Console]에서 자격 증명을 만들 때 생성된 비공개 키를 입력합니다. </p>
          <p>비공개 키 또는 인증서를 추출하려면 다음을 수행합니다.</p>
          <ol>
            <li value="1">
              <p><b>[!UICONTROL 추출]</b>을 클릭합니다.</p>
            </li>
            <li value="2">
              <p>추출할 파일 유형을 선택합니다.</p>
            </li>
            <li value="3">
              <p>비공개 키 또는 인증서가 포함된 파일을 선택합니다.</p>
            </li>
            <li value="4">
              <p>파일의 암호를 입력합니다.</p>
            </li>
            <li value="5">
              <p><b>[!UICONTROL 저장]</b>을 클릭하여 파일을 추출하고 연결 설정으로 돌아갑니다.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.


## [!DNL Adobe PDF Services] 모듈 및 해당 필드

[!DNL PDF Services]를 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 수준과 같은 요인에 따라 추가적인 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL PDF 파일 결합]](#combine-pdf-files)
* [[!UICONTROL PDF 파일 압축]](#compress-pdf-files)
* [[!UICONTROL 문서를 PDF 파일로 변환]](#convert-document-to-pdf-file)
* [[!UICONTROL HTML을 PDF 파일로 변환]](#convert-html-to-pdf-file)
* [[!UICONTROL 이미지를 PDF 파일로 변환]](#convert-image-to-pdf-file)
* [[!UICONTROL PDF를 문서로 변환]](#convert-pdf-to-document)
* [[!UICONTROL PDF를 이미지로 변환]](#convert-pdf-to-image)
* [[!UICONTROL 텍스트 / 테이블 추출]](#extract-text--table)
* [[!UICONTROL 문서 생성]](#generate-document)
* [[!UICONTROL PDF 파일 선형화]](#linearize-a-pdf-file)
* [사용자 정의 API 호출하기](#make-a-custom-api-call)
* [[!UICONTROL PDF 파일용 OCR]](#ocr-for-pdf-file)
* [[!UICONTROL 페이지 조작]](#page-manipulation)
* [[!UICONTROL PDF 접근성 자동 태그]](#pdf-accessibility-auto-tag)
* [[!UICONTROL PDF 파일 속성]](#pdf-file-properties)
* [[!UICONTROL PDF 파일 보호]](#protect-pdf-file)
* [[!UICONTROL PDF 파일 보호 제거]](#remove-protection-of-a-pdf-file)
* [PDF 파일 분할](#split-a-pdf-file)

### [!UICONTROL PDF 파일 결합]

이 액션 모듈은 여러 PDF 파일을 가져와서 하나의 PDF 파일로 결합합니다. 예를 들어, 이 모듈은 프로젝트가 완료되면 [!UICONTROL Workfront] 프로젝트의 모든 문서를 하나의 PDF로 결합할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서]</td> 
   <td> <p>집계기 모듈을 사용하여 PDF로 결합할 문서를 수집하거나 문서를 수동으로 추가할 수 있습니다. </p> <p>이전 모듈의 출력을 집계하기 위해 [!UICONTROL 배열 집계기] 모듈을 사용하는 것을 권장합니다. 집계기를 사용하면 결합할 파일의 이름, 위치 또는 개수를 알 필요가 없습니다. 따라서 집계기를 사용하면 결합할 문서를 수동으로 입력하는 것보다 훨씬 유연하고 확장이 쉽습니다.</p> <p>[!UICONTROL PDF 결합] 파일 모듈을 집계기와 함께 사용하려면 [!UICONTROL 문서] 필드에서 매핑을 활성화해야 합니다. </p> <p>이 예제에서 [!UICONTROL 관련 레코드 읽기] 모듈은 프로젝트와 관련된 문서를 식별하고, [!UICONTROL 문서 다운로드] 모듈은 각 문서를 다운로드합니다. 모든 PDF는 배열로 집계되며, [!UICONTROL PDF 결합] 파일 모듈로 전달됩니다.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>문서를 수동으로 입력할 수도 있습니다.</p> <p>결합된 PDF에 포함할 각 문서의 경우:</p> 
    <ol> 
     <li value="1"> <p>[!UICONTROL 문서 추가]를 클릭합니다.</p> </li> 
     <li value="2"> <p>[!UICONTROL 소스 파일] 필드에서 포함할 문서를 출력하는 모듈을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다. </p> </li> 
     <li value="3"> <p>(선택 사항) 소스 파일에서 특정 페이지만 포함하려면 추가할 각 페이지 범위에 대해 [!UICONTROL 페이지] 필드에서 <strong>[!UICONTROL 항목 추가]</strong>를 클릭한 다음 페이지 범위의 첫 번째와 마지막 페이지를 입력하여 <strong>[!UICONTROL 추가]</strong>를 클릭합니다. 하나의 문서에서 두 개 이상의 페이지 범위를 포함할 수 있습니다.</p> </li> 
     <li value="4"> <p><strong>[!UICONTROL 추가]</strong>를 클릭합니다. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 파일 압축]

이 액션 모듈은 PDF 파일을 가져와 압축합니다. 이는 대역폭이나 메모리를 절약하는 데 유용할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 압축 수준]</td> 
   <td>사용할 압축 수준을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 문서를 PDF 파일로 변환]

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
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
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
   <td role="rowheader">[!UICONTROL 언어]</td> 
   <td> <p>소스 문서의 기본 언어를 선택합니다. 이를 통해 모듈은 소스 파일에 포함되지 않은 글꼴을 적절한 글꼴로 선택할 수 있습니다.</p> <p>다음 언어 중에서 선택합니다.</p> 
    <ul> 
     <li> <p>en-US(기본값): 영어(미국)</p> </li> 
     <li> <p>ca-ES: 카탈로니아어(스페인)</p> </li> 
     <li> <p>cs-CZ: 체코어(체코)</p> </li> 
     <li> <p>da-DK: 덴마크어(덴마크)</p> </li> 
     <li> <p>de-DE: 독일어(독일)</p> </li> 
     <li> <p>en-AE: 영어(아랍에미리트)</p> </li> 
     <li> <p>en-GB: 영어(영국)</p> </li> 
     <li> <p>en-IL: 영어(이스라엘)</p> </li> 
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
     <li> <p>nb-NO: 노르웨이어 부크몰(노르웨이)</p> </li> 
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

### [!UICONTROL HTML을 PDF 파일로 변환]

이 도구는 HTML 파일을 PDF 파일로 변환합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>중요: 소스 파일은 HTML 또는 ZIP 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>HTML에서 JavaScript 변수를 참조하는 경우, 여기에 해당 변수를 포함할 수 있습니다. </p> <p>각 변수에 대해 <strong>[!UICONTROL 항목 추가]</strong>를 클릭하고 변수의 키와 값을 포함합니다.</p> <p>메모:   
     <ul> 
      <li> <p>ZIP 파일에서 PDF를 만들 때 소스 자료에는 <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code>과(와) 같은 스크립트 요소가 포함되어야 합니다. </p> </li> 
      <li> <p>URL에서 PDF를 만들 때, 페이지가 렌더링되기 전에 이 JSON 오브젝트의 콘텐츠가 브라우저 VM에 삽입됩니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 머리글 및 바닥글 포함]</td> 
   <td> <p>PDF 문서의 머리글과 바닥글을 만들려면 이 옵션을 활성화합니다.</p> 
    <ul> 
     <li> <p>머리글에는 날짜와 문서 제목이 포함됩니다.</p> </li> 
     <li> <p>바닥글에는 파일 이름과 페이지 번호가 포함되어 있습니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지 폭]</td> 
   <td>종이의 폭을 인치 단위로 입력합니다. 모듈은 이 정보를 사용하여 생성된 PDF 파일의 페이지 형식을 지정합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지 높이]</td> 
   <td>종이의 높이를 인치 단위로 입력합니다. 모듈은 이 정보를 사용하여 생성된 PDF 파일의 페이지 형식을 지정합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 이미지를 PDF 파일로 변환]

이 도구는 이미지를 PDF 파일로 변환합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 이미지 파일을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF를 문서로 변환]

이 도구는 PDF 파일을 문서로 변환합니다. 출력 파일 형식 중 하나를 선택할 수 있습니다.

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
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력 파일 형식]</td> 
   <td> <p>파일을 출력할 형식을 선택합니다.</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 언어]</td> 
   <td> <p>소스 문서의 기본 언어를 선택합니다. 이를 통해 모듈은 소스 파일에 포함되지 않은 글꼴을 적절한 글꼴로 선택할 수 있습니다.</p> <p>다음 언어 중에서 선택합니다.</p> 
    <ul> 
     <li> <p>en-US(기본값): 영어(미국)</p> </li> 
     <li> <p>ca-ES: 카탈로니아어(스페인)</p> </li> 
     <li> <p>cs-CZ: 체코어(체코)</p> </li> 
     <li> <p>da-DK: 덴마크어(덴마크)</p> </li> 
     <li> <p>de-DE: 독일어(독일)</p> </li> 
     <li> <p>en-AE: 영어(아랍에미리트)</p> </li> 
     <li> <p>en-GB: 영어(영국)</p> </li> 
     <li> <p>en-IL: 영어(이스라엘)</p> </li> 
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
     <li> <p>nb-NO: 노르웨이어 부크몰(노르웨이)</p> </li> 
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

### [!UICONTROL PDF를 이미지로 변환]

이 도구는 PDF를 PNG 또는 JPEG 형식의 이미지로 변환한 다음 목록으로 출력하거나 ZIP로 결합합니다.

ZIP로 출력하면 PDF는 페이지당 하나의 이미지로 변환되고 각 이미지는 페이지 번호로 끝납니다. 그런 다음 이미지 파일이 ZIP 파일로 결합됩니다.

예를 들어, 8페이지 분량의 “TestFile”이라는 파일은 “TestFile_1”이라는 이름의 8개의 이미지를 “TestFile_8”까지 생성합니다. 모듈의 출력은 8개의 이미지가 포함된 ZIP 파일입니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력 파일 형식]</td> 
   <td> <p>파일을 출력할 형식을 선택합니다.</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력 유형]</td> 
   <td> <p>파일을 파일 목록으로 출력할지 ZIP 파일로 출력할지 선택합니다.</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL 텍스트 / 테이블 추출]

이 액션 모듈을 사용하면 PDF 파일에서 데이터를 추출할 수 있습니다. 모듈은 단락이나 텍스트와 같은 개별 텍스트 요소를 테이블의 단일 셀에 출력합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON으로 추출해야 하는 요소]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL 텍스트]</p> </li> 
     <li> <p>[!UICONTROL 테이블]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테두리 상자 추출?]</td> 
   <td>텍스트의 테두리 상자에 대한 데이터를 추출하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력에 대한 스타일 정보를 포함하시겠습니까?]</td> 
   <td>출력 JSON에 스타일 정보를 추가하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 문서 생성]

[!UICONTROL 문서 생성] 모듈은 선택한 데이터가 포함된 PDF를 만드는 강력한 방법입니다. [!DNL Microsoft Word] 템플릿을 사용하거나 JSON 형식으로 데이터를 제공하여 형식을 지정할 수 있습니다.

[!UICONTROL [!DNL Adobe PDF Services]문서 생성] 기능에 대한 자세한 내용은 [!DNL Adobe Document Services] 설명서의 [문서 생성 개요](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html)를 참조하십시오.

* [ [!DNL Microsoft Word] 템플릿](#use-the-generate-document-module-with-a-microsoft-word-template)을 사용하여 [!UICONTROL 문서 생성] 모듈 사용
* [JSON을 사용하여 [!UICONTROL 문서 생성] 모듈 사용](#use-the-generate-document-module-with-json)

#### [!DNL Microsoft Word] 템플릿을 사용하여 [!UICONTROL 문서 생성] 모듈 사용


>[!NOTE]
>
>Microsoft Word 템플릿에 대한 설명은 [Microsoft Word 템플릿 모듈](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md)을 참조하십시오.
>
>PDF Services 문서 생성 모듈을 사용하여 Microsoft Word 템플릿을 사용하려면 Microsoft Word 템플릿 모듈을 사용할 필요가 없습니다.


[!UICONTROL Microsoft Word] 템플릿을 사용하여 [!UICONTROL 생성 문서] 모듈을 사용하려면 먼저 템플릿을 만들어야 합니다. 지침은 [!DNL Microsoft Office] 설명서에서 “템플릿 만들기”를 검색합니다.

다음과 같이 [!UICONTROL 문서 생성] 모듈 필드를 채웁니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>이 소스 파일은 모듈이 새 PDF를 생성하는 데 사용하는 [!DNL Microsoft Word] 템플릿입니다.</p> <p>Workfront Fusion에서 사용하는 [!DNL Microsoft Word] 템플릿에 대해 Workfront에서 프로젝트를 만드는 것이 좋습니다. 그런 다음 Workfront &gt; [!UICONTROL 문서 다운로드] 모듈을 사용하여 적절한 템플릿을 시나리오로 가져올 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력 형식]</td> 
   <td> <p>생성된 문서의 형식을 선택합니다.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 병합용 데이터]</td> 
   <td> <p>템플릿에서 텍스트로 대체할 각 값 태그에 대해 다음을 입력합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 키]</p> <p>키를 입력합니다. 템플릿에서 키는 값 태그에 표시되는 텍스트입니다. 예를 들어 값 태그 <code>&#123;&#123;name&#125;&#125;</code>에 텍스트를 삽입하려면 키 필드에 <code>name </code>를 입력합니다.</p> </li> 
     <li> <p>값 유형</p> <p>값 필드의 데이터가 값인지, 오브젝트인지, 오브젝트 배열인지 선택합니다.</p> </li> 
     <li> <p>[!UICONTROL 값]</p> <p>생성된 문서에 표시할 텍스트를 값 태그 대신 입력하거나 매핑합니다.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### JSON을 사용하여 [!UICONTROL 문서 생성] 모듈 사용

JSON을 사용하여 [!UICONTROL 문서 생성] 모듈을 사용하려면 다음과 같이 필드를 채우십시오.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력 형식]</td> 
   <td> <p>생성된 문서의 형식을 선택합니다.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 병합용 데이터]</td> 
   <td> <p>이 모듈에서 JSON을 사용하려면 이 필드에서 매핑을 활성화해야 합니다.</p> <p>문서를 생성할 JSON을 입력하거나 매핑합니다. </p> <p>JSON을 이 필드에 직접 입력하거나 JSON 모듈에서 JSON 출력을 매핑할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 파일 선형화]

이 도구는 PDF 문서를 선형화하여 웹에 최적화된 PDF 문서를 만듭니다. 선형화된 PDF 문서는 전체 문서를 다운로드할 필요 없이 페이지별로 볼 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용자 정의 API 호출하기

이 액션 모듈은 PDF Services API에 대한 사용자 정의 HTTP 요청입니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> 상대 경로 또는 URL을 입력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>예: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td> <p>API 호출에 추가할 각 필드에 대해 <b>항목 추가</b>를 클릭하고 필드의 키와 선택 값을 입력합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL PDF 파일용 OCR]

이 도구는 파일에 대해 광학 문자 인식(OCR)을 수행하고 PDF를 생성합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 언어]</td> 
   <td>이 문서의 언어를 선택합니다.<p>언어 옵션은 이 문서에서 <a href="#convert-document-to-pdf-file" class="MCXref xref" >문서를 PDF 파일로 변환</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR 유형]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL 수정된 원본 이미지] 유형은 텍스트를 검색하고 선택할 수 있지만, 정리 프로세스에서 원본 이미지를 수정(예: 유지)한 후 보이지 않는 텍스트 레이어를 그 위에 놓습니다. 이 유형은 원치 않는 아티팩트를 제거하고 일부 시나리오에서는 문서를 더 읽기 쉽게 만들 수 있습니다. </p> </li> 
     <li> <p>[!UICONTROL 변경되지 않은 원본 이미지] 유형은 원본 이미지 위에 검색 가능한 텍스트 레이어를 오버레이하지만, 이 경우 원본 이미지는 변경되지 않습니다. 이 유형은 원본 이미지에 대한 최대 충실도를 생성합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 페이지 조작]

이 모듈을 사용하면 PDF 문서에서 페이지를 선택적으로 회전하거나 삭제할 수 있습니다. 예를 들어, 세로 보기를 가로 보기로 변경하거나 PDF 문서에서 특정 페이지를 제거할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 액션]</td> 
   <td> <p>파일에서 수행할 액션을 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL 삭제]</b> </p> <p>문서에서 페이지를 삭제하려면 이 옵션을 선택합니다.</p><p>삭제할 각 페이지 범위에 대해 <strong>[!UICONTROL 추가]</strong>를 클릭한 다음 페이지 범위의 첫 번째 페이지와 마지막 페이지를 입력합니다. </p> <p>메모:   
     <ul> 
      <li> <p>음수를 사용하여 문서 끝 부분부터 다시 계산할 수 있습니다. 문서의 마지막 페이지는 -1, 두 번째에서 마지막 페이지는 -2입니다.</p> </li> 
      <li> <p>단일 페이지를 삭제하려면 범위의 시작 및 끝과 동일한 페이지 번호를 설정합니다.</p></ul> </li> 
     <li> <p><b>[!UICONTROL 회전]</b> </p> <p>페이지를 회전하려면 이 옵션을 선택한 다음 문서 페이지의 시작 방향을 기준으로 회전할 각도를 시계 방향으로 입력합니다.</p> <p>세로에서 가로로 또는 그 반대로 회전하려면 페이지를 90도 또는 270도 회전합니다.</p> <p>페이지가 거꾸로 되어 있으면 180도 회전합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지]</td> 
   <td> <p>삭제할 각 페이지 범위에 대해 <strong>[!UICONTROL 추가]</strong>를 클릭한 다음 페이지 범위의 첫 번째 페이지와 마지막 페이지를 입력합니다. </p> <p>메모:   
     <ul> 
      <li> <p>음수를 사용하여 문서 끝 부분부터 다시 계산할 수 있습니다. 문서의 마지막 페이지는 -1, 두 번째에서 마지막 페이지는 -2입니다.</p> </li> 
      <li> <p>단일 페이지를 삭제하려면 범위의 시작 및 끝과 동일한 페이지 번호를 설정합니다.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 작업할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 접근성 자동 태그]

이 액션 모듈은 접근성 사용 사례에 태그가 지정된 PDF를 만듭니다. 또한 문제를 나열하고 수정 사항을 제안하는 선택적 Microsoft Excel 보고서를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제목 변경]</td> 
   <td> <p>문서의 제목을 변경하려면 이 옵션을 활성화합니다.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보고서 생성]</td> 
   <td> <p>PDF의 접근성 문제와 위치를 나열하고 이러한 문제를 해결하는 방법에 대한 제안을 제공하는 보고서를 생성하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 파일 속성]

이 도구는 문서에 대한 기본 정보를 추출합니다.

* 페이지 카운트
* PDF 버전
* 파일의 암호화 여부
* 파일의 선형화 여부
* 파일에 임베드된 파일 포함 여부

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 파일 보호]

이 도구는 사용자 또는 소유자 암호로 PDF 문서를 보호합니다. 또한 PDF 문서의 인쇄, 편집, 복사와 같은 특정 기능에 대한 제한을 설정합니다. 암호화할 콘텐츠 유형과 암호화 알고리즘을 선택합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 암호 보호 유형]</td> 
   <td> <p>암호를 사용하여 입력 PDF 문서를 암호화하려면 이 옵션을 활성화합니다. 이 옵션을 활성화하면 다음 중 하나 또는 모두에 대한 값을 지정하고 입력해야 합니다. </p> 
    <ul> 
     <li> <p>[!UICONTROL 사용자 암호]</p> </li> 
     <li> <p>[!UICONTROL 소유자 암호] </p> </li> 
    </ul> <p>각 암호는 최대 128자까지 가능합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 암호화 알고리즘]</td> 
   <td> <p>암호화 알고리즘을 선택합니다. </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128 암호화]</p> <p>암호는 LATIN-I 문자만 지원합니다. </p> </li> 
     <li> <p>[!UICONTROL AES-256 암호화]</p> <p>암호는 유니코드 문자 세트를 지원합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 암호화할 콘텐츠]</td> 
   <td> <p>암호화할 콘텐츠의 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 모든 콘텐츠]</p> </li> 
     <li> <p>[!UICONTROL 메타데이터를 제외한 모든 콘텐츠]</p> </li> 
     <li> <p>[!UICONTROL 임베드된 데이터만] </p> </li> 
    </ul> <p>“[!UICONTROL 임베드된 데이터만]”을 선택하면 제공된 모든 액세스 권한이 무효화됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 권한]</td> 
   <td> <p>인쇄, 편집 또는 콘텐츠 복사를 허용하도록 포함할 권한을 선택합니다.</p> <p>권한 설정은 [!UICONTROL 암호 보호 유형] 필드에 [!UICONTROL 소유자 암호]가 설정된 경우에만 사용됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 파일 보호 제거]

이 도구는 PDF 문서에서 보안(암호 보호)을 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 암호]</td> 
   <td>현재 파일을 보호하는 암호를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 파일 분할]

이 액션 모듈은 PDF 문서를 여러 개의 작은 문서로 분할합니다. 파일 수, 파일당 페이지 수 또는 페이지 범위별로 분할할지 여부를 지정합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>이 모듈에 사용할 연결을 선택합니다.</p> [!DNL Adobe PDF Services]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >[!DNL Adobe PDF Services]</a>에 연결하기를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> <p>소스 파일은 PDF 형식이어야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 분할 옵션]</td> 
   <td>파일을 분할할 방법을 선택합니다. 
   <ul>
   <li><p><b>페이지 범위</b></p><p>각 페이지 범위를 별도의 문서로 분할하려면 <b>추가</b>를 클릭하고 시작할 페이지와 종료할 페이지를 입력합니다.</p></li>
   <li><p><b>페이지 카운트</b></p><p>새 문서에 포함할 페이지 수를 입력합니다.</p></li>
   <li><p><b>파일 카운트</b></p><p>문서를 분할할 파일 크기를 동일하게 입력합니다.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

