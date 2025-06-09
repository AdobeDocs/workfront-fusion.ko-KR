---
title: JSONata 모듈
description: Adobe Workfront Fusion JSONata 커넥터는 Adobe Workfront Fusion이 데이터 컨텐츠와 함께 작동할 수 있도록 JSON 형식으로 데이터를 처리하는 모듈을 제공합니다.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: da3bf98f8254228598372fed8c06d6318718721f
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# [!UICONTROL JSONata] 모듈

[!DNL Adobe Workfront Fusion] [!UICONTROL JSONata] 커넥터를 사용하면 JSON 개체를 쿼리할 수 있습니다. 이 모듈에서는 연결할 필요가 없습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <td> <p>새로운 기능: [!UICONTROL Standard]</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p> </td> 
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
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Workfront] 계획: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 계획: [!DNL Workfront Fusion]이(가) 포함되어 있습니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## JSONata 모듈 및 해당 필드

### 평가

이 작업 모듈은 JSON 개체를 쿼리하고 배열을 반환합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 표현식]</td> 
   <td>JSON 개체를 평가하는 데 사용할 표현식을 입력합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data] </td> 
   <td> 평가할 JSON 개체를 입력합니다.  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringify output] </td> 
   <td> 출력을 문자열로 변환하려면 이 옵션을 활성화합니다.  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**예**:

목표는 다음 JSON 개체에서 이름 배열을 반환하는 것입니다.

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. 표현식 필드에 `people.name`을(를) 입력합니다.
1. 데이터 필드에 JSON 개체를 입력합니다.

모듈은 JSON 개체에서 가져온 이름의 배열을 반환합니다.

>[!ENDSHADEBOX]



### JSONata MCP

이 작업 모듈은 지정된 입력 및 출력 스키마를 분석하여 JSONata 표현식을 생성합니다. 사용자는 모델 컨텍스트 프로토콜(MCP)이 입력을 출력으로 변환하는 표현식을 생성하는 데 사용하는 스키마를 제공합니다.




<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>이 모듈에 사용할 LLM(Large Language Model)에 연결하는 데 사용하는 연결을 선택합니다.</p> <p>현재 Anthropic API 키만 지원됩니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 입력 스키마]</td> 
   <td> <p>이 표현식에 사용할 입력 스키마를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력 스키마]</td> 
   <td> <p>이 표현식에 사용할 출력 스키마를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
