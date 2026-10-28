---
title: 라이브 추적을 사용하여 시나리오 실행 검토
description: Live Trail에서는 모듈 요청과 실행 활동을 하나의 목록으로 결합하여 발생하는 대로 실행되는 시나리오를 보여 줍니다. 모든 작업에 대한 요청 및 응답 세부 정보를 열 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 17%
---

# 라이브 추적을 사용하여 시나리오 실행 검토

Live Trail에서 시나리오 실행 상황을 표시합니다. 모듈 요청과 실행 활동을 하나의 시간별 목록으로 결합하므로 시나리오 편집기에서 실행을 따라 캔버스를 벗어나지 않고 무엇이 잘못되었는지 확인할 수 있습니다.

>[!NOTE]
>
>이 기능은 새 시나리오 편집기 경험에서만 사용할 수 있습니다. 자세한 내용은 문서 시나리오 편집기에서 [새 경험 및 클래식 경험](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)을 참조하십시오.

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

## Live Trail 열기

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 검토할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 예를 들어 **한 번 실행**&#x200B;을 클릭하여 시나리오 실행을 시작합니다.



라이브 트레일이 캔버스의 오른쪽에 있는 패널에서 열립니다. 실행 중에 패널을 닫으면 화면 오른쪽에 있는 작은 탭에서 캡처한 이벤트를 손실하지 않고 다시 열 수 있습니다.

## Live Trail에서 이벤트 검토

Live Trail은 모듈 요청을 나열하고 발생하는 순서대로 활동을 실행합니다. 다음과 같은 작업을 수행할 수 있습니다.

* 목록을 검색합니다.
* 상태별로 목록을 필터링합니다.
* 실행이 계속되는 동안 최신 이벤트를 따릅니다.
* 현재 흔적을 지웁니다.

## 요청 및 응답 세부 정보 보기

1. 라이브 추적에서 세부 정보를 보려는 요청을 클릭합니다.

   요청을 수행한 모듈이 캔버스에 표시되고 요청 및 응답 세부 사항이 패널에서 열립니다.

1. 세부 사항을 검토합니다. 세부 사항 보기에는 다음이 포함됩니다.

   * 모듈 작업 간 탐색
   * 요청 헤더 및 본문
   * 응답 헤더 및 본문

1. (선택 사항) **원시 항목 복사** 또는 **cURL 복사**&#x200B;를 클릭하여 다른 곳에서 사용하도록 세부 정보를 복사합니다.

   * 요청 및 응답의 원시 보고서를 복사합니다.
   * 요청에 대한 cURL 명령을 복사합니다.

1. 목록으로 돌아가려면 패널의 왼쪽 상단에 있는 뒤로 화살표를 클릭합니다.

## 요청 및 응답 세부 정보가 사용 가능한지 확인

요청 및 응답 세부 정보는 많은 저장 공간을 차지하기 때문에 예약되거나 트리거되는 모든 실행에 대해 유지되지 않습니다.

* 한 번 실행은 항상 요청 및 응답 세부 정보를 유지합니다.
* 시나리오의 일반 실행의 경우 검사할 실행 전에 시나리오 설정에서 임시 디버그 로그를 켭니다. 자세한 내용은 시나리오 설정 구성 문서에서 [임시 디버그 로그](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs)를 참조하십시오.

실행 기록에서 실행을 열고 요청 및 응답 패널에 데이터가 없는 경우 패널에서는 임시 디버그 로그 설정으로 이동합니다.
