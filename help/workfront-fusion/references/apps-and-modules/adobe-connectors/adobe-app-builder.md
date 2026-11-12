---
title: Adobe App Builder 모듈
description: Adobe App Builder 커넥터를 사용하면 시나리오에서 사용자 정의 함수를 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 02c396f33b6398635462bac8741f446eb82bf5a9
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 16%
---
# Adobe App Builder 모듈

Fusion의 [함수] 영역에서 사용자 정의 함수를 만들 수 있습니다. 그런 다음 이러한 함수를 Adobe App Builder 모듈 형태로 시나리오에 추가합니다.

사용자 지정 기능은 Adobe App Builder을 통해 작동하므로 이를 사용하려면 조직에 Adobe App Builder 라이선스가 있어야 합니다.

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

## Adobe App Builder에 대한 연결 만들기

연결은 App Builder 프로젝트 작업 영역의 Adobe I/O Runtime 자격 증명을 사용합니다. 연결을 만들기 전에 Adobe Developer Console에서 이러한 자격 증명을 가져옵니다.

### 런타임 자격 증명 가져오기

1. App Builder 라이선스가 있는 조직을 사용하여 [Adobe Developer Console](https://developer.adobe.com/console)에 로그인합니다.
1. 함수가 포함된 App Builder 프로젝트를 연 다음 연결할 작업 영역(예: **프로덕션**)을 선택합니다.
1. 작업 영역 구성 JSON 파일을 다운로드하려면 오른쪽 상단의 **모두 다운로드**&#x200B;를 클릭하십시오.
1. 파일을 열고 `runtime` 섹션을 찾습니다. 이 파일에는 다음이 포함되어 있습니다.

   * `namespace`: **네임스페이스** 필드에 입력할 값
   * `auth`: `username:password` 형식의 값입니다. 콜론 앞 부분은 **사용자 이름**&#x200B;이고 콜론 뒤 부분은 **암호**&#x200B;입니다.

   >[!NOTE]
   >
   >Adobe I/O CLI에서 `aio runtime namespace get` 또는 `aio app use`을(를) 실행하여 네임스페이스 및 인증 값을 찾을 수도 있습니다.

### 연결 만들기

1. 모듈에서 **연결** 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL 연결 이름]</td> 
      <td>이 연결의 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 환경]</td> 
      <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 유형]</td> 
      <td><b>서비스 계정</b>을 선택하세요.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 사용자 이름]</td> 
      <td>작업 영역의 <code>auth</code> 값(콜론 앞 부분)에서 사용자 이름을 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 암호]</td> 
      <td>작업 영역의 <code>auth</code> 값(콜론 뒤 부분)에서 암호를 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Namespace]</td> 
      <td>작업 영역 구성 파일의 <code>runtime</code> 섹션에서 <code>namespace</code> 값을 입력합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 저장하려면 **계속**&#x200B;을 클릭하세요.

## Adobe App Builder 모듈

### 사용자 지정 코드 블록 실행

이 모듈에서는 코드 블록을 실행할 수 있습니다. 코드 블록은 모듈을 설정할 때 구성되며 시나리오 실행 중에 모듈이 실행될 때 실행됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td>
   <td>실행할 사용자 지정 함수가 포함된 연결을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 코드 블록]</td> 
   <td>모듈을 실행할 코드 블록을 입력합니다.<p>읽기 쉽도록 코드 서식을 지정하려면 <b>코드 서식</b> 아이콘을 클릭합니다.</td> 
  </tr> 
   </tbody> 
</table>

### 패키지에서 사용자 지정 함수 실행

이 모듈은 패키지에서 함수를 실행합니다.

패키지에 대한 자세한 내용은 [사용자 지정 기능 패키지 사용](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md)을 참조하세요.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td>
   <td>실행할 사용자 지정 함수가 포함된 연결을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지]</td> 
   <td>시나리오에서 실행할 함수가 포함된 패키지를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변수] </td> 
   <td>시나리오에서 실행할 함수를 선택합니다.</p></td> 
  </tr> 
   </tbody> 
</table>

### 패키지의 변수 사용

이 모듈은 패키지에 구성된 변수를 시나리오로 가져옵니다.

패키지에 대한 자세한 내용은 [사용자 지정 기능 패키지 사용](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md)을 참조하세요.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td>
   <td>실행할 사용자 지정 함수가 포함된 연결을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지]</td> 
   <td>시나리오로 가져올 변수가 포함된 패키지를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변수] </td> 
   <td>시나리오에 가져올 변수를 선택합니다.</p></td> 
  </tr> 
   </tbody> 
</table>

### 사용자 지정 함수 또는 코드 블록 실행

이 모듈에서는 함수 영역에 저장된 이전에 구성한 사용자 지정 JavaScript 함수를 사용할 수 있습니다.

사용자 지정 함수 구성에 대한 지침은 [사용자 지정 함수를 사용하여 데이터 매핑](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md)을 참조하십시오.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td>
   <td>실행할 사용자 지정 함수가 포함된 연결을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 액션]</td> 
   <td>실행할 사용자 지정 함수를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 매개 변수] </td> 
   <td>함수 매개 변수에 대한 값을 입력합니다. 사용 가능한 매개 변수는 함수를 만들 때 구성된 매개 변수를 기반으로 합니다.<p>매개 변수에 기본값이 있으면 이 값이 필드에 표시되지 않지만 필드에 값을 입력하거나 매핑하여 재정의할 수 있습니다.</p></td> 
  </tr> 
   </tbody> 
</table>


