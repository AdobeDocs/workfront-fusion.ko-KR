---
title: 작업자 풀
description: 작업자 풀은 하나 이상의 특정 조직에 전용되는 Workfront Fusion 처리 리소스의 수량입니다. 모든 Fusion 작업 및 처리는 조직의 할당된 작업자 풀 컨텍스트에서 발생합니다.
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: b800142d824927e5765eed50a831731e6b5d9925
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 19%
---
# 작업자 풀

작업자 풀은 특정 조직에 전용으로 사용되는 Workfront Fusion 처리 리소스의 수량입니다. 모든 Fusion 작업 및 처리는 조직의 할당된 작업자 풀 컨텍스트에서 발생합니다.

작업자 풀을 사용하면 시나리오를 보다 효율적으로 실행할 수 있으며 Fusion 처리 능력을 위해 다른 조직과 경쟁할 가능성을 배제할 수 있습니다.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 작업자 풀 개요

작업자 풀은 시나리오 실행을 동시에 처리하는 방법입니다. 각 작업자 풀은 다음과 연결되어 있습니다.

* 다수의 작업자들.
* 실행 큐.

시나리오가 실행되면 작업자 풀의 실행 큐에 전달됩니다. 풀의 작업자는 실행 풀에서 작업을 지속적으로 가져와 병렬로 처리합니다.

실행 큐 깊이가 증가하여 모든 기존 작업자가 사용 중인 경우 Workfront Fusion은 더 많은 작업자를 추가하여 풀의 크기를 자동으로 조정합니다. 동적 및 이벤트 기반 방식으로 확장이 가능합니다. 즉, 사용자 또는 조직의 조치 없이 실시간 로드에 따라 용량이 초과되거나 계약됩니다.

Workfront Fusion 팀은 풀의 활용도와 확장 동작을 지속적으로 모니터링하고 임계값 또는 패턴을 검토하여 사용 증가에 따른 일관된 성능을 보장할 수 있습니다.

## 작업자 풀 이름 바꾸기

조직 소유자 및 관리자는 해당 조직에 할당된 작업자 풀의 이름을 변경할 수 있습니다. 각 풀에는 기본적으로 시스템 생성 이름이 표시됩니다. 풀에 `Marketing EU` 또는 `High-volume integrations`과(와) 같은 사용자 지정 이름을 지정하고 필요할 때마다 변경할 수 있습니다.

풀 이름을 바꾸면 레이블이 지정되는 방식만 변경됩니다. 시나리오, 실행 및 풀 용량은 영향을 받지 않습니다. 새 이름은 시나리오를 풀에 할당할 때와 같이 풀이 표시되는 모든 위치에 나타납니다.

>[!NOTE]
>
>**[!UICONTROL 작업자 풀]** 탭은 둘 이상의 작업자 풀이 조직에 할당된 경우에만 나타납니다. 조직에 단일 작업자 풀이 있거나 공유 풀을 사용하는 경우 탭이 표시되지 않습니다.

작업자 풀의 이름을 바꾸려면 다음을 수행하십시오.

1. 왼쪽 탐색에서 **조직 개요**&#x200B;를 클릭합니다
1. 페이지 상단 근처에 있는 **[!UICONTROL 작업자 풀]** 탭을 클릭합니다.

   탭에는 각 풀이 나열되며 할당된 시나리오 수가 표시됩니다.

1. 이름을 바꿀 풀 옆에 있는 **[!UICONTROL 이름 바꾸기]**&#x200B;를 클릭합니다.
1. 열리는 패널에서 새 이름을 입력합니다.
1. **저장**&#x200B;을 클릭합니다.
