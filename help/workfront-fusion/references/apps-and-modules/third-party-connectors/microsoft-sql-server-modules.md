---
title: Microsoft Server 모듈
description: ' [!DNL Adobe Workfront Fusion] 을 사용하여 Microsoft SQL Server에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server]개 모듈

[!DNL Adobe Workfront Fusion]을(를) 사용하여 [!UICONTROL Microsoft SQL Server]에 연결할 수 있습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
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
   <p>레거시: 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## [!DNL Workfront Fusion]에 [!DNL Microsoft SQL Server] 서비스를 연결하는 중

[!DNL Microsoft SQL Server] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion에 연결 만들기] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.

## [!DNL Microsoft SQL Server]개 모듈 사용

저장 프로시저를 통해 데이터베이스 서버에서 직접 사용자 지정 논리를 실행할 수 있습니다. [!DNL Adobe Workfront Fusion]은(는) 입력/출력 매개 변수 및 레코드 집합의 인터페이스를 동적으로 로드하므로 각 매개 변수 또는 값을 개별적으로 매핑할 수 있습니다. 시나리오 구성을 시작하기 전에 데이터베이스에 연결하는 데 사용하는 계정에 `INFORMATION_SCHEMA.ROUTINES` 및 `INFORMATION_SCHEMA.PARAMETERS` 보기에 대한 읽기 권한이 있는지 확인하십시오.

[!DNL Fusion]이(가) [!DNL SQL server] 대상에 대한 연결을 설정하면 [!DNL Fusion] 사용자가 호스트(서버가 호스트되는 도메인 이름 또는 IP 주소)와 포트를 식별합니다. [!DNL Fusion]은(는) 사용 가능한 모든 호스트 및 포트에 연결할 수 있습니다.

[!DNL Workfront Fusion]에서 사용하는 특정 IP 주소에 대한 자세한 내용은 [액세스할 IP 주소 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)를 참조하십시오.

저장 프로시저 만들기에 대한 자세한 내용은 [!DNL Microsoft SQL Server] 설명서를 참조하세요.

>[!NOTE]
>
>[!DNL Workfront Fusion]은(는) 여러 개의 레코드 집합을 지원하지 않습니다. 첫 번째 작업만 처리됩니다.

## 문제 해결 오류 [!UICONTROL ER_LOCK_WAIT_TIMEOUT: 잠금 대기 시간 제한을 초과했습니다. 트랜잭션을 다시 시작해 보십시오]

이 오류는 여러 모듈을 사용하여 동일한 데이터를 수정할 때 발생합니다. 이 오류는 SQL 트랜잭션으로 인해 발생합니다.

SQL 모듈이 실행되면 트랜잭션이 시작됩니다. 시나리오가 완전히 실행된 후에 트랜잭션이 완료됩니다.

다른 모듈이 동일한 데이터에 액세스하려고 하면 이전 트랜잭션이 완료될 때까지 기다려야 합니다. 시나리오가 종료된 후에 첫 번째 거래가 종료되므로 두 번째 거래는 결코 시작할 수 없다.

### 해결 방법:

자동 커밋을 켭니다. 자동 커밋은 모듈 실행이 완료된 직후 모든 트랜잭션을 완료(커밋)합니다.

1. 화면 하단의 [!UICONTROL 시나리오 설정] 아이콘 ![시나리오 설정 아이콘](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)을 클릭합니다.
1. **[!UICONTROL 자동 커밋]** 확인란을 클릭합니다.
1. 시나리오 설정을 저장하려면 **[!UICONTROL 확인]**&#x200B;을 클릭하세요.
