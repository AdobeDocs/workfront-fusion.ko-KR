---
title: Adobe Firefly 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는  [!DNL Adobe Firefly]을(를) 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 200907bb8d80f874227493b489ef1ea450198dc6
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 0%

---

# [!DNL Adobe Firefly]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Adobe Firefly]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스</td> 
   <td> <p>신규: [!UICONTROL Standard]</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Workfront] 플랜: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 플랜 [!DNL Workfront Fusion]이(가) 포함되어 있습니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

## 전제 조건

[!DNL Adobe Firefly] 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 [!DNL Adobe Firefly] 계정이 있어야 합니다.

## Adobe Firefly API 정보

Adobe Firefly 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Adobe Firefly]에 연결 만들기

[!DNL Adobe Firefly] 모듈에 대한 연결을 만들려면:

1. 연결 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>[!UICONTROL Adobe] [!UICONTROL Client ID]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials] 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>[!DNL Adobe] [!UICONTROL Client Secret]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials] 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## [!DNL Adobe Firefly]개 모듈 및 해당 필드

[!DNL Adobe Firefly] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Adobe Firefly] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 사용자 지정 API 호출 만들기

이 작업 모듈은 Firefly API에 대한 사용자 지정 호출을 만듭니다.

사용 가능한 특정 API에 대해서는 Adobe Developer 설명서에서 [Adobe Firefly API](https://developer.adobe.com/firefly-services/docs/firefly-api/)를 참조하십시오.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Firefly]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p><code>https://firefly-api-enterprise-stage.adobe.io/</code>과(와) 관련된 경로를 입력하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 인증 헤더를 자동으로 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### 이미지 확장

이 작업 모듈은 선택적으로 사용자가 제공하는 프롬프트의 콘텐츠로 이미지를 확장합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>이미지를 확장할 내용에 대한 프롬프트를 입력하거나 매핑합니다. 프롬프트가 제공되지 않으면 이미지가 원본 이미지와 일치하는 콘텐츠로 확장됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 확장된 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expanded image format]</td> 
   <td>확장된 이미지를 저장할 파일 형식을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>  <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이미지 파일 이름과 이미지 파일(데이터)을 매핑합니다.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>확장된 이미지를 표시할 크기를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>정수를 입력하거나 매핑합니다. 다른 이미지 모듈 확장에서 이와 동일한 시드를 사용하여 스타일이 다른 유사한 이미지를 생성할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

## 이미지 채우기

이 작업 모듈은 이미지의 마스킹된 영역을 채우며, 원할 경우 제공하는 프롬프트의 콘텐츠로 채웁니다.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>이미지를 채울 콘텐츠에 대한 프롬프트를 입력하거나 매핑합니다. 프롬프트가 제공되지 않으면 이미지는 원본 이미지와 일치하는 콘텐츠로 채워집니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 채워진 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filled image format]</td> 
   <td>채워진 이미지를 저장할 파일 형식을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image]</td> 
   <td>  <p> <b>이미지 추가</b>를 클릭합니다. 이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이미지 파일 이름과 이미지 데이터를 매핑합니다.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask]</td> 
   <td>  <p> <b>마스크 추가</b>를 클릭합니다. 이전 모듈에서 소스 파일을 선택하거나 소스 파일의 마스크 파일 이름과 마스크 데이터를 매핑합니다. 마스크 파일은 생성된 콘텐츠로 채워질 사용자 지정 마스크를 나타냅니다.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>채워진 이미지를 표시할 크기를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>모듈에서 생성할 각 이미지에 대해 <b>항목 추가<b>를 클릭하고 정수를 입력하거나 매핑합니다. 다른 이미지 모듈 확장에서 이와 동일한 시드를 사용하여 스타일이 다른 유사한 이미지를 생성할 수 있습니다. 추가하는 시드 수는 변형 수 필드와 같아야 합니다.</td> 
  </tr> 
 </tbody> 
</table>

## 이미지 생성

이 작업 모듈은 사용자가 제공한 프롬프트를 기반으로 및 이미지를 생성합니다. 선택적 참조 이미지를 제공할 수도 있으며, 생성된 이미지는 참조 이미지의 스타일과 일치합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>만들려는 이미지에 대한 프롬프트를 입력하거나 매핑합니다. 프롬프트에 자세히 설명되어 있으면 이미지에 나타나는 내용을 보다 세밀하게 제어할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>확장된 이미지를 저장할 파일 형식을 선택합니다. 기본값을 선택하면 참조 이미지가 제공되지 않으면 파일 형식이 JPEG이 됩니다. 기준 이미지가 제공된 경우, 생성된 이미지의 파일 포맷은 기준 이미지와 동일할 것이다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>  <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일(데이터)을 매핑합니다. 생성된 이미지는 참조 이미지의 스타일과 일치하도록 만들어집니다.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presets]</td> 
   <td>사전 설정 스타일을 사용하려면 항목 추가 를 클릭하고 사용할 스타일을 입력하거나 매핑합니다.<p>사전 설정된 스타일 목록을 보려면 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >이미지 모델 스타일</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Negative prompt]</td> 
   <td>생성된 콘텐츠에서 피하려는 단어를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content class]</td> 
   <td>생성된 이미지를 사진과 같은 이미지로 할지 또는 생성된 아트와 같은 이미지로 할지 선택합니다. <ul><li><b>사진</b><p>조리개, 셔터 속도(초) 및 시야(밀리미터)의 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>정수를 입력하거나 매핑합니다. 다른 이미지 모듈 확장에서 이와 동일한 시드를 사용하여 스타일이 다른 유사한 이미지를 생성할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>생성된 이미지를 표시할 크기를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strength]</td> 
   <td>생성된 이미지가 사전 설정된 스타일 또는 참조 이미지의 스타일과 일치하는 강도를 나타내는 정수를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visual intensity]</td> 
   <td>사진의 기존 시각적 특성의 전체 강도를 나타내는 정수를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>로케일이 제공되면 모듈은 지정된 로케일과 더 관련이 있는 콘텐츠를 생성합니다. <p>로케일은 ISO 639-1 언어 코드 및 ISO 3166-1 지역에서 제공해야 합니다.</p><p> 예: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>
