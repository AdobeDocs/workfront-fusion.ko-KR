---
title: 함수를 사용하여 항목 매핑
description: 항목을 매핑할 때 함수를 사용하여 단순 또는 복합 공식을 만들 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: b9d7643e-febf-42e2-9ddc-8ec8eba98e7a
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# 함수를 사용하여 항목 매핑

항목을 매핑할 때 함수를 사용하여 단순 또는 복합 공식을 만들 수 있습니다. 사용 가능한 함수는 Excel 및 일부 프로그래밍 언어의 함수와 유사합니다.

* 일반적인 논리, 수학, 텍스트, 날짜 및 배열을 평가합니다.
* 텍스트를 대문자로 변환, 텍스트 트리밍, 날짜를 다른 형식으로 변환 등과 같은 항목 값의 조건부 논리 및 변환을 수행할 수 있도록 해 줍니다.

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

## 필드에 함수 삽입

함수를 필드에 삽입하려면 다음 작업을 수행하십시오.

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 데이터를 매핑할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 함수를 삽입할 필드를 클릭합니다.
1. 매핑 패널에서 삽입할 함수가 포함된 탭을 선택합니다.

   매핑 패널 탭에 대한 자세한 내용은 [함수 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)를 참조하십시오.
   1. 함수 이름을 클릭합니다.

      또는

      함수를 필드로 드래그합니다.
1. 함수 매개 변수를 구성합니다.

   함수 매개 변수에 대한 설명을 보려면 매핑 패널에서 함수 위로 마우스를 가져갑니다.

   함수 및 해당 매개 변수에 대한 자세한 내용은 [함수 참조: 문서 인덱스](/help/workfront-fusion/references/mapping-panel/functions/functions-toc.md)의 문서를 참조하십시오.

1. 모듈 구성을 계속하거나 **확인**&#x200B;을 클릭합니다.

>[!TIP]
>
>다른 필드에서 재사용할 복합 수식을 만들 때 조합이 들어 있는 필드를 클릭하고 Cmd-A 또는 Ctrl-A를 사용하여 선택한 다음 복사하여 다른 필드에 붙여넣을 수 있습니다.


>[!BEGINSHADEBOX]

**예:** 일부 데이터 형식을 사용하면 사용자가 특정 문자 수를 초과하여 입력할 수 없습니다. 하위 문자열 함수를 사용하여 값을 특정 문자 수로 제한할 수 있습니다.

이 예에서 하위 문자열 함수는 프로젝트 이름을 50자로 제한합니다.

![모임 길이 제한 예시](assets/example-meet-length-restriction-350x184.png)

>[!ENDSHADEBOX]

## 함수 중첩

함수를 서로 중첩할 수 있습니다.

>[!BEGINSHADEBOX]

**예:**

이 예에서 하위 문자열 함수는 트리밍된 프로젝트 이름을 50자로 제한합니다.

![트리밍된 이름](assets/trimmed-name-under-50.png)

>[!ENDSHADEBOX]

함수를 중첩하려면 다음을 수행합니다.

1. 수식을 만들 필드를 클릭합니다.

   매핑 패널이 열립니다.

1. 추가할 첫 번째 함수를 클릭합니다. 이것은 바깥에 있는 기능입니다. 다음 예제는 `substring` 함수입니다.
1. 해당 함수에서 중첩 함수를 이동할 위치를 클릭합니다. 이 예에서 중첩 함수는 첫 번째 매개 변수 대신 사용됩니다.
1. 매핑 패널에서 중첩 함수를 클릭합니다. 이 예제에서는 `trim` 함수입니다.
1. 원하는 대로 기능을 계속 구성합니다.
1. 모듈 구성을 계속하거나 **확인**&#x200B;을 클릭합니다.

## [!DNL Google Sheets]개 함수 사용

Workfront Fusion에 사용하려는 함수가 없지만 [!DNL Google Sheets]에 포함된 경우 다음 단계에 따라 사용할 수 있습니다.

1. [!DNL Google Sheets]에서 빈 스프레드시트를 새로 만듭니다.
1. Workfront Fusion에서 시나리오를 엽니다.
1. 시나리오에 **[!DNL Google Sheets]** >**[!UICONTROL 셀 업데이트]** 모듈을 추가합니다.

1. 모듈을 구성합니다.

   1. **[!UICONTROL 스프레드시트]** 필드에서 새로 만든 스프레드시트를 선택합니다.
   1. [!DNL Google Sheets] 함수가 포함된 수식을 **[!UICONTROL Value]** 필드에 삽입하십시오.

      이전 모듈의 출력을 평소대로 사용할 수 있습니다.

      ![Google Sheets 함수 사용](assets/exploit-google-sheet-functions-350x218.png)

1. 계산된 결과를 얻으려면 **[!UICONTROL Google 시트] >[!UICONTROL 셀 가져오기]** 모듈을 삽입하십시오.
1. 4단계에서 사용한 것과 동일한 셀 ID를 사용하여 모듈을 구성합니다.

   ![Google Sheets 함수 사용](assets/exploit-google-sheet-functions-2-350x187.png)
