---
title: 연결 만들기
description: 연결은 연결되는 앱 또는 웹 서비스의 API에 의해 설정된 요구 사항을 준수해야 합니다. 이러한 이유로 연결 설정에 대한 지침은 앱 또는 웹 서비스에 따라 다릅니다. 이 문서는 Adobe Workfront Fusion을 선택한 앱 또는 웹 서비스에 연결하는 지침을 식별하고 찾는 데 도움이 됩니다.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# 연결 만들기

연결은 연결되는 앱 또는 웹 서비스의 API에 의해 설정된 요구 사항을 준수해야 합니다. 이러한 이유로 연결 설정에 대한 지침은 앱 또는 웹 서비스에 따라 다릅니다. 이 문서는 Adobe Workfront Fusion을 선택한 앱 또는 웹 서비스에 연결하는 지침을 식별하고 찾는 데 도움이 됩니다.

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
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>작업 기반: Workfront Fusion 라이센스 요구 사항 없음</p>
   <p>커넥터 기반(레거시): Workfront 제품군 외부 애플리케이션에 연결하려면 작업 자동화 및 통합을 위한 Workfront Fusion이 있어야 합니다 </p>
   </td> 
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 구성이 필요하지 않은 앱 또는 웹 서비스에 연결

대부분의 경우 모듈을 사용하여 추가 정보가 거의 없거나 전혀 없는 연결을 만들 수 있습니다. Workfront Fusion은 인증을 자동으로 처리합니다.

특별한 고려 사항 없이 연결을 만드는 방법에 대한 지침은 [연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

## Adobe 앱 또는 서비스에 연결

Adobe 앱 또는 서비스에 연결하려면 조직 ID 또는 기술 계정 ID와 같은 Adobe Admin Console의 정보가 필요할 수 있습니다.

또한 Adobe Authenticator 모듈을 사용하여 단일 연결을 사용하여 모든 Adobe API에 연결할 수 있습니다. 이렇게 하면 아직 전용 Fusion 커넥터가 없는 Adobe 제품에 보다 쉽게 연결할 수 있습니다.

자세한 지침은 [커넥터에 대한 문서](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products)를 참조하십시오.

## [!DNL Microsoft] 앱 또는 웹 서비스에 연결

Workfront Fusion의 [!DNL Microsoft] 앱 대부분은 추가 정보 없이 연결을 만들 수 있도록 해줍니다.

다음 상황에서는 연결을 만드는 데 추가 단계가 필요합니다.

* Microsoft Dynamics 365 모듈 사용.

  자세한 지침은 [Microsoft Dynamics 365 모듈](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md)을 참조하세요.

* HTTP 모듈을 사용하여 Microsoft Graph API에 연결

  지침은 [MS Graph REST API를 호출](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md)을 참조하십시오.

## [!DNL Google] 앱 또는 웹 서비스에 연결

사용 중인 [!DNL Google] 계정 종류에 따라 [!DNL Google] 앱에 연결하는 프로세스가 다를 수 있습니다. 또한 Workfront Fusion에 연결할 때 [!DNL Google] 보안 조치에 추가 구성이 필요할 수 있습니다.

자세한 내용은 다음을 참조하십시오.

* [사용자 지정 OAuth 클라이언트를 사용하여 Adobe Workfront Fusion을 Google 서비스에 연결](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [업데이트된 보안 조치를 사용하여 Adobe Workfront Fusion을 Google Services에 연결](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## 추가 구성이 필요한 기타 앱

일부 앱 및 서비스는 Workfront Fusion 연결에 대한 기본 구성을 따르지 않습니다. 해당 앱에 대한 문서에서 이러한 앱을 연결하는 방법에 대한 지침을 찾을 수 있습니다.

자세한 지침은 [커넥터에 대한 문서](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications)를 참조하십시오.
