---
title: 체인 모듈
description: 이러한 모듈을 사용하면 시나리오를 서로 연결하여 서로 호출할 수 있습니다.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
source-git-commit: efab436edce8a5253b147c77b87a005f6efc63d0
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 1%

---

# 체인 모듈

체인 모듈을 사용하면 한 시나리오를 다른 시나리오에 연결할 수 있습니다.

<!--This article will be about the specific module configuration-->

체인 시나리오 계획에 대한 지침은 [여러 시나리오를 함께 연결](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)을 참조하십시오.


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

하위 시나리오에 여러 경로가 있는 경우 다른 경로 이후에 항상 실행되고 실행되는 경로에 이 모듈을 추가하는 것이 좋습니다.

응답자 추가 모듈을 구성하려면 다음을 수행하십시오.

1. 기존 데이터 구조를 사용하려면 데이터 구조 필드에서 하위 시나리오가 상위 시나리오로 반환하는 데이터에 사용할 데이터 구조를 선택합니다.

   또는

   데이터에 대한 새 데이터 구조를 만들려면 데이터 구조 필드 옆에 있는 **추가**&#x200B;를 클릭하고 데이터 구조를 만듭니다.

   데이터 구조를 만드는 방법에 대한 지침은 [데이터 구조](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md)를 참조하십시오.

1. **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
