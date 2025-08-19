---
title: 특정 시나리오 실행 보기
description: 시나리오 이벤트 필터링 및 검색을 포함하여 특정 시나리오 실행에 대한 세부 정보를 볼 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: 62b09469c1d85fd2bd1f154cde339cc4a10fc34a
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---

# 특정 시나리오 실행 보기

시나리오 이벤트 필터링 및 검색을 포함하여 특정 시나리오 실행에 대한 세부 정보를 볼 수 있습니다.

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
   <p>Workfront Fusion 라이센스 요구 사항 없음</p>
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

## 특정 실행 보기

시나리오의 시나리오 내역에서 실행을 볼 수 있습니다.


1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭한 다음 시나리오를 클릭합니다.

   또는

   시나리오 편집기에서 시나리오 작업을 수행하는 경우 창의 왼쪽 상단 모서리 근처에 있는 왼쪽 화살표 ![편집 종료 화살표](assets/exit-editing-arrow.png)를 클릭합니다.

1. 시나리오 이름 근처에 있는 **기록**&#x200B;을 클릭합니다.
   ![기록 탭](assets/history-tab.png)


1. 보려는 실행을 찾은 다음 해당 실행의 맨 오른쪽 줄에서 **세부 정보**&#x200B;을(를) 클릭합니다. [!UICONTROL 세부 정보] 링크는 실행에 사용 가능한 세부 정보가 있는 경우에만 표시됩니다.

   오른쪽에 실행 세부 사항 패널이 열려 있는 시나리오 다이어그램이 열립니다.

   이 실행을 위해 출력을 생성한 모듈은 녹색 제목으로 표시됩니다.

   실행되지 않은 모듈은 흐리게 표시됩니다.

1. 모듈의 출력을 보려면 모듈 근처에 있는 출력 세부 정보 풍선을 클릭합니다. 버블의 숫자는 모듈이 출력하는 번들 수를 나타냅니다.

   ![모듈 근처에 있는 출력 버블](assets/output-bubble.png)

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
