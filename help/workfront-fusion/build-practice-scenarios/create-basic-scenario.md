---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 기본 시나리오 만들기
description: Adobe Workfront Fusion을 사용하여 간단한 자동화 시나리오를 만드는 방법에 대해 알아봅니다. 자동화 시나리오는 데이터 조작 및 변형을 포함한 Workfront 프로세스를 자동화합니다. 이 예에서는 Workfront에서 Workfront 작업을 검색하고 이 작업을 프로젝트로 변환하는 시나리오를 만드는 프로세스를 안내합니다.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
source-git-commit: 6269db7454a63e80de3d770ab1012162d5080565
workflow-type: tm+mt
source-wordcount: '1419'
ht-degree: 12%

---

# 기본 시나리오 만들기

Adobe Workfront Fusion의 역할은 동일한 작업을 계속해서 반복하는 대신 새로운 작업에 집중할 수 있도록 프로세스를 자동화하는 것입니다. 데이터를 자동으로 전송하고 변환하는 시나리오를 만들기 위해 앱과 서비스 내에서 그리고 앱과 서비스 간에 액션을 연결하는 방식입니다. 생성한 시나리오는 앱이나 서비스의 데이터를 관찰하고 해당 데이터를 처리하여 원하는 결과를 제공합니다.

이 예에서는 Workfront에서 요청을 검색하고 이 요청을 프로젝트로 변환하는 시나리오를 만드는 프로세스를 안내합니다.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 연습 시나리오 만들기

### 시나리오 만들기 시작

1. **시나리오** 영역에서 **새 시나리오 만들기**&#x200B;를 클릭합니다.

   시나리오 영역을 찾으려면 [Workfront Fusion 탐색](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md)을 참조하십시오.

   중앙에 빈 모듈이 들어 있는 시나리오 편집기가 표시됩니다.

1. 왼쪽 상단에서 **[!UICONTROL 새 시나리오]** 자리 표시자 이름을 선택한 다음 이름을 입력하십시오.
1. [첫 번째 모듈 추가 및 구성](#add-and-configure-the-first-module)을 계속합니다.

### 첫 번째 모듈 추가 및 구성

1. 빈 모듈을 클릭하여 모듈을 선택할 앱을 선택합니다.

   앱 목록이 모듈 오른쪽에 나타납니다.

1. **Adobe Workfront**&#x200B;을(를) 선택합니다. 표시되지 않는 경우 목록 맨 아래에 있는 검색 막대를 클릭하고 &quot;Workfront&quot;를 입력한 다음 목록에 나타나면 선택합니다.

   목록이 변경되어 사용할 수 있는 모든 Workfront 모듈이 표시됩니다.

1. **[!UICONTROL 검색]** 모듈을 클릭합니다.

   모듈 구성 창이 열립니다.

1. [!UICONTROL 연결] 상자에서 Workfront 연결을 선택합니다.

   Workfront 연결이 없는 경우 [연결 만들기](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)를 참조하세요.
1. [!UICONTROL 레코드 종류] 상자에서 **[!UICONTROL 문제]**&#x200B;를 선택합니다. 이렇게 하면 모듈이 요청을 포함하는 문제만 검색하도록 설정됩니다.

   &quot;**[!UICONTROL 문제]**&quot;라는 단어를 입력하면 목록에서 [!UICONTROL 문제]를 찾을 수 있습니다.

1. **[!UICONTROL 결과 집합]** 상자에서 **[!UICONTROL 첫 번째 일치하는 레코드]**&#x200B;을 선택합니다.

   이 옵션은 기준을 충족하는 첫 번째 레코드만 반환하도록 모듈을 설정합니다.
1. **[!UICONTROL 검색 조건]** 영역에서 특정 작업을 반환하도록 조건을 구성하십시오.

   1. [!UICONTROL 검색 조건] 아래의 첫 번째 상자에서 검색에 포함할 필드를 선택합니다. 이 예제에서는 **[!UICONTROL 이름]**&#x200B;을(를) 선택합니다.

      단어 &quot;**[!UICONTROL 이름]**&quot;을(를) 입력하면 목록에서 [!UICONTROL 이름]을(를) 찾을 수 있습니다.
   1. 연산자의 경우 **존재** 옆에 있는 드롭다운 화살표를 클릭하고 [!UICONTROL **포함(대/소문자 구분 안 함)**] (으)로 변경합니다.

      이렇게 하면 전체 이름을 입력하지 않거나 대/소문자가 잘못된 이름(예: 모두 대문자)을 입력하더라도 모듈이 이름에 선택한 단어가 포함된 프로젝트를 찾을 수 있습니다.
   1. [!UICONTROL 검색 조건]의 마지막 필드에 검색 중인 작업 이름에 있는 단어 또는 구를 입력하십시오.

1. **[!UICONTROL 출력]** 목록에서 모듈에서 출력할 필드를 선택합니다. 이 예제에서는 **[!UICONTROL ID]** 및 **[!UICONTROL 이름]** 필드를 선택합니다.

   >[!TIP]
   >
   >**Cmd+F**([!DNL Mac] OS) 또는 **Ctrl-F**([!DNL Windows] OS)를 사용하여 필드를 빠르게 찾을 수 있습니다.

1. **[!UICONTROL 확인]**&#x200B;을 클릭하여 모듈 구성을 저장합니다.

1. 모듈을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL 이름 바꾸기]**&#x200B;를 클릭한 다음 모듈에서 수행할 작업을 설명하는 이름을 입력한 다음(&quot;요청 검색&quot; 등) **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

   모듈 바로 아래에 이름이 표시됩니다. 그 아래에 Workfront Fusion에는 모듈에서 수행되는 작업 유형에 대한 간단한 설명이 포함됩니다.

   ![이름이 변경된 모듈](assets/module-renamed-wf.png)

1. [두 번째 모듈 추가 및 구성](#add-and-configure-the-second-module)을 계속합니다.

## 두 번째 모듈 추가 및 구성

1. 모듈 오른쪽의 부분 원을 마우스로 가리킨 다음 **[!UICONTROL 다른 모듈 추가]**&#x200B;를 클릭합니다.
1. 응용 프로그램 목록에서 Adobe Workfront을 선택한 다음 **[!UICONTROL 개체 변환]** 모듈을 선택합니다.
1. [!UICONTROL 연결] 필드에서 이전 모듈에서 사용한 것과 동일한 Workfront 연결을 선택합니다.
1. 모듈이 문제를 전환하므로 **[!UICONTROL 레코드 종류]** 필드에서 **[!UICONTROL 문제]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL 변환 대상]** 필드에서 **프로젝트**&#x200B;을(를) 선택합니다.
1. 작업 ID 필드 옆에 있는 맵 토글을 클릭하여 활성화합니다.

   활성화되면 토글이 파란색으로 바뀝니다. 이를 통해 이전 모듈의 작업 ID를 매핑할 수 있습니다.

   ![토글 매핑](assets/map-toggle.png)
1. **[!UICONTROL 작업 ID]** 필드를 클릭합니다.

   프로젝트로 전환할 작업의 ID로 사용할 항목을 선택할 수 있는 패널이 열립니다. 매핑을 활성화했으므로 패널에는 이전 모듈의 출력이 포함됩니다. ID를 이전 모듈의 출력으로 선택했으므로 이제 패널에서 사용할 수 있습니다.

   이 패널을 매핑 패널이라고 합니다. 매핑 패널에 대한 자세한 내용은 [매핑 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md)를 참조하십시오.
1. 매핑 패널에서 **ID**&#x200B;을(를) 선택합니다.

   ID 필드가 ID 블록으로 표시됩니다. 매핑된 원본 모듈 번호와 매핑된 필드를 표시합니다.

   ![맵 ID](assets/map-id.png)

1. **템플릿 ID** 필드를 클릭하고 이 프로젝트에 사용할 Workfront 템플릿의 이름을 입력한 다음 목록에 표시될 때 선택합니다.
1. **[!UICONTROL 확인]**&#x200B;을 클릭하여 모듈 구성을 저장합니다.

1. 모듈을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL 이름 바꾸기]**&#x200B;를 클릭한 다음 모듈에서 수행할 작업을 설명하는 이름을 입력한 다음(&quot;프로젝트로 변환&quot; 등) **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

1. [시나리오 테스트](#test-the-scenario)를 계속합니다.

## 시나리오 테스트

시나리오를 활성화하기 전에 한 번 이상 실행하고 결과를 보고 테스트하는 것이 중요합니다. 이렇게 하면 시나리오에 데이터가 흐르는 방식을 이해하고 오류를 찾는 데 도움이 됩니다.

이 시나리오에서는 테스트가 성공하면 요청을 찾아 프로젝트로 전환할 수 있습니다.

1. 시나리오 편집기의 왼쪽 아래에서 **[!UICONTROL 한 번 실행]**&#x200B;을 클릭합니다.
1. 시나리오 실행이 완료되면 첫 번째 모듈 위의 버블을 클릭하여 모듈이 반환한 요청에서 가져온 데이터를 포함하여 모듈이 처리한 데이터 번들에 대한 정보를 볼 수 있습니다.

1. 두 번째 모듈 위의 실행 검사기 버블을 클릭하여 입력(요청)과 출력(변환된 프로젝트)을 확인합니다.

   검사 버블의 데이터에 대한 자세한 내용은 다음을 참조하십시오.

   * 일반 정보는 [시나리오 실행 흐름](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)을 참조하십시오.
   * 처리된 번들에 대한 자세한 내용은 [시나리오 실행, 주기 및 단계](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)를 참조하십시오.

1. Workfront Fusion에서 왼쪽 아래 모서리 근처에 있는 **[!UICONTROL 저장]**&#x200B;을 클릭하여 시나리오에 대한 진행 상황을 저장합니다.

   >[!IMPORTANT]
   >
   >원하는 만큼 자주 저장하고 시나리오를 테스트합니다. 시나리오를 트리거하려면 Workfront 계정에서 새 문제를 만들어야 할 수 있습니다.

>[!TIP]
>
>각 모듈에 대한 메모를 추가하는 옵션이지만 유용한 방법을 권장합니다.
>
>1. 모듈을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL 메모 추가]**&#x200B;를 선택합니다.
>1. 표시되는 노트에 모듈에 대한 개요를 입력합니다.
>
>    한 모듈에 대해 여러 메모를 추가할 수 있습니다.
>
>1. **[!UICONTROL 메모]** 영역을 닫습니다.
>
>     시나리오에 메모를 추가하면 시나리오 편집기 하단의 **[!UICONTROL 메모]** 아이콘 ![메모 아이콘 &#x200B;](assets/notes-icon-w-dot.png)에 점이 표시됩니다.
>
>1. **[!UICONTROL 메모]** 아이콘 ![점이 있는 메모 아이콘](assets/notes-icon-w-dot.png)을 클릭하여 메모를 봅니다. 메모가 열려 있으면 메모 아이콘 주위에 원이 나타납니다.
>

## 시나리오 활성화

시나리오를 만드는 마지막 단계는 활성화하는 것입니다.

이 시나리오는 특정 문제를 검색하는 것이므로 활성화할 필요가 없습니다. 시나리오를 활성화하면 일정에 따라 또는 애플리케이션에서 특정 작업이 발생할 때 시나리오가 실행됩니다. 시나리오를 활성화하면 기본적으로 15분마다 실행됩니다. 실행할 시기와 빈도를 정의하여 변경할 수 있습니다.

시나리오 활성화에 대한 자세한 내용은 [시나리오 활성화 또는 비활성화](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md)를 참조하십시오.

일정에 대한 자세한 내용은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하십시오.

## 다음 단계

* [트리거 모듈을 추가](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md)하여 시나리오가 정기적으로 새 요청을 검색하고 프로젝트로 변환할 수 있도록 합니다.
* 요청이 입력될 때마다 시나리오를 실행할 수 있도록 [Webhook를 추가](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md)합니다.
* [필터를 추가](/help/workfront-fusion/build-practice-scenarios/add-filter-basic-scenario.md)하여 특정 요청만 프로젝트로 변환되도록 합니다.
* 새 프로젝트의 이름을 사용자 지정하는 함수를 [추가](/help/workfront-fusion/build-practice-scenarios/use-function-to-build-practice-scenario.md)합니다.
