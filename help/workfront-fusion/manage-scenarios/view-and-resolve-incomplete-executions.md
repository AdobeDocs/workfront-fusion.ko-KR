---
title: 미완료 실행 보기 및 해결
description: '[!UICONTROL 미완료 실행] 폴더는 오류로 인해 정상적으로 완료되지 않은 시나리오 실행을 저장합니다. 저장된 각 불완전한 실행은 수동 또는 자동으로 해결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 5%

---

# 미완료 실행 보기 및 해결

[!UICONTROL 미완료 실행] 폴더는 오류로 인해 정상적으로 완료되지 않은 시나리오 실행을 저장합니다. 저장된 각 불완전한 실행은 수동 또는 자동으로 해결할 수 있습니다.

>[!NOTE]
>
>기본적으로 미완료 실행 저장은 비활성화되어 있습니다. 활성화하려면 시나리오 고급 설정에서 [!UICONTROL 불완전한 실행 저장 허용] 옵션을 활성화하십시오.
>
>시나리오 설정에 대한 자세한 내용은 [시나리오 설정 구성](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)을 참조하십시오.

## 전체 문서에 대해 강조 표시된 미리 보기 {#highlighted-preview-article-level}

<span class="preview">이 페이지의 정보는 아직 일반적으로 사용할 수 없는 기능을 참조합니다. 미리보기 샌드박스 환경에서만 사용할 수 있습니다.</span>## 불완전한 실행 보기

작업 중 모듈에 오류가 발생하면 미완료 실행 폴더에 새로운 미완료 실행이 추가됩니다. 각 불완전한 실행에는 시나리오의 블루프린트와 실패한 모듈에 매핑할 수 있는 모든 번들이 포함됩니다. 시나리오 세부 정보 페이지에서 [!UICONTROL 불완전 실행] 탭을 클릭하여 불완전 실행 목록을 열 수 있습니다.

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

자세한 내용은 이 문서에서 [불완전한 실행으로 인한 오류](#errors-resulting-into-incomplete-executions)를 참조하십시오.

>[!NOTE]
>
>시나리오당 해결되지 않은 미완료 실행 폴더의 현재 크기 제한은 10MB입니다. 시나리오가 이 제한을 초과하는 경우 다음 오류가 표시될 수 있습니다.
>
>`DLQ limit per scenario has been exceeded`
>
>해결되지 않은 모든 미완료 실행에 대해 팀은 총 500MB로 제한됩니다.
>
>자세한 내용은 시나리오 설정 구성 문서에서 [데이터 손실 사용](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss)을 참조하십시오.


## 미완료 실행 탭에서 미완료 실행 해결

새 미완료 실행이 저장되면 다음과 같이 해결할 수 있습니다.

1. 영향을 받는 시나리오를 엽니다.
1. **[!UICONTROL 미완료 실행]** 탭을 클릭합니다.
1. 해결할 불완전한 실행을 찾은 다음 **[!UICONTROL 세부 정보]**&#x200B;을(를) 클릭합니다.
1. 모든 모듈의 작업이 표시되는 모듈의 로그를 엽니다.
1. 실패한 작업을 찾은 다음 **[!UICONTROL 해결]**&#x200B;을 클릭합니다.

   ![확인 단추](assets/resolve-btn-350x188.png)



## 내역 탭에서 불완전한 실행 해결

불완전한 실행을 해결하기 전에 모든 모듈의 작업 로그를 보려면 [!UICONTROL History] 폴더에서 불완전한 실행을 해결할 수 있습니다.

1. 영향을 받는 시나리오를 엽니다.
1. **[!UICONTROL 기록]** 탭을 클릭합니다.
1. 실패한 시나리오의 실행을 찾은 다음 **[!UICONTROL 세부 정보]**&#x200B;를 클릭합니다.
1. 모든 모듈의 작업이 표시되는 모듈의 로그를 엽니다.
1. 실패한 작업을 찾은 다음 **[!UICONTROL 해결]**&#x200B;을 클릭합니다.

   ![확인 단추](assets/resolve-btn-350x188.png)

## 불완전한 실행과 관련된 옵션

[!UICONTROL 시나리오 설정] 패널의 다음 옵션에 따라 불완전한 실행의 저장 여부와 저장 방법이 결정됩니다.

* 미완료 실행 저장 허용
* 순차적 처리
* 데이터 손실 활성화

이러한 옵션에 대한 자세한 내용은 [시나리오 설정 구성](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)을 참조하십시오.

## 불완전한 실행으로 이어지는 오류

불완전한 실행을 저장하는 몇 가지 범주의 오류가 있습니다. 여기에는 다음이 포함될 수 있습니다.

* 주로 모듈을 통해 모든 데이터를 성공적으로 처리하기 위해 예상되는 누락된 항목 때문에 불완전하거나 잘못된 데이터로 인해 발생하는 유효성 검사 오류.
* 일시적 또는 장기간 연결 실패(예: 이메일 또는 원격 FTP 서버에 연결하는 중)로 인해 최종 대상을 사용할 수 없을 때 발생하는 오류.

시나리오의 첫 번째 모듈에서 오류가 발생하면 실행이 즉시 중지되고 불완전한 실행은 저장되지 않습니다.

다른 모듈에서 오류가 발생하고 첨부된 오류 처리기 경로가 없으면 다음 중 하나가 발생합니다.

* 자동 재시도가 있는 불완전한 실행 레코드는 다음 오류 유형에 대해 저장됩니다.

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* 다음 오류 유형에 대해 자동 재시도 없이 불완전한 실행 레코드가 저장됩니다.

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`

* 오류 유형이 위와 다른 경우 실행이 실패합니다.
