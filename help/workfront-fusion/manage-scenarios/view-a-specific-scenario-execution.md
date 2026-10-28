---
title: 특정 시나리오 실행 보기
description: 시나리오 이벤트 필터링 및 검색을 포함하여 특정 시나리오 실행에 대한 세부 정보를 볼 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
TQID: 'https://experienceleague.adobe.com/Msh3ArxBUIu6YDZjL7eXpxlEBiYABHN-Q7xUlJ-qU0g'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 15%
---
# 특정 시나리오 실행 보기

시나리오 이벤트 필터링 및 검색을 포함하여 특정 시나리오 실행에 대한 세부 정보를 볼 수 있습니다.

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

## 특정 실행 보기

시나리오의 시나리오 내역에서 실행을 볼 수 있습니다.


1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭한 다음 시나리오를 클릭합니다.

   또는

   시나리오 편집기에서 시나리오 작업을 수행하는 경우 창의 왼쪽 상단 모서리 근처에 있는 왼쪽 화살표 ![편집 종료 화살표](assets/exit-editing-arrow.png)를 클릭합니다.

1. 시나리오 이름 근처에 있는 **기록**을 클릭합니다.
   ![기록 탭](assets/history-tab.png)


1. 보려는 실행을 찾은 다음 해당 실행의 맨 오른쪽 줄에서 **세부 정보**&#x200B;을(를) 클릭합니다. [!UICONTROL 세부 정보] 링크는 실행에 사용 가능한 세부 정보가 있는 경우에만 표시됩니다.

   오른쪽에 실행 세부 사항 패널이 열려 있는 시나리오 다이어그램이 열립니다.

   이 실행을 위해 출력을 생성한 모듈은 녹색 제목으로 표시됩니다.

   실행되지 않은 모듈은 흐리게 표시됩니다.

1. 모듈의 출력을 보려면 모듈 근처에 있는 출력 세부 정보 풍선을 클릭합니다. 버블의 숫자는 모듈이 출력하는 번들 수를 나타냅니다.

   ![모듈 근처에 있는 출력 버블](assets/new-output-bubble.png)

1. 필터를 통과한 번들을 보려면 필터를 클릭합니다. 필터 근처의 숫자는 필터를 통과한 번들 수를 나타냅니다.
1. 실행 패널에서 특정 모듈이나 이벤트를 검색하려면 **실행 이벤트 검색** 상자에 검색어를 입력하십시오. 입력한 대로 결과가 표시됩니다.
1. [성공] 또는 [경고] 등의 상태별로 실행 패널 검색 결과를 제한하려면 **상태 필터** 드롭다운을 클릭하고 상태를 선택합니다.




>[!NOTE]
>
>특정 모듈에 대한 링크를 만들려면 다음 페이지를 볼 때 URL에 `?moduleId=<module-id>`을(를) 추가하십시오.
>
>* 시나리오 편집 페이지(URL이 `/edit`에 끝남)
>* 특정 시나리오 실행(URL이 `/logs/<log-id>`에 끝남)
>
>`<module-id>`은(는) 시나리오를 볼 때 모듈 레이블 옆에 있는 숫자를 참조합니다.
>
>이 기능은 시나리오를 디버깅하거나 모듈 구성을 복사할 때 유용합니다.

## 새 시나리오 편집기에서 실행 검토

새 경험에서는 실행 기록에서 실행을 열 때 캔버스 오른쪽 옆에 있는 컨트롤을 사용하여 시나리오를 편집하지 않고 무엇이 잘못되었는지 찾을 수 있습니다.

![실행 검토](assets/review-an-execution.png)

| 컨트롤 | 세부 사항 |
| ---------- | ---------- |
| 다음 오류 또는 경고로 이동 | 현재 주기에서 문제가 발생한 모듈 수를 표시합니다. 클릭할 때마다 다음 클릭, 즉 오류가 먼저 발생한 후 경고가 왼쪽에서 오른쪽으로 이동합니다. 모듈을 중앙에 놓고 첫 번째 실패한 작업을 엽니다. 실행 시 오류 또는 경고가 없으면 버튼이 표시되지 않습니다. |
| 검색 모듈 | 이름으로 모듈을 찾은 다음 캔버스에 가운데로 맞춥니다. Ctrl+K(Windows) 또는 Command+K(Mac)를 누릅니다. |
| 참고 | 시나리오 메모를 표시하거나 숨깁니다. 이 컨트롤은 시나리오에 메모가 있고 메모가 여기서 읽기 전용인 경우에만 표시됩니다. |
| 흐름 설명 | 시나리오의 모듈이 실행되는 순서에 애니메이션을 적용합니다. 다시 클릭하거나 Esc 키를 눌러 중지합니다. |
| 확대, 축소, 포커스 및 미니맵 | 편집 모드와 동일한 방식으로 작업합니다. |

**자세히 보기** 스위치도 오른쪽 상단에서 사용할 수 있습니다. 실행을 검토하면 해당 실행을 보는 동안에만 레이아웃이 변경됩니다. 편집을 위해 작게 보기 설정을 변경하지 않으며 시나리오에 아무것도 저장되지 않습니다.

실행에서 이벤트를 선택하여 일치하는 모듈을 가운데로 정렬하고 강조 표시합니다. 작업 세부 정보를 사용할 수 있으면 요청 및 응답 패널이 열립니다. 패널에 데이터가 없으면 요청 및 응답 세부 사항이 해당 실행에 대해 유지되지 않았습니다. 나중에 실행할 수 있도록 수집하려면 [임시 디버그 로그](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs)를 참조하십시오.
