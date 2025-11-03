---
content-type: reference
title: 오류 유형
description: 시나리오를 실행하는 동안 오류가 발생하는 경우가 있습니다. 이 문제는 일반적으로 서비스에 연결하지 못해서 서비스를 사용할 수 없거나 유효성 검사가 실패하면 발생합니다. 이 문서에서는 일반적인 오류를 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: abf5f844-d13b-416e-a8b8-2d4ee1786262
source-git-commit: 99621f57da1eb294834a0eacfe527dcf017408e9
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---

# 오류 유형

시나리오를 실행하는 동안 오류가 발생하는 경우가 있습니다. 이 문제는 일반적으로 서비스에 연결하지 못해서 서비스를 사용할 수 없거나 유효성 검사가 실패하면 발생합니다.

Adobe Workfront Fusion은 몇 가지 기본 오류 유형을 구별합니다. 오류 유형에 따라 Fusion 시나리오의 다음 작업이 결정됩니다.

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

+++## 연결 오류 

`ConnectionError`

연결 오류는 가장 일반적인 오류 중 하나입니다. 이러한 장애는 일반적으로 오버로드, 유지 관리 또는 중단과 같은 다양한 이유로 서드파티 서비스를 사용할 수 없기 때문에 발생합니다. 이 오류의 기본 처리는 오류가 발생한 모듈에 따라 다릅니다.

* 첫 번째 모듈에서 오류가 발생하면 경고 메시지와 함께 시나리오 실행이 종료된다. 그런 다음 Workfront Fusion은 시간 간격을 늘려 시나리오를 다시 실행하려고 반복적으로 시도합니다. 모든 시도가 실패하면 Workfront Fusion은 시나리오를 비활성화합니다.
* 첫 번째 모듈이 아닌 다른 모듈에서 연결 오류가 발생하는 경우 후속 단계는 시나리오 고급 설정의 불완전 실행 저장 허용 옵션에 따라 다릅니다.

   * 이 옵션을 사용하면 시나리오 실행이 [!UICONTROL 불완전한 실행] 폴더로 이동됩니다. 여기서 Workfront Fusion은 시간 간격을 늘려 시나리오를 다시 실행하려고 반복적으로 시도합니다. 모든 시도가 실패하면, 사용자의 수동 해결을 기다리는 미완료 실행 폴더에 실행이 유지됩니다.

     불완전한 실행에 대한 자세한 내용은 [불완전한 실행 보기 및 해결](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)을 참조하십시오.
   * 이 옵션이 비활성화되면 오류 발생 후 롤백 단계가 발생하여 시나리오 실행이 종료됩니다. 그런 다음 Workfront Fusion은 시간 간격을 늘려 시나리오를 다시 실행하려고 반복적으로 시도합니다. 모든 시도가 실패하면 Workfront Fusion은 시나리오를 비활성화합니다.

  불완전 실행 저장 허용 설정에 대한 자세한 내용은 시나리오 설정 구성 문서에서 [불완전 실행 저장 허용](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions)을 참조하십시오.

### 시간 간격 늘리기

오류가 발생할 때 시도 사이의 시간 간격을 늘리는 알고리즘을 지수 백오프라고 합니다. 증가하는 시간 간격은 다음과 같이 설정됩니다.

1. 10분
1. 1시간
1. 3시간
1. 12시간
1. 24시간

시간 간격이 늘어나면 자주 실행되는 시나리오가 반복적으로 실패한 시도에 작업을 사용하지 못하게 됩니다.

>[!BEGINSHADEBOX]

**예:**

시나리오에 [!DNL Google Sheets] 트리거 [!UICONTROL 행 보기]가 포함되어 있습니다. Workfront Fusion에서 시나리오를 시작할 때 유지 관리로 인해 [!DNL Google Sheets]을(를) 30분 동안 사용할 수 없으므로 새 행을 검색할 수 없습니다. 시나리오가 중지되었다가 10분 후에 다시 시도합니다. [!DNL Google Sheets]을(를) 계속 사용할 수 없으므로 Workfront Fusion에서 새 행에 대한 정보를 계속 가져올 수 없습니다. 다음 시나리오 실행이 1시간 후에 예약됩니다. [!DNL Google Sheets]을(를) 지금 다시 사용할 수 있으며 시나리오가 성공적으로 실행됩니다.

>[!ENDSHADEBOX]

## 데이터 오류

`DataError`

항목이 잘못 매핑되고 Workfront Fusion측 또는 타사 서비스 측에서 수행된 유효성 검사를 통과하지 못할 경우 데이터 오류가 발생합니다.

이 오류가 발생하면 모듈이 실패한 위치까지 시나리오가 불완전 실행 폴더로 이동되며, 여기서 문제를 해결할 수 있습니다. 그러나 시나리오는 중지되지 않고 일정에 따라 계속 실행됩니다. 데이터 오류가 나타날 때 시나리오 실행을 중지하려면 시나리오 설정 패널에서 순차적 처리 옵션을 활성화합니다.

시나리오 설정에서 [!UICONTROL 불완전한 실행 저장 허용] 옵션을 활성화하지 않은 경우 오류가 발생하여 시나리오 실행이 종료되고 롤백이 수행됩니다.

## 중복 데이터 오류

`DuplicateDataError`

Workfront Fusion에서 중복 데이터를 허용하지 않는 서비스에 동일한 번들을 두 번 삽입하려고 하면 중복 데이터 오류가 생성됩니다. 이 오류가 발생하면 Workfront Fusion이 데이터 오류와 동일한 방식으로 진행됩니다.

자세한 내용은 이 문서에서 [데이터 오류](#data-error)를 참조하십시오.


## 잘못된 액세스 토큰 오류

`InvalidAccessTokenError`

Workfront Fusion이 서드파티 서비스에 등록된 계정에 액세스할 수 없는 경우 잘못된 액세스 토큰 오류가 발생합니다. 일반적으로 이 문제는 주어진 서비스 관리에서 Workfront Fusion에 대한 액세스 권한을 취소하는 경우 발생하지만 해당 서비스를 사용하는 시나리오는 일정에 따라 계속 실행됩니다.

이 오류가 발생하면 시나리오 실행이 즉시 중지됩니다. 오류가 발생한 모듈에서 시작하는 나머지 시나리오는 불완전 실행 폴더로 이동합니다.

## 속도 제한 오류

`RateLimitError`

특정 서비스에서 설정한 제한을 초과하면 비율 제한 오류가 생성됩니다. 이 오류가 발생하면 Workfront Fusion이 연결 오류와 동일한 방식으로 진행됩니다.

자세한 내용은 이 문서에서 [연결 오류](#connection-error)를 참조하십시오.

## 불완전한 데이터 오류

`IncompleteDataError`

불완전한 데이터 오류는 트리거에서만 발생합니다. 이 오류는 트리거가 지정된 서비스에서 필요한 데이터를 다운로드하지 못하는 경우 생성됩니다.

시나리오가 `IncompleteDataError`(으)로 종료되면 추가 동작은 [!UICONTROL 최대 연속 오류 수] 설정에 따라 달라집니다.

자세한 내용은 시나리오 설정 구성 문서에서 [연속 오류 수](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors)를 참조하십시오.

>[!BEGINSHADEBOX]

**예:**

시나리오에서는 문서 확인을 위해 Workfront 트리거 [!UICONTROL 레코드 보기]를 설정했습니다. 긴 비디오와 같은 큰 문서를 업로드하는 동안 시나리오가 실행됩니다. [!UICONTROL Workfront Fusion]이 Workfront에 업로드하는 동안 비디오를 다운로드하려고 시도하므로 시나리오는 `IncompleteDataError`과(와) 함께 종료됩니다.

>[!ENDSHADEBOX]

## 런타임 오류

`RuntimeError`

시나리오 실행 중에 나타나며 이러한 오류 유형 중 하나가 아닌 오류는 `RunTimeError`(으)로 보고됩니다.

시나리오가 `RuntimeError`(으)로 종료되는 경우 추가 동작은 [!UICONTROL 최대 연속 오류 수] 설정에 따라 다릅니다.

자세한 내용은 시나리오 설정 구성 문서에서 [연속 오류 수](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors)를 참조하십시오.


>[!NOTE]
>
>시나리오가 인스턴트 트리거로 시작되고 이 오류가 발생하면 [!UICONTROL 최대 연속 오류 수] 설정이 무시되고 시나리오가 즉시 비활성화됩니다.
>&#x200B;>자세한 내용은 문서 모듈 개요에서 [인스턴스 트리거](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers)를 참조하십시오.

## 불일치 오류

`InconsistencyError`

커밋 또는 롤백 단계 중에 이러한 오류가 발생하면 시나리오는 불일치 오류와 함께 종료됩니다.

이 오류가 시나리오에 표시되면 시나리오 실행이 즉시 중지됩니다.

## 경고

시나리오를 실행하는 동안 문제에 대해 알리는 경고가 표시될 수 있습니다. 경고는 시나리오가 성공적으로 완료되는 것을 막지 않습니다.

예를 들어 최대 허용 파일 크기를 초과하고 [!UICONTROL 데이터 손실 사용] 옵션이 비활성화되면 경고가 나타날 수 있습니다.

## 리소스

매핑에 대한 자세한 내용은 [매핑 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md)를 참조하십시오.

불완전한 실행에 대한 자세한 내용은 [불완전한 실행 보기 및 해결](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)을 참조하십시오.

시나리오 설정 패널에 대한 자세한 내용은 [시나리오 설정 구성](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)을 참조하십시오.

일정에 대한 자세한 내용은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하십시오.

시나리오 단계에 대한 자세한 내용은 [시나리오 실행, 주기 및 단계](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)를 참조하십시오.

데이터 손실 사용 옵션에 대한 자세한 내용은 시나리오 설정 구성 문서에서 [데이터 손실 사용](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss)을 참조하십시오.
