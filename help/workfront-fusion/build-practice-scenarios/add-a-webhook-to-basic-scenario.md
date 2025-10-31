---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 기본 시나리오에 웹후크 추가
description: 즉각적인 트리거라고도 하는 웹후크는 주어진 일정이 아닌 변경이 있을 때마다 시나리오를 시작할 수 있는 특정 종류의 트리거 모듈입니다.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# 기본 시나리오에 웹후크 추가

즉각적인 트리거라고도 하는 웹후크는 주어진 일정이 아닌 변경이 있을 때마다 시나리오를 시작할 수 있는 특정 종류의 트리거 모듈입니다.

이 예에서는 특정 요청 대기열에 요청이 제출되는 즉시 시나리오를 시작하기 위해 웹후크를 추가합니다. 그런 다음 시나리오에서는 해당 요청을 프로젝트로 전환합니다.

이 예제에서는 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에서 만든 시나리오를 수정합니다.

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

## 전제 조건

이 절차를 수행하기 전에 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에 설명된 시나리오를 만들어야 합니다.

## Webhook 추가 및 구성


### Webhook 모듈 추가

1. 시나리오 편집기에서 시나리오를 엽니다.
1. 첫 번째 모듈을 마우스 오른쪽 단추로 클릭하고 **모듈 삭제**&#x200B;를 선택합니다.

   모듈이 삭제되고 빈 자리 표시자가 남습니다.

1. 빈 모듈을 클릭하고 앱 목록에서 **Adobe Workfront**&#x200B;을(를) 선택합니다.
1. **이벤트 보기**&#x200B;를 선택합니다.
1. Webhook 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 레코드 유형 필드에서 **문제**&#x200B;를 선택하면 모듈이 문제 변경을 트리거합니다.
1. 상태 필드에서 **새 상태**&#x200B;를 선택합니다. 이 예제에서는 다루지 않는 필터에 사용되는 필수 필드입니다.
1. 레코드 원본 필드에서 **새 레코드만**&#x200B;을(를) 선택합니다. 이렇게 하면 문제가 업데이트 또는 삭제될 때가 아니라 추가될 때 시나리오가 트리거될 수 있습니다.
1. 모듈 구성을 저장하려면 **저장**&#x200B;을 클릭하세요.

## 두 번째 모듈 업데이트

1. 시나리오를 엽니다.
1. **개체 변환** 모듈을 클릭하여 엽니다.
1. Issue ID 필드에서 검정색 ID 블록을 삭제합니다. 블록이 매핑된 모듈을 더 이상 사용할 수 없으므로 블록은 검정색입니다.
1. 첫 번째 모듈(이벤트 보기) 아래에서 ID 블록을 선택하여 두 번째 모듈에 매핑합니다.
1. **확인**&#x200B;을 클릭합니다.



### 테스트 및 활성화

1. 시나리오 편집기의 왼쪽 아래에서 **[!UICONTROL 한 번 실행]**&#x200B;을 클릭합니다.

   새 요청을 시청하려면 시나리오가 실행 중이어야 합니다.
1. Fusion이 연결 중인 Workfront 환경으로 이동하여 문제를 추가합니다.

   시나리오를 실행해야 합니다.
1. 출력을 검사하여 시나리오가 예상대로 실행되었는지 확인합니다.
1. 시나리오가 예상대로 작동하는 경우 화면 왼쪽 하단의 **예약** 전환을 클릭하여 **켜기**&#x200B;로 전환합니다.

   이렇게 하면 시나리오가 활성화됩니다.
1. Workfront Fusion에서 왼쪽 아래 모서리 근처에 있는 **[!UICONTROL 저장]**&#x200B;을 클릭하여 시나리오에 대한 진행 상황을 저장합니다.
