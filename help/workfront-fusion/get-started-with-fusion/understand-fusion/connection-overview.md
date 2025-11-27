---
title: 연결 개요
description: 대부분의 앱에서는 특정 시나리오의 설정에 따라 Adobe Workfront Fusion이 지정된 제3자 서비스와 통신할 수 있는 연결을 만들어야 합니다.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: ht
source-wordcount: '315'
ht-degree: 100%

---

# 연결 개요

Workfront Fusion은 대부분의 애플리케이션에 연결이 필요합니다.  이 연결을 사용하여 지정된 제3자 서비스와 통신합니다.

예를 들어, Workfront에서 정보를 가져오는 시나리오를 만들고 싶다면 Workfront Fusion이 Workfront 계정에 액세스할 수 있는 권한을 부여해야 합니다.

연결은 Fusion이 애플리케이션에 액세스하는 데 사용하는 인증 및 권한을 나타냅니다. 시나리오에서 사용되는 각 애플리케이션에 대해 하나 이상의 연결을 만들 수 있으며, 여러 모듈이나 시나리오에서 동일한 연결을 사용할 수 있습니다.

대부분의 연결은 단일 애플리케이션에만 사용됩니다. 예를 들어, [!UICONTROL Salesforce] 모듈에서는 Workfront 연결을 사용할 수 없습니다. 일부 [!DNL Adobe] 애플리케이션은 연결을 공유할 수 있습니다. 자세한 내용은 [Fusion 애플리케이션 및 해당 모듈 참조: 문서 색인](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)에 나열된 해당 애플리케이션의 문서를 참조하십시오.

연결은 팀이 소유합니다. 팀의 모든 구성원은 팀의 연결에 접근할 수 있으며, 팀 외부의 사용자는 팀의 연결에 접근할 수 없습니다.

## 액세스 권한

모든 연결에 대해 Workfront Fusion은 주어진 시나리오를 성공적으로 완료하는 데 필요한 액세스 권한만 필요합니다. 예를 들어, Workfront에서 문서를 다운로드하는 시나리오를 만들면 Workfront Fusion은 새 프로젝트를 만들 수 있는 권한을 요청하지 않습니다. 나중에 프로젝트를 만들어야 하는 경우 연결을 업데이트하거나 프로젝트를 만들 수 있는 새 연결을 만들 수 있습니다.

모든 서비스가 특정 작업에 대한 액세스를 제한하는 것은 아닙니다. 이 경우 Workfront Fusion은 전체 액세스 권한이 필요합니다. 해당 서비스에 등록된 계정에 Workfront Fusion 접근을 제한하는 방법에 대한 자세한 내용은 [Fusion 애플리케이션 및 해당 모듈 참조: 문서 색인](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)에 나열된 애플리케이션별 설명서를 참조하십시오.
