---
title: 반복자 모듈
description: 반복자 모듈은 배열을 일련의 번들로 변환하는 특별한 유형의 모듈입니다. 각 배열 항목은 별도의 번들로 출력됩니다.
author: Becky
feature: Workfront Fusion
exl-id: 43d39955-3dd7-453d-8eb0-3253a768e114
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 1%

---

# [!UICONTROL Iterator] 모듈

[!UICONTROL Iterator]은(는) 배열을 일련의 번들로 변환하는 모듈 유형입니다. 각 배열 항목은 별도의 번들로 출력됩니다.

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
   <td> 새로운 기능: 표준<p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] 라이센스</td> 
   <td>
   <p>현재: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Workfront] 플랜: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 플랜: [!DNL Workfront Fusion]이(가) 포함되어 있습니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>


보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## [!UICONTROL Iterator] 모듈 구성

일반 반복자 모듈에는 단일 필드인 [!UICONTROL Array] 필드가 있습니다. 이 필드에는 별도의 번들로 변환하거나 분할할 배열이 포함됩니다.

![](assets/set-up-iterator.jpg)

다른 커넥터들은 그 반복기에 특정한 반복기 모듈들을 포함할 수 있다. 여기에는 반복할 배열을 출력하는 모듈을 선택할 수 있는 Source 모듈 필드가 포함되어 있습니다.

![](assets/specialized-iterators.jpg)

자세한 내용은 [모듈 구성](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)을 참조하세요.

>[!BEGINSHADEBOX]

**예:**

* 아래 시나리오는 첨부 파일이 있는 전자 메일을 검색하고 첨부 파일을 선택한 [!DNL Dropbox] 폴더에 단일 파일로 저장하는 방법을 보여 줍니다.

  이메일에는 여러 첨부 파일이 포함될 수 있습니다. 첫 번째 모듈 다음의 [!UICONTROL Iterator] 모듈을 사용하면 시나리오가 각 첨부 파일을 개별적으로 처리할 수 있습니다. [!UICONTROL Iterator] 모듈은 첨부 파일 배열을 단일 번들로 분할합니다. 첨부 파일이 한 개 있는 각 번들은 선택한 [!DNL Dropbox] 폴더에 한 번에 하나씩 저장됩니다. 반복자 모듈의 [!UICONTROL Array] 필드는 `Attachments` 배열을 포함해야 합니다.

  ![](assets/attachments-array.jpg)

>[!ENDSHADEBOX]


## 문제 해결

### 문제: 매핑 패널에 매핑 가능한 항목이 [!UICONTROL Iterator] 모듈에 표시되지 않습니다.

[!UICONTROL Iterator] 모듈에 배열 항목의 구조에 대한 정보가 없는 경우 [!UICONTROL Iterator] 모듈 다음에 있는 모듈의 매핑 패널에 [!UICONTROL Iterator] 모듈 아래에 있는 두 개 항목(`Total number of bundles` 및 `Bundle order position`)만 표시됩니다.

![](assets/mapping-panel-doesnt-display.png)

이는 각 모듈이 출력하는 항목에 대한 정보를 제공해야 하므로 이러한 항목이 후속 모듈의 매핑 패널에 제대로 표시될 수 있기 때문입니다. 그러나 일부 모듈에서 이 정보를 제공하지 못할 수도 있습니다. 예를 들어 데이터 구조가 없는 [!UICONTROL JSON] > [!UICONTROL Parse JSON] 또는 [!UICONTROL Webhooks] > [!UICONTROL Custom Webhook] 모듈은 정보를 제공하지 않습니다.

#### 솔루션

해결 방법은 시나리오를 수동으로 실행하는 것입니다. 이렇게 하면 모듈이 출력을 생성합니다. 그런 다음 Fusion은 이 출력의 형식을 시나리오의 이후 모듈에 적용할 수 있습니다.

예를 들어 시나리오에는 데이터 구조가 없는 [!UICONTROL JSON] > [!UICONTROL Parse JSON] 모듈이 포함되어 있습니다.

![](assets/json-parse-json.png)

이 JSON 모듈에 연결된 [!UICONTROL Iterator] 모듈이 모듈의 출력을 [!UICONTROL Iterator] 모듈의 설치 패널에 있는 배열 필드에 매핑할 수 없습니다.

![](assets/connect-iterator-module.png)

이 문제를 해결하려면

시나리오 편집기에서 시나리오를 수동으로 시작합니다.

>[!NOTE]
>
>전체 시나리오가 실행되지 않도록 하려면 다음을 수행할 수 있습니다.
>
>* 흐름이 더 진행되지 않도록 하려면 [!UICONTROL JSON] > [!UICONTROL Parse JSON] 모듈 뒤에 있는 모듈의 연결을 끊으십시오.
>   또는
>* [!UICONTROL JSON] > [!UICONTROL Parse JSON] 모듈을 마우스 오른쪽 단추로 클릭하고 컨텍스트 메뉴에서 **[!UICONTROL Run this module only]**&#x200B;을(를) 선택하여 [!UICONTROL JSON] > [!UICONTROL Parse JSON] 모듈만 실행합니다.

[!UICONTROL JSON] > [!UICONTROL Parse JSON]이(가) 실행되면 반복자 모듈을 포함하여 모든 후속 모듈에 출력 정보를 제공할 수 있습니다. 그러면 반복자 설정의 매핑 패널에 다음 항목이 표시됩니다.

![](assets/mapping-panel-displays-items.png)

또한 [!UICONTROL Iterator] 모듈 뒤에 연결된 모듈의 매핑 패널에는 배열에 포함된 항목이 표시됩니다.

![](assets/items-contained-in-array.png)
