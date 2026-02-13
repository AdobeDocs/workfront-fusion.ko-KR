---
title: 사용자 정의 함수를 사용하여 데이터 매핑
description: 항목을 매핑할 때 함수를 사용하여 간단하거나 복잡한 공식을 만들 수 있습니다.
author: Becky
feature: Workfront Fusion
source-git-commit: 109ea8a6b3c37918110dc930a19ac85ef3e6d764
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 20%

---

# 사용자 정의 함수를 사용하여 데이터 매핑

Fusion의 [함수] 영역에서 사용자 정의 함수를 만들 수 있습니다. 그런 다음 이러한 함수를 Adobe App Builder 모듈 형태로 시나리오에 추가합니다.

사용자 지정 기능은 Adobe App Builder을 통해 작동하므로 이를 사용하려면 조직에 Adobe App Builder 라이선스가 있어야 합니다.

대부분의 시나리오 요소와 같은 사용자 지정 함수는 팀에서 소유합니다.

Workfront Fusion에는 간단하거나 복잡한 공식을 만들 수 있는 기본 제공 함수도 포함되어 있습니다. 이러한 함수는 배열, 문자열, 숫자 및 이전 모듈의 데이터를 비롯한 다양한 사용 사례를 다룹니다.

기본 제공 함수에 대한 자세한 내용과 지침은 [기본 제공 함수를 사용하여 항목 매핑](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md)을 참조하세요.

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
   <p><ul><li>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li><li>사용자 지정 기능을 사용하려면 Adobe App Builder 라이선스가 있어야 합니다.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 사용자 지정 기능 구성

사용자 지정 함수는 Workfront Fusion의 함수 영역에서 구성됩니다. 함수가 구성된 후 Adobe App Builder 커넥터를 사용하여 시나리오에 해당 함수를 추가할 수 있습니다.

### 런타임 환경 초기화

사용자 지정 함수를 만들려면 먼저 런타임 환경을 초기화해야 합니다. 팀에 사용자 정의 기능이 없는 경우에만 수행해야 합니다.

>[!IMPORTANT]
>
>Adobe App Builder에 대한 액세스 권한이 있는 사용자, IMS 조직 내의 개발자 또는 시스템 관리자만 초기화를 수행할 수 있습니다.
>
>초기화가 완료되면 초기화가 수행된 팀의 모든 사용자가 함수를 만들고 사용할 수 있습니다.

1. 왼쪽 패널에서 **함수** ![함수 아이콘](assets/functions-icon.png) 탭을 클릭합니다.

   런타임을 아직 구성하지 않은 경우 &quot;런타임 환경이 구성되지 않았습니다.&quot;라는 메시지가 표시됩니다.
1. **런타임 초기화**&#x200B;를 클릭합니다.

   잠시 후 두 개의 샘플 함수가 있는 함수 목록이 나타납니다.

### 사용자 지정 함수 만들기

런타임 환경이 구성된 후 사용자 정의 함수를 만들 수 있습니다.

>[!IMPORTANT]
>
>* 사용자 지정 함수 **은(는) JavaScript 함수여야 합니다**.
>* 사용자 지정 함수 **must**&#x200B;이(가) 개체를 반환합니다.
>* 사용자 지정 함수를 만든 후에는 다음 작업을 수행할 수 없습니다.
>
>   * 이름 변경
>   * 기본 매개 변수 값 보기

1. 왼쪽 패널에서 **함수** ![함수 아이콘](assets/functions-icon.png) 탭을 클릭합니다.
1. **함수 추가**&#x200B;를 클릭합니다.
1. 사용자 지정 함수의 이름을 입력합니다.

   나중에 이 이름을 변경할 수 없습니다.
1. 함수의 코드를 입력합니다.
1. 추가할 각 기본 매개 변수 값에 대해 **매개 변수 추가**&#x200B;를 클릭하고 매개 변수 이름과 기본값을 입력하십시오.

   시나리오에 함수를 추가할 때 기본 매개 변수를 재정의할 수 있습니다.
1. **저장**&#x200B;을 클릭합니다

## 시나리오에 사용자 지정 함수 추가

시나리오에 사용자 지정 함수를 추가하려면 Adobe App Builder 커넥터를 사용하십시오.

자세한 지침은 [Adobe App Builder 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md)을 참조하세요.

