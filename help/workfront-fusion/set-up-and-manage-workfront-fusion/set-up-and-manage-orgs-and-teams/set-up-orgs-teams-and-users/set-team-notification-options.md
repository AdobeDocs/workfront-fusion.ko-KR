---
title: 알림 옵션 설정
description: 이메일 알림 옵션은 팀 수준에서 설정됩니다.
author: Becky
feature: Workfront Fusion
exl-id: 570a09fc-01a9-4952-8a2b-8bfdd86d0bd8
TQID: https://experienceleague.adobe.com/-HytP4gfrhiiSn-dg5ndg1YC6NTMC-NURYzSFgO5kIo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 90a58033e240271b88d01b9daef9763f38264056
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 13%

---

# 알림 옵션 설정

조직에서 Adobe 통합 쉘을 사용하는 경우 Adobe 알림 영역을 통해 알림을 받습니다.

조직이 Adobe 통합 쉘로 마이그레이션되지 않은 경우 팀이 받는 알림을 선택할 수 있습니다. 알림은 팀 수준에서 설정됩니다.

알림을 보낼 상황을 제어할 수 있습니다.

* 경고 시 알림: 시나리오 실행에서 경고가 기록되면 Fusion에서 알림을 보냅니다.
* 오류 시 알림: 시나리오 실행이 실패하면 Fusion에서 알림을 보냅니다.
* 시나리오가 비활성화될 때 알림: 너무 많은 연속 오류가 발생한 후와 같이 시나리오가 자동 비활성화될 때 Fusion에서 알림을 보냅니다.

팀 또는 시나리오 수준에서 알림을 설정할 수 있습니다. 시나리오 수준 알림은 팀 수준에서 설정된 알림을 재정의합니다. 즉, 시나리오 설정과 팀 설정이 직접 충돌하는 경우 시나리오 설정을 따릅니다. 팀 알림 설정은 해당 설정에 대한 재정의 여부를 표시합니다.

기본적으로 모든 알림 유형은 Workfront Fusion에서 활성화됩니다.

>[!IMPORTANT]
>
>Workfront Fusion에서 알림을 받으려면 Adobe CX 엔터프라이즈 알림 설정에 Fusion 알림이 활성화되어 있어야 합니다. 화면 오른쪽 상단에 있는 알림 벨을 클릭하고 설정 아이콘을 클릭하여 이러한 설정에 액세스할 수 있습니다.

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
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">역할</td> 
   <td> 
     <p>알림 설정을 조정할 Fusion 조직 및 팀의 멤버여야 합니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 팀 수준 알림 설정 보기 및 관리

1. Workfront Fusion의 왼쪽 탐색에서 **팀 개요**&#x200B;를 클릭합니다.
1. **알림 옵션** 탭을 클릭합니다.

   알림 옵션 목록이 열립니다. 재정의가 있는 경우 해당 설정 옆에 재정의 수가 나타납니다.

1. (조건부) 재정의가 있는 경우 팀 알림 설정을 재정의하는 시나리오를 보려면 해당 설정에 대한 점 3개 메뉴를 클릭합니다.

   이 메뉴에서 시나리오를 클릭하여 해당 시나리오로 직접 이동할 수 있습니다.

   ![시나리오 메뉴 재정의](assets/view-notification-override.png)

1. 알림 유형에 대한 기본 설정을 복원하려면 이 문서에서 [알림 기본값 복원](#restore-notification-defaults)을 참조하십시오.

알림 옵션 목록에 대한 변경 사항은 자동으로 저장됩니다.

## 시나리오 수준 알림 설정

개별 시나리오에 대한 알림 설정은 해당 시나리오의 시나리오 설정 패널에서 설정됩니다.

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 필터를 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 시나리오 하단의 [!UICONTROL 시나리오 설정] 아이콘 ![시나리오 설정 아이콘](assets/scenario-settings-icon.png)을 클릭합니다.
1. 시나리오 설정 패널에서 패널 하단의 **고급 설정 표시**&#x200B;를 클릭합니다.
1. 필요에 따라 **경고 시 알림**, **오류 시 알림** 및 **시나리오가 비활성화될 때 알림** 설정을 조정합니다.
1. 시나리오 설정을 저장하고 종료하려면 **확인**&#x200B;을 클릭하십시오.

## 알림 기본값 복원

알림 옵션 탭에서 팀 알림 설정을 기본값으로 복원할 수 있습니다. 이 옵션은 통지 옵션을 사용으로 설정하고 해당 통지 유형에 대한 시나리오 통지 대체를 제거합니다.

알림 유형이 현재 기본값으로 설정되어 있으면 **기본값으로 복원** 아이콘이 표시되지 않습니다.

1. Workfront Fusion의 왼쪽 탐색에서 **팀 개요**&#x200B;를 클릭합니다.
1. **알림 옵션** 탭을 클릭합니다.

   알림 옵션 목록이 열립니다. 알림 유형이 현재 기본값으로 설정되어 있지 않으면, 해당 알림 유형에 대해 기본값으로 복원 아이콘이 표시됩니다.

   ![기본 보기로 복원](assets/restore-notification-defaults.png)

1. 시나리오 재정의를 포함하여 해당 알림 유형에 대한 기본 설정을 복원하려면 해당 알림 유형에 대해 **기본값으로 재설정** 아이콘 ![기본값으로 재설정](assets/restore-default-icon.png)을 클릭하십시오.

알림 옵션 목록에 대한 변경 사항은 자동으로 저장됩니다.

<!--

## Set notification options

If your organization is not on the Adobe Unified Shell, you can set notification settings directly in Fusion.

Email notification options are set on the team level.

1. In the left navigation panel, click **[!UICONTROL Team]**
1. Select the **[!UICONTROL Notification Options]** tab.
1. Enable the notifications that you want the team to receive.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">'[!UICONTROL Warning in scenario run]'</td> 
      <td> <p>Receive an email when there is a warning in a scenario run</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Errors in scenario run]</td> 
      <td>Receive an email when there is an error in a scenario run.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Scenario deactivation]</p> </td> 
      <td><p>Receive an email when a scenario deactivates.</p><p>In some cases, a scenario might be deactivated by the Workfront Fusion engineering team because the scenario is causing performance or other issues. In these cases, you do not receive notifications in Workfront Fusion. </p></td>

</tr>
</tbody>
</table>

Changes to notification options save automatically.

-->
