---
title: API 개요
description: API(Application Programming Interface)는 애플리케이션과 서비스가 서로 통신하는 방법입니다. Fusion은 API를 사용하여 연결 중인 애플리케이션과 통신합니다. 각 애플리케이션에는 별도의 API가 있습니다.
author: Becky
feature: Workfront Fusion
source-git-commit: 1ee32ad1faa8c105142f85e83f1b522548fc7f93
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Fusion의 API 개요

<!--Add me to TOCs-->

API(Application Programming Interface)는 애플리케이션과 서비스가 서로 통신하는 방법입니다. Fusion은 API를 사용하여 연결 중인 애플리케이션과 통신합니다.

API는 애플리케이션 소유자가 만들고 제어합니다. 예를 들어 Workfront API는 Adobe의 Workfront 팀이 소유하며 Microsoft Graph API는 Microsoft이 소유합니다. API 소유자는 API를 통해 사용할 수 있는 작업을 정의합니다.

## 고려 사항

API는 Fusion이 아닌 해당 소유자에 의해 정의되므로 몇 가지 중요한 고려 사항이 발생합니다.

* **Fusion을 사용하여 공용 API가 있는 모든 앱 또는 서비스에 연결할 수 있습니다**(Fusion에서 해당 앱 또는 서비스에 전용 커넥터를 제공하는지 여부). Fusion의 범용 커넥터를 사용하여 이러한 앱이나 서비스를 시나리오로 가져올 수 있습니다.

  범용 커넥터 목록은 [범용 커넥터](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)를 참조하십시오.

* **응용 프로그램의 API 소유자가 변경한 내용은 Fusion 기능에 영향을 줄 수 있습니다.** 변경 내용이 너무 심하면 Fusion에서 모듈 또는 연결 유형을 업데이트해야 하거나, 경우에 따라 응용 프로그램에 대한 새 커넥터를 만들 수 있습니다.

  &quot;변경 내용 깨기&quot;라고 하는 이러한 극단적인 상황에 대한 자세한 내용은 이 문서의 [변경 내용 깨기](#breaking-changes)를 참조하십시오.


## 주요 변경 사항

API 소유자가 가용성에서 API의 일부 또는 전부를 제거할 때 변경 사항을 중단하는 일반적인 원인은 사용 중단입니다. 이 경우 Fusion 팀은 Fusion 기능을 새로운 버전의 애플리케이션 API와 빠르게 재정렬하기 위해 최선을 다합니다. 일반적으로 새로운 모듈, 연결 유형 또는 커넥터 형태를 취합니다.

Fusion 시나리오는 특정 데이터로 구성되므로 시나리오를 업데이트해야 할 수 있습니다.

* 변경 사항이 인증 또는 권한 부여와 관련된 경우 해당 애플리케이션에 대한 연결을 업데이트해야 할 수 있습니다.
* 변경 사항이 API의 특정 작업(엔드포인트)과 관련된 경우, 해당 작업과 관련된 모듈을 모듈의 새 버전으로 업데이트해야 할 수 있습니다.
* Fusion에서 사용하는 전체 API 버전이 더 이상 사용되지 않는 경우 해당 커넥터의 모든 모듈을 새 버전의 커넥터로 업데이트해야 할 수 있습니다.

대부분의 경우 모듈을 다시 구성할 필요 없이 새 버전의 모듈로 업그레이드할 수 있습니다.

모듈 업그레이드에 대한 자세한 내용과 지침은 [모듈을 새 버전으로 업그레이드](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md)를 참조하십시오.
