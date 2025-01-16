---
title: 연결 만들기 - 기본 지침
description: 연결을 만들 때 대부분의  [!DNL Adobe Workfront Fusion] 커넥터는 사용자 지정 구성이 필요하지 않습니다. 이 문서에서는 기본 연결 생성 프로세스에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 연결 만들기 - 기본 지침

연결을 만들 때 많은 [!DNL Adobe Workfront Fusion] 커넥터에 사용자 지정 구성이 필요하지 않습니다. 이 문서에서는 기본 연결 생성 프로세스에 대해 설명합니다.

>[!NOTE]
>
>
>Adobe Workfront Fusion에서 시나리오에서 사용하려는 웹 서비스용 앱을 제공하지 않는 경우 다음 문서에 설명된 대로 [!DNL Workfront Fusion] HTTP 및 Webhooks 모듈을 사용하여 웹 서비스에 연결할 수 있습니다.
>
>* [API 토큰 인증을 사용하는 웹 서비스에 Adobe Workfront Fusion 연결](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [커넥터 없이 웹 서비스에 대한 웹후크 구성](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
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

## 연결 만들기

[!DNL Workfront Fusion] 모듈 내에서 연결을 만들려면:

1. [!UICONTROL Connection] 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭하여 **[!UICONTROL Create a connection]** 패널을 엽니다.
1. (선택 사항) 기본 **[!UICONTROL Connection name]**&#x200B;을(를) 변경합니다.
1. (조건부) 앱에 ID, 키 또는 [!UICONTROL secret]과(와) 같은 고급 연결 설정이 필요한 경우 해당 정보를 입력하십시오.

   이러한 정보를 입력할 수 있는 필드를 표시하려면 **[!UICONTROL Show advanced settings]**&#x200B;을(를) 클릭해야 할 수 있습니다.

1. **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.
1. 아직 로그인하지 않은 경우 표시되는 로그인 창에서 자격 증명을 입력하여 앱에 로그인합니다.
1. (조건부) **[!UICONTROL Allow]** 단추가 표시되면 커넥터가 수행할 수 있는 작업을 검사한 다음 단추를 클릭하여 앱을 [!DNL Workfront Fusion]에 연결합니다.

   >[!NOTE]
   >
   >일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
   >
   >예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.
