---
title: 시나리오 편집기
description: 시나리오 편집기를 사용하면 시각적 인터페이스에서 시나리오를 만들고 편집할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 3%

---

# 시나리오 편집기

시나리오 편집기를 사용하면 시각적 인터페이스에서 시나리오를 만들고 편집할 수 있습니다.

![시나리오 편집기](assets/scenario-editor.jpg)

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스</td> 
   <td> <p>신규: [!UICONTROL Standard]</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Workfront] 플랜: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 플랜: [!DNL Workfront Fusion]이(가) 포함되어 있습니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성*</td> 
   <td> 
     <p>조직의 [!DNL Workfront Fusion] 관리자여야 합니다.</p>
     <p>팀의 [!DNL Workfront Fusion] 관리자여야 합니다.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 시나리오 편집기를 열고 모듈을 추가합니다.

1. 왼쪽 패널에서 **[!UICONTROL Scenarios]** ![시나리오 아이콘](assets/scenarios-icon.png)을 클릭합니다.
1. 물음표 아이콘 ![물음표 아이콘](assets/question-mark-full-size.png)을 클릭한 다음 시작할 앱 또는 서비스를 찾아 클릭합니다. 모듈 구성에 대한 자세한 내용은 [모듈 구성](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)을 참조하십시오.

## 사용 가능한 시나리오 편집기 작업

### 시나리오 실행

| 액션 | 세부 사항 |
|----------|----------|
| 시나리오 테스트 실행 | 활성화하기 전에 시나리오가 예상대로 실행되는지 확인하십시오. 활성화되면 시나리오는 일정에 따라 실행됩니다. 모든 것이 예상대로 실행되지 않으면 [오류 처리 추가](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)를 참조하여 오류를 처리하는 방법을 알아보십시오. |

![시나리오 실행 단추](assets/run-your-scenario.png)

### 일정 조정

| 액션 | 세부 사항 |
|----------|----------|
| 시나리오 예약 | 기본적으로 시나리오는 15분마다 실행됩니다. 활성화된 시나리오가 실행되는 시기와 빈도를 정의하여 이를 변경할 수 있습니다. Fusion 시나리오는 5분마다 실행되도록 예약할 수 있습니다. 자세한 내용은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하십시오. |

![일정 패널](assets/scheduling-scenario-editor.png)

### 컨트롤

| 액션 | 세부 사항 |
|----------|----------|
| 저장 | 시나리오를 저장하면 나중에 액세스해야 하는 경우 3점 메뉴 아래에서 새 버전을 사용할 수 있습니다. 이전에 저장한 시나리오 버전은 60일 동안만 사용할 수 있습니다. |
| 시나리오 설정 | 시나리오 설정 패널에는 시나리오에 대한 고급 설정이 포함되어 있습니다. 사용 가능한 설정에 대한 자세한 내용은 [시나리오 설정 구성](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)을 참조하십시오. |
| 메모 | 시나리오에 대해 메모를 합니다. 다른 사용자는 시나리오에 있을 때 이러한 메모를 볼 수 있습니다. |
| 자동 정렬 | 시나리오에서 모듈을 자동 정렬합니다. |
| 흐름 설명 | 시나리오의 데이터 흐름 방식을 보여 주는 애니메이션을 봅니다. |
| 개발 도구 | Devtool을 사용하면 시나리오의 모든 수동 실행을 확인하고, 수행된 모든 작업을 검토하고, 수행된 모든 API 호출의 세부 정보를 볼 수 있습니다. 오류를 일으킨 모듈, 작업 또는 단일 응답을 확인하고 해당 지식을 사용하여 시나리오를 구체화할 수 있습니다. 자세한 내용은 [시나리오 디버그](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md)를 참조하십시오. |
| 기타 | 기타 메뉴에서 블루프린트를 가져오거나 내보내고 시나리오를 이전 버전으로 복원할 수 있습니다. |

![컨트롤 패널](assets/controls-editor-scenario.png)

### 도구

| 액션 | 세부 사항 |
|----------|----------|
| 흐름 제어 | 설정을 구성하여 데이터가 이동하는 방식을 제어합니다. 자세한 내용은 [링크 필요]를 참조하세요. |
| 도구 | 도구 섹션에는 시나리오를 향상시킬 수 있는 몇 가지 유용한 모듈이 포함되어 있습니다. 자세한 내용은 [링크 필요]를 참조하세요. |
| 텍스트 구문 분석기 | 텍스트 파서 도구를 사용하여 다른 시나리오 모듈에서 사용할 텍스트를 구문 분석합니다. 텍스트 파서는 연결할 필요가 없습니다. 자세한 내용은 [링크 필요]를 참조하세요. |

![도구 패널](assets/tools-scenario-editor.png)

### 즐겨찾기

즐겨찾기 아이콘을 사용하여 자주 사용하는 모듈을 추가할 수 있습니다.

![즐겨찾기 패널](assets/favorites-scenario-editor.png)
