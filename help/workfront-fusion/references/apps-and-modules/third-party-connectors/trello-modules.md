---
title: Trello 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Trello를 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: a0a53d5c5af0956635f5026bbf8f8ee681946d86
workflow-type: tm+mt
source-wordcount: '4320'
ht-degree: 0%

---

# [!UICONTROL Trello]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!UICONTROL Trello]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
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

## 전제 조건

[!DNL Trello] 모듈을 사용하려면 [!UICONTROL Trello] 계정이 있어야 합니다.

## Trello API 정보

Trello 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Trello]을(를) [!DNL Workfront Fusion]에 연결

[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 [연결 만들기 [!DNL Adobe Workfront Fusion] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하세요.

## [!UICONTROL Trello]개 모듈 및 해당 필드

[!UICONTROL Trello] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!UICONTROL Trello] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [보드](#boards)
* [목록](#lists)
* [카드](#cards)
* [멤버](#members)
* [체크리스트](#checklists)
* [레이블](#labels)
* [댓글](#comments)

### 보드

+++ **[!UICONTROL Archive or Unarchive a Board]**

이 작업 모듈은 지정한 보드를 닫거나(보관) 다시 열거나(보관 해제).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> 닫거나 다시 열 보드의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> 보드를 닫을지(보관) 또는 다시 열지(보관 해제) 여부를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

이 작업 모듈은 사용자가 지정하는 보드에 구성원을 지정합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> 구성원을 추가할 게시판을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email address]</td> 
   <td> <p> 보드에 추가할 구성원의 이메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Member type]</p> </td> 
   <td> <p>새 멤버를 지정할 멤버 유형을 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: 보드 관리자는 보드에서 모든 보드 작업을 수행할 수 있습니다.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: 일반 멤버는 단순히 보드의 멤버입니다.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: 관찰자는 보드에 대한 읽기 전용 액세스 권한을 가진 멤버입니다. <br>관찰자는 [!UICONTROL Trello Business Class]이(가) 있는 팀에서만 사용할 수 있습니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Full name]</td> 
   <td> <p> 보드에 추가할 사용자의 전체 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Board]**

이 작업 모듈은 선택한 설정으로 새 보드를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>새 게시판의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>필요한 경우 보드 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>조직의 ID를 입력하거나 매핑합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>게시판은 권한 수준별로 투표 및 주석 달기 규칙이 다릅니다. 예를 들어 게시판이 [!UICONTROL Private]이고 투표 및 주석 달기 규칙을 [!UICONTROL All](으)로 설정하면 오류가 발생합니다. </p> <p>투표 및 댓글은 각 권한 수준에 대해 다음 그룹으로 제한됩니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      구성원, 구성원 및 옵저버</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      회원, 회원 및 옵저버, 조직 회원</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      구성원, 구성원 및 관찰자, 조직 구성원, 모두</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>이 게시판에서 투표할 수 있는 사람을 지정하는 옵션을 선택하십시오. 권한 수준에 대한 투표 제한에 대해서는 [!UICONTROL Permission level] 필드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>이 보드의 카드에 주석을 달 수 있는 사용자를 지정하는 옵션을 선택합니다. 권한 수준에 대한 댓글 제한에 대해서는 [!UICONTROL Permission level] 필드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Invitations]</p> </td> 
   <td> <p>다른 사람을 이 게시판에 초대할 수 있는 사용자를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-join]</p> </td> 
   <td> <p>팀 구성원이 직접 보드에 가입할 수 있는지 또는 초대해야 하는지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default labels]</p> </td> 
   <td> <p>새 보드에 기본 레이블 집합을 사용할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default lists]</p> </td> 
   <td> <p>기본 목록 집합을 보드에 추가할지 여부를 선택합니다([!UICONTROL To Do], [!UICONTROL Doing], [!UICONTROL Done]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board source ID]</p> </td> 
   <td> <p>새 보드에 복사할 보드 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card Covers]</p> </td> 
   <td> <p>보드에 대한 카드 덮개를 사용하려면 <strong>[!UICONTROL Yes]</strong>을(를) 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Background]</p> </td> 
   <td> <p>배경색 또는 사용자 지정 배경을 선택합니다.</p> <p>참고: 사용자 지정 배경은 [!UICONTROL Trello Gold and Business Class] 구독자만 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> [!UICONTROL Background] 필드에서 사용자 지정 배경을 사용하도록 선택한 경우 사용할 배경의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>두 가지 카드 에이징 모드 중에서 선택합니다. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: 카드는 오래되면 오래된 해적 지도처럼 찢어지고, 노랗게 되고 갈라집니다.</li> 
     <li><strong>[!UICONTROL Regular mode ]</strong>: 카드는 노후화될수록 점점 더 투명해집니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Board]**

이 작업 모듈은 기존 보드의 설정을 편집합니다.

>[!SUCCESS]
>
><table style="table-layout:auto">
<col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>모듈에서 만들 보드의 고유한 [!UICONTROL Trello] ID를 입력하거나 매핑합니다. 보드 ID는 감시 보드 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p> 보드에 대한 새 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New description]</td> 
   <td> <p> 새 게시판 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>모듈에서 편집할 보드의 고유한 [!UICONTROL Trello] ID를 입력하거나 매핑합니다.  </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>옵션을 선택하여 이 모듈에서 사용하는 연결을 소유한 사용자가 보드에 가입되어 있는지 여부를 지정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>게시판은 권한 수준별로 투표 및 주석 달기 규칙이 다릅니다. 예를 들어 게시판이 [!UICONTROL Private]이고 투표 및 주석 달기 규칙을 [!UICONTROL All](으)로 설정하면 오류가 발생합니다. </p> <p>투표 및 댓글은 각 권한 수준에 대해 다음 그룹으로 제한됩니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      구성원, 구성원 및 옵저버</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      회원, 회원 및 옵저버, 조직 회원</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      구성원, 구성원 및 관찰자, 조직 구성원, 모두</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>이 게시판에서 투표할 수 있는 사람을 지정하는 옵션을 선택하십시오. 권한 수준에 대한 투표 제한에 대해서는 [!UICONTROL Permission level] 필드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>이 보드의 카드에 주석을 달 수 있는 사용자를 지정하는 옵션을 선택합니다. 권한 수준에 대한 댓글 제한에 대해서는 [!UICONTROL Permission level] 필드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Invitations] </td> 
   <td> <p>이 게시판에 사람들을 초대할 수 있는 사용자를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-join]</td> 
   <td> <p> 팀 구성원이 직접 보드에 가입할 수 있는지 또는 초대해야 하는지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card covers]</td> 
   <td> <p> 이 보드에 카드 덮개를 표시할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background] </td> 
   <td> <p>배경색 또는 사용자 지정 배경을 선택합니다.</p> <p>참고: 사용자 지정 배경은 [!UICONTROL Trello Gold and Business Class] 구독자만 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> [!UICONTROL Background] 필드에서 사용자 지정 배경을 사용하도록 선택한 경우 사용할 배경의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>두 가지 카드 에이징 모드 중에서 선택합니다. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: 카드는 오래되면 오래된 해적 지도처럼 찢어지고, 노랗게 되고 갈라집니다.</li> 
     <li><strong>[!UICONTROL Regular mode]</strong>: 카드는 노후화될수록 점점 더 투명해집니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar feed enabled]</td> 
   <td> <p> 캘린더 피드의 활성화 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Color> label name]</td> 
   <td> <p> 원하는 색상 레이블에 이름을 지정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>보드를 보관(닫기)할지 여부를 나타내는 옵션을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **[!UICONTROL Get a Board]**

이 작업 모듈은 보드의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>정보를 검색할 게시판의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

이 검색 모듈은 지정한 보드에 대한 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>정보를 보려는 게시판의 이름(또는 이름의 일부)을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned boards]</td> 
   <td> <p> 한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 보드 수를 입력하십시오. 이 값은 1000보다 작거나 같아야 합니다.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partial] </p> </td> 
   <td> <p>기본적으로 이 모듈은 멤버 콘텐츠에서 쿼리의 각 단어와 정확히 일치하는 항목을 검색합니다. [!UICONTROL Partial]이(가) 활성화되면 모듈은 쿼리의 모든 단어로 시작하는 콘텐츠를 찾습니다.</p> <p> 예를 들어 "development"라는 단어를 사용하여 "My Development Status Report"라는 이름의 보드를 찾는 경우 기본적으로 전체 단어를 검색해야 합니다. [!UICONTROL Partial]을(를) 활성화한 경우 "dev"는 검색할 수 있지만 "velopment"는 검색할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Boards] </td> 
   <td> <p>"mine"를 입력하거나, 쉼표로 구분된 보드 ID 목록을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

이 작업 모듈은 보드에서 멤버를 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> 사용자를 제거할 게시판의 ID를 입력(매핑 또는 선택)합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Member] </td> 
   <td> <p>보드에서 제거할 멤버를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Boards]**

이 트리거 모듈은 새 보드가 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 보드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 목록

+++ **[!UICONTROL Create a List]**

이 작업 모듈은 사용자가 지정하는 보드에 목록을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> 목록을 만들 게시판의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>새 목록의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>목록을 카드 맨 위에 추가할지 또는 맨 아래에 추가할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy list]</td> 
   <td> <p> 목록을 복사하는 경우 복사할 목록의 ID를 입력할 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>수동으로 입력</strong> </p> <p><strong>[!UICONTROL List ID]</strong> 필드에 복사할 목록의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>선택</strong> </p> <p>복사할 목록이 포함된 보드를 선택한 다음 목록을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a List]**

이 작업 모듈은 기존 목록을 편집합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td> <p> 업데이트할 목록의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>목록의 새 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> 목록을 이동할 보드를 매핑하거나 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>목록을 카드 맨 위에 추가할지 또는 맨 아래에 추가할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribed]</td> 
   <td> <p>현재 구성원을 목록에 가입시키려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a List]**

이 작업 모듈은 특정 목록에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL List ID]</p> </td> 
   <td> <p>정보를 검색할 목록의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards moved to a list]**

이 트리거 모듈은 카드가 특정 목록으로 이동될 때 활성화됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>카드를 확인할 목록이 포함된 보드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List]</td> 
   <td>카드 확인을 위해 조사할 목록을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 카드

+++ **[!UICONTROL Add an Attachment]**

이 작업 모듈은 선택한 카드에 첨부 파일을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> 첨부 파일을 추가할 카드의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>수동으로 입력</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 첨부 파일을 추가할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>첨부 파일을 추가할 카드가 들어 있는 보드를 선택한 다음 카드가 들어 있는 목록을 선택하고 카드를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment type]</p> </td> 
   <td> <p>파일을 직접 업로드할지 또는 파일에 URL을 제공할지 여부를 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File]</strong> </p> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>파일의 URL을 입력하고 첨부 파일의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Card]**

이 작업 모듈은 카드를 보관하거나 보드에 다시 전송합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card ID]</td> 
   <td> <p> 보관하거나 보드에 다시 보낼 카드의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> 카드를 닫을지(보관), 보드에 다시 보낼지(보관 해제) 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a card]**

이 작업 모듈은 선택한 목록에 카드를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a list ID]</td> 
   <td> <p> 카드를 추가할 목록의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL List ID]</strong> 필드에 카드를 추가할 목록의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>카드를 추가할 목록이 포함된 보드를 선택한 다음 목록을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>카드에 추가할 각 레이블에 대해 <b>항목 추가</b>를 클릭하고 레이블의 ID를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members]</td> 
   <td>카드에 추가하려는 각 구성원에 대해 <b>항목 추가</b>를 클릭하고 구성원의 ID를 입력하십시오. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>새 카드의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Description]</p> </td> 
   <td> <p>카드에 대한 설명을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>카드를 맨 위에 추가할지 또는 목록의 맨 아래에 추가할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> 카드의 기한을 입력하십시오. 지원되는 날짜 및 시간 형식 목록을 보려면 [!DNL Adobe Workfront Fusion]</a>의 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 변환을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> 이 옵션을 활성화하여 만기일에 카드를 완료로 표시하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td> <p>카드에 첨부 파일로 추가할 파일의 URL을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source file]</p> </td> 
   <td> <p>카드에 첨부 파일로 추가할 파일에 대한 정보를 입력하거나 매핑합니다. 이전 모듈에서 파일을 선택하거나 파일의 이름과 데이터를 매핑합니다</p> 
     <p>참고: 첨부 파일당 10MB의 파일 업로드 제한이 있습니다. 그러나 [!UICONTROL Business Class] 및 [!UICONTROL Trello Gold] 구성원의 첨부 파일당 파일 업로드 제한은 250MB입니다.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy card]</td> 
   <td> <p> 기존 카드의 사본으로 새 카드를 만드는 경우 복사할 카드의 ID를 입력할 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 복사할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>복사할 카드가 들어 있는 보드를 선택한 다음 카드가 들어 있는 목록을 선택하고 카드를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Card]**

이 작업 모듈은 기존 카드를 편집합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Card ID]</td> 
   <td> <p> 편집할 카드의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 편집할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>편집할 카드가 포함된 보드를 선택한 다음 카드가 포함된 목록을 선택하고 카드를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p>카드의 새 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New description]</p> </td> 
   <td> <p>카드에 대한 새 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Move a card]</p> </td> 
   <td> <p>보드 또는 보드를 선택하고 카드를 이동할 위치를 나열합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>카드에 추가할 각 레이블에 대해 <b>항목 추가</b>를 클릭하고 레이블의 ID를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>목록의 맨 위에 카드를 추가할지 또는 맨 아래에 카드를 [!UICONTROL append]할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> 카드의 기한을 입력하십시오. 지원되는 날짜 및 시간 형식 목록을 보려면 [!DNL Adobe Workfront Fusion]</a>의 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 변환을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> 이 옵션을 활성화하여 만기일에 카드를 완료로 표시하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members] </td> 
   <td> <p>카드에 추가하려는 각 구성원에 대해 <b>항목 추가</b>를 클릭하고 해당 구성원의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment cover ID]</p> </td> 
   <td> <p>카드를 표지로 사용할 이미지 첨부 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>카드를 구독할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>카드를 보관(닫기)할지 여부를 나타내는 옵션을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Card]**

이 작업 모듈은 선택한 카드의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p>세부 정보를 검색할 카드가 포함된 보드의 ID를 입력합니다. 이렇게 하면 보드의 사용자 정의 필드 이름을 볼 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> 세부 정보를 검색할 카드의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 세부 정보를 검색할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>세부 정보를 검색할 카드가 포함된 보드를 선택한 다음 카드가 포함된 목록을 선택하고 카드를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Cards]**

이 작업 모듈은 검색 쿼리와 일치하는 카드를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>검색할 보드를 선택합니다. 보드를 선택하지 않으면 모든 보드가 검색됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Query]</p> </td> 
   <td> <p>검색 쿼리를 입력합니다. 다음 검색 연산자를 사용하여 검색을 구체화할 수 있습니다.</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>연산자에 "-"를 추가하여 음수 검색을 수행할 수 있습니다(예: <code>[!UICONTROL -has:members]</code>: 할당된 구성원이 없는 카드를 검색하기 위해).</p> </li> 
     <li><code><strong>@name</strong></code> <p>멤버에 할당된 카드를 반환합니다. <code>member:</code>을(를) 사용할 수도 있습니다. <code>@me</code>을(를) 사용하여 카드만 포함하십시오.</p> </li> 
     <li><code><strong>#label</strong></code> <p>레이블이 지정된 카드를 반환합니다. <code>label:</code>을(를) 사용할 수도 있습니다. 예를 들어 <code>label:"FIX IT"</code>은(는) "FIX IT"이라는 레이블이 있는 카드를 반환합니다.</p> </li> 
     <li><code><strong>board:id</strong></code> <p>특정 보드 내에서 카드를 반환합니다. 예를 들어 <code>board:Trello</code>은(는) 보드 이름에 [!UICONTROL Trello]이(가) 있는 보드에 카드를 반환합니다.</p> </li> 
     <li><code><strong>list:name</strong></code> <p>이름이 "name"인 목록 내에서 카드를 반환합니다.</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>첨부 파일이 있는 카드를 반환합니다. <code>has</code>: 연산자는 <code>has:description</code>, <code>has:cover</code>, <code>has:members</code> 또는 <code>has:stickers</code>과(와) 같은 다른 특성에도 사용할 수 있습니다.</p> </li> 
     <li><code><strong>due:day</strong></code> <p>24시간 이내에 카드를 반환합니다. <code>due:</code> 연산자는 <code>due:week</code>, <code>due:month</code> 또는 <code>due:overdue</code>과(와) 같은 다른 기간에 사용할 수도 있습니다. 특정 날짜 범위를 검색할 수도 있습니다. 예를 들어 <code>due:14</code>을(를) 검색에 추가하면 향후 14일 이내에 만기가 도래하는 카드가 포함됩니다.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>지난 24시간 동안 만든 카드를 반환합니다. <code> created:</code> 연산자는 <code>created:week</code> 또는 <code>created:month</code>과(와) 같은 다른 일정에 사용할 수도 있습니다. 특정 날짜 범위를 검색할 수도 있습니다. 예를 들어 검색에 <code>created:14</code>을(를) 추가하면 지난 14일 동안 만들어진 카드가 포함됩니다.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>지난 24시간 동안 편집된 카드를 반환합니다. <code>edited:</code> 연산자는 <code>edited:week</code> 또는 <code>edited:month</code>과(와) 같은 다른 기간에 사용할 수도 있습니다. 특정 날짜 범위를 검색할 수도 있습니다. 예를 들어 <code>edited:21</code>을(를) 검색에 추가하면 지난 21일 동안 편집된 카드가 포함됩니다.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>카드 설명, 체크리스트, 주석 또는 이름의 텍스트와 일치하는 카드를 반환합니다. 예를 들어 <code>comment:"FIX IT"</code>은(는) 댓글에 "FIX IT"이 포함된 카드를 반환합니다.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>열려 있거나 보관된 카드를 반환합니다. 둘 다 지정하지 않으면 [!UICONTROL Trello]에서 두 형식을 모두 반환합니다.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>별표가 표시된 보드에만 카드가 포함됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned cards]</td> 
   <td> <p> 한 실행 주기 동안 [!DNL Workfront Fusion]에서 반환할 최대 카드 수를 입력하거나 매핑합니다. 이 값은 1000보다 작거나 같아야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>기본적으로 이 모듈은 멤버 콘텐츠에서 쿼리의 각 단어와 정확히 일치하는 항목을 검색합니다. [!UICONTROL Partial]이(가) 활성화되면 모듈은 쿼리의 모든 단어로 시작하는 콘텐츠를 찾습니다.</p> <p> 예를 들어 "development"라는 단어를 사용하여 "My Development Status Report"라는 이름의 보드를 찾는 경우 기본적으로 전체 단어를 검색해야 합니다. [!UICONTROL Partial]을(를) 활성화한 경우 "dev"는 검색할 수 있지만 "velopment"는 검색할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cards] </td> 
   <td> <p>특정 카드를 검색하려면 <b>항목 추가</b>를 클릭하고 카드 ID를 추가하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards]**

새 카드가 추가되면 이 트리거 모듈이 활성화됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>카드 위치를 선택하십시오.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards]</strong> </li> 
     <li> <p><strong>특정 보드에 있는 카드</strong> </p> <p>카드를 확인할 보드를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Cards on specific list]</strong> </p> <p>카드를 검사할 목록이 들어 있는 보드를 선택한 다음 목록을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>한 실행 주기 동안 최대 카드 수 [!DNL Workfront Fusion]이(가) 반환됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 멤버

+++ **[!UICONTROL Add a Member to a Card]**

이 작업 모듈은 지정된 멤버를 지정된 카드에 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter card ID and member ID]</p> </td> 
   <td> <p>카드 ID와 구성원 ID를 입력할 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 및 <strong>[!UICONTROL Member ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>구성원을 추가할 카드가 들어 있는 보드를 선택한 다음 카드, 카드 자체 및 카드에 추가할 구성원이 들어 있는 목록을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

[게시판](#boards) 아래의 &quot;[!UICONTROL Assign a Member to a Board]&quot;을(를) 참조하십시오.

+++

+++ **[!UICONTROL Search for Members]**

이 작업 모듈은 [!UICONTROL Trello]명의 구성원에 대한 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>찾으려는 사용자의 전체 이름 또는 사용자 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>기본적으로 이 모듈은 멤버 콘텐츠에서 쿼리의 각 단어와 정확히 일치하는 항목을 검색합니다. [!UICONTROL Partial]이(가) 활성화되면 모듈은 쿼리의 모든 단어로 시작하는 콘텐츠를 찾습니다.</p> <p> 예를 들어 "development"라는 단어를 사용하여 "My Development Status Report"라는 이름의 보드를 찾는 경우 기본적으로 전체 단어를 검색해야 합니다. [!UICONTROL Partial]을(를) 활성화한 경우 "dev"는 검색할 수 있지만 "velopment"는 검색할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned members]</td> 
   <td> <p> 한 실행 주기 동안 최대 구성원 수 [!DNL Workfront Fusion]이(가) 반환됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

[게시판](#boards) 아래의 &quot;[!UICONTROL Unassign a Member from a Board]&quot;을(를) 참조하십시오.

+++

### 체크리스트

+++ **[!UICONTROL Create a Checklist]**

이 작업 모듈은 선택한 카드에 체크리스트를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> 체크리스트를 추가할 카드의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 검사 목록을 추가할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>체크리스트를 추가할 카드가 들어 있는 보드를 선택한 다음, 카드가 들어 있는 목록을 선택한 다음 카드를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>체크리스트의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>검사 목록을 카드 맨 위에 추가할지 [!UICONTROL append the] 검사 목록을 카드 맨 아래에 추가할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter checklist ID]</p> </td> 
   <td> <p>새 체크리스트에 복사할 소스 체크리스트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Checklist Item]**

이 작업 모듈은 특정 체크리스트에 항목을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter checklist ID]</td> 
   <td> <p> 항목을 추가하려는 체크리스트의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Checklist ID]</strong> 필드에 검사 목록을 추가할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>체크리스트를 추가할 카드가 들어 있는 보드를 선택한 다음, 카드가 들어 있는 목록을 선택하고 카드를 선택한 다음 체크리스트를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>새 항목의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>항목을 검사 목록의 맨 위에 추가할지 [!UICONTROL append]의 맨 아래에 추가할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Checked]</p> </td> 
   <td> <p>항목을 이미 선택된 상태로 추가하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Checklist Item]**

이 작업 모듈은 기존 체크리스트를 편집합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Card ID and Checklist Item ID]</td> 
   <td> <p> 항목을 편집할 카드 ID 및 체크리스트를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Checklist ID]</strong> 필드에 검사 목록을 추가할 카드의 ID를 입력하거나 매핑합니다.</p> <p><strong>[!UICONTROL Checklist Item ID]</strong> 필드에 검사 목록의 ID를 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>체크리스트를 추가할 카드가 들어 있는 보드를 선택한 다음, 카드가 들어 있는 목록을 선택하고 카드를 선택한 다음 체크리스트를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklist ID]</td> 
   <td>체크리스트 항목을 이동할 체크리스트를 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>새 항목의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>항목을 체크리스트의 맨 위에 추가할지 또는 맨 아래에 추가할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL State]</p> </td> 
   <td> <p>체크리스트 항목의 완료 또는 미완료 여부를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 레이블

+++ **[!UICONTROL Add a Label to a Card]**

이 작업 모듈은 선택한 카드에 레이블을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> 체크리스트를 추가할 카드의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 검사 목록을 추가할 카드의 ID를 입력하거나 매핑합니다. <strong>[!UICONTROL Label ID]</strong> 필드에 추가할 레이블의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>체크리스트를 추가할 카드가 들어 있는 보드를 선택한 다음, 카드가 들어 있는 목록을 선택한 다음 카드를 선택합니다. </p> <p>카드에 추가할 레이블을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 댓글

+++ **[!UICONTROL Create a Comment in a Card]**

이 작업 모듈은 선택한 카드에 주석을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> 주석을 추가할 카드의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 댓글을 추가할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>주석을 추가할 카드가 들어 있는 보드를 선택한 다음 카드가 들어 있는 목록을 선택하고 카드를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment] </td> 
   <td> <p>선택한 카드에 추가할 설명을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Comments in a Card]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> 주석을 추가할 카드의 ID를 입력하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL Card ID]</strong> 필드에 댓글을 추가할 카드의 ID를 입력하거나 매핑합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>주석을 추가할 카드가 들어 있는 보드를 선택한 다음 카드가 들어 있는 목록을 선택하고 카드를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> 한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 댓글 수를 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since] </td> 
   <td> <p>댓글이 생성된 기간의 시작 날짜를 설정합니다. 지원되는 날짜 및 시간 형식 목록을 보려면 [!DNL Adobe Workfront Fusion]</a>의 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 변환을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before] </td> 
   <td> <p>댓글이 생성된 기간의 종료 날짜를 설정합니다. 지원되는 날짜 및 시간 형식 목록을 보려면 [!DNL Adobe Workfront Fusion]</a>의 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 변환을 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Comments]**

지정된 위치에 새 주석이 있으면 주석 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Trello] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>댓글을 감시할 위치를 선택합니다.</p> 
    <ul> 
     <li>모든 곳에서 <strong>[!UICONTROL All cards]개</strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>댓글을 확인할 게시판을 선택합니다</p> </li> 
     <li> <p><strong>[!UICONTROL List]</strong> </p> <p>주석을 감시할 목록이 포함된 보드를 선택한 다음 목록을 선택합니다.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>댓글을 확인할 카드가 들어 있는 보드를 선택한 다음 카드가 들어 있는 목록을 선택한 다음 카드를 선택합니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>한 실행 주기 동안 최대 댓글 수 [!DNL Workfront Fusion]이(가) 반환됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL Trello] 개체 ID

* [ [!DNL Trello]에서 카드의 ID 또는 바로 가기 링크를 찾는 방법](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [ [!DNL Trello]에서 다른 개체의 ID를 찾는 방법](#how-to-find-ids-of-other-objects-in-trello)

### [!DNL Trello]에서 카드의 ID 또는 바로 가기 링크를 찾는 방법

카드를 편집하거나 새 주석을 만들려면 카드의 ID나 바로 가기 링크를 알고 있어야 합니다. [!UICONTROL New Card] 트리거의 출력에서 이 정보를 가져올 수 있습니다. 카드를 열고 [!UICONTROL Share] 단추를 클릭하면 카드에 대한 바로 가기 링크를 얻을 수도 있습니다. 바로 가기 링크는 URL 끝에 있는 [!UICONTROL Link to this card] 상자에서 `https://trello.com/c/` 다음에 찾을 수 있습니다.

![외 항목 공유](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### [!DNL Trello]에서 다른 개체의 ID를 찾는 방법

게시판, 목록 및 주석 ID는 트리거를 사용해서만 얻을 수 있습니다. [!DNL trello.com] 웹 사이트에 이러한 ID가 표시되지 않습니다.
