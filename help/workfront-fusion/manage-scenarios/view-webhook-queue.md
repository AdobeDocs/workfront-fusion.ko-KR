---
title: k의 큐
description: '많은 서비스는 서비스에서 특정 변경 사항이 발생할 때마다 즉시 알림을 전송할 수 있도록 웹후크를 제공합니다. Webhooks라고도 하는 인스턴스 트리거는 이러한 이벤트를 사용하여 시나리오를 시작할 수 있습니다. 이벤트가 처리를 기다리는 동안(예: 시나리오가 이미 실행 중인 경우) 웹후크의 대기열로 이동합니다. 웹후크의 큐를 볼 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# 웹후크의 대기열 보기

많은 서비스는 서비스에서 특정 변경 사항이 발생할 때마다 즉시 알림을 전송할 수 있도록 웹후크를 제공합니다. Webhooks라고도 하는 인스턴스 트리거는 이러한 이벤트를 사용하여 시나리오를 시작할 수 있습니다. 이벤트가 처리를 기다리는 동안(예: 시나리오가 이미 실행 중인 경우) 웹후크의 대기열로 이동합니다. 웹후크의 큐를 볼 수 있습니다.

들어오는 웹후크 데이터는 시나리오 설정 패널에서 데이터 기밀성 옵션을 설정한 방법과 관계없이 항상 대기열에 저장됩니다. 데이터가 시나리오에서 처리된 후 큐에서 영구적으로 삭제됩니다.

웹후크에 대한 자세한 내용은 [인스턴트 트리거(웹후크)](/help/workfront-fusion/references/modules/webhooks-reference.md)를 참조하십시오.

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

## 웹후크의 대기열 보기

들어오는 웹후크의 모든 메시지는 웹후크의 큐에 저장됩니다.

현재 시나리오에 대기열이 있는 경우 해당 시나리오에 배너가 표시됩니다.

![큐 배너](assets/queue-banner.png)

Webhook의 대기열을 보려면

1. 왼쪽 메뉴에서 **[!UICONTROL 웹후크]**&#x200B;를 클릭합니다.
1. 대기열을 보려는 웹후크를 찾습니다.
1. 수신된 이벤트 단추에서 이벤트 수를 찾습니다.

   ![Webhook 큐](assets/webhook-queue.png)

1. 대기열의 이벤트에 대한 세부 사항을 보려면 버튼을 클릭합니다.
