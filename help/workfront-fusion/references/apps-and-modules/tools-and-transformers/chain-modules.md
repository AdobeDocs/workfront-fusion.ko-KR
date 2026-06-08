---
title: 체인 모듈
description: 이러한 모듈을 사용하면 시나리오를 서로 연결하여 서로 호출할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
TQID: https://experienceleague.adobe.com/AlHUrliXikCc3OVHiBTjLNQFndCf5qLzOLuBvnDTUfA
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 81d1dfcdb5c15f6a93e2793f9a0e41821b65c7e3
workflow-type: tm+mt
source-wordcount: 883
ht-degree: 10%

---

# 체인 모듈

>[!IMPORTANT]
>
>이 기능은 Beta에 있으며 미션 크리티컬 프로덕션 워크플로우에는 권장되지 않습니다. Beta 기능에서는 동작이 변경되고 극단적 사례는 완전히 처리되지 않을 수 있습니다.
>
>안정적인 통합을 위해 HTTP 요청 모듈을 사용하여 웹후크를 통해 두 번째 시나리오를 트리거하는 것을 고려해 보십시오. 이 패턴은 완전히 지원되는 기본 형식을 사용하고 각 시나리오에 독립적인 실행 제어를 제공합니다.
>
>체인 시나리오를 사용하려면 [여러 시나리오를 함께 연결](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)하여 디자인 지침을 확인하십시오.

체인 모듈을 사용하면 한 시나리오를 다른 시나리오에 연결할 수 있습니다.

<!--This article will be about the specific module configuration-->

체인 시나리오 계획에 대한 지침은 [여러 시나리오를 함께 연결](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)을 참조하십시오.


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



## 체인 모듈 및 해당 필드

### 트리거

#### 상위 항목에서 데이터 수신

이 모듈은 하위 시나리오의 트리거 모듈이며, 상위 시나리오의 하위 시나리오 호출 모듈에 의해 트리거됩니다. 상위 시나리오로부터 데이터를 수신하며, 이 데이터는 하위 시나리오에서 처리할 수 있습니다.

상위 모듈에서 데이터 수신을 구성하려면 다음을 수행합니다.

1. 기존 데이터 구조를 사용하려면 데이터 구조 필드에서 시나리오의 입력 데이터에 사용할 데이터 구조를 선택합니다.

   또는

   시나리오의 입력 데이터로 사용할 새 데이터 구조를 만들려면 데이터 구조 필드 옆에 있는 **추가**&#x200B;를 클릭하고 데이터 구조를 만듭니다.

   데이터 구조를 만드는 방법에 대한 지침은 [데이터 구조](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md)를 참조하십시오.

1. **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

### 액션

#### 하위 시나리오 호출

이 모듈은 상위 시나리오에 있습니다. 필드는 하위 시나리오의 상위 모듈에서 데이터 수신 모듈에 설정된 데이터 구조를 반영합니다.

>[!IMPORTANT]
>
> 프로덕션 시나리오에서 이 모듈을 구성하기 전에 다음을 검토하십시오.
>
> * 실행 및 삭제 기능이 비활성화되어 있으면 이 시나리오에서 **CTL(커밋 트리거 마지막)을 사용하지 않음**. CTL은 하위 응답을 기다리는 동안 시나리오를 다시 시도하여 제한되지 않은 다시 시도 루프를 만듭니다.
> * **이 모듈을 반복기에 넣을 때 주의하십시오.** 큰 반복기의 각 항목에 대해 하위 시나리오를 발송하면 상당한 플랫폼 로드가 생성됩니다. 하위 시나리오의 논리 또는 반복기 외부에서 공유된 조회를 미리 계산하는 것을 고려하십시오.
> * **실행 및 삭제**&#x200B;은(는) 부모가 하위 항목을 실행했는지 또는 성공했는지 여부를 볼 수 없음을 의미합니다. 하위 오류가 독립적으로 모니터링되는 경우에만 사용합니다.
>
> 전체 디자인 지침을 보려면 [여러 시나리오를 함께 연결](https://experienceleague.adobe.com/ko/docs/workfront-fusion/using/create-scenarios/plan-a-scenario/chain-scenarios)을 참조하십시오.

>[!NOTE]
>
>* 기존 하위 시나리오를 선택하거나 이 모듈을 통해 새 하위 시나리오를 만들 수 있습니다.
>* 하위 시나리오를 만들 때 데이터 구조를 만들 수 있습니다.

하위 시나리오 호출 모듈을 구성하려면

1. 하위 시나리오 호출 모듈을 시나리오에 추가합니다.
1. 기존 하위 시나리오를 사용하려면 체인 필드에서 호출할 하위 시나리오를 선택합니다.

   또는

   새 하위 시나리오를 만들려면 체인 필드 옆에 있는 추가를 클릭합니다. 하위 시나리오는 별도의 창에 표시되며, 상위 모듈에서 데이터 수신 및 상위 모듈에서 응답 반환 이 표시됩니다.

   하위 시나리오의 트리거 모듈에 구성된 필드가 하위 시나리오 호출 모듈에 나타납니다.

1. 하위 시나리오에 전달할 정보를 하위 시나리오 호출 모듈에 입력하거나 매핑합니다.
1. (조건부) 하위 시나리오의 응답을 기다리지 않고 상위 시나리오가 실행을 계속하도록 하려면 **실행 및 삭제** 옵션을 활성화합니다.
1. **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

>[!NOTE]
>
>이 모듈에 대한 새 하위 시나리오를 만들면 하위 시나리오가 별도의 브라우저 창에서 열리므로 상위 시나리오와 하위 시나리오를 동시에 보고 구성할 수 있습니다.

#### 부모에게 응답 반환

이 시나리오는 하위 시나리오에 있으며 선택한 구조의 데이터를 상위 시나리오로 보냅니다. 상위 시나리오의 이후 모듈에서 이 데이터를 매핑할 수 있습니다.

>[!IMPORTANT]
>
> 하위 시나리오에 경로가 여러 개인 경우 **반드시**&#x200B;해야 모든 실행 경로에서 부모 모듈에 대한 반환 응답을 연결할 수 있습니다. 반환 응답 모듈이 건너뛰거나 실행되지 않는 경로에 있는 경우 상위 시나리오는 도달하지 않는 응답을 무기한 기다립니다.
>
> 라우터의 결과에 관계없이 항상 실행되는 라우터에서 부모 모듈에 반환 응답을 추가하거나, 오류 처리를 추가하여 오류가 발생하더라도 응답이 항상 반환되도록 합니다.

응답자 추가 모듈을 구성하려면 다음을 수행하십시오.

1. 기존 데이터 구조를 사용하려면 데이터 구조 필드에서 하위 시나리오가 상위 시나리오로 반환하는 데이터에 사용할 데이터 구조를 선택합니다.

   또는

   데이터에 대한 새 데이터 구조를 만들려면 데이터 구조 필드 옆에 있는 **추가**&#x200B;를 클릭하고 데이터 구조를 만듭니다.

   데이터 구조를 만드는 방법에 대한 지침은 [데이터 구조](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md)를 참조하십시오.

1. **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
