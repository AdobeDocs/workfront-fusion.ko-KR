---
title: Adobe Marketo Engage 모듈
description: Adobe Marketo Engage MCP 모듈을 사용하면 자연어 프롬프트를 Adobe Marketo Engage의 MCP(Model Context Protocol) 서버로 보낼 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: e14a7f57-c82c-4874-a495-5d036cbbdc3d
    internal-label: Resource management
subfeature_v2:
  - id: b70a979b-965d-47a9-a360-e7ec2a19b8c1
    internal-label: Digital content and documents
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 9e08c421a53c7ca499715fa8e32be6c10fbde1d9
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 9%
---
# Adobe Marketo Engage 모듈

Adobe Marketo Engage MCP 모듈을 사용하면 AI 모델을 사용하여 자연어 프롬프트를 Adobe Marketo Engage의 MCP(Model Context Protocol) 서버로 전송하여 요청을 해석하고 Marketo의 자체 도구를 호출하여 이를 이행할 수 있습니다. 각 모듈이 &quot;리드 만들기&quot;와 같은 하나의 고정 작업을 수행하는 기존 Marketo 커넥터와 달리 이 커넥터에는 일반 영어로 개방형 지침을 수락하고 AI가 이를 충족하는 데 필요한 Marketo 작업을 결정할 수 있도록 하는 단일 모듈이 있습니다.

이 커넥터는 특히 Marketo Engage 자체 MCP 서버용입니다

다른 응용 프로그램의 MCP에 연결하려면 [시나리오에 AI 프롬프트 추가](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md)를 참조하십시오.

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
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>운영 기반: 운영 기반 라이센스가 있는 조직에서 사용 가능</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

* Adobe Marketo Engage 계정과 유효한 Marketo 인스턴스가 있어야 합니다.

## Adobe Marketo Engage MCP를 Workfront Fusion에 연결 {#connect-adobe-marketo-engage-mcp-to-workfront-fusion}

Adobe Marketo Engage MCP 모듈 내에서 직접 Marketo 인스턴스에 대한 연결을 만들 수 있습니다.

1. Adobe Marketo Engage MCP 모듈에서 **연결** 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새로운 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>
          <p>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>
          <p>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>
          <p>Marketo LaunchPoint에서 만든 대로 Marketo REST API 서비스에 대한 클라이언트 ID를 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>
          <p>Marketo LaunchPoint에서 만든 대로 Marketo REST API 서비스에 대한 클라이언트 암호를 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Munchkin ID]</td>
        <td>
          <p>Marketo 인스턴스의 Munchkin ID를 입력합니다(예: '123-ABC-456'). Munchkin ID는 Marketo의 <b>관리자 → Munchkin</b>에 표시됩니다.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. 연결을 만들고 모듈로 돌아가려면 **계속**&#x200B;을 클릭하세요.

>[!IMPORTANT]
>
> * 관리자 계정을 다시 사용하는 대신 시나리오에 필요한 최소 역할 및 권한으로 전용 API 전용 Marketo 사용자를 사용하십시오.
> * 연결을 만들어도 자격 증명의 유효성을 확인할 수 없습니다. Fusion은 테스트 호출 없이 연결을 저장하므로 값이 잘못되거나 잘못 입력되더라도 연결이 성공적으로 생성된 것처럼 보일 수 있습니다. 자격 증명이 잘못된 경우, 일반적으로 모듈이 처음 Marketo에 연결하려고 하거나 도구 목록이 로드되지 않으면 나중에 오류가 표시됩니다.

## 모듈: &quot;사용자 프롬프트 처리&quot;

이는 커넥터가 제공하는 유일한 모듈입니다. 시나리오는 다음을 제공하여 사용합니다.

1. **연결** — 위에서 만든 Marketo 연결입니다.
2. **프롬프트 입력** — 지침, 일반 영어(예: &quot;지난 주에 봄 웨비나 목록에 추가된 모든 리드를 찾고 회사 이름이 설정되지 않은 리드를 알려 주십시오.&quot;)
3. **도구**(선택 사항) — 아래에 설명되어 있습니다. 이러한 필드는 연결을 선택한 경우에만 나타납니다.
4. **LLM 키**(선택 사항, 고급) — 아래에 설명되어 있습니다.

AI의 최종 답변을 텍스트로 반환하고, 해당 답변을 제작하는 동안 발생한 일에 대한 전체 감사 추적을 반환합니다.

## Adobe Marketo Engage MCP 모듈 및 해당 필드

### 사용자 프롬프트 처리

이 액션 모듈은 Adobe Marketo Engage의 MCP 서버에 영어 일반 지침을 보내고 AI의 응답을 반환합니다.

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">LLM 키 <i>(선택 사항, 고급)</i></td>
   <td><p>기본적으로 이 모듈은 Adobe의 자체 AI 서비스를 사용하여 프롬프트를 처리하며 키를 선택할 필요가 없습니다.</p><p>대신 자체 AI 공급자를 사용하려면 기존 LLM 키를 선택하거나 <b>추가</b>를 클릭하고 다음 정보를 입력하여 새 키를 만드십시오.</p>
    <ul>
     <li><b>키 이름</b>: 새 키의 이름을 입력하십시오.</li>
     <li><b>LLM</b>: 이 키와 연결된 큰 언어 모델을 선택하십시오. 지원되는 제공업체는 OpenAI, Anthropic Claude, Amazon Bedrock입니다.</li>
     <li><b>키</b>: 선택한 공급자에 대한 API 키를 입력하거나 매핑합니다.</li>
     <li><b>모델</b>: 키에 사용할 LLM 모델을 선택하십시오.</li>
     <li><b>기타 필드</b>: LLM에 필요한 다른 필드의 값을 입력하십시오.</li>
    </ul>
   </td>
  </tr>
  <tr>
   <td role="rowheader">연결</td>
   <td><p>Marketo 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-adobe-marketo-engage-mcp-to-workfront-fusion" class="MCXref xref">Adobe Marketo Engage MCP를 Workfront Fusion에 연결</a>을 참조하십시오.</p></td>
  </tr>
  <tr>
   <td role="rowheader">사용자 프롬프트</td>
   <td><p>AI가 수행할 지침을 일반 영어로 입력하거나 매핑합니다.</p><p>예: <i>지난 7일 동안 봄 웨비나 목록에 추가된 모든 리드를 찾아 가장 일반적인 산업을 요약합니다.</i></p></td>
  </tr>
 </tbody>
</table>

### 모듈 출력

출력은 다음을 포함하는 단일 번들입니다.

* 응답: AI의 최종 답변입니다(텍스트). 이 데이터를 후속 모듈에 매핑할 수 있습니다.
* 감사 추적: 세션 ID, 원래 프롬프트, 시작 및 종료 시간, 총 기간, 전체 상태, 최종 응답 및 도구 호출 목록을 포함한 실행에 대한 세부 레코드입니다. 각 도구 호출 항목 은 실행된 Marketo 도구, 해당 인수, 출력, 시작 및 종료 시간과 기간, 성공 여부, 시퀀스 순서 등을 기록합니다.
* 요약: 총 도구 호출, 성공한 호출, 실패한 호출, 처리 시간 및 상태 계산에 압축된 동일한 실행입니다.

### AI 모델

기본적으로 모듈은 입력할 키 또는 자격 증명이 없이 Adobe의 자체 관리 AI 서비스를 자동으로 사용합니다.

조직에 이러한 계정 중 하나가 있는 경우 대신 특정 LLM 키를 선택하여 OpenAI, Anthropic Claude 또는 Amazon Bedrock을 사용할 수 있습니다.

### AI가 취할 수 있는 Marketo 작업 선택

연결을 선택하면 모듈은 Marketo MCP 서버에 어떤 도구를 제공하는지 질문하고 각 도구에는 몇 개의 도구가 포함되어 있는지를 보여 주는 다중 선택 목록으로 표시합니다.

* 읽기 전용 도구: 잠재 고객 찾기, 캠페인 멤버 나열 또는 프로그램 세부 정보 읽기와 같이 상승만 하고 아무것도 변경하지 않는 작업입니다.
* 쓰기/삭제 도구: 잠재 고객 만들기 또는 업데이트, 목록에 사용자 추가, 캠페인 활성화 또는 이메일 승인 또는 전송과 같이 변경 작업을 수행하는 작업입니다.
* 기타 도구: Marketo 서버가 읽기 전용 또는 비전용 레이블이 지정되지 않은 도구를 제공하는 경우에만 표시되는 세 번째 목록입니다. 이는 안전하거나 안전하지 않은 것으로 간주되기 보다는 별도로 표시됩니다. 서버에서 모든 레이블을 지정하는 경우 이 목록이 표시되지 않습니다.

도구를 선택하지 않으면 AI가 모든 도구를 사용할 수 있습니다. 특정 작업으로 목록을 제한할 수 있습니다. 예를 들어 &#39;읽기 전용&#39;은 그대로 두고 구체적인 &#39;쓰기&#39; 동작 2개만 선택하면 AI가 필요한 것은 무엇이든 자유롭게 조회할 수 있지만 그런 2가지 특정 변화만 가능해진다. 목록을 비워 두면 해당 카테고리의 모든 작업이 허용됩니다. AI를 제한하려면 해당 범주에서 허용할 특정 작업을 적극적으로 선택해야 합니다. 이렇게 하면 AI가 라이브 마케팅 데이터에 대해 예상치 못한 파괴적인 조치를 취하지 않도록 하면서도 자유롭게 정보를 수집할 수 있습니다.

목록은 Marketo 서버에서 실시간으로 읽히므로, Adobe이 해당 서버를 업데이트할 때 표시되는 정확한 도구가 변경될 수 있습니다.

### 지속적인 대화 기록 없음

이 모듈의 각 실행은 독립적인 단일 실행입니다. AI가 후속 질문을 할 수 없고 답변을 기다릴 수 없다. 대신 최선의 판단을 내려야 한다. 한 번의 시험으로 완결된 해답을 내놓아야 한다. 요청이 애매할 경우 AI는 합리적인 가정을 하고 그 가정을 답의 일부로 기술하고 진행하게 된다. 한 번 실행 내에 회신을 받을 수 있는 방법이 없기 때문에 중단되지 않고 사용자에게 명확하게 요청합니다.

또한 Marketo 데이터가 이전 실행 이후 변경될 수 있으므로 AI는 메모리에 의존하지 않고 도구 호출로 사실을 확인하라는 지침을 받습니다.

AI는 프롬프트가 실제로 작업을 요청한 경우에만 쓰기, 업데이트 또는 삭제 작업을 수행합니다. 이 서비스는 사용자가 요청한 다른 작업을 수행하는 동일한 실행에서도 캠페인 활성화 또는 비활성화, 리드 및 목록 만들기 또는 삭제, 이메일 승인 또는 전송 등 요청되지 않은 작업을 수행하지 않습니다.

각 실행은 독립적이기 때문에 AI는 스스로 이전 실행에 대한 메모리가 없습니다. 다중 전환 채팅 같은 경험을 원하는 시나리오는 이전 질문과 대답을 Fusion의 데이터 저장소에 저장하거나 모듈 간에 전달하는 것과 같이 새 프롬프트의 시작 시 텍스트로 포함시킨 후 새 질문에 답하는 것과 같이 새 프롬프트의 일부로 해당 기록을 명시적으로 제공해야 합니다. 이전 실행을 자동으로 기억하는 세션이나 대화 ID는 없습니다.

## 프롬프트 예

다음과 같은 프롬프트를 사용할 수 있습니다.

* *지난 7일 동안 &#39;Q3 제품 출시&#39; 프로그램에 참여한 잠재 고객을 나열하고 해당 기업이 속한 업종을 요약합니다.*
* *시작 시리즈 스마트 캠페인이 현재 활성 상태인지 확인하고, 참여 인원을 알려주세요.*
* *가격 책정 페이지에서 사용할 양식을 찾아 필수 필드로 표시된 필드를 알려주십시오.*
* *전자 메일이 `jane@example.com`인 잠재 고객을 &#39;VIP 고객&#39; 정적 목록에 추가합니다.*
* *봄 뉴스레터 프로그램에 있는 모든 전자 메일의 성능을 요약합니다.*

<!--

## What a content writer should NOT claim

* Connection form: Do not describe the connection as an OAuth or "sign in with Adobe" flow. It is not one. It is three credential fields that the user copies out of Marketo's LaunchPoint and Munchkin admin pages. Screenshots or steps borrowed from the AEM MCP connector docs would be wrong here.
* Credential validation: Do not imply that the connection form validates the credentials. It saves them without testing them.
* Module scope: This is not a substitute for individual Marketo action modules. It is a single, flexible AI-driven module, not a set of deterministic single-purpose modules.
* Reliability: Results are AI-generated and can occasionally be imperfect, even with every safeguard above in place. This is appropriate for automation where a human is not reviewing every single run in real time, but it is not a guarantee of 100% deterministic behavior the way a traditional Marketo module is. This deserves extra emphasis for Marketo specifically, because a write action here can email real customers or alter real lead records.
* Tool restrictions: The read/write tool split limits what categories of Marketo actions the AI can take. It is not a way to sandbox or limit what the AI is capable of reasoning about or discussing in its answer text.
* Tool naming: Do not name specific Marketo MCP tools or actions unless they are verified against the live tool list. This document intentionally describes capability areas, such as leads, lists, campaigns, programs, emails, forms, snippets, and bulk operations, rather than exact tool names, since the server's exact tool set may evolve.
* API limits: Do not state Marketo API rate limits, quotas, or daily call caps as if this connector defines them. Any such limit comes from the user's own Marketo subscription and REST API allowance; verify with the Marketo team before publishing numbers.

## Reference links used while compiling this

* Adobe Marketo Engage MCP server (developer documentation):
  https://experienceleague.adobe.com/ko/docs/marketo-developer/marketo/mcp-server

  -->
