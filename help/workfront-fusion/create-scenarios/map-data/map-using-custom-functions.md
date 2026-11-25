---
title: 사용자 정의 함수를 사용하여 데이터 매핑
description: 항목을 매핑할 때 함수를 사용하여 간단하거나 복잡한 공식을 만들 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: dc4e697a-a65c-48bc-99de-8e26fbeb7ba7
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: c716296d771974ffdb59e916f9865c9efb2ad5a9
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 11%
---
# 사용자 정의 함수를 사용하여 데이터 매핑

Fusion의 [함수] 영역에서 사용자 정의 함수를 만들 수 있습니다. 그런 다음 이러한 함수를 Adobe App Builder 모듈 형태로 시나리오에 추가합니다.

사용자 지정 기능은 Adobe App Builder을 통해 작동하므로 이를 사용하려면 조직에 Adobe App Builder 라이선스가 있어야 합니다.

대부분의 시나리오 요소와 같은 사용자 지정 함수는 팀에서 소유합니다.

함수는 간단한 JavaScript 함수입니다. 함수 논리에 변수 또는 종속성을 포함하려면 패키지를 사용하십시오.

패키지에 대한 자세한 내용은 [사용자 지정 기능 패키지 사용](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md)을 참조하세요.

Workfront Fusion에는 간단하거나 복잡한 공식을 만들 수 있는 기본 제공 함수도 포함되어 있습니다. 이러한 함수는 배열, 문자열, 숫자 및 이전 모듈의 데이터를 비롯한 다양한 사용 사례를 다룹니다.

기본 제공 함수에 대한 자세한 내용과 지침은 [기본 제공 함수를 사용하여 항목 매핑](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md)을 참조하세요.

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
   <p><ul><li>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li><li>사용자 지정 기능을 사용하려면 Adobe App Builder 라이선스가 있어야 합니다.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 사용자 지정 기능 구성

여러 시나리오에서 사용할 수 있는 함수 영역에서 사용자 정의 함수를 생성하거나 개별 시나리오 내에서 사용자 정의 함수를 구성할 수 있습니다.

* [여러 시나리오에서 사용할 사용자 지정 함수 만들기](#create-a-custom-function-to-use-in-multiple-scenarios)
* [시나리오 내에 사용자 지정 함수 만들기](#create-a-custom-function-within-a-scenario)

### 여러 시나리오에서 사용할 사용자 지정 함수 만들기

여러 시나리오에서 사용할 수 있는 사용자 정의 함수는 Workfront Fusion의 함수 영역에서 구성합니다. 함수가 구성된 후 Adobe App Builder 커넥터를 사용하여 시나리오에 해당 함수를 추가할 수 있습니다.

* [런타임 환경 초기화](#initialize-your-runtime-environment)
* [기존 App Builder 프로젝트 연결](#connect-an-existing-app-builder-project)
* [함수 영역에서 사용자 지정 함수 만들기](#create-a-custom-function-in-the-functions-area)

#### 런타임 환경 초기화

사용자 지정 함수를 만들려면 먼저 런타임 환경을 초기화해야 합니다. 팀에 사용자 정의 기능이 없는 경우에만 수행해야 합니다.

>[!IMPORTANT]
>
>Adobe App Builder에 대한 액세스 권한이 있는 사용자, IMS 조직 내의 개발자 또는 시스템 관리자만 초기화를 수행할 수 있습니다.
>
>초기화가 완료되면 초기화가 수행된 팀의 모든 사용자가 함수를 만들고 사용할 수 있습니다.

1. 왼쪽 패널에서 **함수** ![함수 아이콘](assets/functions-icon.png) 탭을 클릭합니다.

   런타임을 아직 구성하지 않은 경우 &quot;런타임 환경이 구성되지 않았습니다.&quot;라는 메시지가 표시됩니다.
1. **런타임 초기화**&#x200B;를 클릭합니다.

   잠시 후 두 개의 샘플 함수가 있는 함수 목록이 나타납니다.

#### 기존 App Builder 프로젝트 연결

Fusion은 App Builder 프로젝트를 만들 때 런타임 설정을 처리합니다. Fusion을 사용하기 전에 만들어진 App Builder 프로젝트가 이미 팀에 있는 경우 해당 프로젝트의 런타임 네임스페이스와 자격 증명을 사용하는 App Builder 연결을 만들어 수동으로 연결해야 합니다. 프로젝트를 다시 만들 필요는 없습니다.

>[!NOTE]
>
>Fusion에 입력하는 자격 증명은 런타임 자격 증명입니다. Adobe 로그인 세부 정보가 아닙니다. 다운로드한 구성 파일을 안전하게 유지하고 해당 `auth` 값을 공유하지 마십시오.

1. Fusion에서 연결이 필요한 팀을 선택합니다.
1. 왼쪽 패널에서 **연결** 탭을 클릭한 다음 **연결 만들기**&#x200B;를 클릭합니다.
1. 연결 유형으로 **Adobe App Builder**&#x200B;을(를) 선택하고 기존 프로젝트를 식별하는 이름을 입력하십시오.
1. [Adobe Developer Console](https://developer.adobe.com/console)에서 기존 프로젝트를 연 다음 연결할 작업 영역을 선택합니다.
1. 프로젝트 개요에서 **모두 다운로드**&#x200B;를 클릭하여 작업 영역 구성 JSON 파일을 다운로드하고 텍스트 편집기에서 파일을 엽니다.
1. 파일의 `runtime` 섹션에서 `namespace` 값을 찾습니다. Fusion에서 **네임스페이스** 필드에 값을 입력합니다.
1. `runtime` 섹션에서 `auth` 값을 찾습니다. 형식은 `username:password`입니다.

   * Fusion에서 **사용자 이름** 필드에 콜론 앞에 부분을 입력합니다.
   * Fusion에서 **암호** 필드에 콜론 뒤에 부분을 입력합니다.

1. 연결을 저장하려면 **계속**&#x200B;을 클릭하세요.
1. Fusion의 **함수** 탭으로 돌아가서 필요한 경우 페이지를 새로 고칩니다.

연결 필드에 대한 자세한 내용은 [Adobe App Builder 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md#create-a-connection-to-adobe-app-builder)을 참조하세요.

#### 함수 영역에서 사용자 지정 함수 만들기

런타임 환경이 구성된 후 사용자 정의 함수를 만들 수 있습니다.

>[!IMPORTANT]
>
>* 사용자 지정 함수 **은(는) JavaScript 함수여야 합니다**.
>* 사용자 지정 함수 **must**&#x200B;이(가) 개체를 반환합니다.
>* 사용자 지정 함수를 만든 후에는 다음 작업을 수행할 수 없습니다.
>
>   * 이름 변경
>   * 기본 매개 변수 값 보기

1. 왼쪽 패널에서 **함수** ![함수 아이콘](assets/functions-icon.png) 탭을 클릭합니다.
1. **함수 추가**&#x200B;를 클릭합니다.
1. 사용자 지정 함수의 이름을 입력합니다.

   나중에 이 이름을 변경할 수 없습니다.
1. 함수의 코드를 입력합니다.
1. 추가할 각 기본 매개 변수 값에 대해 **매개 변수 추가**&#x200B;를 클릭하고 매개 변수 이름과 기본값을 입력하십시오.

   시나리오에 함수를 추가할 때 기본 매개 변수를 재정의할 수 있습니다.
1. **저장**&#x200B;을 클릭합니다

### 시나리오 내에 사용자 지정 함수 만들기

시나리오 내에서 사용자 지정 함수를 만들려면 Adobe App Builder 커넥터의 **사용자 지정 코드 블록 실행** 모듈을 사용하십시오.

자세한 지침은 [Adobe App Builder 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md)을 참조하세요.

## 시나리오에 사용자 지정 함수 추가

시나리오에 사용자 지정 함수를 추가하려면 Adobe App Builder 커넥터를 사용하십시오.

자세한 지침은 [Adobe App Builder 모듈](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md)을 참조하세요.

