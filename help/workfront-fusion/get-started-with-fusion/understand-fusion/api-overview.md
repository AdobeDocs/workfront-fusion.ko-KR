---
title: API 개요
description: 애플리케이션 프로그래밍 인터페이스(API)는 애플리케이션과 서비스가 서로 통신할 수 있는 방법입니다. Fusion은 API를 사용하여 연결 중인 애플리케이션과 통신합니다. 각 애플리케이션에는 별도의 API가 있습니다.
author: Becky
feature: Workfront Fusion
source-git-commit: 74308a6a43418296b29739f03683f23357d545bc
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 87%

---

# Fusion의 API 개요

<!--Add me to TOCs-->

애플리케이션 프로그래밍 인터페이스(API)는 애플리케이션과 서비스가 서로 통신할 수 있는 방법입니다. Fusion은 API를 사용하여 연결 중인 애플리케이션과 통신합니다.

API는 애플리케이션 소유자가 만들고 제어합니다. 예를 들어, Workfront API는 Adobe의 Workfront 팀이 소유하고, Microsoft Graph API는 Microsoft가 소유합니다. API 소유자는 API를 통해 사용할 수 있는 액션을 정의합니다.

>[!NOTE]
>
>Workfront Fusion에는 Fusion에서 작업을 자동화하는 데 사용할 수 있는 자체 API가 있습니다.
>API는 점진적으로 릴리스되고 있으며 현재 실험으로 표시되어 있습니다. Fusion 팀은 API를 활발하게 개발 및 확장하고 있으며 새로운 기능을 사용할 수 있게 되면 업데이트가 게시됩니다.
>Workfront Fusion API에 대한 설명서는 [Workfront Fusion API](https://developer.adobe.com/workfront-fusion-apis/)를 참조하십시오.

## 고려 사항

API가 Fusion이 아닌 소유자에 의해 정의되므로 몇 가지 중요한 고려 사항이 발생합니다.

* **Fusion을 사용하여 해당 앱이나 서비스에 전용 커넥터를 제공하는지 여부에 관계없이** 공개 API가 있는 모든 앱이나 서비스에 연결할 수 있습니다. Fusion의 범용 커넥터를 사용하여 이러한 앱이나 서비스를 시나리오로 가져올 수 있습니다.

  범용 커넥터 목록은 [범용 커넥터](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)를 참조하십시오.

* **애플리케이션의 API를 소유자가 변경하면 Fusion 기능에 영향을 줄 수 있습니다.** 변경 내용이 너무 심각하다면 Fusion은 모듈이나 연결 유형을 업데이트해야 할 수도 있고, 극단적인 경우 애플리케이션을 위한 새 커넥터를 만들 수도 있습니다.

  이러한 극단적인 상황, 즉 “주요 변경 사항”에 대한 자세한 내용은 이 문서의 [주요 변경 사항](#breaking-changes)을 참조하십시오.


## 주요 변경 사항

API 소유자가 가용성에서 API의 일부 또는 전부를 제거하는 경우 주요 변경 사항의 일반적인 원인은 사용 중단입니다. 이 경우 Fusion 팀은 신규 버전의 애플리케이션 API로 Fusion 기능을 신속하게 재조정하기 위해 모든 노력을 기울입니다. 일반적으로 새로운 모듈, 연결 유형 또는 커넥터의 형태를 취합니다.

Fusion 시나리오는 특정 데이터로 구성되므로 시나리오를 업데이트해야 할 수도 있습니다.

* 변경 사항이 인증 또는 권한 부여와 관련된 경우 해당 애플리케이션의 연결을 업데이트해야 할 수도 있습니다.
* 변경 사항이 API의 특정 액션(엔드포인트)과 관련된 경우 해당 작업과 관련된 모듈을 신규 버전의 모듈로 업데이트해야 할 수도 있습니다.
* Fusion에서 사용하는 전체 API 버전이 더 이상 사용되지 않는 경우, 해당 커넥터의 모든 모듈을 신규 버전의 커넥터로 업데이트해야 할 수도 있습니다.

대부분의 경우 모듈을 재구성할 필요 없이 신규 버전의 모듈로 업그레이드할 수 있습니다.

모듈 업그레이드에 대한 자세한 내용과 지침은 [모듈을 신규 버전으로 업그레이드](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md)를 참조하십시오.
