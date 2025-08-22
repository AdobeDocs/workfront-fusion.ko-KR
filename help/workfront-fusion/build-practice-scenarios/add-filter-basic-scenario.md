---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 기본 시나리오에 필터 추가
description: 필터를 사용하면 특정 조건이 충족되는 경우에만 시나리오가 진행되도록 할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 78ab27fe-e2dd-4b52-b986-77b4b7ea3b5e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 1%

---

# 기본 시나리오에 필터 추가

필터를 사용하면 특정 조건이 충족되는 경우에만 시나리오가 진행되도록 할 수 있습니다.

이 예제에서는 요청이 특정 요청 대기열에 제출된 경우에만 요청에서 새 프로젝트를 만들 수 있도록 하는 필터를 시나리오에 추가합니다.

이 예제에서는 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에서 만든 시나리오를 수정합니다.

>[!NOTE]
>
>Workfront 트리거 모듈에는 특정 조건이 충족되는 경우에만 시나리오를 시작할 수 있도록 하는 필터가 포함됩니다. 그러나 모듈간 필터는 트리거가 아닌 모든 및 Workfront이 아닌 사용 사례에 사용되므로 모듈 간에 필터를 사용하는 방법을 알아보는 것이 중요합니다. 이 예제에서는 모듈 내 필터에서 충족할 수 있는 기능을 위해 모듈 간 필터를 사용합니다.

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
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] Workfront 플랜: 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li><li>[!UICONTROL Ultimate] Workfront 계획: Workfront Fusion이 포함됩니다.</li></ul>
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

이 절차를 수행하기 전에 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에 설명된 시나리오를 만들어야 합니다.

## 필터 추가

### 필터 추가 준비

1. 시나리오를 엽니다.
1. 첫 번째 모듈을 클릭하여 엽니다.
1. **출력** 영역에서 `Project`을(를) 선택합니다.
이제 `ID`, `Name` 및 `Project`이(가) 선택되었습니다.
1. 확인 을 클릭하여 모듈 설정을 저장합니다.
1. Workfront을 엽니다.
1. Workfront에서 Fusion 시나리오가 작동할 요청 대기열을 나타내는 프로젝트를 찾습니다.

   이 프로젝트는 Fusion 연결이 설정된 Workfront 계정과 동일한 계정에 있어야 합니다.

1. URL에 프로젝트 ID를 기록합니다.

   예: https://\&lt;MyDomain\>.my.workfront.com/project/\&lt;ProjectID\>/tasks

### 필터 추가 및 구성

1. 시나리오 편집기의 시나리오로 돌아갑니다.
1. 첫 번째 모듈과 두 번째 모듈 사이에 있는 렌치 아이콘 ![렌치 아이콘](assets/wrench-icon.png)을 클릭하고 **필터 설정**&#x200B;을 선택합니다.
1. 레이블 필드에 &quot;요청 대기열에 대한 필터&quot;와 같은 이 필터의 레이블을 입력합니다.
1. **Condition** 영역의 맨 위 필드에서 첫 번째 모듈의 `projectID`을(를) 매핑합니다.

   ![맵 프로젝트 ID](assets/map-proj-id.png)
1. **Condition** 연산자를 같음(으)로 둡니다.
1. **조건** 영역의 아래쪽 필드에서 [필터 추가 준비](#prepare-to-add-the-filter)의 프로젝트 URL에서 메모한 프로젝트 ID에 붙여 넣습니다.
1. **확인**&#x200B;을 클릭하여 필터 설정을 저장합니다.

### 테스트 및 활성화

1. Fusion이 연결 중인 Workfront 환경으로 이동하여 필터에 지정한 프로젝트에 문제를 추가합니다. 다른 프로젝트에 다른 문제를 추가합니다.
1. 시나리오 편집기의 왼쪽 아래에서 **[!UICONTROL 한 번 실행]**&#x200B;을 클릭합니다.
1. 출력을 검사하여 시나리오가 예상대로 실행되었는지 확인합니다.

   두 문제는 모두 첫 번째 모듈의 출력에 표시되지만, 지정된 프로젝트의 문제만 두 번째 모듈에 대한 입력으로 표시되어야 합니다.
1. 시나리오가 예상대로 작동하는 경우 화면 왼쪽 하단의 **예약** 전환을 클릭하여 **켜기**&#x200B;로 전환합니다.

   이렇게 하면 시나리오가 활성화됩니다.
1. Workfront Fusion에서 왼쪽 아래 모서리 근처에 있는 **[!UICONTROL 저장]**&#x200B;을 클릭하여 시나리오에 대한 진행 상황을 저장합니다.

   >[!IMPORTANT]
   >
   >원하는 만큼 자주 저장하고 시나리오를 테스트합니다.

## 리소스

* 필터에 대한 자세한 내용은 [시나리오에 필터 추가](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md)를 참조하십시오.
