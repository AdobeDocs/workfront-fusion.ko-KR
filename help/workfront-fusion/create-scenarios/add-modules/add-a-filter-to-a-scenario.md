---
title: 시나리오에 필터 추가
description: 일부 시나리오에서는 특정 기준을 충족하는 번들로만 작업해야 합니다. 필터를 사용하여 해당 번들을 선택할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 17%

---

# 시나리오에 필터 추가

일부 시나리오에서는 특정 기준을 충족하는 번들로만 작업해야 합니다. 필터를 사용하여 해당 번들을 선택할 수 있습니다.

예를 들어 Workfront의 [!UICONTROL 레코드 보기] 트리거를 사용하여 특정 사용자에게 할당된 작업만 캡처하는 시나리오를 만들 수 있습니다.

두 모듈 사이에 필터를 추가하고 이전 모듈에서 받은 번들이 특정 필터 조건을 충족하는지 확인할 수 있습니다.

* 번들이 그러한 경우 시나리오의 다음 모듈로 전달됩니다.
* 그렇지 않으면 번들 처리가 종료됩니다.

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
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 전제 조건

두 모듈 사이에 필터를 추가하려면 먼저 두 모듈을 시나리오에 추가해야 합니다.

## 다음 두 모듈 사이에 필터를 추가합니다.

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 필터를 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 필터를 추가할 모듈 사이에 있는 렌치 아이콘 ![렌치 아이콘](assets/wrench-icon.png)을 클릭하고 **필터 설정**&#x200B;을 선택합니다.
1. 표시되는 상자에 필터에 대한 **[!UICONTROL 레이블]**&#x200B;을 입력합니다.
1. 필터 **[!UICONTROL 조건]**&#x200B;을(를) 정의합니다.

   첫 번째 필드, 연산자 및 (필요한 경우) 필드를 비교할 값을 기준으로 필터링할 필드를 입력합니다.

   >[!TIP]
   >
   >매핑 패널에서 필터 필드에 값을 입력할 수 있습니다
   >매핑에 대한 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

   예를 들어 필터가 XML로 끝나는 Adobe Workfront의 파일을 전달하게 하려면 첫 번째 상자에 **[!UICONTROL 파일 이름]**&#x200B;을 입력하고두 번째 상자에 **[!UICONTROL xml]**&#x200B;이 있습니다. 이 두 메뉴 사이의 드롭다운 메뉴에서 **[!UICONTROL 다음으로 끝남(대/소문자 구분 안 함)]**&#x200B;을 선택합니다. 이 필터는 첫 번째 모듈(Workfront)에서 들어오는 번들에 적용됩니다. XML 파일이 포함된 번들만 다음 모듈로 전달됩니다.

   ![필터 설정](assets/set-up-filter-box.png)

1. **[!DNL OK]**&#x200B;을(를) 클릭합니다.

## 필터 복사

현재 시나리오 편집기에는 필터를 복사하는 기능이 포함되어 있습니다.

>[!NOTE]
>
>필터의 양쪽에 있는 모듈을 복사하면 필터도 복사됩니다.
>
>모듈 복사에 대한 자세한 내용은 [Adobe Workfront Fusion의 모듈 또는 시나리오 복사](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md)를 참조하십시오.

모듈을 복사하지 않고 필터를 복사하려면 Fusion DevTool을 사용합니다

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 필터를 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 화면 하단 근처에 있는 DevTool 아이콘 ![DevTool 아이콘](assets/debugger-icon.png)을 클릭하여 Fusion DevTool을 엽니다.

   DevTool 아이콘이 보이지 않으면 [시나리오 디버그](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md)에서 DevTool을 여는 방법을 참조하십시오.

1. 왼쪽 막대에서 **[!UICONTROL 도구]** 아이콘 ![DevTool 도구](assets/devtools-tools-icon.png)을 클릭합니다.

1. **[!UICONTROL 필터 복사]**&#x200B;를 클릭한 다음 오른쪽 패널에서 **[!UICONTROL 필터 복사]** 도구를 구성합니다.

   1. **[!UICONTROL Source 모듈]**&#x200B;을(를) 복사할 필터 바로 뒤에 모듈로 설정하십시오.
   1. **[!UICONTROL Target 모듈]**&#x200B;을 바로 뒤에 필터를 배치할 모듈로 설정하십시오.

1. **[!UICONTROL 실행]**&#x200B;을 클릭합니다.
