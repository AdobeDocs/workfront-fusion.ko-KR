---
title: 팀 역할 보기 및 관리
description: 각 팀에는 팀의 역할을 보고, 고유한 역할을 만들고, 각 역할에 포함되는 권한을 선택하고, 역할을 업데이트 또는 삭제할 수 있는 역할 탭이 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: a3a6922afd713cd002cdf472c7ef62c1855b80d9
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 9%
---
# 팀 역할 보기 및 관리

팀에서 사용 가능한 역할을 보고, 고유한 역할을 만들고, 각 역할에 포함되는 권한을 선택할 수 있습니다. 역할을 업데이트하고 삭제할 수도 있습니다.

사용자 정의 역할은 다음과 같은 이점을 제공합니다.

* 각 팀 구성원은 작업에 필요한 액세스 권한만 보유하므로 중요한 시나리오에 실수로 변경되는 것의 위험이 줄어듭니다.
* 사용자 정의 역할은 팀을 사전 정의된 역할에 맞추는 대신 조직의 작동 방식과 더 잘 일치시킬 수 있습니다.
* 지원 센터에 문의하지 않고도 직접 액세스를 관리할 수 있습니다.

조직, 팀 및 사전 정의된 팀 역할에 대한 개요는 [조직 및 팀 개요](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/org-and-team-overview.md)를 참조하십시오. 미리 정의된 역할에 포함된 권한은 [조직 및 팀 역할](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md)을 참조하세요.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성</td> 
   <td> 
     <p>팀에 <b>[!UICONTROL 구성원 관리]</b> 권한이 있어야 합니다. 사전 정의된 역할에서 이 권한은 팀 관리자 및 조직 소유자 역할에 포함됩니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 팀 역할을 관리할 수 있는 사람

팀에서 **[!UICONTROL 구성원 관리]** 권한이 있는 모든 사용자는 해당 팀의 역할을 만들고, 업데이트하고, 삭제하고, 사용자를 할당할 수 있습니다.

* 조직 소유자는 모든 팀에서 역할을 만들고 관리할 수 있습니다.
* 조직 관리자는 자신이 구성원으로 있는 팀과 **[!UICONTROL 구성원 관리]** 권한이 있는 팀에서만 역할을 관리할 수 있습니다.
* 팀 관리자는 자신의 팀에서 역할을 관리할 수 있습니다.

## 역할 만들기 또는 편집

1. Fusion의 왼쪽 탐색에서 **팀 개요**&#x200B;를 클릭합니다.
1. (조건부) 역할을 보려는 팀의 페이지에 없으면 페이지 상단 근처에 있는 **팀** 드롭다운을 클릭하고 올바른 팀을 선택하십시오.
1. **[!UICONTROL 역할]** 탭을 엽니다.

   탭에는 미리 정의된 역할을 포함하여 팀에서 사용할 수 있는 역할이 나열됩니다. 각 역할에 대해, 목록에 역할 이름과 &quot;권한 없음&quot;, &quot;멤버&quot; 또는 &quot;사용자 지정 · 19 권한&quot;과 같은 권한 요약이 표시됩니다.

1. 역할을 만들려면 **[!UICONTROL 역할 만들기]**&#x200B;를 클릭하세요.

   또는

   역할을 편집하려면 편집할 역할의 행에서 **[!UICONTROL 편집]**&#x200B;을 클릭하세요.

   <!-- BECKY CHECK ME: The Edit button is available for the predefined roles as well as custom roles. Confirm the title of the edit page, whether you can rename the predefined roles, and what happens to users who already have the role. -->

1. **[!UICONTROL 역할 이름]** 필드에 역할 이름을 입력하십시오.
1. **[!UICONTROL 역할 템플릿]** 드롭다운에서 시작할 템플릿을 선택합니다.

   템플릿은 역할에 대한 초기 권한을 설정합니다. 기본 템플릿은 **[!UICONTROL 뷰어]**&#x200B;입니다.

1. **[!UICONTROL 범위가 지정된 권한]** 영역에서 역할에 포함할 권한을 선택합니다.

   권한은 **[!UICONTROL 자동화]**, **[!UICONTROL 연결]**, **[!UICONTROL 팀]** 등 영역별로 그룹화됩니다. 각 영역에 대해 다음 중 하나를 수행할 수 있습니다.

   * 한 영역에 있는 모든 권한을 한 번에 설정하려면 영역 이름 옆에 있는 **[!UICONTROL 액세스 권한 없음]**, **[!UICONTROL 선택한 항목만 보기]** 또는 **[!UICONTROL 전체 액세스]**&#x200B;를 클릭합니다.
   * 특정 권한을 선택하려면 각 권한에 대한 확인란을 선택하거나 선택을 취소합니다.

   권한 목록은 이 문서에서 [역할에 포함할 수 있는 권한](#permissions-that-you-can-include-in-a-role)을 참조하십시오.

   <!-- BECKY CHECK ME: Confirm the options in the Role template dropdown and what each one selects. Confirm exactly what No access, View only, and Full access select in each area (in the screenshot, View only selects the view permissions). Confirm whether there is a Description field, and whether there are areas below Team on the page (the screenshots end at Team). -->

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다. 저장하지 않고 페이지를 닫으려면 **[!UICONTROL 취소]**&#x200B;를 클릭하십시오.
1. (선택 사항) 역할을 삭제하려면 **[!UICONTROL 역할]** 탭의 역할 행에서 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.

   <!-- BECKY CHECK ME: Confirm why the Delete button is unavailable (dimmed) for some roles, such as Team Operator, Team Member, and Team Admin in the screenshot, whether there is a confirmation prompt, and what happens to users who have the role. Update this step and add a note, if needed. -->

생성하는 역할은 팀에서 사용할 수 있습니다. 팀 멤버에게 할당할 수 있습니다.

### 역할에 포함할 수 있는 권한

<table style="table-layout:auto">
 <col>
 <col>
 <thead>
  <tr>
   <th>영역</th>
   <th>권한</th>
  </tr>
 </thead>
 <tbody>
 <tr>
   <td role="rowheader">[!UICONTROL Automations]</td>
   <td>목록 보기, 세부 사항 보기, 실행 내역 보기, 알림 관리, 통계 재설정, 한 번 실행, 일정 편집, 활성화, 비활성화, 생성, 편집, 게시, 삭제</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL 미완료 실행]</td>
   <td>보기, 관리</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Webhooks]</td>
   <td>보기, 대기열 보기, 만들기, 편집, 대기열 관리, 우선순위 변경, 삭제</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL 연결]</td>
   <td>보기, 만들기, 편집, 삭제</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL 키]</td>
   <td>보기, 만들기, 편집, 삭제</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL 데이터 저장소]</td>
   <td>목록 보기, 레코드 찾아보기, 만들기, 편집, 삭제</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL 데이터 구조]</td>
   <td>보기, 만들기, 편집, 삭제</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Templates]</td>
   <td>목록 보기, 세부 정보 보기, 만들기, 편집, 삭제</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL 팀]</td>
   <td>팀 보기, 팀 설정 편집, 구성원 관리, 팀 삭제</td>
  </tr>
 </tbody>
</table>

<!-- BECKY CHECK ME: Confirm that this list is complete, and add a description of what each permission allows, if needed. The list is taken from the Create role page, which may have more areas below Team. -->

## 다른 팀에 역할 복제

한 팀의 역할을 다른 팀에 복사할 수 있으므로 각 팀에서 동일한 역할을 다시 만들 필요가 없습니다.

1. 이 문서의 [역할 만들기 또는 편집](#create-or-edit-a-role)에 설명된 대로 팀의 **[!UICONTROL 역할]** 탭을 엽니다.
1. **[!UICONTROL 팀에 복제]**&#x200B;를 클릭합니다.

   **[!UICONTROL 다른 팀에 역할 복제]** 페이지가 열립니다.

1. **[!UICONTROL Target 팀]** 드롭다운에서 역할을 복제할 팀을 선택합니다.

   현재 팀의 역할이 나열된 표가 나타납니다.

1. 테이블의 각 역할에 대해 다음을 검토하고 설정합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Source 역할]</td> 
      <td> <p>권한 요약과 함께 현재 팀의 역할입니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 액션]</td> 
      <td> <p>역할 작업 예를 들어 <b>[!UICONTROL을 기존 역할에 복사]</b>은(는) 원본 역할의 권한을 대상 팀에 이미 있는 역할에 복사합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Target]</td> 
      <td> <p>소스 역할이 복사된 대상 팀의 역할입니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Changes]</td> 
      <td> <p>대상 역할이 소스 역할과 다른지 여부. 예를 들어 <b>[!UICONTROL이 이미 동기화 중]</b>은(는) 대상 역할에 이미 원본 역할과 동일한 권한이 있음을 의미합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 사용자]</td> 
      <td> <p>역할을 가진 사용자에 대한 정보입니다. 예를 들어 <b>[!UICONTROL 일치하는 사용자 없음]</b>은(는) 포함할 사용자가 없음을 의미합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 상태]</td> 
      <td> <p>복제 후 역할에 대한 결과입니다.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. **[!UICONTROL 복제]**&#x200B;를 클릭합니다. 복제하지 않고 페이지를 닫으려면 **[!UICONTROL 취소]**&#x200B;를 클릭하십시오.

<!-- BECKY CHECK ME: The screenshot shows the Clone roles to another team page after a target team is selected. Confirm the options in the Action dropdown (for example, whether you can create a new role in the target team), the options in the Target dropdown, what the checkbox in the Users column does (for example, whether it also assigns the role to matching users in the target team) and what "matching users" means, what the Changes column shows when the roles differ, and what the Status column shows before and after you clone. -->

<!-- BECKY CHECK ME: Confirm whether the Target team dropdown lists all teams or only the teams that you can manage, and whether the Clone to team button is visible to everyone who can manage roles. -->

## 사용자에게 역할 할당

사전 정의된 역할을 할당하는 것과 동일한 방식으로 사용자 정의 역할을 할당합니다. 지침은 [팀에 사용자 추가](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) 및 [사용자 역할 보기 또는 편집](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md#view-or-edit-user-roles-for-a-team)을 참조하십시오.

<!-- BECKY CHECK ME: Confirm that custom roles appear in the role dropdowns in both of these procedures. -->

## 고려 사항

* 조직 권한이 계단식으로 표시됩니다. 누군가에게 모든 팀에서 작업을 수행할 수 있는 액세스 권한을 부여하려면 팀 역할을 만드는 대신 조직 역할을 할당하십시오. 자세한 내용은 [조직 및 팀 역할](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md)을 참조하세요.
* 만드는 역할은 한 팀에 속합니다.

<!-- BECKY CHECK ME: The Slack thread says that defining a role that is available in all teams was out of scope for the initial release. Confirm that a role belongs to a single team, and that you clone it to use it in another team. -->
