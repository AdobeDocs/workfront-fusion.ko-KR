---
title: 즉시 트리거(웹후크)
description: 많은 서비스는 서비스에서 특정 변경 사항이 발생할 때마다 즉시 알림을 전송할 수 있도록 웹후크를 제공합니다. 이러한 알림을 처리하려면 인스턴트 트리거를 사용하는 것이 좋습니다. 이 문서에서는 Adobe Workfront Fusion에서 인스턴트 트리거의 사용 및 기능에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: 5bfda2b2-dc1c-4ff6-9236-b480bfda2e58
source-git-commit: 3746ba1cd213a19a042da1a30b0d57bd1140907c
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# 즉시 트리거(웹후크)

많은 서비스는 서비스에서 특정 변경(이벤트)이 발생할 때마다 즉각적인 알림을 전달하기 위해 웹후크를 제공합니다. 이러한 이벤트를 처리하려면 인스턴트 트리거를 사용하는 것이 좋습니다. 인스턴스 트리거는 지정된 커넥터의 모듈 목록에 `Instant` 태그를 표시합니다.

![즉시](assets/instant.png)

>[!TIP]
>
>커넥터의 모듈 목록을 확인하여 인스턴트 트리거가 있는지 확인하거나 [Fusion 응용 프로그램 및 해당 모듈 참조](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)에서 해당 커넥터의 설명서를 확인할 수 있습니다.
>
>Adobe Workfront 인스턴트 트리거 설명서는 Workfront 모듈 문서에서 [트리거](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#triggers)를 참조하십시오.

커넥터에 웹후크가 포함되지 않은 경우 다음 중 하나를 수행할 수 있습니다.

* Webhook 모듈을 사용하여 사용자 정의 Webhook을 생성합니다.
자세한 내용은 [웹후크](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)를 참조하십시오.
* 폴링 트리거를 사용하여 서비스를 정기적으로 폴링합니다.
자세한 내용은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하세요.

Workfront Fusion의 Webhooks에 대한 비디오 소개는 다음을 참조하십시오.

* [Webhooks 소개](https://video.tv.adobe.com/v/3427025/){target=_blank}
* [중간 웹후크](https://video.tv.adobe.com/v/3427030/){target=_blank}

## 웹후크 세부 정보 보기

[웹후크] 영역에서 웹후크 목록을 볼 수 있습니다.

1. Webhooks 영역을 열려면 왼쪽 탐색에서 Webhooks 아이콘 ![Webhooks](assets/webhooks-icon.png)을 클릭합니다.

   여기에서 웹후크 목록을 볼 수 있습니다.

   ![Webhook 목록](assets/list-of-webhooks.png)

1. 특정 웹후크를 검색하려면 검색 상자에 검색어를 입력합니다.
1. 웹후크를 복사하려면 해당 웹후크 행의 URL 근처에 있는 복사 아이콘 ![웹후크 복사 아이콘](assets/copy-webhook-icon.png)을 클릭합니다.
1. 웹후크를 비활성화하거나 활성화하려면 해당 웹후크 행의 상태 열에서 토글을 비활성화하거나 활성화합니다.
1. 웹후크 대기열이 가득 찼는지 확인하려면 [전체 대기열] 열을 선택합니다. 이 열의 숫자는 현재 큐에 있는 항목의 수입니다.
1. Webhook에서 처리한 작업을 보려면 해당 Webhook의 전체 대기열 열에서 **작업**&#x200B;을 클릭합니다.
1. 웹후크가 만료되었는지 확인하려면 만료됨 열을 선택합니다. 만료된 웹후크는 시나리오에 연결되어 있지 않거나 120시간 동안 이벤트를 받지 않았습니다.
1. 웹후크가 사용되는 시나리오를 보려면 해당 웹후크에 대한 시나리오 열에서 **시나리오** 단추를 클릭하십시오.
1. 이 웹후크에 사용된 연결을 보려면 해당 웹후크의 연결 열에서 **연결** 단추를 클릭하십시오.
1. 열을 숨기거나 이전에 숨겨진 열을 표시하려면 **열** 아이콘 ![열 아이콘](assets/glist-column.png)을 클릭하고 열 이름을 선택하거나 선택 취소합니다.

## 인스턴트 트리거 예약

인스턴트 트리거를 구성할 때 트리거 실행 시기를 선택하라는 메시지가 표시됩니다.

![일정 설정](assets/schedule-setting.png)

Workfront Fusion이 서비스에서 새 이벤트를 받을 때 시나리오를 즉시 실행하려면 `Immediately`을(를) 선택합니다. 이러한 이벤트는 즉시 대기열로 전송되며 데이터가 수신되는 순서로 한 번에 하나씩 시나리오에서 처리됩니다.

시나리오가 실행되면 대기열에 대기 중인 총 보류 이벤트 양이 계산되고 시나리오는 보류 중인 이벤트만큼 주기를 수행하여 주기당 하나의 이벤트를 처리합니다.

주기에 대한 자세한 내용은 [시나리오 실행, 주기 및 단계](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)를 참조하십시오.

>[!NOTE]
>
>* 주기는 시나리오 실행과 동일하지 않습니다. 한 시나리오 실행 내에 여러 주기가 있을 수 있습니다.
>* `Immediately` 실행 예정인 인스턴스 트리거를 사용하여 시나리오를 실행할 경우 다음 예외가 적용됩니다.
>
>     * 두 실행 사이의 간격은 가격 계획에 따른 최소 간격의 적용을 받지 않는다.
>
>       예를 들어 시나리오의 실행이 완료되면 웹후크의 대기열이 다시 확인됩니다. 보류 중인 웹후크가 있는 경우 시나리오는 즉시 다시 실행되어 보류 중인 모든 웹후크를 다시 처리합니다.
>   
>     * 최대 주기 수 시나리오 설정이 무시되고 100으로 설정되므로 단일 시나리오 실행 중에 100개 이하의 보류 중인 웹후크가 처리됩니다(주기당 이벤트 1개 비율).
>


[!UICONTROL 즉시] 이외의 다른 일정 설정을 사용하는 경우 지정한 간격으로 시나리오가 실행됩니다. 간격 동안 큐에 여러 개의 웹 후크를 수집할 수 있으므로 한 시나리오 실행에서 더 많은 웹 후크를 처리하려면 [!UICONTROL 최대 주기 수] 옵션을 기본 1보다 높은 값으로 설정하는 것이 좋습니다.

1. 시나리오 하단의 [!UICONTROL 시나리오 설정] 아이콘 ![시나리오 설정 아이콘](assets/scenario-settings-icon.png)을 클릭합니다.
1. 표시되는 **[!UICONTROL 시나리오 설정]** 패널에서 **[!UICONTROL 최대 주기 수]** 필드에 숫자를 입력하여 시나리오를 실행할 때마다 실행할 큐의 이벤트 수를 나타냅니다.

다음에 시나리오를 실행할 때 큐에 남아 있는 이벤트는 최대 주기 필드에 설정된 수까지 처리됩니다.

## 웹후크 가드레일

Workfront Fusion에는 원활한 성능 확보를 위해 다음과 같은 웹 후크 보호 기능이 있습니다.

### 비율 제한

현재 속도 제한은 초당 5개의 웹후크입니다. 한도를 초과하면 `429` 상태 코드가 반환됩니다.

### 비활성 웹후크 만료

120시간 이상 시나리오에 할당되지 않은 웹후크가 제거됩니다.

### Webhook 페이로드

Workfront Fusion은 30일 동안 웹후크 페이로드를 저장합니다. 웹후크 페이로드가 생성된 후 30일이 지난 후에 액세스하면 [!UICONTROL `Failed to read file from storage.`] 오류가 발생합니다

### 오류 처리

즉시 트리거를 사용하는 시나리오에서 오류가 있는 경우 시나리오는 다음과 같습니다.

* 시나리오가 [!UICONTROL 즉시]을 실행하도록 설정된 경우 즉시 중지됩니다.
* 시나리오가 예약대로 실행되도록 설정된 경우 3번의 시도 실패(오류 3회) 후 중지됩니다.

시나리오 실행 중에 오류가 발생하면 인스턴트 트리거의 롤백 단계 중에 이벤트가 다시 큐에 배치됩니다. 이러한 상황에서는 시나리오를 수정하고 다시 실행할 수 있습니다.

자세한 내용은 시나리오 실행, 주기 및 단계 문서에서 [롤백](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback)을 참조하십시오.

시나리오에 Webhook 응답 모듈이 있으면 오류가 Webhook 응답으로 전송됩니다. 웹후크 응답 모듈은 항상 마지막으로 실행됩니다(시나리오 설정의 [!UICONTROL 자동 커밋] 옵션이 활성화되지 않은 경우).

자세한 내용은 문서 Webhooks에서 [Webhooks에 응답](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md#responding-to-webhooks)을 참조하십시오.

### Webhook 비활성화

다음 중 하나가 적용되는 경우 웹후크는 자동으로 비활성화됩니다.

* 웹후크가 5일 이상 어떤 시나리오에도 연결되지 않았습니다.
* 웹후크는 30일 이상 비활성 상태인 비활성 시나리오에서만 사용됩니다.

비활성화된 웹후크는 시나리오에 연결되지 않은 경우 자동으로 삭제되고 등록 취소되며 30일 이상 비활성화된 상태입니다.

## 사용자 지정 웹 후크

자신만의 웹후크를 만들 수 있습니다. 자세한 내용은 [웹후크](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)를 참조하십시오.

## 리소스

주기에 대한 자세한 내용은 [시나리오 실행, 주기 및 단계](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)를 참조하십시오.
