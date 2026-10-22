---
title: Adobe Fusion MCP 모듈
description: Adobe Fusion MCP 모듈을 사용하면 Adobe Fusion의 MCP 서버에 영어 일반 프롬프트를 보내고 AI 모델이 요청을 수행하도록 할 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 06ba1c54288fff09f866bffa5c3fce7381c71ad2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 14%
---
# Adobe Fusion MCP 모듈

Adobe Fusion MCP 커넥터는 하나의 일반 영어 프롬프트를 Adobe Fusion Model Context Protocol(MCP) 서버에 보냅니다. AI 모델은 요청을 해석하고 완료하는 데 필요한 Fusion 도구를 호출합니다.

커넥터는 호스팅되는 Adobe Fusion MCP 서버에서만 작동합니다. 다른 MCP 서버를 지정할 수 없습니다.

Fusion 시나리오의 MCP에 대한 자세한 내용은 [시나리오에 AI 프롬프트 추가](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md)를 참조하십시오.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## Adobe Fusion MCP를 Workfront Fusion에 연결

Adobe Fusion MCP 모듈 내에서 직접 연결을 만들 수 있습니다.

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
    </tbody>
   </table>

1. **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

Adobe의 로그인 페이지로 리디렉션됩니다. Adobe 계정으로 로그인하고 액세스를 승인합니다. Workfront Fusion으로 다시 리디렉션되고 새 연결은 모듈에서 사용할 수 있습니다.

## Adobe Fusion MCP 모듈 및 해당 필드

### 사용자 프롬프트 처리

이 작업 모듈은 영어 일반 프롬프트를 Adobe Fusion MCP 서버로 보냅니다. AI 모델은 프롬프트를 해석하고 완료에 필요한 Fusion 도구를 호출한 다음 결과를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM 키 <i>(선택 사항, 고급)</i></td> 
   <td> <p>기본적으로 이 모듈은 Adobe Managed AI를 사용하여 프롬프트를 처리하며 키를 선택할 필요가 없습니다.</p> <p>대신 자체 AI 공급자를 사용하려면 기존 LLM 키를 선택하거나 <b>추가</b>를 클릭하고 다음 정보를 입력하여 새 키를 만드십시오.</p>
     <ul>
       <li><b>키 이름</b>: 새 키의 이름을 입력하십시오.</li>
       <li><b>LLM</b>: 이 키와 연결된 큰 언어 모델을 선택하십시오. 지원되는 공급자는 OpenAI, Anthropic 및 Amazon Bedrock입니다.</li>
       <li><b>키</b>: 선택한 공급자에 대한 API 키를 입력하거나 매핑합니다.</li>
       <li><b>모델</b>: 키에 사용할 LLM 모델을 선택하십시오.</li>
       <li><b>기타 필드</b>: LLM에 필요한 다른 필드의 값을 입력하십시오.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Adobe Fusion MCP를 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-adobe-fusion-mcp-to-workfront-fusion" class="MCXref xref">Adobe Fusion MCP를 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>읽기 전용 도구 <i>(선택 사항)</i></td> 
   <td> <p>특정 읽기 전용 도구를 선택하여 AI를 제한합니다. 선택하지 않으면 이 범주의 모든 읽기 전용 도구가 허용됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>쓰기/삭제 도구 <i>(선택 사항)</i></td> 
   <td> <p>특정 쓰기 또는 삭제 도구를 선택하여 AI를 제한합니다. 선택하지 않으면 이 범주의 모든 쓰기 및 삭제 도구가 허용됩니다.</p> <p>무인 시나리오가 파괴적인 작업을 수행하지 않도록 하려면 이 필드를 제한 없이 두지 않고 의도적으로 빈 선택 항목으로 설정하는 것이 좋습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>프롬프트 입력</td> 
   <td> <p>AI가 수행할 지침을 일반 영어로 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### AI가 호출할 수 있는 도구 제한

읽기 전용 도구 및 쓰기/삭제 도구 필드에서 도구를 선택하여 AI가 호출할 수 있는 Fusion 도구를 제한할 수 있습니다.

* 필드를 비워 두면 AI가 해당 카테고리의 모든 도구를 호출할 수 있습니다.
* 두 필드를 모두 비워 두면 AI가 Fusion MCP 서버의 모든 도구를 호출할 수 있습니다.

무인 시나리오가 쓰기 또는 삭제 작업을 수행하지 않도록 하려면 읽기 전용 도구 필드에서 허용할 도구만 선택하고 쓰기/삭제 도구 필드에서 AI 호출에 익숙한 하나 이상의 도구를 선택합니다.

목록에 있는 도구 이름은 Fusion MCP 서버에서 가져옵니다.

#### 모듈에서 프롬프트를 처리하는 방법

* 모듈에 후속 전환이 없습니다. 프롬프트가 명확하지 않을 경우 AI가 합리적인 가정을 하고 질문을 하지 않고 응답에 명시합니다.
* AI는 도구를 사용하여 변경 가능한 정보를 확인합니다.
* AI는 프롬프트가 요청하는 것 외에는 어떠한 쓰기 또는 삭제 작업도 수행하지 않습니다.
* 모듈에 유효한 연결이 필요합니다. 그거 없이는 안되요.

#### 출력

모듈은 시나리오에서 후속 모듈에 매핑할 수 있는 다음 정보를 반환합니다.

* **응답**: AI의 최종 답변입니다(텍스트).
* **감사 추적**: 호출된 도구, 해당 인수 및 결과, 시간이 포함된 세션의 레코드입니다.
* **요약**: 성공한 도구 호출 수와 최종 상태를 포함한 세션의 합계입니다.
