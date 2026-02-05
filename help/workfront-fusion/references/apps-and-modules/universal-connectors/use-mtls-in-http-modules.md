---
title: Adobe Workfront Fusion의 HTTP 모듈에서 상호 TLS 사용
description: Adobe Workfront Fusion HTTP 모듈에서 Mutual TLS를 사용하여 정보 트랜잭션의 양쪽에서 상대방의 ID를 확인할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 6a4bf090e7804f0b2b9ca6eefbb7490d1c35b6ce
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 16%

---

# Adobe Workfront Fusion의 HTTP 모듈에서 상호 TLS 사용

## 상호 TLS 개요

인터넷을 통해 데이터를 보낼 때는 데이터를 올바른 위치로 이동하거나 올바른 위치에서 가져오는지, 의도한 수신자만 읽을 수 있는지 확인하는 것이 중요합니다. TLS가 활성화된 상태에서 클라이언트(정보를 요청하는 컴퓨터)는 인증서를 사용하여 서버(정보를 제공하는 컴퓨터)의 ID를 확인합니다. 이렇게 하면 보안 HTTP 연결이 설정됩니다.

상호 TLS를 통해 이 신원 확인은 두 가지 방법으로 가능하다. 서버가 해당 ID를 확인하기 위해 인증서를 클라이언트에 보내면 클라이언트의 인증서도 요청합니다. 이렇게 하면 서버가 정보를 오용할 사이트나 사용자에게 보내지 않습니다.

>[!INFO]
>
>**예:**
>
>* **TLS**: 브라우저에 &quot;MyGreatBank.com&quot;을 입력하면 뱅킹 정보를 오용하거나 판매하는 웹 사이트가 아니라 My Great Bank로 이동하는지 확인하려고 합니다. 그들은 또한 그들의 은행 계좌 정보가 암호화되어 있는지 확인하기를 원한다.
>
>   브라우저(클라이언트)가 MyGreatBank.com(서버)에 연결하면 TLS는 MyGreatBank.com에서 인증서를 요청하여 ID를 확인합니다. 인증서는 [!DNL DigiCert] 또는 [!DNL Thawte] 등의 인증 기관에서 제공합니다. 브라우저는 인증 기관을 신뢰하므로 연결을 허용합니다.
>
>* **상호 TLS**: MySoftware.com은 MyGreatBank.com API의 정보가 필요한 소프트웨어 클라이언트입니다. MyGreatBank는 신뢰할 수 있는 클라이언트만 서버에 연결할 수 있도록 합니다. 따라서 MyGreatBank.com의 ID를 확인하는 일반 TLS 외에 TLS/인증서 기관 프로세스는 MySoftware.com의 요청도 확인합니다.

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

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
   <p>작업 기반: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## Workfront Fusion 공개 인증서 제공

HTTP 요청을 사용하여 웹 서비스에 연결할 경우 일반적으로 웹 서비스에는 확인을 위한 Workfront Fusion 공개 인증서가 필요합니다. 이렇게 하면 웹 서비스가 인증서가 웹 서비스의 허용 목록에 추가하다에 있는지 확인하는 방법으로 HTTP 요청에 표시된 인증서를 파일에 있는 인증서와 비교할 수 있습니다.

Adobe Workfront Fusion 공개 인증서를 웹 서비스에 업로드하는 방법에 대한 지침은 웹 서비스의 설명서를 참조하십시오.

>[!NOTE]
>
>인증서 외에 다른 정보를 제공해야 할 수도 있습니다. 웹 서비스에 필요한 사항에 대한 자세한 내용은 웹 서비스의 API 설명서를 참조하십시오.

다음 링크를 사용하여 Workfront Fusion 공개 인증서를 다운로드할 수 있습니다. 데이터 센터를 찾으려면 조직의 허용 목록에 추가하다에서 Fusion에 대한 IP 주소 구성 문서의 [데이터 센터 식별](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)을 참조하십시오.

### 2026년 인증서

>[!IMPORTANT]
>
>* 이러한 Workfront Fusion 공개 인증서는 클러스터에 따라 다른 날에 만료됩니다. 만료일을 확인하려면 아래 차트를 확인하십시오. 만료되면 웹 서비스에 새 인증서를 업로드해야 합니다. 권장 사항:
>
>   * 만료 날짜를 기록하고 인증서를 웹 서비스에 업로드하도록 미리 알림을 설정하십시오.
>   * 새 인증서를 쉽게 찾으려면 이 페이지에 책갈피를 지정합니다.
>
>* 이는 비 와일드카드 mTLS 인증서입니다.

| 데이터 센터 | 다운로드 링크 | 유효한 날짜 |
| --- | --- | --- |
| 미국 AWS 데이터 센터 | [Workfront Fusion US 인증서 2026 다운로드](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-us-mtls-certificate-2026.pem) | 2026년 1월 29일~2027년 3월 2일 |
| US Azure 클러스터 | [Workfront Fusion US Azure 인증서 2026 다운로드](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-az-mtls-certificate.pem) | 2025년 9월 21일~2026년 10월 23일 |
| EU AWS 데이터 센터 | [Workfront Fusion EU 인증서 2026 다운로드](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-eu-mtls-certificate-2026.pem) | 2026년 1월 29일~2027년 3월 2일 |
| EU Azure 클러스터 | [Workfront Fusion EU Azure 인증서 2026 다운로드](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-eu-az-mtls-certificate-2026.pem) | 2026년 2월 4일~2027년 3월 8일 |


### 2025년 인증서

>[!IMPORTANT]
>
>* 위에서 제공하는 2026년 인증서를 설치하는 것이 좋습니다.
>* 이러한 Workfront Fusion 공개 인증서는 **2026년 4월 4일**(미국 및 유럽 연합) 또는 **2025년 11월 25일**(Azure)에 만료됩니다. 만료되면 웹 서비스에 새 인증서를 업로드해야 합니다. 권장 사항:
>
>   * 만료 날짜를 기록하고 인증서를 웹 서비스에 업로드하도록 미리 알림을 설정하십시오.
>   * 새 인증서를 쉽게 찾으려면 이 페이지에 책갈피를 지정합니다.
>
>* 이는 비 와일드카드 mTLS 인증서입니다.

| 데이터 센터 | 다운로드 링크 | 유효한 날짜 |
| --- | --- | --- |
| 미국 데이터 센터 | [Workfront Fusion US 인증서 2025 다운로드](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | 2025년 3월 3일~2026년 4월 4일 |
| EU 데이터 센터 | [Workfront Fusion EU 인증서 2025 다운로드](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | 2025년 3월 3일~2026년 4월 4일 |
| Azure 클러스터 | [Workfront Fusion Azure 인증서 2025 다운로드](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | 2024년 10월 24일~2025년 11월 25일 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These Workfront Fusion public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download Workfront Fusion Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download Workfront Fusion EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## Workfront Fusion HTTP 모듈에서 상호 TLS 활성화

모든 Workfront Fusion [!UICONTROL HTTP] 요청 모듈에는 Mutual TLS를 활성화하는 옵션이 있습니다.

[!UICONTROL HTTP] 요청 모듈에서 Mutual TLS를 활성화하려면 다음을 수행하십시오.

1. 시나리오에 [!UICONTROL HTTP] 요청 모듈을 추가합니다.
1. 모듈 구성을 시작합니다.

   [!UICONTROL HTTP] 요청 모듈을 구성하는 방법에 대한 지침은 [Universal connectors](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)의 해당 문서를 참조하십시오.

1. 모듈 아래쪽에서 **[!UICONTROL 고급 설정 표시]**&#x200B;를 사용하도록 설정합니다.
1. **[!UICONTROL 상호 TLS 사용]**&#x200B;을 사용하도록 설정합니다.
