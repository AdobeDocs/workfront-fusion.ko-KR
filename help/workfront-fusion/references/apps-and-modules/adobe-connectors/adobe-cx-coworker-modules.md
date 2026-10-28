---
title: Adobe CX Enterprise Coworker 모듈
description: Adobe Workfront Fusion의 Adobe CX Enterprise Coworker 커넥터를 사용하여 Coworker에 자연어 프롬프트를 보내고 시나리오에서 해당 응답을 사용합니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 6efe84af0487893a3c33ba2bf6e3db5200f25446
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 6%
---
# Adobe CX Enterprise Coworker 모듈

Adobe Workfront Fusion의 Adobe CX Enterprise Coworker 커넥터를 사용하여 Coworker에 자연어 프롬프트를 보내고 시나리오에서 해당 응답을 사용합니다. 동료는 요청을 해석하고 계정에서 사용할 수 있는 도구를 사용하여 작업을 수행할 수 있습니다.

커넥터는 다음 두 가지 모듈을 제공합니다.

* **[!UICONTROL 프롬프트 실행]**&#x200B;은(는) 새 요청을 시작하고 기본적으로 결과를 기다립니다.
* **[!UICONTROL 실행 상태 가져오기]**&#x200B;에서 이전에 시작한 요청을 확인합니다.

## 액세스 요구 사항

<!-- BECKY CHECK ME: This table is copied from other Fusion connector articles. The source material does not list access requirements, but says you need an Adobe account that has access to Coworker. Confirm the requirements and whether Coworker needs its own license or entitlement. -->

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 전제 조건

Adobe CX Enterprise Coworker에 액세스할 수 있는 Adobe 계정이 있어야 합니다.

## Adobe CX Enterprise Coworker을 Workfront Fusion에 연결

요청에 필요한 Coworker 및 모든 서비스에 액세스할 수 있는 Adobe 계정으로 로그인합니다.

연결을 만들려면 다음 작업을 수행하십시오.

1. Adobe Fusion MCP 모듈에서 **연결** 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">연결 이름</td>
        <td>
          <p>이 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">환경</td>
        <td>
          <p>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">유형</td>
        <td>
          <p>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">클라이언트 ID</td>
        <td>
          <p>이 연결에 대한 선택적 재정의를 입력하거나 매핑합니다. 그렇지 않으면 이 계정 유형의 platform-managed clientId를 사용하십시오. 표시된 Fusion 콜백 URL을 전용 Coworker 계정에 등록합니다.</p>
        </td>
      <tr>
        <td role="rowheader">클라이언트 비밀</td>
        <td>
          <p>이 연결에 대한 선택적 재정의를 입력하거나 매핑합니다. 그렇지 않으면 이 계정 유형의 플랫폼 관리 clientSecret을 사용하십시오. 구성된 IMS 환경에 발급된 자격 증명을 사용합니다.</p>
        </td>
    </tbody>
   </table>

1. **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

로그인하거나 필요한 서비스를 사용할 수 없는 경우 관리자에게 문의하십시오.

## Adobe CX Enterprise Coworker 모듈 및 해당 필드

>[!WARNING]
>
>암호나 다른 자격 증명을 프롬프트에 포함하지 마십시오.

### 실행 상태 가져오기

이 작업 모듈은 **[!UICONTROL 프롬프트 실행]**&#x200B;에 의해 시작된 작업의 현재 상태를 확인합니다.

이 모듈은 작업을 한 번 확인합니다. 작업이 완료될 때까지 새 작업을 시작하거나 계속 확인하지 않습니다. 결과가 아직 보류 중인 경우 나중에 다시 확인하십시오.

>[!NOTE]
>
>작업 ID를 숫자로 변환하거나, 반올림하거나, 형식을 바꾸지 마십시오. Coworker가 작업 ID 없이 원래 프롬프트에 즉시 응답한 경우 상태를 확인할 필요가 없습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 원시 결과 포함] <i>(선택 사항, 고급)</i></td> 
   <td> <p>이 옵션은 기본적으로 꺼져 있습니다. 출력에 전체 Coworker 응답을 포함합니다. 응답에는 중요한 정보가 포함될 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>원래 <b>[!UICONTROL 프롬프트 실행]</b> 실행에서 사용한 것과 동일한 연결을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 작업 ID]</td> 
   <td> <p><b>[!UICONTROL 프롬프트 실행]</b>에서 반환된 작업 ID를 매핑합니다. 반환한 대로 정확히 텍스트로 유지합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 프롬프트 실행

이 작업 모듈은 텍스트 요약 또는 계정에서 사용할 수 있는 도구를 사용한 정보 수집과 같은 지침을 Coworker에 보냅니다.

실행할 때마다 프롬프트가 한 번 전송되고 새 대화가 시작됩니다. AI 모델을 선택하거나 별도의 AI 공급자 키를 제공할 필요가 없습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>동료 연결을 선택합니다. 자세한 내용은 이 문서에서 <a href="#connect-adobe-cx-coworker-to-workfront-fusion" class="MCXref xref">Adobe CX Enterprise Coworker을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 사용자 프롬프트]</td> 
   <td> <p>지침을 입력합니다. 여러 줄을 사용하고 이전 모듈의 정보를 매핑할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 완료 대기] <i>(선택 사항, 고급)</i></td> 
   <td> <p>이 옵션은 기본적으로 켜져 있습니다. 모듈이 작업이 완료되기를 기다리거나 주의가 필요한 경우 이 옵션을 활성화합니다. 초기 결과를 즉시 반환하려면 이 기능을 끕니다.</p><p>자세한 내용은 이 문서에서 <a href="#wait-for-completion">완료 대기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 원시 결과 포함] <i>(선택 사항, 고급)</i></td> 
   <td> <p>이 옵션은 기본적으로 꺼져 있습니다. 모듈에서 출력에 전체 Coworker 응답을 포함하려면 이 옵션을 활성화합니다. 응답에는 중요한 정보가 포함될 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
> 특정 목적을 위해 전체 응답이 필요하지 않은 경우 **[!UICONTROL 원시 결과 포함]**&#x200B;을 해제하는 것이 좋습니다. 원시 결과에는 중요한 정보가 포함될 수 있으며 모든 작업에 대해 보장되는 전체 기록은 아닙니다. 원시 결과를 저장하거나 공유하거나 다른 서비스에 전달하기 전에 원시 결과를 검토하십시오.

#### 완료 대기

**[!UICONTROL 완료 대기]**&#x200B;가 설정되어 있으면 모듈은 5초 대기 후 작업을 확인합니다. 작업이 아직 보류 중인 경우 모듈은 다시 확인하기 전에 5초 더 기다립니다. 각 검사는 응답을 받는 데도 시간이 소요됩니다. 상태를 확인해도 프롬프트가 다시 전송되지 않습니다.

작업이 완료, 실패, 취소 또는 거부되거나 입력 또는 승인이 필요한 경우 대기가 중지됩니다. Coworker가 즉시 답변을 제공하면 모듈은 더 이상 확인하지 않고 답변을 반환합니다.

**[!UICONTROL 완료 대기]**&#x200B;가 해제되면 모듈은 작업이 완료될 때까지 기다리지 않고 첫 번째 결과를 반환합니다. **[!UICONTROL 상태]**, **[!UICONTROL 완료됨]** 및 **[!UICONTROL 다음에 수행할 작업을 결정하려면 주의가 필요함]**&#x200B;을 검사하십시오. 첫 번째 결과가 도착할 때 작업이 이미 완료될 수 있습니다.

대기 중인 경우 Fusion의 모듈 시간 초과가 발생할 수 있습니다. 모듈이 시간 초과되거나 중지되는 경우 Coworker가 계속 작업할 수 있습니다. 이 경우 출력 또는 작업 ID를 받지 못할 수 있습니다.

더 이상 작업하지 않으려면 대기를 끄고 나중에 작업을 확인할 수 있도록 초기 **[!UICONTROL 작업 ID]**&#x200B;를 저장하세요. 시간 초과 후 메시지를 자동으로 다시 실행하지 마십시오. 첫 번째 요청이 이미 진행 중일 수 있으며 이를 반복하면 변경 사항이 중복될 수 있습니다.


## 모듈 출력

두 모듈 모두 오류 없이 완료되면 다음 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 ID]</td> 
   <td> <p>작업을 식별합니다. Coworker가 작업을 생성하지 않고 즉각적인 답변을 제공하는 경우에는 비어 있습니다. 이 값은 <b>[!UICONTROL Get Execution Status]</b>에 사용하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 컨텍스트 ID]</td> 
   <td> <p>대화를 식별합니다. 그것은 대화를 계속하기 위한 입력이 아니다.</p><p>자세한 내용은 이 문서에서 <a href="#use-previous-answers">이전 답변 사용</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상태]</td> 
   <td> <p>현재 작업 상태입니다. 이 문서에서 <a href="#task-states" class="MCXref xref">작업 상태</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 완료]</td> 
   <td> <p>작업이 완료되거나 Coworker에서 즉시 답변을 제공하는 경우 True입니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 주의 사항]</td> 
   <td> <p>Coworker에서 입력 또는 인증이 필요한 경우 True입니다.</p><p>자세한 내용은 이 문서에서 <a href="#requests-that-need-attention">주의가 필요한 요청</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Final Assistant text]</td> 
   <td> <p>작업이 완료되면 최종 답변이 제공됩니다. 작업이 보류 중이거나 주의가 필요한 동안에는 비어 있습니다. 완료된 응답에는 응답 텍스트가 없을 수도 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text artifact (중간 텍스트를 포함할 수 있음)]</td> 
   <td> <p>작업 중 텍스트가 반환되었습니다. 각 항목에는 아티팩트 ID, 이름 및 텍스트가 포함될 수 있습니다. 이 항목들이 반드시 최종적인 답은 아니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 원시 결과(옵트인)]</td> 
   <td> <p>전체 응답입니다. <b>[!UICONTROL 원시 결과 포함]</b>이(가) 켜져 있는 경우에만 포함됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

모든 텍스트 아티팩트를 결합하는 대신 답변에 **[!UICONTROL 최종 길잡이 텍스트]**&#x200B;를 사용하십시오. 가공물에는 진행률 설명 또는 기타 중간 텍스트가 포함될 수 있습니다.

### 주의가 필요한 요청

계속하기 전에 동료에게 추가 정보나 승인이 필요할 수 있습니다. 이 경우 **[!UICONTROL 주의가 필요합니다]**&#x200B;은(는) true이고 **[!UICONTROL 완료됨]**&#x200B;은(는) false입니다. 완료된 작업으로 처리하는 대신 결과를 사람에게 전달합니다.

이러한 모듈은 후속 질문에 답변하거나 귀하를 대신하여 작업을 승인할 수 없습니다. **[!UICONTROL 실행 상태 가져오기]**&#x200B;에서 작업의 상태가 변경되었는지 확인할 수 있지만 입력 또는 권한 부여에 대한 요청이 확인되지 않습니다.

### 이전 답변 사용

**[!UICONTROL 프롬프트 실행]**&#x200B;할 때마다 새 대화가 시작됩니다. 이전 답변을 참조하려면 관련 질문과 답변을 새 프롬프트에 텍스트로 포함하십시오. 이렇게 하면 동료 컨텍스트가 제공되지만 이전 대화는 재개되지 않습니다.

**[!UICONTROL 컨텍스트 ID]**&#x200B;은(는) 결과와 연결된 대화를 식별합니다. 이러한 모듈에 제공하여 대화를 계속할 수 없습니다.

>[!IMPORTANT]
>
>**[!UICONTROL 완료됨]**&#x200B;은(는) 요청한 비즈니스 작업이 성공했음을 보장하지 않습니다. 예를 들어 필요한 도구를 사용할 수 없음을 설명하여 Coworker를 완료할 수 있습니다. 다음 작업을 수행하기 전에 답변을 검토하고 필요한 결과를 확인합니다.

### 작업 상태

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><code>submitted</code>, <code>working</code></td> 
   <td> <p>작업이 보류 중입니다. <b>[!UICONTROL Completed]</b>이(가) false입니다. <b>[!UICONTROL 프롬프트 실행]</b>이(가) 대기 중일 때 계속 대기합니다. 그렇지 않으면 작업 ID를 저장하고 나중에 확인합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>completed</code></td> 
   <td> <p><b>[!UICONTROL Completed]</b>이(가) true입니다. <b>[!UICONTROL 최종 길잡이 텍스트]</b> 및 예상 결과를 검토하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>input-required</code>, <code>auth-required</code></td> 
   <td> <p>이 작업에는 주의가 필요합니다. <b>[!UICONTROL Completed]</b>이(가) false이고 <b>[!UICONTROL Required attention]</b>이(가) true입니다. 대기 중지. 사람 검토를 위해 결과를 보냅니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>failed</code>, <code>canceled</code>, <code>rejected</code></td> 
   <td> <p>정상 결과 대신 모듈에서 오류가 보고됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

모듈이 오류 없이 반환되더라도 보류 중인 결과 또는 주의가 필요한 결과는 성공적으로 완료되지 않습니다.

## 예

### 업데이트 요약

1. **[!UICONTROL 프롬프트 실행]**&#x200B;을(를) 추가하고 연결을 선택합니다.
1. **[!UICONTROL 사용자 프롬프트]** 필드에 다음을 입력하십시오.

   ```text
   Summarize the following project update in three bullet points.
   Use only the supplied text; do not call tools or change any records.
   
   The planning workshop is complete. Two dependencies need confirmation.
   The team will review the delivery estimate on Friday.
   ```

1. **[!UICONTROL 완료 대기]**&#x200B;를 켜고 **[!UICONTROL 원시 결과를 포함]**&#x200B;합니다.
1. **[!UICONTROL 주의가 필요합니다]**&#x200B;이(가) true인 경우 사람이 검토할 수 있도록 결과를 회람하십시오. **[!UICONTROL 완료됨]**&#x200B;이(가) true이면 **[!UICONTROL 최종 길잡이 텍스트]**&#x200B;를 다음 단계에 매핑합니다.

AI가 생성하는 표현은 다양할 수 있습니다. 정확성이 중요한 결과를 검토합니다.

### 나중에 더 긴 작업 확인

1. **[!UICONTROL 프롬프트 실행]**&#x200B;을(를) 추가하고 연결을 선택한 다음 지침을 입력하십시오.
1. **[!UICONTROL 완료 대기]**&#x200B;를 끕니다.
1. 초기 결과를 검사합니다.

   * 작업이 완료되면 결과를 처리합니다.
   * 작업에 주의가 필요한 경우 검토를 위해 결과를 회람합니다.
   * 작업이 보류 중인 경우 **[!UICONTROL 작업 ID]**&#x200B;를 텍스트로 저장하고 사용한 연결을 확인합니다.

1. 나중에 해당 연결 및 작업 ID를 사용하여 **[!UICONTROL 실행 상태 가져오기]**&#x200B;를 사용하십시오.
1. 작업이 아직 보류 중인 경우 시나리오의 제한 내에 다른 검사를 정렬합니다. 완료 시 결과를 한 번 처리하고 주의나 오류를 별도로 처리합니다.

진행 상황을 확인하기 위해 원래 프롬프트를 다시 실행하지 마십시오.

## 사용 고려 사항

* 동료는 도구를 사용하고 레코드 변경을 포함하여 계정에서 허용하는 작업을 수행할 수 있습니다. 적절한 액세스 권한을 가진 신뢰할 수 있는 프롬프트 및 계정을 사용합니다.
* 이러한 모듈은 개별 도구를 제한하는 방법을 제공하지 않습니다. &quot;아무것도 변경하지 마십시오&quot;와 같은 지침은 의도를 설명하지만 강제 읽기 전용 모드가 아닙니다.
* 사용 가능한 도구 및 기술은 계정에 따라 다릅니다. 커넥터는 기술 선택기를 제공하지 않으며 여정 만들기 또는 프로젝트 업데이트와 같은 특정 작업을 보장하지 않습니다. 승인이 필요한 요청은 자동으로 완료된다고 가정하지 마십시오.
* 커넥터가 시작되고 Coworker 요청을 확인합니다. 프로젝트 변경을 모니터링하거나 다른 애플리케이션에 대한 답변을 자동으로 저장하지 않습니다. 필요에 따라 적절한 트리거, 스토리지 및 후속 모듈을 시나리오에 추가합니다.
* AI가 생성한 답변은 불완전하거나 부정확할 수 있습니다. 중요한 결과를 사용하여 변경 또는 결정을 내리기 전에 유효성을 검사하십시오.
* 커넥터는 실패한 요청을 자동으로 다시 시도하지 않습니다. 시나리오의 오류 처리가 결과가 불확실한 프롬프트를 반복하지 않도록 하십시오.

## 문제 해결

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">필수 필드가 누락되었습니다.</td> 
   <td> <p>연결을 선택하고 필요한 프롬프트 또는 작업 ID를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">로그인이 실패하거나 액세스가 거부되었습니다.</td> 
   <td> <p>다시 로그인하고 Adobe 계정이 Coworker 및 필수 서비스에 액세스할 수 있는지 확인합니다. 필요한 경우 관리자에게 문의하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">작업을 찾을 수 없음</td> 
   <td> <p>작업 ID가 변경되지 않았으며 원래 연결을 사용하고 있는지 확인하십시오. 새 작업이 즉시 표시되지 않을 수 있습니다. 나중에 프롬프트를 다시 보내는 대신 상태를 확인하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">상태 확인 실패</td> 
   <td> <p>오류에 허용된 작업 ID가 포함된 경우 <b>[!UICONTROL 실행 상태 가져오기]</b>를 사용하여 해당 작업을 조사하십시오. 프롬프트를 자동으로 다시 시작하지 마십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">프롬프트 실행 시간 초과 또는 응답 누락</td> 
   <td> <p>해당 ID를 받지 못했더라도 작업이 시작되었을 수 있습니다. 중복 작업을 방지하기 위해 요청을 반복하기 전에 조사하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">기다리는 동안 Fusion 시간 초과</td> 
   <td> <p>동료가 아직 작업 중일 수 있습니다. 해당 ID가 있는 경우 작업을 확인합니다. 이후 긴 작업의 경우 대기를 해제하고 먼저 초기 ID를 저장하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">동료 또는 필수 서비스를 사용할 수 없음</td> 
   <td> <p>자격 증명이나 중요한 결과 콘텐츠 없이 표시된 오류를 관리자와 공유합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact module and field labels in the UI (Run a Prompt, Get Execution Status, User prompt, Wait for completion, Include raw result, Task ID, and the output item names). Also confirm that the module is listed under "Adobe CX Enterprise Coworker" in the app picker. -->
