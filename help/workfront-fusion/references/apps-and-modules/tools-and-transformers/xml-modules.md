---
title: XML
description: XML 앱을 사용하면 XML &gt; Parse XML 모듈을 통해 XML 형식의 텍스트를 구문 분석하고 번들로 변환하여 데이터를 다른 모듈에서 사용할 수 있도록 할 수 있습니다. XML &gt; Create XML 모듈을 통해 번들을 XML 형식의 텍스트로 변환할 수도 있습니다
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: 5351c2386ed6f2d030df1df01fcf9ea0de7d813f
workflow-type: tm+mt
source-wordcount: '1292'
ht-degree: 2%

---

# XML

[!UICONTROL XML] 앱을 사용하면 [!UICONTROL XML] > [!UICONTROL Parse XML] 모듈을 통해 XML 형식의 텍스트를 구문 분석하고 번들로 변환하여 다른 모듈에서 데이터를 사용할 수 있도록 할 수 있습니다. [!UICONTROL XML] > [!UICONTROL Create XML] 모듈을 통해 번들을 XML 형식의 텍스트로 변환할 수도 있습니다

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

## XML 만들기

[!UICONTROL XML] > [!UICONTROL Create XML] 모듈은 번들을 XML 형식의 텍스트로 변환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>데이터 구조는 결과 XML의 구조를 설명합니다. 만들려는 XML 샘플이 있는 경우 이를 사용하여 데이터 구조를 생성할 수 있습니다.</p> 
    <ol> 
     <li value="1"><strong>[!UICONTROL Add]</strong> 단추를 클릭합니다.</li> 
     <li value="2"><strong>[!UICONTROL Generator]</strong> 단추를 클릭합니다.</li> 
     <li value="3">XML 샘플을 복사하여 샘플 데이터 필드에 붙여넣습니다.</li> 
     <li value="4"><strong>[!UICONTROL Save]</strong> 단추를 클릭합니다.</li> 
     <li value="5">데이터 구조가 성공적으로 생성되었는지 확인합니다.</li> 
     <li value="6">데이터 구조를 저장하려면 <strong>[!UICONTROL Save]</strong>을(를) 클릭합니다.</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Root element name]</td> 
   <td>XML의 루트 요소 이름을 입력합니다. 기본값은 <code>root</code>입니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype SYSTEM ID]</td> 
   <td><code>!DOCTYPE SYSTEM</code> 선언에 사용할 파일 이름을 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype PUBLIC ID]</td> 
   <td><code>!DOCTYPE PUBLIC</code> 선언에 사용할 파일 이름을 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strip Xml Declaration]</td> 
   <td>XML 선언 <code>&lt;?xml ... ?&gt;</code> 및 <code>&lt;!DOCTYPE ... &gt;</code>을(를) 제거하고 XML 루트 요소와 해당 콘텐츠만 남겨두려면 이 옵션을 활성화하십시오.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**예:**

일반적인 사용 사례는 [!DNL Google] >스프레드시트의 데이터를 XML로 변환하는 것입니다.

1. 시나리오에 [!DNL Google Sheets] > [!UICONTROL Select rows] 모듈을 배치하여 데이터를 가져옵니다. [!DNL Google] 스프레드시트에서 행을 검색하도록 모듈을 설정합니다. 테스트 목적으로 {&#x200B;0}을(를) 작은 수로 설정하십시오(예: 3개). **[!UICONTROL Maximum number of returned rows]** [!DNL Google Sheets] 모듈을 마우스 오른쪽 단추로 클릭하고 &quot;**[!UICONTROL Run this module only]**&quot;을(를) 선택하여 실행합니다. 모듈의 출력을 확인합니다.
1. [!DNL Google Sheets] 모듈 뒤에 [!UICONTROL Array Aggregator] 모듈을 연결합니다. 모듈의 설정에서 **[!UICONTROL Source node]** 필드의 [!DNL Google Sheets] 모듈을 선택합니다. 다른 필드는 현재 상태로 두십시오.
1. [!UICONTROL Array Aggregator] 모듈 뒤에 [!UICONTROL XML] > [!UICONTROL Create XML] 모듈을 연결합니다.

   모듈의 설정에는 XML 출력의 구조를 설명하는 데이터 구조가 필요합니다. 데이터 구조 설정을 열려면 **[!UICONTROL Add]** 단추를 클릭하십시오. 이 데이터 구조를 만드는 가장 쉬운 방법은 XML 샘플에서 자동으로 생성하는 것입니다.

1. **[!UICONTROL Generator]** 단추를 클릭하고 XML 샘플을 [!UICONTROL Sample data] 필드에 붙여 넣습니다.

   ![샘플 데이터 필드](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   이제 데이터 구조의 사양 필드에 생성된 구조가 포함됩니다.
1. 데이터 구조의 이름을 보다 구체적으로 변경하고 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   루트 배열 속성에 해당하는 필드는 JSON 모듈의 설정에서 매핑 가능한 필드로 표시됩니다.
1. 필드 옆에 있는 **[!UICONTROL Map]** 단추를 클릭하고 [!UICONTROL Array aggregator] 출력의 `Array[]` 항목을 매핑합니다.
1. XML 모듈의 설정을 닫으려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하십시오.
1. [!UICONTROL Array Aggregator] 모듈의 설정을 엽니다. **[!UICONTROL Target structure]**&#x200B;을(를) 사용자 지정에서 부모 XML 요소에 해당하는 XML 모듈의 필드로 변경합니다. [!DNL Google Sheets] 모듈의 항목을 적절한 필드에 매핑합니다.
1. Array Aggregator 모듈의 설정을 닫으려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하십시오.
1. 시나리오를 실행합니다.

   XML 모듈은 올바른 XML 파일을 출력합니다.

1. [!DNL Google Sheets] 모듈의 설정을 열고 [!UICONTROL Maximum number of returned rows] 숫자를 스프레드시트의 행 수보다 크게 늘려 모든 데이터를 처리합니다.

   결과 XML을 [!DNL Dropbox]에 저장하고, 전자 메일을 통해 첨부 파일로 보내고, FTP를 통해 서버로 업로드하는 등의 작업을 수행할 수 있습니다.

>[!ENDSHADEBOX]

### XML 속성 추가

복합 노드(다른 노드를 포함할 노드)에 특성을 추가하려면 사용자 지정 데이터 구조에서 복합 메모에 대해 이름이 `_attributes`인 컬렉션을 추가해야 합니다. 이 컬렉션은 노드 속성에 매핑됩니다. 텍스트 노드에 특성을 추가하려면(예: `<node attr="1">abc</node>`) 사용자 지정 데이터 구조에서 특성에 대한 컬렉션 `_attributes`과(와) 이 노드의 노드 값에 대한 텍스트 속성 `_value`을(를) 추가해야 합니다.

```
{
   "name": "node",
   "type": "collection",
   "spec": [
      {
         "name": "_attributes",
         "type": "collection"
         "spec": [
            {
               "name": "attr1",
               "type": "text"
            }
         ]
      },
      {
         "name": "_value",
         "type": "text"
      }
   ]
}
```

## [!UICONTROL Parse XML]

[!UICONTROL XML] > [!UICONTROL Parse XML] 모듈은 XML 형식의 텍스트를 구문 분석하고 XML에서 추출된 모든 정보가 포함된 단일 번들을 출력합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>데이터 구조는 다음 모듈에 대한 매핑 패널에서 모듈의 출력을 사용할 수 있도록 하는 XML의 구조를 설명합니다.</p> <p>구문 분석하려는 XML 샘플이 있는 경우 이를 사용하여 데이터 구조를 생성할 수 있습니다.</p> 
    <ol> 
     <li value="1"><strong>[!UICONTROL Add]</strong> 단추를 클릭합니다.</li> 
     <li value="2"><strong>[!UICONTROL Generator]</strong> 단추를 클릭합니다.</li> 
     <li value="3">XML 샘플을 복사하여 <strong>[!UICONTROL Sample data]</strong> 필드에 붙여넣습니다.</li> 
     <li value="4"><strong>[!UICONTROL Save]</strong>을(를) 클릭합니다.</li> 
     <li value="5">데이터 구조가 성공적으로 생성되었는지 확인합니다.</li> 
     <li value="6"> <p><strong>[!UICONTROL Save]</strong> 단추를 클릭하여 데이터 구조를 저장합니다.</p> <p>2~5단계를 건너뛰고 빈 데이터 구조를 제공할 수 있습니다. 데이터 구조가 비어 있는 경우 모듈이 한 번 이상 실행될 때까지 모듈의 출력을 매핑 패널에서 사용할 수 없습니다.</p> </li> 
    </ol> <p>자세한 내용은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">데이터 구조</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve numbers as text]</td> 
   <td>숫자가 텍스트(문자열) 값으로 유지되도록 하려면 이 옵션을 활성화합니다. 그렇지 않으면 숫자가 숫자 값으로 변환됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL XML]</p> </td> 
   <td> <p>구문 분석할 XML 형식 텍스트를 입력하거나 매핑합니다.</p> <p>수식을 사용하는 경우 결과 값 형식이 [!UICONTROL Text] 데이터 형식인지(또는 자동으로 강제 변환할 수 있는지) 확인하십시오. </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>결과 값 형식이 [!UICONTROL Buffer](이진 데이터)이면 <code>toString()</code> 함수를 사용하여 Text 데이터 형식으로 변환합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a> 및 <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">항목 데이터 형식</a>을 참조하세요.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**예:**

URL에서 XML 파일을 다운로드하고 해당 콘텐츠를 구문 분석하려면 다음을 수행합니다.

1. 새 시나리오를 만듭니다.
1. [!UICONTROL HTTP] > [!UICONTROL Get a file] 모듈 추가
1. 모듈의 구성을 열고 다음과 같이 구성합니다.

   **URL**: XML 파일의 URL(예: `https://siftrss.com/f/rqLy05ayMBJ`)

   ![XML 파일 예제](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)

1. **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 모듈의 구성을 저장하고 닫습니다.
1. [!UICONTROL XML] > [!UICONTROL Parse XML] 모듈을 추가하고 [!UICONTROL HTTP] > [!UICONTROL Get a file] 모듈 뒤에 연결한 후 다음과 같이 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Data structure]</td> 
      <td> 
       <ol> 
        <li value="1"><strong>[!UICONTROL Add]</strong> 단추를 클릭합니다.</li> 
        <li value="2"><strong>[!UICONTROL Generator]</strong> 단추를 클릭합니다.</li> 
        <li value="3">웹 브라우저에서 새 탭이나 창을 엽니다.</li> 
        <li value="4">세 번째 단계에서 사용한 URL을 주소 표시줄에 넣고 XML 파일을 가져옵니다.</li> 
        <li value="5">모든 XML 텍스트를 선택하여 클립보드에 복사합니다.</li> 
        <li value="6">탭이나 창을 닫고 시나리오로 돌아갑니다.</li> 
        <li value="7">복사된 XML 텍스트를 샘플 데이터 필드에 붙여넣습니다.</li> 
        <li value="8"><strong>[!UICONTROL Save]</strong>을(를) 클릭합니다.</li> 
        <li value="9">데이터 구조가 성공적으로 생성되었는지 확인합니다.</li> 
        <li value="10">데이터 구조를 저장하려면 <strong>[!UICONTROL Save]</strong>을(를) 클릭합니다.</li> 
       </ol> <p>2~9단계를 건너뛰고 빈 데이터 구조를 제공할 수 있습니다. 데이터 구조가 비어 있는 경우 모듈이 한 번 이상 실행될 때까지 모듈의 출력을 매핑 패널에서 사용할 수 없습니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL XML]</td> 
      <td> <p>[!UICONTROL HTTP] &gt; [!UICONTROL Get a file] 모듈의 출력에서 <code>Data </code>항목을 필드에 매핑합니다. <code>toString()</code> 함수를 사용하여 해당 값을 [!UICONTROL Buffer](이진 데이터) 형식에서 [!UICONTROL Text] 데이터 형식으로 변환합니다.</p> <p>수식의 코드를 복사하여 필드에 붙여넣을 수 있습니다. <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>Buffer 및 Text 데이터 형식에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Item 데이터 형식</a>을 참조하십시오.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png"> </p> </td> 
     </tr> 
    </tbody> 
   </table>

>[!ENDSHADEBOX]

### [!UICONTROL Parsing XML attributes]

기본적으로 [!UICONTROL XML] > [!UICONTROL Parse XML] 모듈은 이러한 특성을 가진 노드의 하위 집합으로 특수 컬렉션 `_attributes`에 특성을 넣습니다. 노드가 텍스트 노드이고 특성이 있는 경우 특성 `_attributes`과(와) 노드의 텍스트 내용 `_value`, 이렇게 두 개의 특수 속성이 추가됩니다.

>[!BEGINSHADEBOX]

**예:** 이 XML:

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

이 번들로 변환됩니다.

![번들로 변환된 XML](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png)

>[!ENDSHADEBOX]

## 문제 해결: [!UICONTROL Parse XML] 모듈에서 데이터를 매핑할 수 없음

데이터 구조가 올바르게 정의되었는지 확인하십시오. 또는 빈 데이터 구조를 사용하고 모듈을 한 번 이상 실행하여 XML 입력을 처리할 수 있습니다.
