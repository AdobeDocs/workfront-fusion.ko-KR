---
title: 시간대 보기 및 관리
description: Adobe Workfront Fusion에서 표준 시간대 설정을 보고 관리하는 방법에 대해 알아봅니다.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9910d9b4-5a7a-4f4a-9e66-8600d3b6c785
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 39c34b17e766678e187837e07c90b67f365a4f1d
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 17%
---
# 시간대 보기 및 관리

Adobe Workfront Fusion에는 조직 및 사용자 수준의 시간대에 대한 컨트롤이 포함되어 있습니다.

* 조직 시간대: 시나리오에서는 조직 시간대를 사용하여 예약된 이벤트가 발생하는 시기를 결정합니다.

* 사용자 시간대: 사용자 시간대는 사용자에게 표시되는 시간을 결정합니다.

>[!BEGINSHADEBOX]

예:

조직은 뉴욕시를 기반으로 하며 조직 시간은 UTC-5(아메리카/뉴욕)로 설정됩니다. 시나리오 A는 이 조직이 소유하며 매일 오전 9시에 실행되도록 예약되어 있습니다. 시나리오는 뉴욕 시간대에서 오전 9시에 실행됩니다.

이 조직의 사용자는 Los Angeles에 거주하며 사용자 시간대가 UTC-8(아메리카/로스앤젤레스)로 설정되어 있습니다. 이 사용자가 시나리오 A의 시나리오 실행 기록을 보면 시나리오가 오전 6시에 실행된 것을 알 수 있습니다. 뉴욕에서는 시간에 따라 시나리오가 실행되었지만, 사용자는 시간을 자체 시간대로 전환한 것으로 봅니다.

>[!ENDSHADEBOX]



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
  <tr> 
   <td role="rowheader">액세스 수준</td> 
   <td> 해당 조직의 시간대를 편집하려면 조직의 소유자 또는 관리자여야 합니다. </td>
   </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 사용자 시간대 보기 및 관리

1. Fusion에서 화면 오른쪽 상단의 Adobe 프로필 아이콘을 클릭합니다.
1. 열려 있는 메뉴에서 **Fusion 프로필**&#x200B;을 선택합니다.
1. **시간대 옵션** 탭을 선택합니다. 탭은 사용자 이름 바로 아래에 있습니다.
시간대 옵션(Time Zone Options) 목록이 열립니다.
1. 시간대 옵션 목록의 웹 영역에서 이름을 찾습니다.

   현재 사용자 시간대 설정이 이름 오른쪽에 표시됩니다.
1. 시간대를 편집하려면 시간대 옆에 있는 ![시간대 편집](assets/edit-timezone-icon.png)을 클릭합니다.
1. 변경 세부 정보 창의 **시간대** 필드에서 직접 설정할 시간대를 선택합니다.
1. **저장**&#x200B;을 클릭합니다.


## 조직의 시간대 보기 및 관리

>[!NOTE]
>
>해당 조직의 시간대를 편집하려면 조직의 소유자 또는 관리자여야 합니다.

1. Fusion에서 화면 오른쪽 상단의 Adobe 프로필 아이콘을 클릭합니다.
1. 열려 있는 메뉴에서 **Fusion 프로필**&#x200B;을 선택합니다.
1. **시간대 옵션** 탭을 선택합니다. 탭은 사용자 이름 바로 아래에 있습니다.
시간대 옵션(Time Zone Options) 목록이 열립니다.
1. 시간대 옵션 목록의 시나리오 영역에서 시간대를 보거나 관리할 조직을 찾습니다.

   조직의 현재 시간대 설정이 조직 이름 오른쪽에 표시됩니다.
1. 시간대를 편집하려면 시간대 옆에 있는 ![시간대 편집](assets/edit-timezone-icon.png)을 클릭합니다.
1. 변경 세부 정보 창의 **시간대** 필드에서 조직에 설정할 시간대를 선택합니다.
1. **저장**&#x200B;을 클릭합니다.


