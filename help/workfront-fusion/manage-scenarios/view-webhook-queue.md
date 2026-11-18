---
title: k의 큐
description: '많은 서비스는 서비스에서 특정 변경 사항이 발생할 때마다 즉시 알림을 전송할 수 있도록 웹후크를 제공합니다. Webhooks라고도 하는 인스턴스 트리거는 이러한 이벤트를 사용하여 시나리오를 시작할 수 있습니다. 이벤트가 처리를 기다리는 동안(예: 시나리오가 이미 실행 중인 경우) 웹후크의 대기열로 이동합니다. 웹후크의 큐를 볼 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: 'https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 1c28e4007e3e9d6503618482002e506f9393ee57
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 16%
---
# 웹후크의 대기열 보기

많은 서비스는 서비스에서 특정 변경 사항이 발생할 때마다 즉시 알림을 전송할 수 있도록 웹후크를 제공합니다. Webhooks라고도 하는 인스턴스 트리거는 이러한 이벤트를 사용하여 시나리오를 시작할 수 있습니다. 이벤트가 처리를 기다리는 동안(예: 시나리오가 이미 실행 중인 경우) 웹후크의 대기열로 이동합니다. 웹후크의 큐를 볼 수 있습니다.

들어오는 웹후크 데이터는 시나리오 설정 패널에서 데이터 기밀성 옵션을 설정한 방법과 관계없이 항상 대기열에 저장됩니다. 데이터가 시나리오에서 처리된 후 큐에서 영구적으로 삭제됩니다.

웹후크에 대한 자세한 내용은 [인스턴트 트리거(웹후크)](/help/workfront-fusion/references/modules/webhooks-reference.md)를 참조하십시오.

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

## 웹후크의 대기열 보기

들어오는 웹후크의 모든 메시지는 웹후크의 큐에 저장됩니다.

현재 시나리오에 대기열이 있는 경우 해당 시나리오에 배너가 표시됩니다.

![큐 배너](assets/queue-banner.png)

웹후크의 큐 페이지에 **[!UICONTROL 시나리오]** 및 **[!UICONTROL 웹후크]** 목록과 동일한 레이아웃이 있습니다.

>[!NOTE]
>
>검색 및 정렬은 전체 큐가 아니라 현재 테이블에 로드된 이벤트에만 적용됩니다. 더 많은 이벤트를 포함하려면 먼저 추가 이벤트를 로드하십시오.

Webhook의 대기열을 보고 관리하려면

1. 왼쪽 메뉴에서 **[!UICONTROL 웹후크]**&#x200B;를 클릭합니다.
1. 대기열을 보려는 웹후크를 찾습니다.
1. [이벤트 가득 참 대기열] 열의 수를 찾습니다.

   ![Webhook 큐](assets/webhook-queue.png)

1. 큐의 이벤트에 대한 세부 정보를 보려면 **작업** 단추를 클릭하십시오.

   Webhook의 대기열 페이지가 열립니다. 페이지에 다음 열이 있는 테이블의 큐에 이벤트가 나열됩니다. **[!UICONTROL ID]**, **[!UICONTROL 만든 날짜]**, **[!UICONTROL 크기]** 및 **[!UICONTROL 세부 정보]**.

1. (선택 사항) 테이블의 이벤트를 필터링하려면 테이블 위의 **[!UICONTROL 검색]** 필드에 텍스트를 입력하십시오.
1. (선택 사항) 이벤트를 정렬하려면 **[!UICONTROL ID]**, **[!UICONTROL 만든 날짜]** 또는 **[!UICONTROL 크기]** 열 헤더를 클릭합니다.
1. (선택 사항) 각 페이지에 표시되는 이벤트 수를 변경하려면 페이지 하단의 **[!UICONTROL 표시]** 드롭다운 목록에서 숫자를 선택합니다.
1. (선택 사항) 이벤트 페이지 간에 이동하려면 페이지 하단에 있는 **[!UICONTROL 처음]**, **[!UICONTROL 이전]**, **[!UICONTROL 다음]** 또는 **[!UICONTROL 마지막]**&#x200B;을 클릭합니다.

   큐에 이벤트 페이지가 하나만 있는 경우에는 이 단추를 사용할 수 없습니다.

1. (선택 사항) 이벤트의 페이로드를 보려면 해당 이벤트의 행에서 **[!UICONTROL 세부 정보]**&#x200B;를 클릭합니다.

   세부 정보 대화 상자가 열리고 이벤트의 페이로드가 표시됩니다.

1. (선택 사항) 이벤트를 삭제하려면

   1. 다음 중 하나를 수행하여 삭제할 이벤트를 선택합니다.

      * 선택할 각 이벤트 옆에 있는 확인란을 선택합니다.
      * **[!UICONTROL 모두 선택]** 확인란을 선택하여 현재 로드된 이벤트뿐만 아니라 전체 대기열을 선택합니다. 그런 다음 선택 항목에서 제외하려는 모든 이벤트에 대한 확인란의 선택을 취소할 수 있습니다.

   1. 화면 하단 근처에 있는 표시줄에서 **삭제**&#x200B;를 클릭합니다.
