---
title: Microsoft Teams 모듈
description: Adobe Workfront Fusion 시나리오에서는 팀을 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 서드파티 애플리케이션 및 서비스에 연결할 수도 있습니다.
author: Becky
feature: Workfront Fusion
source-git-commit: f5b49cca308fad01167aed27e4716a3d630cb026
workflow-type: tm+mt
source-wordcount: '3642'
ht-degree: 2%

---

# Microsoft Teams 모듈

<!-- ADD REDIRECTS -->

Adobe Workfront Fusion 시나리오에서는 Microsoft Teams을 사용하는 워크플로를 자동화할 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

Microsoft Teams 모듈을 사용하려면 모듈에서 작업을 수행할 수 있는 Microsoft Teams 계정이 있어야 합니다.

## Workfront Fusion에 Microsoft Teams 서비스 연결

Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 [Adobe Workfront Fusion 연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.

## Microsoft Teams 모듈 및 해당 필드

Microsoft Teams 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Microsoft Teams 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [팀](#team)
* [채널](#channel)
* [메시지](#message)
* [멤버](#member)
* [온라인 모임](#online-meeting)
* [기타](#other)

### 팀

* [그룹에서 팀 만들기](#create-a-team-from-a-group)
* [Office 365 그룹 만들기](#create-an-office-365-group)
* [팀 또는 그룹 삭제](#delete-a-team-or-group)
* [팀 받기](#get-a-team)
* [모든 팀 및 그룹 나열](#list-all-teams-and-groups)
* [가입한 팀 목록](#list-joined-teams)
* [팀 업데이트](#update-a-team)
* [팀 보기](#watch-teams)

#### 그룹에서 팀 만들기

이 작업 모듈은 기존 Microsoft Office 365 그룹에서 팀을 만들고 새 팀에 대한 설정을 구성합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 ID</td> 
   <td> <p>팀을 만들 그룹을 선택합니다.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">멤버가 채널을 만들고 업데이트할 수 있도록 허용</td> 
   <td>멤버가 채널을 만들고 업데이트할 수 있도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">멤버가 채널을 삭제하도록 허용</td> 
   <td>멤버가 채널을 삭제할 수 있도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">구성원이 앱을 추가하거나 제거하도록 허용</td> 
   <td>구성원이 앱을 추가하거나 제거할 수 있도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">구성원이 탭을 만들고, 업데이트하고, 제거하도록 허용</td> 
   <td>구성원이 탭을 만들고, 업데이트하고, 제거할 수 있도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">멤버가 커넥터를 만들고 제거하도록 허용</td> 
   <td>멤버가 커넥터를 만들고 제거할 수 있도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자가 메시지를 편집할 수 있도록 허용</td> 
   <td>사용자의 메시지 편집을 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자가 메시지를 삭제하도록 허용</td> 
   <td>사용자의 메시지 삭제를 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">소유자가 메시지를 삭제하도록 허용</td> 
   <td>소유자의 메시지 삭제를 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">@team 언급 허용</td> 
   <td>@team 언급을 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">@channel 언급 허용</td> 
   <td>@channel 언급을 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Giphy 허용</td> 
   <td>이 팀에 Giphy 사용을 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스티커 및 밈 허용</td> 
   <td>사용자가 스티커 및 밈을 포함하도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자 지정 밈 허용</td> 
   <td>사용자가 사용자 지정 밈을 포함할 수 있도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">게스트가 채널을 만들고 업데이트할 수 있도록 허용</td> 
   <td>게스트가 채널을 만들고 업데이트하는 것을 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">게스트가 채널을 삭제하도록 허용</td> 
   <td>게스트가 채널을 삭제하는 것을 허용할지 여부를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### Office 365 그룹 만들기

이 작업 모듈은 Microsoft Office 365에 그룹을 만듭니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">표시 이름</td> 
   <td> <p>이 그룹이 주소록에 표시하는 이름을 입력하거나 매핑합니다.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">그룹의 별칭</td> 
   <td>이 그룹의 전자 메일 별칭을 입력하거나 매핑합니다. 소문자, 숫자 및 밑줄을 포함할 수 있습니다. Office 365 그룹 유형의 경우 그룹의 전자 메일 별칭([Alias]@[Your Domain].onmicrosoft.com)입니다. 보안 그룹 유형의 경우 별칭은 별명으로 작동합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 유형</td> 
   <td>Office 365 그룹을 만들지 보안 그룹을 만들지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">설명</td> 
   <td>이 그룹에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">보안 활성화됨</td> 
   <td>그룹의 보안을 활성화하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">소유자</td> 
   <td>이 그룹의 소유자를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">멤버</td> 
   <td>이 그룹의 구성원을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 팀 또는 그룹 삭제

이 작업 모듈은 지정된 팀 또는 그룹을 삭제합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 ID</td> 
   <td> <p>삭제하려는 그룹의 ID를 입력하거나 매핑합니다.</p> 
   </tr> 
 </tbody> 
</table>

#### 팀 받기

이 모듈은 지정된 Microsoft 팀 또는 Office 365 그룹에 대한 속성 및 관계를 검색합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 ID</td> 
   <td> <p>세부 정보를 검색할 그룹의 ID를 입력하거나 매핑합니다.</p> 
   </tr> 
 </tbody> 
</table>

#### 모든 팀 및 그룹 나열

이 모듈에는 조직과 연결된 Microsoft Teams 및 Office 365 그룹의 모든 팀이 나열됩니다. 지정한 기준을 충족하는 결과만 반환하도록 필터링할 수 있습니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">필터</td> 
   <td> <p>선택한 기준을 충족하는 팀 및 그룹만 반환하도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터를 평가할 필드, 연산자 및 필터를 허용할 값을 입력합니다. AND 또는 OR 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> </td> 
   </tr> 
  <tr> 
   <td>반환된 최대 결과 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 팀 또는 그룹 수를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>


#### 가입한 팀 목록

이 작업 모듈에는 이 모듈에 사용된 연결과 연결된 사용자가 가입한 팀이 나열됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>반환된 최대 결과 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 팀 또는 그룹 수를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 팀 업데이트

이 작업 모듈은 Microsoft Teams 또는 Office 365 그룹에서 지정된 팀의 속성을 업데이트합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">표시 이름</td> 
   <td> <p>이 그룹이 주소록에 표시하는 이름을 입력하거나 매핑합니다.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">그룹의 별칭</td> 
   <td>이 그룹의 전자 메일 별칭을 입력하거나 매핑합니다. 소문자, 숫자 및 밑줄을 포함할 수 있습니다. Office 365 그룹 유형의 경우 그룹의 전자 메일 별칭([Alias]@[Your Domain].onmicrosoft.com)입니다. 보안 그룹 유형의 경우 별칭은 별명으로 작동합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">설명</td> 
   <td>이 그룹에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">보안 활성화됨</td> 
   <td>그룹의 보안을 활성화하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">가시성</td> 
   <td>Office 365 그룹의 가시성을 지정하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### 팀 보기

이 트리거 모듈은 팀이 만들어질 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">필터</td> 
   <td> <p>선택한 기준을 충족하는 팀 및 그룹만 보도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터를 평가할 필드, 연산자 및 필터를 허용할 값을 입력합니다. AND 또는 OR 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> </td> 
   </tr> 
  <tr> 
   <td>반환된 최대 결과 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 팀 또는 그룹 수를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 채널

* [채널 만들기](#create-a-channel)
* [채널 삭제](#delete-a-channel)
* [채널 받기](#get-a-channel)
* [채널 나열](#list-channels)
* [채널 업데이트](#update-a-channel)

#### 채널 만들기

이 작업 모듈은 지정된 팀에 대한 새 채널을 만듭니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>Microsoft Teams에서 채널을 만들려는 팀을 선택합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 이름</td> 
   <td>새 채널의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>설명</td> 
   <td>새 채널에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 채널 삭제

이 작업 모듈은 Microsoft 팀에서 지정된 채널을 삭제합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>채널을 삭제하려는 Microsoft Teams의 팀 ID를 입력하거나 매핑합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 ID</td> 
   <td>삭제하려는 채널의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  </tbody> 
</table>

#### 채널 받기

이 모듈은 채널의 속성 및 관계를 검색합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>세부 정보를 검색할 채널을 소유한 Microsoft Teams의 팀 ID를 입력하거나 매핑합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 ID</td> 
   <td>세부 정보를 검색할 채널의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  </tbody> 
</table>

#### 채널 나열

이 모듈에는 Microsoft Teams의 지정된 팀이 소유한 채널이 나열됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>Microsoft Teams에서 채널을 나열할 팀을 선택합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>반환된 최대 결과 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 채널 수를 설정합니다.</td> 
  </tr> 
  </tbody> 
</table>

#### 채널 업데이트

이 작업 모듈은 지정된 채널의 설명을 업데이트합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>업데이트할 채널을 소유한 Microsoft Teams의 팀을 선택합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 이름</td> 
   <td>업데이트할 채널의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>설명</td> 
   <td>채널에 대한 새 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 메시지

* [채널 메시지에 회신](#reply-to-a-channel-message)
* [메시지 보내기](#send-a-message)
* [메시지 보기](#watch-messages)
* [새 답변 보기](#watch-new-replies)

#### 채널 메시지에 회신

이 작업 모듈은 지정된 채널에 있는 메시지에 대한 회신을 만듭니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>회신하려는 메시지가 포함된 채널을 소유한 Microsoft Teams의 팀을 선택합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 ID</td> 
   <td>회신하려는 메시지가 포함된 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>메시지 ID</td> 
   <td>회신할 메시지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>컨텐츠 유형</td> 
   <td>메시지를 일반 텍스트로 보낼지 HTML 형식으로 보낼지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>회신 메시지</td> 
   <td>전송하려는 회신 메시지의 본문을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 메시지 보내기

이 작업 모듈은 팀의 채널 또는 채팅에 메시지를 보냅니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">메시지 유형/td&gt; 
   <td> <p>채널 메시지를 보낼지 채팅 메시지를 보낼지 선택합니다.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>채널에 메시지를 보내는 경우 메시지를 보낼 채널을 소유한 Microsoft Teams의 팀 ID를 입력하거나 매핑합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 ID</td> 
   <td>채널에 메시지를 보내는 경우 메시지를 보낼 채널의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>새 채팅 만들기</td> 
   <td>채팅 메시지를 보내는 경우 새 채팅을 만들지 여부를 선택합니다.
   <ul><li><b>예</b><p>일대일 채팅을 원하는지 그룹 채팅을 원하는지 선택하고 채팅에 포함할 구성원을 선택합니다. 이 모듈에서 사용하는 연결과 연결된 사용자를 선택해야 하며, 일대일 채팅에는 해당 사용자와 다른 사용자 한 명만 포함되어야 합니다.</p><p>그룹 채팅을 만드는 경우 주제 필드에서 주제를 설정할 수 있습니다.</p>
   <li><b>아니요</b><p>메시지를 보낼 채널을 소유한 팀의 ID를 입력하거나 매핑한 다음 채널의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>메시지</td> 
   <td>보낼 메시지의 본문을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>컨텐츠 유형</td> 
   <td>메시지를 일반 텍스트로 보낼지 HTML 형식으로 보낼지 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 메시지 보기

이 트리거 모듈은 메시지가 팀의 채널 또는 채팅으로 전송될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">조사할 메시지 유형</td> 
   <td> <p>채널 메시지를 볼지 채팅 메시지를 볼지 선택합니다.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>채널 메시지를 보고 있는 경우 메시지를 볼 채널을 소유한 Microsoft Teams의 팀을 선택합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 ID</td> 
   <td>채널 메시지를 보는 경우 메시지를 볼 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>채팅 ID</td> 
   <td>채팅 메시지를 보고 있는 경우 메시지를 확인할 채팅을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>반환되는 최대 메시지 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 메시지 수를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 새 답변 보기

이 트리거 모듈은 지정된 메시지에 의해 새 회신이 수신되면 시나리오를 시작합니다.

개인 계정에는 이 모듈을 사용할 수 없습니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> <p>회신을 감시하는 채널을 소유한 Microsoft Teams의 팀을 선택합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>채널 ID</td> 
   <td>답글을 감시할 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>메시지 ID</td> 
   <td>답글을 확인할 채팅을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>반환되는 최대 회신 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 답글 수를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 멤버

* [구성원 추가](#add-a-member)
* [그룹에 구성원 추가](#add-a-member-to-a-group)

#### 구성원 추가

이 작업 모듈은 Microsoft Teams에 구성원을 추가합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">멤버 이름</td> 
   <td> <p>Microsoft Teams에 추가할 멤버의 이름을 입력하거나 매핑합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>암호</td> 
   <td>멤버의 암호를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 그룹에 구성원 추가

이 작업 모듈은 Office 365 그룹에 구성원을 추가합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">그룹 ID</td> 
   <td> <p>구성원을 추가할 그룹을 선택합니다.</p> </td> 
   </tr> 
  <tr> 
   <td>구성원 ID</td> 
   <td>그룹에 추가할 구성원을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 온라인 모임

* [온라인 모임 만들기](#create-an-online-meeting)
* [온라인 모임 삭제](#delete-an-online-meeting)
* [온라인 모임 가져오기](#get-an-online-meeting)
* [온라인 모임 업데이트](#update-an-online-meeting)

#### 온라인 모임 만들기

이 작업 모듈은 사용자 달력의 이벤트와 연결되지 않은 독립형 회의를 생성합니다. 이 모임은 사용자의 일정에 표시되지 않습니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">제목</td> 
   <td>이 모임의 제목을 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">시작 날짜 및 시간</td> 
   <td>회의를 시작할 날짜 및 시간을 입력하거나 매핑합니다. 지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">종료 날짜 및 시간</td> 
   <td>회의를 종료하려는 날짜 및 시간을 입력하거나 매핑합니다. 지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">허용된 발표자</td> 
   <td>이 모임에 참석할 수 있는 그룹을 선택하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">참석자</td> 
   <td>모임에 추가하려는 각 참석자에 대해 <b>항목 추가</b>를 클릭하고 참석자의 이름과 역할을 선택하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">참석자가 카메라를 활성화할 수 있도록 허용</td> 
   <td>참석자가 자신의 카메라를 사용하도록 허용할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">참석자가 마이크를 사용할 수 있도록 허용</td> 
   <td>참석자가 자신의 마이크를 사용하도록 허용할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">모임 채팅 허용</td> 
   <td>모임 채팅을 사용할 수 있도록 설정할지, 사용하지 않도록 설정할지, 모임 호출 기간으로 제한할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">팀 반응 허용</td> 
   <td>이 모임에 대해 팀 반응을 사용할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">스레드 ID</td> 
   <td>이 모임과 연결된 스레드의 ID를 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">메시지 ID</td> 
   <td>이 모임과 연결된 메시지의 ID를 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">응답 체인 메시지 ID</td> 
   <td>이 모임과 연결된 회신 체인의 ID를 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">시작 및 종료 알림</td> 
   <td>참석자가 입장할 때 또는 퇴장할 때 회의를 공지할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">범위</td> 
   <td>로비에서 대기하지 않아도 되는 참석자 그룹을 선택하십시오. 이 참석자는 직접 회의에 참석합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">전화 접속 사용자가 로비를 우회하도록 설정</td> 
   <td>전화 접속 사용자가 로비를 우회하도록 할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">자동으로 기록</td> 
   <td>모임을 자동으로 기록할지 여부를 선택합니다.</td> 
   </tr> 
   </tbody> 
</table>

#### 온라인 모임 삭제

이 작업 모듈은 지정된 ID의 온라인 모임을 삭제합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">모임 ID</td> 
   <td> <p>삭제할 모임의 ID를 입력하거나 매핑합니다.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### 온라인 모임 가져오기

이 작업 모듈은 지정된 ID를 사용하여 온라인 모임의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">모임 ID</td> 
   <td> <p>세부 정보를 검색할 모임의 ID를 입력하거나 매핑합니다.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### 온라인 모임 업데이트

이 작업 모듈은 지정된 ID로 온라인 모임을 업데이트합니다.



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">모임 ID</td> 
   <td>업데이트할 모임의 ID를 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">제목</td> 
   <td>이 모임의 제목을 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">시작 날짜 및 시간</td> 
   <td>회의를 시작할 날짜 및 시간을 입력하거나 매핑합니다. 지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">종료 날짜 및 시간</td> 
   <td>회의를 종료하려는 날짜 및 시간을 입력하거나 매핑합니다. 지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">허용된 발표자</td> 
   <td>이 모임에 참석할 수 있는 그룹을 선택하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">참석자</td> 
   <td>모임에 추가하려는 각 참석자에 대해 <b>항목 추가</b>를 클릭하고 참석자의 이름과 역할을 선택하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">참석자가 카메라를 활성화할 수 있도록 허용</td> 
   <td>참석자가 자신의 카메라를 사용하도록 허용할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">참석자가 마이크를 사용할 수 있도록 허용</td> 
   <td>참석자가 자신의 마이크를 사용하도록 허용할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">모임 채팅 허용</td> 
   <td>모임 채팅을 사용할 수 있도록 설정할지, 사용하지 않도록 설정할지, 모임 호출 기간으로 제한할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">팀 반응 허용</td> 
   <td>이 모임에 대해 팀 반응을 사용할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">스레드 ID</td> 
   <td>이 모임과 연결된 스레드의 ID를 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">메시지 ID</td> 
   <td>이 모임과 연결된 메시지의 ID를 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">응답 체인 메시지 ID</td> 
   <td>이 모임과 연결된 회신 체인의 ID를 입력하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">시작 및 종료 알림</td> 
   <td>참석자가 입장할 때 또는 퇴장할 때 회의를 공지할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">범위</td> 
   <td>로비에서 대기하지 않아도 되는 참석자 그룹을 선택하십시오. 이 참석자는 직접 회의에 참석합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">전화 접속 사용자가 로비를 우회하도록 설정</td> 
   <td>전화 접속 사용자가 로비를 우회하도록 할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">자동으로 기록</td> 
   <td>모임을 자동으로 기록할지 여부를 선택합니다.</td> 
   </tr> 
   </tbody> 
</table>

### 기타

* [사용자 유무 확인](#check-presence-of-users)
* [사용자 지정 API 호출 만들기](#make-a-custom-api-call)
* [사용자 검색](#search-users)

#### 사용자 유무 확인

이 작업 모듈은 선택한 사용자가 Microsoft Teams에 있는지 여부를 확인합니다.

이 모듈은 개인 계정을 지원하지 않습니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">사용자 ID</td> 
   <td> <p>현재 상태를 확인할 사용자를 선택합니다.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### 사용자 지정 API 호출 만들기

이 작업 모듈은 Microsoft Teams API에 대한 사용자 지정 요청을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://graph.microsoft.com</code>과(와) 관련된 경로를 입력하십시오. 예:<code> /v1.0/groups</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 검색

이 모듈은 지정한 기준을 사용하여 사용자를 검색합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Microsoft Teams 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">필터</td> 
   <td> <p>선택한 기준을 충족하는 사용자만 반환하도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터를 평가할 필드, 연산자 및 필터를 허용할 값을 입력합니다. AND 또는 OR 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> </td> 
   </tr> 
  <tr> 
   <td>반환된 최대 결과 수</td> 
   <td>한 실행 주기 동안 Workfront Fusion이 반환할 최대 팀 또는 그룹 수를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>



