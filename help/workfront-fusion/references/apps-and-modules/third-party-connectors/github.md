---
title: GitHub 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 GitHub를 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: 899fc717f5107433d6f1aea31c4d079243a85822
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 0%

---

# [!DNL GitHub]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!UICONTROL GitHub]를 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

## 전제 조건

[!DNL GitHub] 모듈을 사용하려면 [!DNL GitHub] 계정이 있어야 합니다.

## [!DNL GitHub]을(를) [!DNL Workfront Fusion]에 연결

[!DNL GitHub] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion에 연결 만들기] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

## [!DNL GitHub]개 모듈 및 해당 필드.

[!DNL GitHub] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL GitHub] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)

### 트리거

* [[!UICONTROL 댓글 보기]](#watch-comments)
* [[!UICONTROL 분기점 보기]](#watch-forks)
* [[!UICONTROL 문제 보기]](#watch-issues)
* [[!UICONTROL 끌어오기 요청 보기]](#watch-pull-requests)
* [[!UICONTROL 저장소 보기]](#watch-repositories)

#### [!UICONTROL 댓글 보기]

이 트리거 모듈은 새 주석이 추가되거나 기존 주석이 수정되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>보려는 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문제 번호]</td> 
   <td>특정 문제에 대한 새로운 의견만 검색하여 검색을 제한하려면 문제 번호를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 문제 수]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환하는 최대 댓글 수를 설정하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>새 주석만 감시할지 또는 주석 및 모든 변경 사항을 감시할지 여부를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 분기점 보기]

이 트리거 모듈은 새 포크를 만들 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>포크를 검사할 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 포크 수]</td> 
    <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 포크 수를 입력하거나 매핑합니다.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문제 보기]

이 트리거 모듈은 새 문제가 추가되거나 기존 문제가 수정되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보고 싶습니다]</td> 
   <td>이 계정과 연결된 모든 저장소를 감시할지 하나의 저장소만 감시할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>한 저장소에서만 문제를 확인하도록 선택한 경우 확인하려는 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 문제 수]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환하는 최대 문제 수를 설정하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>새 문제만 감시할지, 새 문제 및 모든 변경 사항을 감시할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>감시할 문제를 연결된 방법별로 필터링할 수 있습니다.</p> 
    <ul> 
     <li>[!UICONTROL 모든 문제]</li> 
     <li>[!UICONTROL만 나에게 할당된 문제]</li> 
     <li>[!UICONTROL 내가 만든 문제만 해당]</li> 
     <li>[!UICONTROL만 나를 언급하는 문제]</li> 
     <li>[!UICONTROL 다음에 대한 업데이트를 구독하는 문제만 발생]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상태]</td> 
   <td>진행 중인 문제만 볼 것인지 종료된 문제만 볼 것인지 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레이블]</td> 
   <td>추가할 각 태그에 대해 <b>항목 추가</b>를 클릭하고 태그를 입력하십시오. 모듈은 이러한 태그의 문제를 감시합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 끌어오기 요청 보기]

이 모듈은 새 끌어오기 요청이 추가되거나 기존 끌어오기 요청이 수정되면 트리거됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>보려는 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 풀 요청 수]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환하는 최대 가져오기 요청 수를 설정하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상태]</td> 
   <td>[!UICONTROL only open pull] 요청, [!UICONTROL only closed ones] 또는 모든 pull 요청을 시청할지 여부를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>새 끌어오기 요청만 감시할지, 새 끌어오기 요청 및 모든 변경 사항을 감시할지 여부를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 저장소 보기]

이 트리거 모듈은 저장소가 생성되거나 수정될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 저장소 수]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환하는 최대 저장소 수를 설정하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>새 저장소 및 모든 변경 사항을 감시할지 또는 새 저장소만 감시할지 여부를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 피할당자 추가]](#add-assignees)
* [[!UICONTROL 문제에 레이블 추가]](#add-labels-to-an-issue)
* [[!UICONTROL 댓글 만들기]](#create-a-comment)
* [[!UICONTROL 문제 만들기]](#create-an-issue)
* [[!UICONTROL 문제 가져오기]](#get-an-issue)
* [[!UICONTROL 댓글 나열]](#list-comments)
* [[!UICONTROL 문제에서 레이블 제거]](#remove-a-label-from-an-issue)
* [[!UICONTROL 피할당자 제거]](#remove-assignees)
* [[!UICONTROL 문제 검색]](#search-for-an-issue)
* [[!UICONTROL 문제 업데이트]](#update-an-issue)

#### [!UICONTROL 피할당자 추가]

이 모듈은 지정된 문제에 피할당자를 추가합니다

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>피할당자를 추가하려는 문제가 포함된 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 담당자]</td> 
   <td>문제에 할당할 사람을 선택합니다. 사용 가능한 할당자에는 저장소에 대한 쓰기 권한이 있는 모든 사용자와 저장소에 대한 읽기 권한이 있는 조직 구성원이 포함됩니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>피할당자를 추가하려는 문제의 문제 번호를 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문제에 레이블 추가]

이 모듈은 문제에 레이블을 추가합니다. 레이블은 저장소 수준에서 정의되며 저장소에 대한 쓰기 권한이 있는 사용자만 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>레이블을 추가할 문제가 포함된 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레이블]</td> 
   <td>문제에 추가할 레이블을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>레이블을 추가할 문제의 문제 번호를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 만들기]

이 모듈은 지정된 문제에 대한 주석을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>댓글을 작성하려는 문제가 포함된 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>댓글을 작성하려는 문제의 문제 번호를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>주석의 내용을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문제 만들기]

이 모듈은 선택한 저장소에 새 문제를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>문제를 만들려는 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 담당자]</td> 
   <td>문제에 할당할 사람을 선택합니다. 사용 가능한 할당자에는 저장소에 대한 쓰기 권한이 있는 모든 사용자와 저장소에 대한 읽기 권한이 있는 조직 구성원이 포함됩니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이정표]</td> 
   <td>새 문제와 연결할 이정표를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레이블]</td> 
   <td>새 문제에 적용할 레이블을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>새 문제의 제목을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>설명 또는 추가 정보 등 문제의 본문을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문제 가져오기]

이 모듈은 지정된 문제에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>세부 정보를 가져올 문제가 포함된 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>세부 정보를 검색할 문제의 문제 번호를 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 나열]

이 모듈에는 지정된 문제에 대한 모든 주석이 나열됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>의견을 나열할 문제가 포함된 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>주석을 나열할 문제의 문제 번호를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>모듈은 이 날짜 이후에 작성된 주석을 반환합니다. 지원되는 날짜 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">형식 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 주석 수]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환하는 최대 댓글 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문제에서 레이블 제거]

이 모듈은 문제에서 단일 레이블을 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>레이블을 제거할 문제가 포함된 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레이블]</td> 
   <td>문제에서 제거할 레이블을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>레이블을 제거할 문제의 문제 번호를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 피할당자 제거]

이 모듈은 지정된 문제에서 피할당자를 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>피할당자를 제거하려는 문제가 포함된 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 담당자]</td> 
   <td>문제에서 제거할 사람을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>피할당자를 제거할 문제의 문제 번호를 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문제 검색]

이 모듈은 검색 기준과 일치하는 문제를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 문제 수]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환하는 최대 문제 수를 설정하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 정렬 기준]</td> 
   <td> <p>검색 결과를 정렬할 방법을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 최적 일치] </p> </li> 
     <li>[!UICONTROL 만든 날짜]</li> 
     <li>[!UICONTROL 날짜 업데이트됨]</li> 
     <li>[!UICONTROL 댓글 수]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 정렬 방향]</td> 
   <td> <p>오름차순 또는 내림차순을 선택합니다. </p> <p>날짜의 경우 <strong>[!UICONTROL 내림차순]</strong>을(를) 선택하면 가장 최근 날짜가 먼저 반환됩니다. </p> <p>[!UICONTROL number of comments]에 대해 <strong>[!UICONTROL descending]</strong>을(를) 선택하면 댓글 수가 가장 많은 문제가 먼저 반환됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>검색 쿼리를 입력하거나 매핑합니다. 검색 옵션에 대한 자세한 설명은 <a href="https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests"> 도움말 사이트에서 </a>문제 및 가져오기 요청 검색[!DNL GitHub]을 참조하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문제 업데이트]

이 모듈은 기존 [!DNL GitHub] 문제를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL GitHub] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 저장소]</td> 
   <td>문제를 업데이트할 저장소를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 담당자]</td> 
   <td>문제에 할당할 사람을 선택합니다. 사용 가능한 할당자에는 저장소에 대한 쓰기 권한이 있는 모든 사용자와 저장소에 대한 읽기 권한이 있는 조직 구성원이 포함됩니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이정표]</td> 
   <td>문제와 연결할 이정표를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레이블]</td> 
   <td>문제에 적용할 레이블을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>업데이트하려는 문제의 문제 번호를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상태]</td> 
   <td>문제를 업데이트할 상태를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>문제에 대한 새 제목을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>문제에 대한 설명 또는 추가 정보 등의 새 본문을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>
