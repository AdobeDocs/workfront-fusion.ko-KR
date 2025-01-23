---
title: 도구
description: ' [!DNL Adobe Workfront Fusion Tools] 섹션에는 시나리오를 향상시킬 수 있는 몇 가지 유용한 모듈이 포함되어 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: d9425f5b-4f4a-42da-9aca-1c1783be5fa7
source-git-commit: 757580687ff5d1617f83432952d9870bd697925e
workflow-type: tm+mt
source-wordcount: '1962'
ht-degree: 0%

---

# [!UICONTROL Tools]

[!DNL Adobe Workfront Fusion Tools] 섹션에는 시나리오를 향상시킬 수 있는 몇 가지 유용한 모듈이 포함되어 있습니다.

[!UICONTROL Tools] 모듈은 앱 목록 또는 화면 하단의 [!UICONTROL Tools] 아이콘 ![](/help/workfront-fusion/references/apps-and-modules/assets/tools-icon-small.png)에서 사용할 수 있습니다.

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

## [!UICONTROL Tools] 및 해당 필드

* [트리거](#triggers)
* [액션](#actions)
* [집계자](#aggregators)
* [트랜스포머](#transformers)

### 트리거

#### [!UICONTROL Basic trigger]

이 모듈에서는 사용자 지정 트리거를 만들고 해당 입력 번들을 정의할 수 있습니다.

예를 들어 연락처 또는 지정된 전자 메일 주소(예: [!UICONTROL Email] >[!UICONTROL Send an Email] 또는 [!DNL Gmail] >[!UICONTROL Send an Email] 모듈)로 보내도록 예약된 다른 목록에 대해 또는 원할 때마다 트리거되는 간단한 미리 알림으로 이 모듈을 사용할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bundle]</td> 
   <td> <p>배열 항목을 추가하여 사용자 지정 번들을 만듭니다. 이 배열은 이름 - 값 쌍으로 구성됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL Get Multiple Variables]](#get-multiple-variables)
* [[!UICONTROL Get Variable]](#get-variable)
* [[!UICONTROL Increment function]](#increment-function)
* [[!UICONTROL Set Multiple Variables]](#set-multiple-variables)
* [[!UICONTROL Set Variable]](#set-variable)
* [[!UICONTROL Sleep]](#sleep)

#### [!UICONTROL Get Multiple Variables]

이 모듈은 [!UICONTROL Set Variable] 또는 [!UICONTROL Set Multiple Variables] 모듈에서 이전에 만든 값을 검색합니다.

이 모듈은 변수가 [!UICONTROL Get Multiple Variables] 모듈이 있는 경로가 아닌 다른 경로에 설정된 경우에도 시나리오의 어느 위치에나 설정된 변수를 읽을 수 있습니다. [!UICONTROL Tools] > [!UICONTROL Set Variable] 또는 [!UICONTROL Tools] > [!UICONTROL Set Multiple Variable] 모듈이 [!UICONTROL Tools] > [!UICONTROL Get Multiple Variables] 모듈 전에 실행되어야 합니다. 모듈 실행 순서에 대한 자세한 내용은 [의 라우터 모듈 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)을 참조하세요.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Variables]</td>
        <td>모듈에서 가져올 변수를 추가합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Variable name]</td>
        <td>추가하는 각 변수에 대해 가져올 변수의 이름을 매핑합니다.</td>
    </tr>
</table>

>[!INFO]
>
>**예:** [!UICONTROL Set]/[!UICONTROL Get (multiple) variable(s)] 모듈을 다음과 같이 사용할 수 있습니다.
>
>* 다른 경로에서도 나중에 사용할 수 있도록 계산된 값을 저장합니다. 이 기능은 값이 여러 모듈에 사용되고 값을 계산하는 수식이 너무 복잡한 경우에 유용합니다.
>* 수식을 디버깅합니다. 모듈에 사용된 수식이 올바른 결과를 제공하지 않는 경우 수식을 복사하여 관련 모듈 앞에 삽입하는 [!UICONTROL Set Variable] 모듈에 붙여넣습니다. [!UICONTROL Set Variable] 모듈 뒤에 있는 모듈의 연결을 끊고 시나리오를 실행합니다. [!UICONTROL Set Variable] 모듈의 출력을 확인하고 수식을 조정하거나 단순화한 후 시나리오를 다시 실행한 다음 문제가 해결될 때까지 계속 실행합니다.


#### [!UICONTROL Get Variable]

이 모듈은 [!UICONTROL Set Variable] 또는 [!UICONTROL Set Multiple Variables] 모듈에서 이전에 만든 값을 검색합니다.

이 모듈은 변수가 [!UICONTROL Get Variable] 모듈이 있는 경로가 아닌 다른 경로에 설정된 경우에도 시나리오의 어느 위치에나 설정된 변수를 읽을 수 있습니다. [!UICONTROL Tools] > [!UICONTROL Set Variable] 또는 [!UICONTROL Tools] > [!UICONTROL Set Multiple Variables] 모듈이 [!UICONTROL Tools] > [!UICONTROL Get Variable] 모듈 전에 실행되어야 합니다. 모듈 실행 순서에 대한 자세한 내용은 [의 라우터 모듈 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)을 참조하세요.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable name]</td> 
   <td> <p>모듈에서 가져올 변수의 이름을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Increment function]

이 모듈은 각 모듈의 작업 후 1씩 증가하는 값을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reset a value]</td> 
   <td> <p>모듈에서 값을 증가시키려는 경우 선택합니다. </p> 
    <ul> 
     <li>[!UICONTROL After one cycle]</li> 
     <li>[!UICONTROL After one scenario run]</li> 
     <li>[!UICONTROL Never]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**예:**
>
>모듈의 용도 중 하나는 작업, 리드, 이메일 등을 그룹의 사용자에게 &quot;라운드 로빈&quot; 할당하는 것입니다. 알고리즘은 보통 목록의 맨 위에서 맨 아래로 가면서 그룹에서 피할당자를 몇 가지 합리적인 순서로 선택합니다. 알고리즘이 목록 끝에 도달하면 목록의 맨 위에 있는 사용자에게 다음 할당을 부여하고 목록 아래로 계속 할당합니다.
>
>다음 시나리오는 홀수 시나리오가 실행될 때마다 첫 번째 수신자에게 이메일을 보내고, 짝수 시나리오가 실행될 때마다 두 번째 수신자에게 이메일을 보냅니다.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-email-350x246.gif)
>
>1. 이 시나리오를 만들려면 다음 작업을 수행하십시오.
>1. 모듈의 **[!UICONTROL Reset a value]** 필드를 Never로 설정하십시오.
>1. 홀수 값에 대한 경로를 설정합니다. `1`과(와) 같은 계수 계산 함수를 사용하여 이 경로에 대한 필터를 설정하십시오.
>
>   ![](/help/workfront-fusion/references/apps-and-modules/assets/odd-350x459.png)
>
>  **참고**: [!UICONTROL Equal to] 연산자를 기본 [!UICONTROL Text] 연산자에서 [!UICONTROL Numeric] 연산자로 변경하는 것을 잊지 마십시오.
>
>1. `0`과(와) 같은 계수 계산 함수를 사용하여 짝수 값의 경로를 설정하십시오.
>
>증가 함수는 시나리오가 실행될 때마다 1을 추가합니다. 필터는 증가를 확인하고 해당 값에 따라 작동하여 이메일이 균일하게 배포되도록 합니다.

#### [!UICONTROL Set Multiple Variables]

이 모듈은 경로의 다른 모듈에서 매핑할 수 있는 변수를 만듭니다. 변수는 시나리오의 모든 경로에 대해 [!UICONTROL Get Variable] 또는 [!UICONTROL Get Multiple Variables] 모듈에 매핑될 수도 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Variables]</td> 
   <td>모듈에서 설정할 변수를 추가합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable name] </td> 
   <td>각 변수에 대해 변수 이름을 입력합니다. 이 이름은 다른 모듈에서 변수를 매핑할 때 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable value] </td> 
   <td>각 변수에 대해 변수 값을 입력합니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable lifetime] </td> 
   <td> <p>변수를 유효한 상태로 유지할 기간을 선택합니다(동일한 값 유지).</p> 
    <ul> 
     <li><strong>[!UICONTROL One cycle]</strong>: 변수가 한 주기에 유효합니다. 한 시나리오 실행에서 여러 개의 웹후크를 받을 때 유용합니다(더 많은 웹후크 = 더 많은 주기). </li> 
     <li><strong>[!UICONTROL One execution]</strong>: 변수가 한 시나리오 실행에 대해 유효합니다. 하나의 실행에는 하나 이상의 사이클이 포함될 수 있습니다.</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Set Variable]

이 모듈은 경로의 다른 모듈에서 매핑할 수 있는 변수를 만듭니다. 변수는 시나리오의 모든 경로에 대해 [!UICONTROL Get Variable] 또는 [!UICONTROL Get Multiple Variables] 모듈에 매핑될 수도 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Variable name] </td> 
   <td>변수 이름을 입력합니다. 이 이름은 다른 모듈에서 변수를 매핑할 때 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable lifetime] </td> 
   <td> <p>변수를 유효한 상태로 유지할 기간을 선택합니다(동일한 값 유지).</p> 
    <ul> 
     <li><strong>[!UICONTROL One cycle]</strong>: 변수가 한 주기에 유효합니다. 한 시나리오 실행에서 여러 개의 웹후크를 받을 때 유용합니다(더 많은 웹후크 = 더 많은 주기). </li> 
     <li><strong>[!UICONTROL One execution]</strong>: 변수가 한 시나리오 실행에 대해 유효합니다. 하나의 실행에는 하나 이상의 사이클이 포함될 수 있습니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable value] </td> 
   <td>변수에 대한 값을 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Sleep]

이 모듈에서는 시나리오 흐름을 최대 300초(5분) 동안 지연할 수 있습니다.

이 함수는 예를 들어, 대량 SMS 또는 이메일을 보낼 때 [!DNL target] 서비스 서버 로드를 줄이거나 사람의 동작을 모방하려는 경우 유용할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Delay]</p> </td> 
   <td> <p>시나리오가 일시 중지될 시간(초)을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!TIP]
>
>더 긴 시간 동안 흐름을 일시 중지하려면 시나리오를 두 개의 시나리오로 분할하는 것이 좋습니다.
>
>* 첫 번째 시나리오에는 일시 정지 전에 해당 부분이 포함됩니다.
>* 두 번째 시나리오에서는 그 뒤에 부분이 포함됩니다.
>
>첫 번째 시나리오에서는 현재 타임스탬프와 함께 필요한 모든 정보를 데이터 저장소에 저장합니다. 두 번째 시나리오는 의도한 지연보다 오래된 타임스탬프를 갖는 레코드에 대해 데이터 저장소를 정기적으로 확인하고, 레코드를 검색하고, 데이터 처리를 완료하고, 데이터 저장소에서 레코드를 제거합니다.
>
><!--For more information on data stores, see [Data Stores in [!DNL Adobe Workfront Fusion]]().-->
>
>특정 데이터 저장소 모듈에 대한 자세한 내용은 [[!UICONTROL Data store]개의 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md)을 참조하세요.

### 집계자

* [[!UICONTROL Numeric aggregator]](#numeric-aggregator)
* [[!UICONTROL Table aggregator]](#table-aggregator)
* [[!UICONTROL Text aggregator]](#text-aggregator)

#### [!UICONTROL Numeric aggregator]

이 모듈에서는 숫자 값을 검색한 다음 선택한 함수(SUM, AVG, COUNT, MAX, MIN) 중 하나를 적용하고 결과를 하나의 번들로 반환할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source module]</p> </td> 
   <td> <p>필드를 집계할 모듈을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Aggregate function]</p> </td> 
   <td> <p>값을 집계하는 데 사용할 함수를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>집계된 출력을 그룹화할 표현식을 정의합니다. 이 표현식은 하나 이상의 매핑된 항목을 포함할 수 있습니다. 그런 다음 집계된 데이터는 이 표현식의 값을 사용하여 그룹으로 구분됩니다. 각 그룹은 키(평가된 표현식)와 값(집계된 값)을 가진 별도의 번들로 출력합니다. 키는 후속 모듈에서 필터로 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>결과가 없을 때 시나리오를 중지하려면 이 옵션을 활성화하십시오.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Value]</p> </td> 
   <td> <p>집계할 값을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Table aggregator]

이 모듈은 지정된 열 및 행 구분 기호(표를 만들 수 있음)를 사용하여 수신된 번들의 선택한 필드의 값을 단일 번들로 병합합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source module]</p> </td> 
   <td> <p>필드를 집계할 모듈을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aggregated fields]</td> 
   <td> <p> 위에서 선택한 모듈에서 하나의 번들로 집계할 값이 포함된 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Column separator]</p> </td> 
   <td> <p>결과 번들의 필드 값 열을 구분하는 구분 문자 유형을 선택하거나 입력합니다. [!UICONTROL Other]을(를) 선택하는 경우 구분 문자 필드에 값을 구분하는 데 사용할 문자를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Row separator]</p> </td> 
   <td> <p>결과 번들에서 필드 값 행을 구분하는 구분 문자 유형을 선택하거나 입력합니다. [!UICONTROL Other]을(를) 선택하는 경우 구분 문자 필드에 값을 구분하는 데 사용할 문자를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>집계된 출력을 그룹화할 표현식을 정의합니다. 이 표현식은 하나 이상의 매핑된 항목을 포함할 수 있습니다. 그런 다음 이 표현식의 값을 사용하여 집계된 데이터가 그룹으로 분리됩니다. 각 그룹은 키(평가된 표현식)와 값(집계된 값)을 가진 별도의 번들로 출력합니다. 키는 후속 모듈에서 필터로 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>결과가 없을 때 시나리오를 중지하려면 이 옵션을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Text aggregator]

이 모듈은 수신한 번들의 선택된 필드 값을 단일 번들로 병합합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source module]</p> </td> 
   <td> <p>필드를 집계할 모듈을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Row separator]</p> </td> 
   <td> <p>결과 번들에서 필드 값 행을 구분하는 구분 문자 유형을 선택하거나 입력합니다. [!UICONTROL Other]을(를) 선택하는 경우 구분 문자 필드에 값을 구분하는 데 사용할 문자를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>하나 이상의 매핑된 항목을 포함하는 표현식을 정의합니다. 집계된 데이터는 동일한 표현식 값을 가진 그룹 아래에 구분됩니다. 각 그룹은 평가된 표현식 및 집계된 텍스트가 있는 키가 포함된 별도의 번들로 출력됩니다. 이렇게 하면 키를 이후 모듈에서 필터로 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text]</td> 
   <td> <p> 모듈을 집계할 텍스트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>결과가 없을 때 시나리오를 중지하려면 이 옵션을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**예:** 텍스트 집계기를 사용하여 단일 번들에 더 많은 값(예: 고객 이름 또는 메모)을 삽입하고 전자 메일 본문 또는 전자 메일 제목에 있는 모든 값이 들어 있는 전자 메일을 보낼 수 있습니다.

### 트랜스포머

* [[!UICONTROL Compose a string]](#compose-a-string)
* [[!UICONTROL Convert the encoding of the text]](#convert-the-encoding-of-the-text)
* [[!UICONTROL Switch]](#switch)

#### [!UICONTROL Compose a string]

모든 값을 문자열 데이터 형식(텍스트)으로 변환합니다. 이진 데이터 등의 매핑 시 매핑이 더 쉬워집니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p>텍스트로 변환할 데이터를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Convert the encoding of the text]

입력한 입력 텍스트(또는 이진 데이터)를 선택한 인코딩으로 변환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Input data]</p> </td> 
   <td> <p>변환할 콘텐츠를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Input data codepage]</td> 
   <td> <p>입력 데이터의 인코딩 유형을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Output data codepage]</p> </td> 
   <td> <p>대상(출력) 데이터의 인코딩 유형을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Switch]

입력 값이 제공된 값 목록과 일치하는지 확인합니다. 결과를 기반으로 출력을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Input]</p> </td> 
   <td> <p>평가할 표현식을 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use regular expressions to match]</td> 
   <td> <p>정규 표현식을 사용하려면 이 옵션을 활성화합니다. 모듈은 정확한 일치가 아닌 정규 표현식을 기반으로 사례를 결정합니다.</p> 
    <div> 
     <p>정규 표현식은 각 문자가 특별한 의미를 갖는 메타문자 또는 리터럴 의미를 갖는 정규 문자인 문자의 시퀀스입니다. 이러한 문자 및 메타문자는 텍스트 검색에 사용할 수 있는 패턴을 식별합니다. 예를 들어 이름을 검색하려면 정규 표현식을 설정하여 대문자로 시작하는 연속된 두 단어로 구성된 패턴을 검색할 수 있습니다. 정규 표현식은 텍스트를 검색하고 조작할 수 있는 강력한 도구입니다.</p> 
     <p>정규 표현식에 대한 논의는 이 글의 범위를 벗어난다. 다음 리소스를 권장합니다.</p> 
     <ul> 
      <li>전체 메타문자 목록은 MDN 웹 문서에서 <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions">정규 표현식</a>을(를) 참조하십시오.</li> 
      <li>정규식을 만드는 방법에 대한 자습서를 보려면 <a href="https://regexone.com/">RegexOne</a>을 사용하는 것이 좋습니다.</li> 
      <li>정규식으로 실험하려면 <a href="https://regex101.com/">정규식 101</a> 웹 사이트를 사용하는 것이 좋습니다. 왼쪽 패널에서 ECMAScript(JavaScript) 버전 을 선택합니다.</li> 
     </ul> 
    </div> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cases] </td> 
   <td> <p>입력에 [!UICONTROL Pattern] 필드에 입력한 값이 포함되어 있으면 [!UICONTROL Output] 필드에 입력한 값이 반환됩니다.</p> <p>입력이 [!UICONTROL Pattern] 필드에 설정한 값과 일치하지 않으면 다음 중 하나가 발생합니다.</p> 
    <ul> 
     <li>[!UICONTROL Else] 필드의 값이 반환됨</li> 
     <li>[!UICONTROL Else] 필드에 값이 없으면 출력이 반환되지 않습니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Else]</p> </td> 
   <td> <p>사례 필드에 설정된 기준이 충족되지 않을 때 반환되는 값을 입력합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
