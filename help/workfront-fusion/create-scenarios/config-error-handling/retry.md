---
title: 재시도 오류 처리 해결 방법 구성
description: 경우에 따라 실패 사유가 빠르게 해결될 가능성이 있는 경우, 실패한 모듈을 다시 실행하는 것이 유용합니다.
author: Becky
feature: Workfront Fusion
exl-id: 08e19a1a-7ca9-4c79-a165-f200048a5cda
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# `retry` 오류 처리 해결 방법 구성

경우에 따라 실패 사유가 빠르게 해결될 가능성이 있는 경우, 실패한 모듈을 다시 실행하는 것이 유용합니다.

Adobe Workfront Fusion은 현재 `retry` 오류 처리 지시문을 제공하지 않지만 `retry` 기능을 모방하는 데 두 가지 해결 방법을 사용할 수 있습니다.

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

## [!UICONTROL 다시 시도] 오류 처리 지시문에 대한 해결 방법

Workfront Fusion은 현재 `retry` 오류 처리 지시문을 제공하지 않습니다. 다음 해결 방법 중 하나를 사용하여 재시도 기능을 모방하십시오.

지침은 [오류 처리에 대한 지시문](/help/workfront-fusion/references/errors/directives-for-error-handling.md)을 참조하십시오.

* [Break 지시문 사용](#use-the-break-directive)
* [반복 모듈 사용](#use-the-repeater-module)

### Break 지시문 사용

Break 지시문이 실행되면 시나리오 실행 상태가 불완전한 실행 큐에 저장됩니다. 이 경우 불완전한 실행을 수동으로 해결할 수 있습니다.

지침은 [Break 지시문에서 처리한 오류 해결](/help/workfront-fusion/create-scenarios/config-error-handling/resolve-error-from-break-directive.md)을 참조하십시오.

불완전한 실행 해결에 대한 지침은 [불완전한 실행 보기 및 해결](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)을 참조하십시오.

#### 단점

* 최소 재시도 간격은 1분입니다.
* 모듈이 여러 번들을 처리하고 번들 처리가 실패하면 부분 실행(오류를 일으킨 번들만)이 불완전한 실행 폴더로 이동되고 [!UICONTROL Break] 지시문 설정에 따라 다시 시도하도록 예약됩니다. 하지만 현재 실행은 계속되고 모듈은 후속 번들을 계속 처리합니다.

  미완료 실행 폴더에 저장된 실행이 정상적으로 해결될 때까지 시나리오가 다시 실행되지 않도록 하려면 [!UICONTROL 시나리오 설정]에서 &quot;[!UICONTROL 순차적 처리]&quot; 옵션을 사용하도록 설정하십시오.

불완전한 실행에 대한 자세한 내용은 [불완전한 실행 보기 및 해결](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)을 참조하십시오.

### 반복 모듈 사용

반복 모듈의 해결 방법은 보다 복잡하지만 사용자 정의가 더 용이합니다.

#### 오류 처리기 경로 구성

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 해결 방법을 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. **흐름 제어** 아이콘 ![흐름 제어](assets/flow-control-icon.png)를 클릭하고 **반복**&#x200B;을 선택합니다.
1. 반복 모듈에서 **[!UICONTROL 반복]** 필드를 시나리오가 다시 시도할 최대 횟수로 설정합니다.
1. **[!UICONTROL 반복]** 모듈 뒤에 오류가 발생할 수 있는 모듈을 연결합니다.
1. 오류 처리기 경로를 실패할 수 있는 모듈에 연결합니다.

   자세한 내용은 [오류 처리 추가](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)를 참조하십시오.
1. **[!UICONTROL 도구] > [!UICONTROL 절전 모드]** 모듈을 오류 처리기 경로에 추가하고 **[!UICONTROL 지연]** 필드를 다시 시도 간격(초)으로 설정합니다.

1. **[!UICONTROL 도구]** > **[!UICONTROL 절전 모드] 모듈 뒤에 [!UICONTROL Ignore]** 지시문을 추가하십시오.
1. [기본 경로 구성](#configure-the-default-route)을 계속합니다.

#### 기본 경로 구성

1. 실패할 가능성이 있는 모듈 뒤에 별도의(오류가 아닌 처리기) 경로에 **[!UICONTROL 도구] > [!UICONTROL 변수 설정]** 모듈을 추가하고 `Result`과(와) 같이 이름이 지정된 변수에 모듈의 결과를 저장하도록 구성합니다.

1. **[!UICONTROL 도구]** > **[!UICONTROL 변수 설정] 뒤에 [!UICONTROL 배열 집계]** 모듈을 추가하고 Source 모듈 필드에서 **[!DNL Repeater]** 모듈을 선택합니다.

1. **[!UICONTROL 배열 집계] 모듈 뒤에 [!UICONTROL 도구]** > **[!UICONTROL 변수 가져오기]** 모듈을 추가하고 `Result` 변수의 값을 매핑합니다.

1. **[!UICONTROL Repeater] 모듈과 실패할 가능성이 있는 모듈 사이에 [!UICONTROL Tools]** > **[!UICONTROL 변수 가져오기]** 모듈을 삽입하고 `Result` 변수의 값을 매핑하십시오.

1. 이 **[!UICONTROL 도구] > [!UICONTROL 변수 가져오기]** 모듈과 실패할 가능성이 있는 모듈 사이에 필터를 삽입하여 `Result` 변수가 없는 경우에만 계속합니다.

>[!BEGINSHADEBOX]

**예:**

이 샘플 시나리오에서는 [!UICONTROL HTTP] > [!UICONTROL 요청 만들기] 모듈이 실패할 수 있는 모듈을 나타냅니다.

![HTTP 요청 만들기](assets/http-make-request.png)

>[!ENDSHADEBOX]

실패할 가능성이 있는 모듈의 결과가 너무 복잡하여 간단한 변수에 저장할 수 없는 경우 데이터 저장소를 사용하여 결과를 저장하고 검색할 수 있습니다. 데이터 저장소에는 하나의 레코드만 포함됩니다. 레코드의 키(예: `Result`)는 다음과 같습니다.

데이터 저장소에 대한 자세한 내용은 [데이터 저장소](/help/workfront-fusion/create-scenarios/map-data/data-stores.md)를 참조하십시오.

#### 단점

* 이 해결 방법은 보다 복잡합니다.
* 이 해결 방법은 더 많은 작업을 사용하는 것입니다.

## 리소스

* Repeater 모듈 및 break 지시문에 대한 자세한 내용은 [흐름 컨트롤](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md)을 참조하십시오.
* 변수 모듈 가져오기에 대한 자세한 내용은 [도구](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md)를 참조하십시오.
