---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: errors
title: Throw 오류 해결 방법 구성
description: 롤백 또는 커밋 단계 다음에 나오는 시나리오 실행을 강제로 중지하거나 경로 처리를 중단하고 필요에 따라 보기 큐에 저장한 다음 Adobe Workfront Fusion에서 불완전한 실행을 해결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 4bf2a6c7-16b2-4545-9adf-be3947a7017d
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# `throw` 오류 해결 방법 구성

경우에 따라 롤백 또는 커밋 단계 다음에 나오는 시나리오 실행을 강제로 중지하거나, 경로 처리를 중지하고 선택적으로 완료되지 않은 실행 큐에 저장할 수 있습니다.

현재 오류 처리 지시문은 오류 처리기 경로 범위 내에서 사용할 수 없으며 Adobe Workfront Fusion에서는 오류를 쉽게 조건부 생성(throw)할 수 있는 모듈을 제공하지 않습니다.

다음 해결 방법을 사용하여 `throw` 오류 기능을 모방할 수 있습니다.

불완전한 실행에 대한 자세한 내용은 [Adobe Workfront Fusion에서 불완전한 실행 보기 및 해결](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)을 참조하십시오.

오류 처리 지시문에 대한 자세한 내용은  [!DNL Adobe Workfront Fusion][&#128279;](/help/workfront-fusion/references/errors/directives-for-error-handling.md)의 오류 처리에 대한 지시문을 참조하십시오.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 플랜 선택: 귀사는 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 플랜: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## `throw`에 대한 해결 방법

오류를 조건부로 발생시키려면 작업 중에 모듈을 의도적으로 실패하도록 구성할 수 있습니다. 선택적으로 오류(`BundleValidationError`)를 발생시키도록 구성된 [!UICONTROL JSON] > [!UICONTROL JSON 구문 분석] 모듈을 사용할 수 있습니다.

![JSON 오류](assets/json-parse-json.png)

그런 다음 오류 처리 지시문 중 하나를 오류 처리 경로에 첨부할 수 있습니다.

* **롤백**: 시나리오 실행을 중지하고 롤백 단계를 수행합니다.
* **커밋**: 시나리오 실행을 중지하고 커밋 단계를 강제로 수행합니다.
* **무시**: 경로 처리를 중지합니다.
* **중단**: 경로 처리를 중지하고 미완료 실행 큐에 저장합니다.

다음 예제에서는 [!DNL Rollback] 지시문을 사용하는 방법을 보여 줍니다.

![Rollback 지시문](assets/rollback-directive.png)
