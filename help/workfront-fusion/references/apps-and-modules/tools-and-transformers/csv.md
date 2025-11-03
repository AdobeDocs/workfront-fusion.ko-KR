---
title: CSV
description: Adobe Workfront Fusion CSV 모듈을 사용하면 CSV 파일을 만들고 수신된 텍스트 값 또는 파일에서 CSV 텍스트를 구문 분석할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# CSV

Adobe Workfront Fusion [!UICONTROL CSV] 모듈을 사용하면 CSV 파일을 만들고 수신된 텍스트 값 또는 파일에서 CSV 텍스트를 구문 분석할 수 있습니다.

변환기이므로 이러한 모듈은 연결이 필요하지 않습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++



## [!UICONTROL CSV 만들기]

[!UICONTROL CSV 만들기] 집계를 사용하면 수신된 텍스트 값에서 CSV 텍스트를 만들 수 있습니다.

집계자에 대한 자세한 내용은 [집계 모듈](/help/workfront-fusion/references/modules/aggregator-module.md)을 참조하십시오.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>CSV를 만드는 데 사용할 필드를 출력하는 모듈을 선택합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 집계된 필드]</td>
        <td>사용 가능한 필드 목록에서 집계할 필드를 선택합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 첫 번째 행에 헤더 포함]</td>
        <td>결과에 헤더를 포함하려면 이 옵션을 선택합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>결과를 그룹화할 필터를 입력합니다. 예를 들어 날짜를 입력합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 빈 집계 후 처리 중지]</td>
        <td>결과가 없을 때 시나리오를 중지하려면 이 옵션을 선택합니다.</td>
    </tr>
</table>

## [!UICONTROL CSV 만들기(고급)]

[!UICONTROL CSV 만들기(고급)] 집계를 사용하면 수신된 텍스트 값에서 CSV 텍스트를 만들 수 있습니다. 결과 CSV 파일의 CSV 열을 정의하는 데이터 구조를 사용합니다. 정의된 열은 CSV 모듈 설정에서 필드로 표시되며, 시나리오의 이후 모듈에 매핑될 수 있습니다.

집계자에 대한 자세한 내용은 [집계 모듈](/help/workfront-fusion/references/modules/aggregator-module.md)을 참조하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>CSV를 만드는 데 사용할 필드를 출력하는 모듈을 선택합니다.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 데이터 구조]</td> 
   <td> <p>원하는 방식으로 필드를 집계할 데이터 구조를 선택합니다. 데이터 구조를 정의한 후 해당 필드에 항목을 매핑할 수 있습니다.</p> <p>자세한 내용은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">데이터 구조</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 첫 번째 행에 헤더 포함] </td> 
   <td>결과에 헤더를 포함하려면 이 옵션을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>결과를 그룹화할 필터를 입력합니다. 예를 들어 날짜를 입력합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 빈 집계 후 처리 중지] </td> 
   <td>결과가 없을 때 시나리오를 중지하려면 이 옵션을 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>


>[!BEGINSHADEBOX]

**예**:

이 예에서는 &quot;전체 이름&quot; 및 &quot;이메일&quot;이라는 두 개의 열을 사용하여 Google 연락처를 CSV 파일로 내보내는 방법을 보여 줍니다. [!UICONTROL Google 연락처] > [!UICONTROL 그룹에서 연락처 가져오기] 모듈의 출력 번들에는 다음과 같은 구조가 있습니다. 전자 메일 주소는 <code>[!UICONTROL 전자 메일[]] 내부에 저장됩니다.</code> item: 컬렉션의 배열이며 각 컬렉션에는 두 개의 항목이 들어 있습니다. <code>레이블</code> 및 <code>전자 메일</code>.
![변환](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

간단한 [!DNL Create CSV] 모듈에서는 번들의 최상위 항목에 해당하는 확인란 목록을 제공합니다. <code>전체 이름을 선택하려고 하면</code> 및 <code>개의 전자 메일</code> [!UICONTROL CSV 만들기] 모듈에서 다음 출력을 생성합니다. 이 출력은 원하는 출력이 아닐 수 있습니다.

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

항목 <code>전체 이름</code> 는 단순 텍스트 유형이며 예상대로 내보내집니다. 항목 <code>전자 메일</code>복잡한 형식의 컬렉션 배열인 를 [개체]&#x200B;(으)로 내보냅니다. 이 개체는 기본적으로 컬렉션과 배열이 텍스트로 변환되는 방식입니다.

자세한 내용은 [항목 데이터 형식](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)을 참조하세요.


<code>전자 메일의 콘텐츠를 내보내려면 </code><code>전자 메일[]의 첫 번째 컬렉션 항목</code> 대신 [!UICONTROL CSV 만들기(고급)] 모듈을 사용해야 합니다. 이 모듈에서는 CSV 파일의 개별 열을 정의하고 중첩된 열을 포함하여 항목을 해당 열에 매핑할 수 있습니다.

1. 시나리오에 [!UICONTROL CSV 만들기(고급)] 모듈을 삽입합니다.
1. <strong>[!UICONTROL 데이터 구조]</strong> 필드 옆에 있는 [!UICONTROL 추가] 단추를 클릭하여 새 데이터 구조를 만듭니다.
1. 데이터 구조의 이름을 입력하고 <strong>[!UICONTROL 항목 추가]</strong>를 클릭하여 개별 열을 추가합니다. &quot;전체 이름&quot;과 &quot;이메일&quot;, 이렇게 두 개의 열을 내보내려면 결과 데이터 구조가 다음과 같습니다.

   ![Google 연락처 출력](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. 데이터 구조를 정의한 후 각 개별 열에 해당하는 필드가 [!UICONTROL CSV 만들기(고급)] 모듈의 구성에 표시되므로 항목을 매핑할 수 있습니다. <code>[!UICONTROL 전자 메일[]]에서 첫 번째 항목 가져오기</code> 해당 항목 <code>전자 메일 배열 및 매핑 </code>필드/열 이메일로:

   ![CSV 고급 모듈 만들기](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. 시나리오를 실행합니다. 항목 <code>전자 메일[1]: 전자 메일</code> &quot;이메일&quot; 열에 매핑되는 단순 유형이 텍스트입니다. 올바르게 내보냅니다.

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

## [!UICONTROL CSV 구문 분석]

[!UICONTROL CSV 구문 분석] 변환기를 사용하면 수신된 텍스트 값 또는 파일에서 CSV 텍스트를 구문 분석할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 열 수]</td> 
   <td>CSV 파일의 열 수를 지정합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV에 헤더 포함]</td> 
   <td> <p>CSV 텍스트의 첫 행에 머리글이 포함된 경우 이 옵션을 선택합니다.</p> <p>참고: 모듈은 이러한 헤더를 사용하여 출력의 열에 레이블을 지정하지 않습니다. 대신 이 필드에서는 헤더가 출력 데이터에 포함되지 않도록 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>CSV 파일의 구분 기호를 선택합니다. 구분 기호는 별도의 값 또는 필드 사이의 경계를 나타내는 텍스트 문자입니다.</p> 
    <ul> 
     <li>[!UICONTROL 쉼표]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>[!UICONTROL Other]를 선택하는 경우 CSV 파일에서 값을 구분하는 데 사용하는 구분 기호를 입력합니다. 정확히 하나의 문자를 입력해야 합니다.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 인용되지 않은 필드 내에 따옴표 유지]</td> 
   <td>견적을 유지하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>구문 분석할 CSV 파일을 입력하거나 매핑합니다.<p>참고: <p>데이터가 이진 형식(일반적으로 파일에서)으로 제공되는 경우 'toString()' 함수를 사용하여 이진 데이터를 [!UICONTROL String](으)로 변환해야 합니다.</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
