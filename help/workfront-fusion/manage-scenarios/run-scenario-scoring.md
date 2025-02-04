---
title: 시나리오 채점 전문가 실행
description: 시나리오 채점 전문가는 모범 사례를 따르는 방식으로 시나리오가 구성되도록 하는 데 도움이 될 수 있습니다. 시나리오를 확인하고 구조 및 조직에 대한 권장 사항을 제공합니다.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 1ac1c4358901ef81bb7375c24fcdf1a44119af13
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 1%

---

# 시나리오 채점 전문가 실행

>[!IMPORTANT]
>
>시나리오 채점 전문가가 일시적으로 비활성화되었습니다.

시나리오 채점 전문가는 모범 사례를 따르는 방식으로 시나리오가 구성되도록 하는 데 도움이 될 수 있습니다. 시나리오를 확인하고 구조 및 조직에 대한 권장 사항을 제공합니다.

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

## 시나리오 채점 전문가 실행

1. 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 시나리오 채점 전문가를 실행할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 화면 하단 근처에 있는 시나리오 채점 전문가 아이콘 ![시나리오 채점 전문가](assets/scoring-expert-icon.png)을(를) 클릭합니다.

   시나리오 채점 전문가 패널이 열립니다.
1. **평가**&#x200B;를 클릭합니다.

시나리오 채점 전문가가 10점 만점을 반환하고 합격 또는 실패한 검사를 표시합니다. 검사가 실패한 경우 시나리오 채점 전문가가 시나리오가 이러한 검사를 충족하는지 확인하는 방법에 대한 권장 사항을 제공합니다.

![시나리오 점수](assets/scenario-score.png)

## 시나리오 채점 확인

시나리오 채점 전문가는 다음 검사를 사용합니다.

* 시나리오에 이름을 지정해야 합니다.
* 모든 모듈에 레이블이 지정되어야 합니다.
* 시나리오는 정해진 일정에 따라 실행되어야 합니다.

  지침은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하세요.
* 시나리오 블루프린트 크기는 5MB 미만이어야 합니다.

  자세한 내용은 [Fusion 성능 보호](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios)를 참조하십시오.
* Workfront 인스턴트 트리거 모듈을 사용하는 경우 필터링해야 합니다.

  자세한 내용은  [!DNL Workfront] > [!UICONTROL Watch Events] 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules)에서 [이벤트 구독 필터를 참조하십시오.
