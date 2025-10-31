---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 기본 시나리오에 트리거 모듈 추가
description: 시나리오가 정기적으로 새 요청을 검색하고 프로젝트로 변환할 수 있도록 트리거 모듈을 추가하는 방법을 알아봅니다.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 1%

---

# 기본 시나리오에 트리거 모듈 추가

트리거 모듈은 시나리오의 시작 부분에 배치됩니다. 이러한 모듈은 지정된 서비스가 변경되면 시나리오 실행을 시작합니다. 새 레코드 만들기, 레코드 삭제, 레코드 업데이트 등이 변경 내용이 될 수 있습니다. 시나리오를 시작하는 변경 사항에 대한 기준을 지정합니다.

폴링 모듈은 설정된 시간 간격으로 서비스를 확인하고 해당 시간 간격 동안 발생한 변경 사항에 대한 정보를 반환합니다. 변경 사항이 없으면 트리거에서 시나리오를 실행하지 않습니다.

이 예에서는 15분마다 실행되고 요청이 특정 대기열에 제출된 경우 시나리오를 시작하는 트리거 모듈을 추가합니다. 그런 다음 시나리오에서는 해당 요청을 프로젝트로 전환합니다.

이 예제에서는 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에서 만든 시나리오를 수정합니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 전제 조건

이 절차를 수행하기 전에 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에 설명된 시나리오를 만들어야 합니다.

## 트리거 모듈 추가 및 구성

### 트리거 모듈 추가

1. 시나리오 편집기에서 시나리오를 엽니다.
1. 첫 번째(검색) 모듈을 마우스 오른쪽 단추로 클릭하고 **모듈 삭제**&#x200B;를 선택합니다.

   모듈이 삭제되고 빈 자리 표시자가 남습니다.

1. 빈 모듈을 클릭하고 앱 목록에서 **Adobe Workfront**&#x200B;을(를) 선택합니다.
1. **레코드 보기**&#x200B;를 선택하십시오.
1. 모듈이 시나리오의 나머지 모듈과 동일한 연결을 사용하는지 확인합니다.
1. 레코드 유형 필드에서 **문제**&#x200B;를 선택합니다.
1. 필터 필드에서 **새 레코드만**&#x200B;을(를) 선택합니다.
1. 출력 상자에서 `ID`, `Name` 및 `Project ID`을(를) 선택합니다.
1. **확인**&#x200B;을 클릭하여 모듈 설정을 저장합니다.

   시작 위치 선택 창이 나타납니다.

1. **지금부터**&#x200B;을(를) 선택합니다.

### 트리거 모듈 예약

1. Watch Records 모듈에서 시계를 클릭합니다.

   스케줄 설정 창이 열립니다.

1. 실행 시나리오 필드에서 **일정한 간격으로**&#x200B;을(를) 선택합니다.

1. **확인**&#x200B;을 클릭합니다.

### 두 번째 모듈 업데이트

첫 번째 모듈이 대체되었으므로 두 번째 모듈은 새 첫 번째 모듈에 매핑되어야 합니다.

1. Convert 개체 모듈을 엽니다.
1. Issue ID 필드에서 검정색 ID 블록을 삭제합니다. 블록이 매핑된 모듈을 더 이상 사용할 수 없으므로 블록은 검정색입니다.
1. 첫 번째 모듈(레코드 보기) 아래에서 ID 블록을 선택하여 두 번째 모듈에 매핑합니다.
1. **확인**&#x200B;을 클릭합니다.

### 테스트 및 활성화

1. Fusion이 연결 중인 Workfront 환경으로 이동하여 문제를 추가합니다.
1. 시나리오 편집기의 왼쪽 아래에서 **[!UICONTROL 한 번 실행]**&#x200B;을 클릭합니다.
1. 출력을 검사하여 시나리오가 예상대로 실행되었는지 확인합니다.
1. 시나리오가 예상대로 작동하는 경우 화면 왼쪽 하단의 **예약** 전환을 클릭하여 **켜기**&#x200B;로 전환합니다.

   이렇게 하면 시나리오가 활성화됩니다.
1. Workfront Fusion에서 왼쪽 아래 모서리 근처에 있는 **[!UICONTROL 저장]**&#x200B;을 클릭하여 시나리오에 대한 진행 상황을 저장합니다.

   >[!IMPORTANT]
   >
   >원하는 만큼 자주 저장하고 시나리오를 테스트합니다.

## 리소스

* 트리거 모듈에 대한 자세한 내용은 문서 모듈 개요에서 [트리거 모듈](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)을(를) 참조하십시오.
