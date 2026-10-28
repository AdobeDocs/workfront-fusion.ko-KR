---
title: 코드 조각으로 시나리오 섹션 저장 및 재사용
description: 코드 조각은 다른 시나리오에서 다시 사용할 수 있도록 저장하는 모듈 그룹입니다. 코드 조각을 구성, 공유, 가져오기 및 내보낼 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 5b049973107f23e46d1aadae8e0d157839e8a7f3
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 15%
---

# 코드 조각으로 시나리오 섹션 저장 및 재사용

>[!NOTE]
>
>이 기능은 새 시나리오 편집기 경험에서만 사용할 수 있습니다. 자세한 내용은 문서 시나리오 편집기에서 [새 경험 및 클래식 경험](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)을 참조하십시오.

코드 조각은 단위로 저장하는 모듈 그룹입니다. 다른 시나리오에 코드 조각을 추가할 수 있으므로 시나리오의 동일한 섹션을 두 번 이상 빌드할 필요가 없습니다.

[코드 조각] 패널을 사용하면 코드 조각을 검색, 태그 지정, 미리 보기, 고정 및 정렬하고, 시나리오에 끌어다 놓고, 가져와 내보내고, 팀 또는 조직과 공유하거나 다른 사용자에게 복사본을 보낼 수 있습니다.

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
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 코드 조각 만들기

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 저장할 모듈이 포함된 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. Shift 키를 누른 상태에서 코드 조각에 포함할 모듈을 클릭합니다.
1. 선택한 모듈 중 하나를 마우스 오른쪽 단추로 클릭한 다음 코드 조각 만들기를 선택합니다.
1. 코드 조각의 이름을 입력합니다.
1. **저장**&#x200B;을 클릭합니다

## 시나리오에 코드 조각 추가

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 코드 조각을 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 컨트롤 영역에서 **코드 조각** 아이콘 ![코드 조각](assets/snippets-icon.png)을 클릭합니다.

   코드 조각 아이콘을 보려면 컨트롤 영역에서 세 점 아이콘을 클릭해야 할 수 있습니다.

1. (선택 사항) 미리 볼 코드 조각을 선택합니다.
1. 코드 조각을 클릭하여 편집기에 추가합니다.
1. 스니펫을 시나리오에 연결합니다.
1. 스니펫이 추가된 시나리오와 함께 작동하도록 스니펫의 모든 필드를 업데이트합니다.

## 코드 조각 구성

[코드 조각] 패널에서 다음 작업을 수행할 수 있습니다.

* 코드 조각을 검색합니다.
* 자주 사용하는 코드 조각을 고정합니다.
* 코드 조각을 JSON 파일로 내보냅니다.
* 다른 조직, 팀 또는 사용자와 스니펫을 공유합니다.
* 시나리오에 추가하기 전에 코드 조각을 미리 봅니다.
* 코드 조각 목록을 정렬합니다.
  <!--* Add tags to a snippet, and use tags to find it later.-->

## 코드 조각 공유

팀 또는 조직과 코드 조각을 공유하거나 사본을 다른 사용자에게 직접 보낼 수 있습니다.

다음과 같은 작업을 수행할 수 있습니다.

* **팀 또는 조직과 공유**: 다른 구성원이 사용할 수 있도록 코드 조각을 공유합니다.
* **사용자에게 복사본 보내기**: 한 사용자에게 복사본을 보냅니다. 사용자는 자신의 복사본을 받습니다.


1. 컨트롤 영역에서 **코드 조각** 아이콘 ![코드 조각](assets/snippets-icon.png)을 클릭합니다.
1. 공유할 코드 조각 위로 마우스를 가져간 다음, 공유 아이콘이 나타나면 클릭합니다.
1. 다른 조직, 팀 또는 사용자와 코드 조각을 공유할지 여부를 선택합니다.
1. **다음**&#x200B;을 클릭합니다.
1. 코드 조각을 공유할 조직 또는 팀을 선택하거나 코드 조각을 공유할 사용자의 사용자 ID를 입력합니다.
1. **공유**&#x200B;를 클릭합니다.

사용자와 공유되는 코드 조각은 [코드 조각] 패널의 **나와 공유** 탭에 표시됩니다.

## 코드 조각 가져오기 및 내보내기

코드 조각을 JSON 파일로 내보내고 다른 시나리오나 환경으로 가져올 수 있습니다.

1. 컨트롤 영역에서 **코드 조각** 아이콘 ![코드 조각](assets/snippets-icon.png)을 클릭합니다.
1. 공유할 코드 조각 위로 마우스를 가져간 다음, 나타나면 내보내기 아이콘을 클릭합니다.
