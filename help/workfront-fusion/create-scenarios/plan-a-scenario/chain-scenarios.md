---
title: 여러 시나리오를 함께 연결
description: 시나리오를 서로 연결하여 한 시나리오가 다른 시나리오를 트리거하고 두 번째 시나리오의 데이터 출력을 첫 번째 시나리오로 반환할 수 있습니다.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: b41f7795273d35dc4e0c019c568f8939926b875a
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 0%

---


# 여러 시나리오를 함께 연결

시나리오를 서로 연결하여 한 시나리오가 다른 시나리오를 트리거하고 두 번째 시나리오의 데이터 출력을 첫 번째 시나리오로 반환할 수 있습니다. 이렇게 하면 여러 시나리오에서 시나리오 섹션을 복제할 필요가 없는 보다 모듈식 시나리오 생성을 수행할 수 있습니다.

상위 시나리오에서 여러 하위 시나리오를 호출할 수 있고 여러 상위 시나리오에서 하위 시나리오를 호출할 수 있습니다. 하위 시나리오를 중첩하여 다른 시나리오에서 호출할 수도 있습니다.

상위 시나리오가 하위 시나리오가 데이터를 반환하기를 기다리는 경우 해당 시간은 상위 시나리오의 시간 제한에 포함되지 않습니다. 예를 들어 상위 시나리오는 5개의 하위 시나리오를 호출하며, 각 시나리오가 실행되는 데 총 50분 동안 10분이 소요됩니다. 상위 시나리오의 모듈 자체는 실행하는 데 15분이 소요됩니다. 총 65분이 경과하여 시간 제한 40분을 초과하더라도 상위 시나리오는 시간 초과되지 않습니다.

시간 초과를 포함하여 Fusion의 성능 보호 기능에 대한 자세한 내용은 [Fusion 성능 보호 기능](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md)을 참조하십시오.

체인 모듈 구성에 대한 지침은 [체인 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)을 참조하십시오.

## 상위 및 하위 시나리오

* **상위** 시나리오가 다른 시나리오를 호출합니다. **체인** > **하위 시나리오 호출** 모듈을 사용합니다. 이후 시나리오 모듈에서 처리할 수 있는 하위 시나리오의 출력을 받습니다.
* **자식** 시나리오는 부모 시나리오에서 호출됩니다. 해당 트리거 모듈은 상위 시나리오로부터 데이터를 수신하고 출력을 상위 시나리오로 반환합니다.

상위 시나리오에는 하위 시나리오의 응답이 필요합니다. 데이터를 반환하지 않는 하위 시나리오는 현재 지원되지 않습니다.

## 체인 시나리오의 데이터 구조

Workfront Fusion은 데이터 구조를 사용하여 상위 시나리오에서 하위 시나리오로 정보를 전송합니다. 데이터 구조는 하위 시나리오에 구성됩니다. 상위 시나리오에서 하위 시나리오가 선택되면 하위 시나리오의 입력으로 사용되는 데이터 구조의 필드가 상위 시나리오에 나타납니다. 이러한 필드에 값을 매핑할 수 있으며, 이 필드는 하위 시나리오가 트리거될 때 전달됩니다.

상위 및 하위 시나리오에서 구성할 모듈에 대한 자세한 내용은 [체인 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)을 참조하세요.

데이터 구조에 대한 자세한 내용은 [데이터 구조](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md)를 참조하십시오.

## 데이터 흐름

1. 데이터는 상위 시나리오를 통해 흐릅니다.
1. 데이터가 하위 시나리오 호출 모듈에 도달합니다. 데이터는 하위 시나리오 호출 모듈의 필드에 매핑되며, 이 필드는 하위 시나리오의 트리거 모듈에 사용된 데이터 구조의 필드와 일치합니다.
1. 하위 호출 시나리오의 데이터가 하위 시나리오에 전달됩니다.
1. 하위 시나리오는 데이터를 처리하고 작업을 수행합니다.
1. 하위 시나리오는 상위 모듈에 대한 반환 응답으로 끝납니다.
1. 상위 모듈에 대한 반환 응답의 출력이 상위 시나리오에 전달됩니다.
1. 하위 시나리오 호출 시나리오의 출력은 하위 시나리오의 출력입니다. 이 출력은 나중에 상위 시나리오에서 처리할 수 있습니다.

## 사용 사례

체인 시나리오에 대한 다음 사용 사례를 고려하십시오.

* **재사용 가능한 논리**: 여러 시나리오에 사용된 반복된 작업에 대해 시나리오를 연결할 수 있습니다. 예를 들어 콘텐츠를 보관하는 시나리오가 여러 개 있는 경우 &quot;콘텐츠 보관&quot;이라는 단일 하위 시나리오를 만들어 콘텐츠를 보관하는 모든 워크플로우에 대해 하위 시나리오로 사용할 수 있습니다.

* **오류 처리**: 조직에서 여러 시나리오(예: 데이터 저장소에 오류 로그를 보내고 Slack 알림을 만드는 오류 처리 경로)에서 동일한 오류 처리 작업을 수행하는 것이 일반적입니다. 이러한 작업으로 하위 시나리오를 만들고 여러 시나리오의 오류 처리 경로에서 해당 시나리오를 연결할 수 있습니다.

* **시간 연장**: 파일을 내보내고 가져오는 경우와 같이 실행 시간이 긴 일괄 처리 작업에 대해 체인 기능을 사용할 수 있습니다. 파일이 많은 경우 이 작업은 시간이 걸립니다. 하위 시나리오는 상위 시나리오의 시간 초과에 대해 계산되지 않으므로 여러 하위 시나리오를 사용하여 파일을 내보내거나 가져오면 실행 시간을 초과할 수 있습니다.

* **반복기를 바꿀 경우** 반복기를 하위 시나리오로 바꾸면 메모리 부족 오류가 발생하는 반복의 복잡한 작업과 같이 메모리 사용량이 줄어들 수 있습니다. 복잡한 작업에 대해 별도의 시나리오를 만들고 반복기를 하위 시나리오 호출 모듈로 바꿀 수 있습니다

* **레코드를 검색하고 만들기**: 예를 들어 사용자를 검색하는 시나리오를 만들 수 있습니다. 이러한 사용자가 존재하는 경우, 스케줄러는 이 사용자를 검토 및 승인해야 하는 액세스 권한이 있는 승인자로 추가합니다. 존재하지 않는 경우 시나리오에서는 관리자가 새 사용자를 온보딩하도록 요청을 만듭니다.

## 체인 시나리오에 대한 실행 내역 보기

체인에 포함된 각 시나리오의 내역을 보고 연결된 시나리오의 실행 내역을 볼 수 있습니다. 예를 들어 상위 시나리오의 실행 내역에는 상위 시나리오에서 직접 처리된 모듈 및 데이터에 대한 정보가 포함됩니다. 하위 시나리오에서 처리된 모듈 및 데이터의 실행 기록을 보려면 하위 시나리오를 열고 여기에서 실행 기록을 보십시오.

하위 시나리오 호출 모듈의 **하위 시나리오로 이동** 단추를 사용하여 실행 기록을 볼 수 있는 하위 시나리오로 빠르게 이동하는 것이 좋습니다. 하위 시나리오가 다른 브라우저 창에서 열리면 상위 시나리오와 하위 시나리오를 동시에 볼 수 있습니다.

![하위 시나리오로 이동 단추](assets/go-to-the-child-button.png)

## 오류 및 불완전한 실행

### 오류 처리

하위 시나리오가 오류일 경우 데이터를 다시 상위로 가져오는 데 영향을 줄 수 있습니다.

하위 시나리오에서 문제가 발생할 경우 상위 시나리오가 하위 시나리오의 응답을 기다리는 동안 중단되지 않도록 하위 시나리오에서 오류 처리를 구성하는 것이 좋습니다.

## 모범 사례

시나리오를 연결할 때 다음 모범 사례를 고려하십시오.

### 시나리오를 연결할 때 재귀 방지

재귀는 무한 루프에 있는 시나리오 자신의 새 실행을 트리거하고 새 실행을 트리거하는 등의 경우에 발생합니다.

재귀를 사용하면 재귀 시나리오를 소유한 조직과 다른 조직 모두에 성능 문제가 발생할 수 있습니다.

시나리오를 연결할 때 재귀를 방지하려면 다음 방법을 따르십시오.

* **하위 시나리오가 상위 시나리오를 트리거할 수 없는지 확인**. 예를 들어 요청이 생성될 때 상위 시나리오가 트리거되는 경우 하위 시나리오가 요청을 생성하지 않는지 확인하십시오.
* **하위 시나리오가 서로 호출하지 않는지 확인**. 예를 들어 하위 시나리오 A가 하위 시나리오 B를 호출하는 경우 하위 시나리오 B가 하위 시나리오 A를 호출하지 않는지 확인합니다.
* **시나리오가 자신을 호출할 수 없는지 확인합니다**. 예를 들어, 하나의 시나리오는 작업을 만들 때 트리거되며, 이 시나리오는 두 개의 작업을 만듭니다. 새로 만든 작업은 모두 시나리오를 다시 트리거하여 4개의 새 작업을 만듭니다. 작업이 생성될 때마다 시나리오가 트리거되고 시나리오가 실행될 때마다 작업 수가 두 배가 됩니다. 작업 수가 기하급수적으로 증가합니다.

>[!IMPORTANT]
>
>* **시나리오가 재귀되면 성능 문제를 방지하기 위해 Fusion 엔지니어링 팀에서 이를 비활성화합니다.**
>* 재귀는 시나리오 설계의 결과이므로 시나리오를 트리거하는 작업이 시나리오에 포함되지 않도록 하는 방식으로 시나리오를 설계해야 합니다.

### 오류 처리를 사용하여 응답 확인

상위 시나리오가 계속하기 전에 하위 시나리오의 응답을 기다리고 있으므로 오류가 발생하더라도 응답을 제공하도록 하위 시나리오가 빌드되었는지 확인해야 합니다.
