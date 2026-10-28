---
title: 시나리오에서 변수, 소스 및 연결 찾기 및 바꾸기
description: 찾기 및 바꾸기를 사용하여 매핑된 변수를 바꾸거나, 한 소스 모듈에서 다른 소스 모듈로 참조를 다시 매핑하거나, 시나리오에서 연결을 다른 모듈로 복사합니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 15%
---

# 시나리오에서 변수, 소스 및 연결 찾기 및 바꾸기

>[!NOTE]
>
>이 기능은 새 시나리오 편집기 경험에서만 사용할 수 있습니다. 자세한 내용은 문서 시나리오 편집기에서 [새 경험 및 클래식 경험](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)을 참조하십시오.

찾기 및 바꾸기 를 사용하면 한 번에 많은 모듈에서 동일한 내용을 변경할 수 있습니다. 다음과 같은 작업을 수행할 수 있습니다.

* 전체 시나리오 또는 하나의 모듈에서 매핑된 변수를 바꿉니다.
* 한 소스 모듈에서 다른 소스 모듈로 참조를 다시 매핑합니다.
* 동일한 앱에서 호환되는 모듈 하나 또는 모두에 연결을 복사합니다.

변경하기 전에 찾기 및 바꾸기는 영향을 받을 모듈의 미리보기를 표시합니다.

클래식 경험에서는 DevTool의 Swap 변수, Remap 소스 및 Swap 연결 도구를 사용하여 이러한 작업을 수행할 수 있습니다. 자세한 내용은 [시나리오 디버그](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md)를 참조하십시오.

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

## 찾기 및 바꾸기 열기

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 변경할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 컨트롤 영역에서 **찾기 및 바꾸기** 아이콘 ![찾기 및 바꾸기](assets/find-replace-icon.png)를 클릭합니다.

   찾기 및 바꾸기 아이콘을 보려면 컨트롤 영역에서 점 3개를 클릭해야 할 수도 있습니다.

캔버스 오른쪽의 패널에서 열기 찾기 및 바꾸기

## 변수 바꾸기

**변수** 탭을 사용하여 매핑된 변수를 바꾸십시오.

1. 찾기 및 바꾸기를 연 다음 **변수** 탭을 클릭합니다.
1. 찾을 변수 필드에 바꿀 변수에 을 붙여넣습니다.
1. 다음으로 바꾸기 필드에서 이전 변수를 바꿀 변수에 을 붙여 넣습니다.
1. 모듈 필드에서 변경 사항을 적용할 모듈을 선택하거나 **전체 시나리오**&#x200B;를 선택하여 시나리오의 영향을 받는 모든 모듈에 변경 사항을 적용합니다.
1. **바꾸기** 클릭
1. 영향을 받을 모듈의 미리보기를 검토합니다. 캔버스에서 모듈로 이동하려면 미리 보기에서 해당 행을 선택합니다.
1. **적용**&#x200B;을 클릭합니다.

## 소스 다시 매핑

**Source** 탭을 사용하여 다른 모듈의 매핑이 참조하는 모듈을 변경합니다.

1. 찾기 및 바꾸기를 연 다음 **Source** 탭을 클릭합니다.
1. Source 모듈 필드에서 매핑이 현재 참조하는 소스 모듈을 선택합니다.
1. Target 모듈 필드에서 대신 참조할 모듈을 선택합니다.
1. 모듈 필드에서 변경 사항을 적용할 모듈을 선택하거나 **전체 시나리오**&#x200B;를 선택하여 시나리오의 영향을 받는 모든 모듈에 변경 사항을 적용합니다.
1. **바꾸기** 클릭
1. 영향을 받을 모듈의 미리보기를 검토합니다. 캔버스에서 모듈로 이동하려면 미리 보기에서 해당 행을 선택합니다.
1. **적용**&#x200B;을 클릭합니다.

## 다른 모듈에 연결 복사

동일한 앱의 두 개 이상의 모듈에서 동일한 연결을 사용하려면 **연결** 탭을 사용하십시오.

1. 찾기 및 바꾸기를 연 다음 **연결** 탭을 클릭합니다.
1. 다음에서 연결 필드에서 다른 모듈에 사용할 연결이 현재 있는 모듈을 선택합니다.
1. 적용 대상 필드에서 변경 사항을 적용할 모듈을 선택하거나 시나리오에서 호환되는 모든 모듈에 변경 사항을 적용할지 여부를 선택합니다.
1. **적용**&#x200B;을 클릭합니다.
