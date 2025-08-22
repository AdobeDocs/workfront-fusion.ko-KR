---
content-type: reference
title: 오류 처리를 위한 지시문
description: 이 문서에서는 Adobe Workfront Fusion 시나리오에서 오류 처리에 사용할 수 있는 지침을 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 15%

---

# 오류 처리를 위한 지시문

오류 처리 지시문을 사용하면 시나리오에 오류가 발생할 때 발생하는 작업을 선택할 수 있습니다.

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
   <td> 새로운 기능: 표준<p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] 라이선스</td> 
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


보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 Workfront 관리자에게 문의하십시오.

Adobe Workfront Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 오류 처리를 위한 지시문

Workfront Fusion에서 사용할 수 있는 오류 처리 지침은 다음과 같습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Rollback</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>시나리오 실행이 즉시 중지됩니다.</li><li>롤백 단계는 모든 모듈을 초기 상태로 되돌리기 위해 모든 모듈에서 시작됩니다. </li><li>후속 모듈은 처리되지 않습니다.</p></li><li> <p>대부분의 경우 시나리오는 시나리오 설정에 지정된 연속 오류 수 이후에 비활성화됩니다. 자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref">연속 오류 수</a>를 참조하십시오.</p> </li><li><p>시나리오 실행 상태가 "오류"로 표시됩니다.</p></li></ul> <p><b>참고</b>: 모듈에 오류 처리기 경로가 연결되어 있지 않고 [!UICONTROL 시나리오 설정] 아래에 있는 <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref">불완전 실행 저장 허용</a>불완전 실행 저장 허용 설정이 선택되어 있지 않은 경우 기본 동작입니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>커밋</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>시나리오 실행이 즉시 중지됩니다.</li><li>모든 모듈에서 커밋 단계가 시작됩니다. </li><li>후속 모듈은 처리되지 않습니다.</p></li><li> <p>처리되지 않은 모든 번들은 무시됩니다.</p> </li><li><p>시나리오 실행 상태는 “성공”으로 표시됩니다. </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Resume</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>대체 출력이 지정되어 오류가 발생한 모듈에 제공됩니다.</p> </li><li><p>이후 모듈이 처리됩니다.</p></li><li> <p>시나리오 실행 상태는 “성공”으로 표시됩니다.</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>무시</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>오류가 무시됩니다.</li><li> 후속 모듈은 처리되지 않습니다.</p> </li><li><p>처리되지 않은 번들이 있으면 시나리오 실행이 정상적으로 계속됩니다.</p> </li><li><p>시나리오 실행 상태는 “성공”으로 표시됩니다.</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Break</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>시나리오 실행 상태가 오류를 수동으로 해결할 수 있는 불완전한 실행 대기열에 저장됩니다. 자세한 내용은 <a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">불완전한 실행 보기 및 해결</a>을 참조하십시오.</p> <p>그러나 몇 가지 예외가 있습니다. 자세한 내용은 시나리오 설정 구성 문서에서 <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref">불완전한 실행 저장 허용</a>을 참조하십시오</a>.</p></li><li> <p>후속 모듈은 처리되지 않습니다.</p></li><li> <p>처리되지 않은 번들이 있으면 시나리오 실행이 정상적으로 계속됩니다.</p> </li><li><p>[!UICONTROL 자동으로 실행 완료] 옵션을 비활성화하면 시나리오 실행 상태가 "경고"로 표시됩니다.</p></li></ul> <p>자세한 내용은 이 문서의 <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> 섹션을 참조하십시오</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>다시 시도</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>경우에 따라 실패 원인이 시간이 지남에 따라 전달될 가능성이 있는 경우 실패한 모듈을 다시 실행하는 것이 유용할 수 있습니다.</p> <p>Workfront Fusion은 현재 Retry 지시문을 제공하지 않지만 몇 가지 해결 방법을 사용하여 해당 기능을 모방할 수 있습니다. 자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref">오류 처리 다시 시도</a>를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* 오류 처리 지시문은 오류 처리 경로 외부에서 사용할 수 없습니다.
>* Workfront Fusion은 현재 해당 기능을 모방하도록 해결 방법을 사용할 수 있지만 오류를 쉽게 생성(throw)할 수 있는 Throw 모듈을 제공하지 않습니다.
>
>  자세한 내용은 [구성 `throw` 오류 해결 방법](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md)을 참조하세요.

## 리소스

* 롤백 및 롤백 단계에 대한 자세한 내용은 시나리오 실행, 주기 및 단계 문서에서 [롤백](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback)을 참조하십시오.
* 커밋 단계에 대한 자세한 내용은 시나리오 실행, 주기 및 단계 문서에서 [커밋](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit)을 참조하십시오.
