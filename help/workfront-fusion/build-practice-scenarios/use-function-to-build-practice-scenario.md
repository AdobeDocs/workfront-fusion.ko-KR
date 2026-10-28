---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 함수를 사용하여 기본 시나리오에서 프로젝트 업데이트
description: Workfront에서 작업 항목을 업데이트하는 기능을 추가하는 방법을 알아봅니다.
author: Becky
feature: Workfront Fusion
exl-id: aa082ac8-48e8-4569-880e-024dd77feaa1
TQID: https://experienceleague.adobe.com/F0kYjSMVgit8t-gPAR4U7O-1v8Qxy7UxSRK6uYxKItg
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 4cd8b43e9ce9a16aca16397ce140cdd2467bf7d4
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 10%
---
# 함수를 사용하여 기본 시나리오에서 프로젝트 업데이트

Workfront 작업 항목 업데이트는 Workfront Fusion의 일반적인 사용 사례입니다. 이 예제에서는 함수를 사용하여 프로젝트 이름을 대문자로 변경합니다.

Fusion에는 데이터에 대해 조건부 논리를 변환하고 수행할 수 있는 다양한 유형의 함수가 포함되어 있습니다. 함수 사용에 대한 자세한 내용은 [함수 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)를 참조하십시오.

이 예제에서는 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에서 만든 시나리오를 수정합니다.

>[!NOTE]
>
>Workfront Fusion에서 시나리오 편집기를 새 경험으로 전환합니다. 이 전환 중에 클래식 경험과 새 경험을 모두 사용할 수 있으며 언제든지 전환할 수 있습니다. 새 경험을 사용하는 것이 좋습니다. 자세한 내용은 문서 시나리오 편집기에서 [새 경험 및 클래식 경험](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)을 참조하십시오.

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

## 전제 조건

이 절차를 수행하기 전에 [기본 시나리오 만들기](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)에 설명된 시나리오를 만들어야 합니다.

## 함수를 사용하여 새 경험에서 프로젝트를 업데이트합니다(권장)

* [시나리오에 레코드 업데이트 모듈 추가](#add-the-update-a-record-module-to-your-scenario)
* [이름 업데이트를 위한 함수 매핑](#map-the-function-for-the-name-update)
* [테스트 및 활성화](#test-and-activate)

### 시나리오에 레코드 업데이트 모듈 추가

1. 시나리오 편집기에서 시나리오를 엽니다.
1. 두 번째 모듈의 오른쪽 가장자리를 마우스로 가리킨 다음 **[!UICONTROL 다른 모듈 추가]**&#x200B;가 나타나면 클릭합니다.
1. 응용 프로그램 목록에서 Adobe Workfront을 선택한 다음 **[!UICONTROL 레코드 업데이트]** 모듈을 선택합니다.
1. ID 필드에서 Convert 개체 모듈 아래에 있는 ID 블록을 선택합니다. 해당 모듈에서 출력된 프로젝트의 ID입니다.

   ![레코드 업데이트 모듈의 매핑된 ID](assets/new-mapped-update-record.png)

1. 업데이트할 개체가 프로젝트이므로 레코드 유형 필드에서 프로젝트를 선택합니다.
1. 매핑할 필드 선택 영역에서 이름을 선택합니다.

   이름 필드가 열립니다.
1. [이름 업데이트에 대한 함수 매핑](#map-the-function-for-the-name-update)을(를) 계속합니다.

### 이름 업데이트를 위한 함수 매핑

이 시나리오가 요청을 프로젝트로 변환할 때 프로젝트의 이름이 요청과 동일합니다. 여기서 함수는 해당 이름을 사용하고 그 안에 있는 모든 문자를 대문자로 바꿉니다.

1. **이름** 필드를 클릭합니다.

   매핑 패널이 열립니다.
1. 매핑 패널에서 **텍스트 및 이진 함수** 아이콘을 클릭합니다. ![텍스트 함수 아이콘](assets/new-text-binary-function.png)
1. **upper** 함수를 선택하십시오.

   이 함수는 기대하는 입력에 대한 형식을 포함하여 이름 필드에 나타납니다.

   이 예제의 입력은 프로젝트가 전환된 문제의 이름입니다.

1. 입력이 진행될 위치이므로 커서를 괄호 사이로 이동합니다.
1. 매핑 패널에서 **모듈 출력** 아이콘을 클릭합니다. ![모듈 출력 아이콘](assets/new-module-output-icon.png)
1. 첫 번째 모듈에서 출력한 이름 블록을 선택합니다.

   이름 블록이 함수에 나타납니다.

   ![함수의 이름 블록](assets/new-mapped-name-block.png)

1. **확인**&#x200B;을 클릭하여 모듈 설정을 저장합니다.

### 테스트 및 활성화

1. **[!UICONTROL 한 번 실행]** 아이콘을 클릭하여 시나리오를 테스트합니다.

   한 번 실행은 새 경험에서 아이콘 전용입니다. 아이콘 위로 마우스를 가져가면 **[!UICONTROL 한 번 실행]** 도구 설명을 볼 수 있습니다.

   ![시나리오 실행 단추](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

1. 출력을 검사하여 시나리오가 예상대로 실행되었는지 확인합니다.
1. 시나리오가 예상대로 작동하는 경우 **예약** 전환을 클릭하여 **켜기**&#x200B;로 전환합니다.

   이렇게 하면 시나리오가 활성화됩니다. 활성 시나리오는 트리거 모듈에 설정된 일정에 따라 실행됩니다.

   ![예약 전환](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. 시나리오에 대한 진행률을 저장하려면 컨트롤 영역에서 **저장** 아이콘 ![저장 아이콘](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png)을 클릭합니다.

   >[!IMPORTANT]
   >
   >원하는 만큼 자주 저장하고 시나리오를 테스트합니다. 시나리오를 트리거하려면 Workfront 계정에서 새 문제를 만들어야 할 수 있습니다.

## 함수를 사용하여 클래식 경험에서 프로젝트를 업데이트합니다.

* [레코드 업데이트 모듈을 시나리오에 추가(클래식)](#add-the-update-a-record-module-to-your-scenario-classic)
* [이름 업데이트에 대한 함수 매핑(클래식)](#map-the-function-for-the-name-update-classic)
* [테스트 및 활성화(클래식)](#test-and-activate-classic)

### 레코드 업데이트 모듈을 시나리오에 추가(클래식)

1. 시나리오 편집기에서 시나리오를 엽니다.
1. 두 번째 모듈의 오른쪽에 있는 부분 원을 마우스로 가리킨 다음 **[!UICONTROL 다른 모듈 추가]**&#x200B;를 클릭합니다.
1. 응용 프로그램 목록에서 Adobe Workfront을 선택한 다음 **[!UICONTROL 레코드 업데이트]** 모듈을 선택합니다.
1. ID 필드에서 Convert 개체 모듈 아래에 있는 ID 블록을 선택합니다. 해당 모듈에서 출력된 프로젝트의 ID입니다.

   ![개체 변환의 ID](assets/id-convert-object.png)

1. 업데이트할 개체가 프로젝트이므로 레코드 유형 필드에서 프로젝트를 선택합니다.
1. 매핑할 필드 선택 영역에서 이름을 선택합니다.

   이름 필드가 열립니다.
1. [이름 업데이트(클래식)에 대한 함수 매핑](#map-the-function-for-the-name-update-classic)을 계속합니다.

### 이름 업데이트에 대한 함수 매핑(클래식)

이 시나리오가 요청을 프로젝트로 변환할 때 프로젝트의 이름이 요청과 동일합니다. 여기서 함수는 해당 이름을 사용하고 그 안에 있는 모든 문자를 대문자로 바꿉니다.

1. **이름** 필드를 클릭합니다.

   매핑 패널이 열립니다.
1. 매핑 패널에서 **텍스트 및 이진 함수** 아이콘을 클릭합니다. ![텍스트 함수 아이콘](assets/toolbar-icon-text-binary-functions.png)
1. **upper** 함수를 선택하십시오.

   이 함수는 기대하는 입력에 대한 형식을 포함하여 이름 필드에 나타납니다.

   이 예제의 입력은 프로젝트가 전환된 문제의 이름입니다.

1. 입력이 진행될 위치이므로 커서를 괄호 사이로 이동합니다.
1. 매핑 패널에서 **모듈 출력** 아이콘을 클릭합니다. ![모듈 출력 아이콘](assets/toolbar-icon-functions-you-map-from-other-modules.png)
1. 첫 번째 모듈에서 출력한 이름 블록을 선택합니다.

   이름 블록이 함수에 나타납니다.

   ![함수의 이름 블록](assets/map-name.png)

1. **확인**&#x200B;을 클릭하여 모듈 설정을 저장합니다.

### 테스트 및 활성화(클래식)

1. 화면 왼쪽 하단의 **한 번 실행**&#x200B;을 클릭하여 시나리오를 테스트합니다.
1. 출력을 검사하여 시나리오가 예상대로 실행되었는지 확인합니다.
1. 시나리오가 예상대로 작동하는 경우 화면 왼쪽 하단의 **예약** 전환을 클릭하여 **켜기**&#x200B;로 전환합니다.

   이렇게 하면 시나리오가 활성화됩니다. 활성 시나리오는 트리거 모듈에 설정된 일정에 따라 실행됩니다.
1. Workfront Fusion에서 왼쪽 아래 모서리 근처에 있는 **[!UICONTROL 저장]**&#x200B;을 클릭하여 시나리오에 대한 진행 상황을 저장합니다.

   >[!IMPORTANT]
   >
   >원하는 만큼 자주 저장하고 시나리오를 테스트합니다. 시나리오를 트리거하려면 Workfront 계정에서 새 문제를 만들어야 할 수 있습니다.

## 리소스

* [기본 제공 함수를 사용하여 항목 매핑](/help//workfront-fusion/create-scenarios/map-data/map-using-functions.md)
