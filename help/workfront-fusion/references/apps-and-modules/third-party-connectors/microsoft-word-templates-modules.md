---
title: Microsoft Word 템플릿 모듈
description: Adobe Workfront Fusion 시나리오에서는 Microsoft Word 템플릿을 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: a5ba5634-226b-4886-a4f1-3a14948c1605
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 0%

---

# [!DNL Microsoft Word Template]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Microsoft Word Templates]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>조직에서 이 문서에 설명된 기능을 사용하려면 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구입해야 합니다.</td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Access level configurations*</td> 
    <td> 
      <p>You must be a Workfront Fusion administrator for your organization.</p>
     --> <!--
      <p>You must be a Workfront Fusion administrator for your team.</p>
     --> </td> 
   </tr>
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

## 전제 조건

[!DNL Adobe Workfront Fusion]에 [!DNL Miscrosoft Word Templates]을(를) 사용하려면 [!DNL Office 365] 계정이 있어야 합니다. `www.office.com`에서 만들 수 있습니다.



## [!DNL Workfront Fusion]에 [!DNL Office] 서비스를 연결하는 중

[!DNL Office] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하세요.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.

## [!DNL Microsoft Word Templates]개 모듈 사용

[!DNL Microsoft Word Template] 모듈을 사용하여 여러 웹 서비스의 데이터를 [!DNL Microsoft Word] 문서로 병합할 수 있습니다.

예를 들어 이 [!DNL Microsoft Word] 템플릿을 사용할 수 있습니다.

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-before-filled-350x62.png)

이 문서를 만들려면 다음 작업을 수행하십시오.

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-exampled-filled-350x85.png)

## 값 태그 정보

[!DNL Microsoft Word] 템플릿은 데이터를 병합하거나 채우는 위치와 방법을 결정하는 특수 태그가 텍스트에 포함된 일반 [!DNL Microsoft Word] 문서(.docx 파일)입니다. 태그는 다음 세 가지 유형이 있습니다.

* [단순 값 태그](#simple-value-tag)
* [조건 태그](#condition-tag)
* [루프 태그](#loop-tag)

### 단순 값 태그 {#simple-value-tag}

단순 값 태그는 해당 값으로 간단히 대체됩니다. 태그의 이름은 이중 중괄호 안에 있는 [!UICONTROL Key] 필드의 값에 해당합니다(예: `{{name}}`).

**예:** &quot;안녕하세요!&quot;라는 문서를 만들려면 [!DNL Microsoft Word Template] 모듈을 사용하여 다음 템플릿을 만들 수 있습니다.

```
> Hi {{name}}!
```

이렇게 하려면 다음과 같이 모듈을 설정합니다.

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-simple-value-350x286.png)

### 조건 태그 {#condition-tag}

조건 태그를 사용하여 특정 조건이 충족될 때만 렌더링해야 하는 텍스트를 줄 바꿈할 수 있습니다. 텍스트를 둘러싸려면 데이터에 전화번호가 포함되는지 여부가 조건에 해당하는 경우 &quot;hasPhone&quot;과 같이 여는 조건 태그와 닫는 조건 태그 사이에 텍스트를 배치합니다. 여는 태그의 이름 앞에는 # 해시 기호가 사용되고, 닫는 태그의 이름 앞에는 아래 예와 같이 슬래시 / 기호가 추가됩니다.

**예:** 입력 데이터에 전화번호가 있지만 전자 메일 주소가 없는 경우 고객의 전화번호가 포함된 문서를 만들려면 [!DNL Microsoft Word Template] 모듈을 사용하여 다음 템플릿을 만들 수 있습니다.

```
> {{#hasPhone}}Phone: {{phone}} {{/hasPhone}}
> {{#hasEmail}}Email: {{email}} {{/hasEmail}}
```

이렇게 하려면 다음과 같이 모듈을 설정합니다.

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-conditional-350x501.png)

이 문서에서 전화 번호는 다음과 같이 표시됩니다.

```
> Phone: 4445551234
```

### 루프 태그 {#loop-tag}

루프 태그(섹션 태그)를 사용하여 텍스트 섹션을 반복할 수 있습니다. 열기 및 닫기 루프 태그 사이에 텍스트를 배치하여 텍스트를 줄바꿈합니다. 여는 태그의 이름 앞에는 # 해시 기호가 붙고, 닫는 태그의 이름 앞에는 슬래시 / 기호가 붙습니다.

* [문서 모듈 채우기로 태그 반복](#loop-tag-with-fill-out-a-document-module)
  <!-- [Loop tag with Fill a document with a batch of data module](#loop-tag-with-fill-a-document-with-a-batch-of-data-module)-->

#### 문서 모듈 채우기로 태그 반복 {#loop-tag-with-fill-out-a-document-module}

**예:** 고객 목록에 있는 각 연락처의 이름과 전화 번호가 나열된 문서를 만들려면 [!DNL Microsoft Word Template] 모듈을 사용하여 다음 템플릿을 만들 수 있습니다.

```
> {{#contact}}
>     {{name}}, {{phone}}
> {{/contact}}
```

이렇게 하려면 다음과 같이 모듈을 설정합니다.


![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-fill-out-a-document-350x732.png)

모듈은 다음 문서를 만듭니다.

```
> Jan Toman, 4445551234
> Eduard Salo, 4445552345
```

<!--

#### Loop tag with Fill a document with a batch of data module {#loop-tag-with-fill-a-document-with-a-batch-of-data-module}

**Example:** You can export Google contacts into a table that you create using loop tags.

The first module loads the template. The next module retrieves all contacts from the group you specify in [!DNL Google Contacts]. The aggregator module aggregates all values retrieved from Google Contacts and merges them into the template. And the last module saves the filled template to the desired location.

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-scenario-350x124.png)

You could use this scenario with the following template:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-template-350x26.png)

To do this, you would set up the module as follows:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-module-setup-350x323.png)

The module would create the following document:

![](/help/workfront-fusion/references/apps-and-modules/assets/word-template-batch-document-350x46.png)
-->

## [!DNL Microsoft Word Template]개 모듈

이러한 모듈은 연결할 필요가 없습니다.

* [문서 작성](#fill-out-a-document)
* [데이터 배치로 문서 채우기](#fill-a-document-with-a-batch-of-data)

### [!UICONTROL Fill out a document] {#fill-out-a-document}

이 변환기 모듈을 사용하면 지정한 데이터로 문서를 채울 수 있습니다. 단순 값 태그, 조건부 태그 또는 루프 태그와 함께 사용할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>바꿀 텍스트의 시작 부분을 표시할 문자를 입력합니다. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>다음 텍스트와 유사한 텍스트를 바꾸려면 <code>&#91;&#91;</code>을(를) 입력하십시오. <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>바꿀 텍스트의 끝을 표시할 문자를 입력합니다. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>다음 텍스트와 유사한 텍스트를 바꾸려면 <code>&#93;&#93;</code>을(를) 입력하십시오. <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> 이전 모듈에서 업로드할 파일을 매핑합니다(예: HTTP &gt; 파일 가져오기 또는 Dropbox &gt; 파일 모듈 가져오기). 또는 데이터 파일을 수동으로 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>대상 출력 파일의 파일 이름(확장명 포함)을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data source]</td> 
   <td> <p>사용 중인 데이터가 양식에서 생성되었는지 원시 데이터 수집(처리되지 않은 컴퓨터 데이터)에서 생성되었는지 여부를 나타내는 옵션을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>이는 다음과 같은 컬렉션의 배열이어야 합니다.</p> 
    <ul> 
     <li>각 컬렉션은 하나의 데이터 항목에 해당하고 하나의 항목을 포함합니다 <code>entry</code></li> 
     <li><code>entry </code> 항목에 <code>key </code>의 컬렉션이 포함되어 있습니다. <code>value</code></li> 
     <li>항목 <code>key </code>에 태그의 이름이 포함되어 있습니다.</li> 
     <li>항목 <code>value </code>에 태그의 값이 포함되어 있습니다.</li> 
    </ul> 
    <p>항목을 추가하려면 다음 작업을 수행하십시오.</p>
    <ol> 
     <li> <b>[!UICONTROL Add Item]</b>을(를) 클릭합니다. </li> 
     <li>항목의 값 유형을 선택합니다.</li> 
     <li>이름 및 값을 추가합니다. 자세한 내용은 이 문서에서 선택한 값 유형에 대한 예를 참조하십시오. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">단순 값 태그</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">조건 태그</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">루프 태그</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Fill a document with a batch of data] {#fill-a-document-with-a-batch-of-data}

이 집계 모듈은 데이터 항목이 별도의 번들로 제공되는 경우에 유용합니다. 이 모듈을 사용하면 값 필드에 필요한 구조를 쉽게 설정하고 항목을 각 값 항목에 매핑할 수 있습니다. 문서 채우기 모듈과 달리 데이터 모듈 배치로 문서 채우기 의 값 필드는 변수를 포함하는 단일 항목만 허용합니다.

*반복자* 모듈을 사용하여 배열의 콘텐츠를 일련의 번들로 변환하면 데이터 항목이 배열로 제공되는 경우에도 이 모듈을 사용할 수 있습니다.

각 수신 번들에 대해 실제 값이 생성되고 채워집니다. 템플릿은 모든 입력 번들이 처리된 후에 생성됩니다.

이 집계 모듈은 목록 또는 보고서를 만들 때 특히 유용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>텍스트 소스인 모듈을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>바꿀 텍스트의 시작 부분을 표시할 문자를 입력합니다. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>다음 텍스트와 유사한 텍스트를 바꾸려면 <code>&#91;&#91;</code>을(를) 입력하십시오. <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>바꿀 텍스트의 끝을 표시할 문자를 입력합니다. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span>다음 텍스트와 유사한 텍스트를 바꾸려면 <code>&#93;&#93;</code>을(를) 입력하십시오. <code>[[replace_me]]</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td> 하나 이상의 매핑된 항목을 포함하는 표현식을 정의합니다. 집계된 데이터는 동일한 표현식 값을 가진 그룹 아래에 구분됩니다. 각 그룹은 평가된 표현식 및 집계된 텍스트가 있는 키가 포함된 별도의 번들로 출력됩니다. 이렇게 하면 키를 이후 모듈에서 필터로 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>집계에 번들이 포함되지 않은 경우 처리를 중지하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> 이전 모듈에서 업로드할 파일을 매핑합니다(예: HTTP &gt; 파일 가져오기 또는 Dropbox &gt; 파일 모듈 가져오기). 또는 데이터 파일을 수동으로 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>대상 출력 파일의 파일 이름(확장명 포함)을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data source]</td> 
   <td> <p>사용 중인 데이터가 양식에서 생성되었는지 원시 데이터 수집(처리되지 않은 컴퓨터 데이터)에서 생성되었는지 여부를 나타내는 옵션을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>이는 다음과 같은 컬렉션의 배열이어야 합니다.</p> 
    <ul> 
     <li>각 컬렉션은 하나의 데이터 항목에 해당하고 하나의 항목을 포함합니다 <code>entry</code></li> 
     <li><code>entry </code> 항목에 <code>key </code>의 컬렉션이 포함되어 있습니다. <code>value</code></li> 
     <li>항목 <code>key </code>에 태그의 이름이 포함되어 있습니다.</li> 
     <li>항목 <code>value </code>에 태그의 값이 포함되어 있습니다.</li> 
    </ul> 
    <p>항목을 추가하려면 다음 작업을 수행하십시오.</p>
    <ol> 
     <li> <b>[!UICONTROL Add Item]</b>을(를) 클릭합니다. </li> 
     <li>항목의 값 유형을 선택합니다.</li> 
     <li>이름 및 값을 추가합니다. 자세한 내용은 이 문서에서 선택한 값 유형에 대한 예를 참조하십시오. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">단순 값 태그</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">조건 태그</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">루프 태그</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
