---
title: OpenAI(ChatGPT) 모듈
description: Adobe Workfront Fusion 시나리오에서는 OpenAIT(ChatGPT)를 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: c8138d82-fa5a-4e69-b3cb-aa232099cb33
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1389'
ht-degree: 0%

---

# [!DNL OpenAI (ChatGPT & DALL-E)]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL OpenAI (ChatGPT & DALL-E)]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 플랜*</td>
  <td> <p>[!UICONTROL Pro] 이상</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이센스*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td> <p>작업 자동화 및 통합을 위한 [!UICONTROL Workfront Fusion] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>이 문서에 설명된 기능을 사용하려면 조직에서 Adobe Workfront Fusion과 Adobe Workfront을 구매해야 합니다.</td> 
  </tr> 
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 Workfront 관리자에게 문의하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

## 전제 조건

[!DNL OpenAI (ChatGPT & DALL-E)] 모듈을 사용하려면 API 키와 조직 ID를 포함한 [!DNL OpenAI] 계정이 있어야 합니다.

## OpenAI(ChatGPT 및 DALL-E) API 정보

OpenAI(ChatGPT &amp; DALL-E) 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.11.1</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결 중

[!DNL OpenAI (ChatGPT & DALL-E)] 모듈 내에서 직접 [!DNL OpenAI (ChatGPT & DALL-E)] 계정에 연결할 수 있습니다.

1. [!DNL OpenAI (ChatGPT & DALL-E)] 모듈에서 **[!UICONTROL 연결]** 필드 옆에 있는 [!UICONTROL 추가]를 클릭합니다.
1. 다음 정보를 입력합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 이름]</p> </td> 
      <td> <p>새 연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API 키]</td> 
      <td>OpenAI 사용자 설정에서 API 키를 찾을 수 있습니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 조직 ID] </td> 
      <td>OpenAI의 조직 설정 페이지에서 조직 ID를 찾을 수 있습니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.


## [!DNL OpenAI (ChatGPT & DALL-E)]개 모듈 및 해당 필드

[!DNL OpenAI (ChatGPT & DALL-E)] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL OpenAI (ChatGPT & DALL-E)] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 완료 만들기

>[!IMPORTANT]
>
>이 모듈은 더 이상 사용되지 않습니다.

<!--

This action module creates a completion for the provided prompt or chat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Enter or map the ID of the model to use. You can use the Get models module to see all of your available models. </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Temperature]</td> 
   <td> This value must be between 0 and 2, and determines the randomness of the output. Higher values produce output that is more random, while lower values produce more focused output. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating completions in the <a href="https://platform.openai.com/docs/api-reference/completions/create" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### 중재 만들기

이 작업 모듈은 텍스트가 OpenAI의 콘텐츠 정책을 위반하는지 여부를 결정합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> 포함할 각 텍스트 샘플에 대해 <b>항목 추가</b>를 클릭하고 텍스트를 입력하거나 매핑합니다. 전체 텍스트 샘플을 포함합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델]</td> 
   <td> 사용할 모델의 ID를 입력하거나 매핑합니다. 모델 가져오기 모듈을 사용하여 사용 가능한 모든 모델을 볼 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

### 편집 만들기

이 작업 모듈은 사용자의 지침에 따라 사용자가 제공한 프롬프트의 편집된 버전을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델]</td> 
   <td> 사용할 모델의 ID를 입력하거나 매핑합니다. 모델 가져오기 모듈을 사용하여 사용 가능한 모든 모델을 볼 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> 편집할 텍스트를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 명령]</td> 
   <td> 편집에 대한 지침을 입력하거나 매핑합니다. 예: "맞춤법 오류 수정" </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 고급 설정]</td> 
   <td> <p>이 모듈의 선택적 고급 설정에 대한 자세한 내용은 <a href="https://platform.openai.com/docs/api-reference/edits/create" class="MCXref xref">OpenAI API 설명서</a>에서 편집 만들기에 대한 정보를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 포함 만들기

이 액션 모듈은 입력 텍스트를 나타내는 임베딩 벡터를 생성한다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델]</td> 
   <td> 사용할 모델의 ID를 입력하거나 매핑합니다. 모델 가져오기 모듈을 사용하여 사용 가능한 모든 모델을 볼 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 포함할 입력 텍스트]</td> 
   <td> 포함할 텍스트를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사용자 ID]</td> 
   <td> 최종 사용자를 나타내는 고유 식별자를 입력하거나 매핑하면 OpenAI가 남용을 모니터링하고 감지하는 데 도움이 됩니다 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> 각 시나리오 실행 주기 동안 모듈에서 작업할 최대 편집 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 채팅 만들기 완료

대화를 설명하는 메시지 목록이 주어지면 이 작업 모듈은 응답을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델]</td> 
   <td> 사용할 모델의 ID를 입력하거나 매핑합니다. 모델 가져오기 모듈을 사용하여 사용 가능한 모든 모델을 볼 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>메시지는 지금까지의 대화에 대해 설명합니다. 추가할 각 메시지에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.
   <ul>
   <li> <b>역할</b>: 이 메시지의 작성자 역할을 선택하십시오.</li>
   <li> <b>내용</b>: 이 메시지의 내용을 입력하거나 매핑합니다.</li>
   <li> <b>이름</b>: 이 메시지의 작성자 이름을 입력하거나 매핑합니다. 이름에는 대/소문자, 숫자 및 밑줄을 포함할 수 있습니다. 이름의 최대 길이는 64자입니다.</li>
   </ul>
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 고급 설정]</td> 
   <td> <p>이 모듈의 선택적 고급 설정에 대한 자세한 내용은 <a href="https://platform.openai.com/docs/api-reference/chat/create" class="MCXref xref">OpenAI API 설명서</a>에서 채팅 완료 만들기에 대한 정보를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Edit image

This action module makes edits or creates variations of existing images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to create edits or variations of the image.
   <p>NOTE: Images must be a valid PNG file, less than 4MB, and square. If mask is not provided, the image must have transparency, which will be used as the mask.</p> 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Text description of desired image]</td> 
   <td> <p>If editing an image, enter or map a description of the edits you want to create. Maximum length is 1000 characters.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating image edits or variations in the <a href="https://platform.openai.com/docs/api-reference/images/createEdit" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### 이미지 생성

이 작업 모듈은 Dall-E 모델로 이미지를 생성하거나 조작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 원하는 이미지의 텍스트 설명]</td> 
   <td> 원하는 이미지의 설명을 입력하거나 매핑합니다. 최대 설명 길이는 1000자입니다. 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 고급 설정]</td> 
   <td> <p>이 모듈의 선택적 고급 설정에 대한 자세한 내용은 <a href="https://platform.openai.com/docs/api-reference/images/create" class="MCXref xref">OpenAI API 설명서</a>에서 이미지 만들기에 대한 정보를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 모델 가져오기

이 모듈에서는 OpenAI API에서 사용할 수 있는 다양한 모델을 나열하고 설명합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> 모든 모델 목록을 가져올 것인지 특정 모델을 검색할 것인지 선택합니다.
    <ul>
    <li><p><b>목록 모델 </b></p><p>이 작업은 현재 사용 가능한 모델을 나열하고 소유자 및 가용성과 같은 각 모델에 대한 기본 정보를 제공합니다.</p></li>
    <li><p><b>모델 검색 </b></p><p>검색할 모델의 ID를 입력하거나 매핑합니다. </p></li>
   </ul>
 </td> 
  </tr>
 </tbody> 
</table>

### 사용자 지정 API 호출 만들기

이 작업 모듈은 OpenAI API에 대한 사용자 지정 HTTP 요청입니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p><code>https://api.openai.com/v1/</code>과(와) 관련된 경로 입력 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 인증 헤더를 자동으로 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Manage Audio

This action modules converts audio to text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to transcribe the audio into the input language, or into English.
   <p>If transcribing into the input language, you can select the language in this module's advanced settings. </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Enter or map the maximum number of edits you want the module to work with during each scenario execution cycle.</td> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating transcriptions in the <a href="https://platform.openai.com/docs/api-reference/audio/createTranscription" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

-->

### 파일 관리

이 작업 모듈은 파일 또는 파일 컨텐츠를 나열, 삭제 또는 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> 수행할 작업을 선택합니다. 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td> 파일을 삭제하거나 파일 또는 파일 내용을 검색하는 경우 파일 ID를 입력하거나 매핑합니다. 
  </tr> 
</tbody>
</table>

### 미세 조정 관리

특정 교육 데이터에 맞게 모델을 맞춤화하기 위해 세부 조정 작업을 관리합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL OpenAI (ChatGPT & DALL-E)] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL OpenAI (ChatGPT & DALL-E)] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 선택]</td> 
   <td> 수행할 작업을 선택합니다.
   <ul>
   <li><p>데이터 세트에서 모델 미세 조정</p><p>원하는 이미지에 대한 설명을 입력하거나 매핑합니다.</p>
     <li><p>미세 조정 작업에 대한 정보 가져오기</p><p>작업 ID를 입력하거나 매핑합니다.</p>
   <li><p>미세 조정 작업 취소</p><p>작업 ID를 입력하거나 매핑합니다.</p>
   <li><p>미세 조정 작업 취소</p><p>작업 ID를 입력하거나 매핑합니다.</p>
   <li><p>미세 조정 작업에 대한 상태 업데이트 가져오기</p><p>작업 ID를 입력하거나 매핑하고 이러한 업데이트를 스트리밍할지 여부를 선택합니다.</p>
   <li><p>미세 조정된 모델 삭제</p><p>삭제할 모델의 ID를 입력하거나 매핑합니다.</p>
 </ul> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td> 파일을 삭제하거나 파일 또는 파일 내용을 검색하는 경우 파일 ID를 입력하거나 매핑합니다. 
  </tr> 
</tbody>
