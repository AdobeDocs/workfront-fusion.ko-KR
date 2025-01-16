---
title: 오류 처리 추가
description: 시나리오 실행 중에 오류가 발생하면 일반적으로 실패로 인해 서비스를 사용할 수 없거나, 서비스가 예기치 않은 데이터에 응답하거나, 입력 데이터의 유효성 검사에 실패하기 때문입니다.
author: Becky
feature: Workfront Fusion
exl-id: 82ddaf73-ecf9-4fd6-8f8e-909351023c77
source-git-commit: 0668441df8405610488e3e33658635e4cc7db270
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# 오류 처리 추가

시나리오 실행 중에 오류가 발생할 수 있습니다.

예를 들어 다음과 같은 이유로 오류가 발생할 수 있습니다.

* 오류로 인해 서비스를 사용할 수 없음
* 서비스가 예기치 않은 데이터에 응답합니다.
* 입력 데이터 유효성 검사 실패
* 다른 이유

시나리오 실행 중에 모듈에 오류가 발생하고 모듈에 연결된 오류 처리 경로가 없으면 기본 오류 처리 논리가 실행됩니다.

모듈에 오류 처리기 경로를 추가하여 기본 오류 처리 논리를 자체 오류 처리 논리로 바꿀 수 있습니다. Adobe Workfront Fusion은 오류 핸들러 경로 끝에 삽입할 수 있는 5가지 디렉티브를 제공합니다.

기본 오류 처리에 대한 자세한 내용은 [오류 유형](/help/workfront-fusion/references/errors/error-processing.md)을 참조하십시오.

오류 처리 지시문에 대한 자세한 내용은 [오류 처리에 대한 지시문](/help/workfront-fusion/references/errors/directives-for-error-handling.md)을 참조하십시오.

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
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
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

## 오류 처리기 추가

모듈에 오류 핸들러를 추가하려면 다음을 수행하십시오.

1. 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 오류 처리 경로를 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 오류 처리기 경로를 추가할 모듈을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add error handler]**&#x200B;을(를) 선택합니다.

   ![](assets/error-handler-route.png)

   오류 처리기 경로가 모듈에 추가됩니다. 모듈이 경로의 마지막 모듈인 경우 오류 핸들러는 모듈을 바로 따릅니다. 모듈 뒤에 모듈이 더 있으면 별도의 오류 핸들러 경로가 추가됩니다.

   오류 처리 모듈에는 시나리오에 사용 중인 앱과 디렉티브 목록이 표시됩니다.

   ![오류 경로](assets/error-route.png)

1. 지시어 중 하나를 선택합니다.

   또는

   하나 이상의 모듈을 오류 처리기 경로에 추가합니다.

   경로에 모듈을 더 추가하면 기본적으로 Ignore 지시문이 적용됩니다. 오류가 발생하면 해당 경로의 후속 모듈이 처리됩니다.

   지시문에 대한 자세한 내용은 이 문서에서 [오류 처리 지시문](#error-handling-directives)을 참조하십시오.

1. (선택 사항) 오류 처리 경로에 필터를 추가합니다. 자세한 내용은 [오류 처리 경로에 필터링 및 중첩 추가](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)를 참조하십시오.

>[!NOTE]
>
>오류 처리기 경로는 투명한 원으로 구성되고 일반 경로는 실선 원으로 구성됩니다.

## 오류 처리 지시문

지침이 아래에 간략하게 설명되어 있습니다. 자세한 내용은 [오류 처리에 대한 지시문](/help/workfront-fusion/references/errors/directives-for-error-handling.md)을 참조하십시오.

5개의 지시문이 있으며, 이 지시문은 오류 발생 후 시나리오 실행이 계속되는지 여부에 따라 다음 카테고리로 그룹화할 수 있습니다.

다음 지시어는 시나리오 실행이 계속되도록 합니다.

* **[!UICONTROL Resume]**: 오류가 있는 모듈에 대한 대체 출력을 지정할 수 있습니다. 시나리오 실행 상태가 성공으로 표시됩니다.
* **[!UICONTROL Ignore]**: 오류를 무시합니다. 시나리오 실행 상태가 성공으로 표시됩니다.
* **[!UICONTROL Break]**: 미완료 실행 큐에 대한 입력을 저장합니다. 시나리오 실행 상태가 경고로 표시됩니다.

  자세한 내용은 [불완전한 실행 보기 및 해결](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)을 참조하십시오.

오류가 발생할 때 시나리오 실행을 중지해야 하는 경우 다음 지시문 중 하나를 사용합니다.

* **[!UICONTROL Rollback]**: 시나리오 실행을 즉시 중지하고 상태를 오류로 표시합니다.
* **[!UICONTROL Commit]**: 시나리오 실행을 즉시 중지하고 상태를 성공으로 표시합니다.

## 리소스

오류 처리에 대한 자세한 내용은 다음을 참조하십시오.

* [Adobe Workfront Fusion의 오류 처리에 대한 지침](/help/workfront-fusion/references/errors/directives-for-error-handling.md)
* [오류 처리 경로에 필터링 및 중첩 추가](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)
