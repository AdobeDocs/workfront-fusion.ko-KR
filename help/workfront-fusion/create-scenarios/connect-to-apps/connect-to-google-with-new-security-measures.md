---
title: 업데이트된 보안 조치를 사용하여 Adobe Workfront Fusion을 Google Services에 연결
description: Google은 사용자가 API를 사용하는 방법에 대한 제한 사항을 도입했습니다. 이 문서에서는 이러한 업데이트 보안 조치를 고려하여 Adobe Workfront Fusion을 Google에 연결하는 방법에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# 업데이트된 보안 조치를 사용하여 Adobe Workfront Fusion을 Google Services에 연결

Google은 사용자가 API를 사용하는 방법에 대한 제한 사항을 도입했습니다. 이 문서에서는 이러한 업데이트 보안 조치를 고려하여 Adobe Workfront Fusion을 Google에 연결하는 방법에 대해 설명합니다.

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

## Google 서비스 제한 사항

Google은 2020년 6월 1일부터 사용자가 API를 사용할 수 있는 방법에 대한 제한 사항을 도입했습니다. 이러한 보안 조치를 통해 Google 사용자는 Google에서 개인 데이터가 유출되거나 오용되지 않도록 보호할 수 있습니다.

이러한 제한 사항은 Gmail 및 Google 드라이브 앱과 관련되어 있습니다.

이러한 제한 사항에 대한 자세한 내용은 [Google API 서비스 사용자 데이터 정책](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)의 &quot;특정 API 범위에 대한 추가 요구 사항&quot;을 참조하십시오

제한된 범위에 액세스하려면 연결된 서비스(Adobe Workfront Fusion 또는 API를 통해 사용자의 데이터에 액세스하는 기타 서비스)를 확인해야 하며, 서비스가 데이터를 사용하는 방법에 대해 안전하고 투명하게 제공된다는 것을 입증하는 평가 서신이 있어야 합니다. Workfront Fusion은 제한된 범위에 액세스하기 위한 Google의 모든 요구 사항을 준수합니다. 그러나 Workfront Fusion의 서드파티 연결 서비스 대부분은 평가 서신이 없으므로 Google 약관을 준수하지 않습니다. 이러한 이유로 Workfront Fusion에서는 이러한 서비스에 데이터를 보낼 수 없습니다.

## Google 서비스 제한 예외

새로운 제한 사항을 위반하지 않고 평가 서신이 없는 승인되지 않은 서드파티 서비스로 데이터를 보낼 수 있도록 하는 몇 가지 예외가 있습니다. 이는 Workfront Fusion OAuth 클라이언트가 있는 Google Workspace, 다른 OAuth 클라이언트가 있는 Google Workspace 또는 @gmail.com 및 @googlemail.com에 따라 다릅니다.

* [Workfront Fusion OAuth 클라이언트가 있는 Google Workspace](#google-workspace-with-workfront-fusion-oauth-client)
* [다른 OAuth 클라이언트와 함께 Google Workspace](#google-workspace-with-another-oauth-client)
* [@gmail.com 및 @googlemail.com](#gmailcom-and-googlemailcom)

### Workfront Fusion OAuth 클라이언트가 있는 Google Workspace

Workfront Fusion에서는 도메인 전체 설치 예외를 사용합니다. 도메인 전체 설치는 Google Workspace 사용자에게 적합하며, 사용자가 승인되지 않은 서비스를 제한 없이 통합할 수 있도록 합니다. Google Workspace 사용자의 경우 추가 단계를 수행하지 않아도 되며 승인되지 않은 서비스에 직접 연결할 수 있습니다.

### 다른 OAuth 클라이언트와 함께 Google Workspace

Workfront Fusion OAuth 클라이언트를 사용하는 대신 자체 OAuth 클라이언트를 사용하는 Google Workspace 사용자는 내부 사용 접근 방식을 통해 Google 서비스에 연결할 수 있습니다. 이 옵션은 고급 사용자를 위한 것입니다. 지침은 [사용자 지정 OAuth 클라이언트를 사용하여 Adobe Workfront Fusion을 Google 서비스에 연결](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)을 참조하십시오.

### @gmail.com 및 @googlemail.com {#gmailcom-and-googlemailcom}

@gmail.com 또는 @googlemail.com을 통해 Google 서비스에 액세스하는 사용자는 개인 사용 접근 방식을 통해 Google 서비스에 연결할 수 있습니다. 이 옵션은 고급 사용자를 위한 것입니다. 지침은 [사용자 지정 OAuth 클라이언트를 사용하여 Adobe Workfront Fusion을 Google 서비스에 연결](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)을 참조하십시오.

## FAQ

* [영향을 받는 Adobe Workfront Fusion 앱은 무엇입니까?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Google Workspace 계정이 있습니까?](#do-i-have-a-g-suite-account)
* [@gmail.com 또는 @googlemail.com 사용자인 경우 어떻게 해야 합니까?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [Google Workspace 사용자인 경우 어떻게 해야 합니까?](#what-should-i-do-if-im-a-g-suite-user)

### 영향을 받는 Adobe Workfront Fusion 앱은 무엇입니까? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google 드라이브, Gmail 및 이메일(Gmail 계정에 연결됨).

### Google Workspace 계정이 있습니까? {#do-i-have-a-g-suite-account}

이메일 주소가 @gmail.com 또는 @googlemail.com으로 끝나는 경우 계정은 Google Workspace 계정이 아닙니다. Google 계정이 @my-company.com과 같은 사용자 정의 도메인으로 끝나는 경우 Google Workspace 계정입니다.

### @gmail.com 또는 @googlemail.com 사용자인 경우 어떻게 해야 합니까? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

이러한 새 제한 사항은 Google 드라이브 또는 Gmail을 통합하는 경우에만 적용됩니다. Google 드라이브 또는 Gmail에 연결하려면 다음을 수행할 수 있습니다.

* Google Workspace으로 전환

  또는

* 사용자 지정 OAuth 클라이언트를 만듭니다. 이 옵션은 고급 사용자를 위한 것입니다.

  지침은 [사용자 지정 OAuth 클라이언트를 사용하여 Adobe Workfront Fusion을 Google 서비스에 연결](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)을 참조하십시오.

Google Drive 또는 Gmail 이외의 다른 서비스를 통합하려는 경우 이러한 제한 사항이 적용되지 않습니다.

### Google Workspace 사용자인 경우 어떻게 해야 합니까? {#what-should-i-do-if-im-a-g-suite-user}

필요한 작업이 없습니다.
