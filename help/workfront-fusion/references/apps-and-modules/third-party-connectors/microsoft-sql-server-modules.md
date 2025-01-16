---
title: Microsoft Server 모듈
description: ' [!DNL Adobe Workfront Fusion] 을 사용하여 Microsoft SQL Server에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server]개 모듈

[!DNL Adobe Workfront Fusion]을(를) 사용하여 [!UICONTROL Microsoft SQL Server]에 연결할 수 있습니다.

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 플랜*</td>
  <td> <p>[!UICONTROL Pro] 이상</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재 라이선스 요구 사항: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합을 위한 [!UICONTROL [!DNL Workfront Fusion]] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>현재 제품 요구 사항: [!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Adobe Workfront] 플랜이 있는 경우 조직에서 이 문서에 설명된 기능을 사용하려면 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다. [!DNL Workfront Fusion]이(가) [!UICONTROL Ultimate] [!DNL Workfront] 계획에 포함되어 있습니다.</p>
   <p>또는</p>
   <p>레거시 제품 요구 사항: 이 문서에 설명된 기능을 사용하려면 조직에서 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.



## [!DNL Workfront Fusion]에 [!DNL Microsoft SQL Server] 서비스를 연결하는 중

[!DNL Microsoft SQL Server] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하세요.

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

## 문제 해결 오류 [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction]

이 오류는 여러 모듈을 사용하여 동일한 데이터를 수정할 때 발생합니다. 이 오류는 SQL 트랜잭션으로 인해 발생합니다.

SQL 모듈이 실행되면 트랜잭션이 시작됩니다. 시나리오가 완전히 실행된 후에 트랜잭션이 완료됩니다.

다른 모듈이 동일한 데이터에 액세스하려고 하면 이전 트랜잭션이 완료될 때까지 기다려야 합니다. 시나리오가 종료된 후에 첫 번째 거래가 종료되므로 두 번째 거래는 결코 시작할 수 없다.

### 해결 방법:

자동 커밋을 켭니다. 자동 커밋은 모듈 실행이 완료된 직후 모든 트랜잭션을 완료(커밋)합니다.

1. 화면 하단의 [!UICONTROL Scenario settings] 아이콘 ![](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)을(를) 클릭합니다.
1. **[!UICONTROL Auto commit]** 확인란을 클릭합니다.
1. 시나리오 설정을 저장하려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.
