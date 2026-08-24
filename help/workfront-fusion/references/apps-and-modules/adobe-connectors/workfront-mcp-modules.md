---
title: Adobe Workfront Mcp 모듈
description: Adobe Workfront MCP 모듈을 사용하면 Adobe Workfront의 MCP 서버에 일반 영어 프롬프트를 보내고 AI 모델이 요청을 수행하도록 할 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 88515edc81bafe2d1a81df627fd51dd4ed674c02
workflow-type: tm+mt
source-wordcount: 884
ht-degree: 16%

---

# Adobe Workfront Mcp 모듈

Adobe Workfront MCP 커넥터는 Adobe Workfront의 자체 MCP(Model Context Protocol) 서버를 위한 전용 Fusion 통합입니다. 각 모듈이 하나의 고정된 작업을 수행하는 일반적인 커넥터와 달리 이 커넥터에는 개방형 일반 영어 지침을 수락하는 단일 모듈이 있어 AI 모델이 이를 이행하는 데 필요한 Workfront 작업을 결정할 수 있도록 합니다.

예를 들어, &quot;예정보다 늦은 내 활성 프로젝트를 모두 찾고 상태를 요약하십시오.&quot;라는 메시지를 입력할 수 있으며, 모듈은 여러 Get 및 Filter 모듈을 함께 체인으로 연결하는 대신 합성 답변을 반환합니다.

AI가 수행할 수 있는 Workfront 작업을 제한할 수 있으므로 무인 시나리오에서도 예기치 않은 파괴적인 작업이 수행되지 않도록 할 수 있습니다.

기본적으로 이 모듈에서는 `claude-sonnet-5` 모델을 사용하는 Adobe Managed AI를 사용합니다. 제공한 키 및 기타 자격 증명을 사용하여 다른 LLM을 사용하도록 모듈을 구성할 수 있습니다.

>[!NOTE]
>
>Adobe Managed AI의 사용은 조직당 월별 25달러로 제한됩니다.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## Adobe Workfront MCP를 Workfront Fusion에 연결

Adobe Workfront MCP 커넥터는 OAuth 2.0을 사용하여 Workfront에 연결합니다. 다른 Workfront 커넥터와는 달리, 입력할 호스트, 클라이언트 ID 또는 클라이언트 암호와 같은 수동 연결 필드는 없습니다.

연결을 만들려면 다음 작업을 수행하십시오.

1. Adobe Workfront MCP 모듈에서 연결 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
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
          <p>이 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</td>
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   Workfront에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인 및 액세스 승인.

Workfront Fusion으로 다시 리디렉션되고 새 연결은 모듈에서 사용할 수 있습니다.

>[!NOTE]
>
>처음 사용 시 연결은 자동으로 Workfront의 MCP 서버에 등록되고 사용자가 만드는 모든 후속 연결에 대해 해당 등록을 재사용합니다.

## Adobe Workfront MCP 모듈 및 해당 필드

### 사용자 프롬프트 처리

이 작업 모듈은 지정한 언어 모델을 사용하여 Workfront의 MCP 서버에 대해 일반 영어 프롬프트를 처리하고 AI의 답변을 반환합니다.

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
  </tr>   <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-adobe-workfront-mcp-to-workfront-fusion" class="MCXref xref">Adobe Workfront MCP를 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>읽기 전용 도구 <i>(선택 사항)</i></td> 
   <td> <p>AI가 호출할 수 있는 읽기 전용 Workfront 작업을 제한합니다. 도구를 선택하지 않으면 모든 읽기 전용 도구가 허용됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>쓰기/삭제 도구 <i>(선택 사항)</i></td> 
   <td> <p>AI가 호출할 수 있는 Workfront 작업 쓰기 또는 삭제를 입력합니다. 이 항목을 비워 두면 모든 쓰기 및 삭제 도구가 허용됩니다.</p> <p>무인 시나리오가 파괴적인 작업을 수행하지 않도록 하려면 이 필드를 제한 없이 두지 않고 의도적으로 빈 선택 항목으로 설정하는 것이 좋습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>프롬프트 입력</td> 
   <td> <p>AI가 수행할 지침을 일반 영어로 입력하거나 매핑합니다.</p> <p>예: <i>일정보다 늦은 나에게 할당된 모든 프로젝트를 찾으십시오.</i></p> </td> 
  </tr>  </tbody> 
</table>

읽기 전용 도구 및 쓰기/삭제 도구 필드에 대해 선택할 수 있는 도구 목록은 Workfront 설명서의 [Adobe Workfront MCP 서버 도구](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-tools)를 참조하십시오.

모듈은 시나리오에서 후속 모듈에 매핑할 수 있는 다음 정보를 반환합니다.

* **응답**: AI의 최종 답변입니다(텍스트).
* **감사 추적**: 원래 프롬프트, 시작 및 종료 시간, AI가 만든 각 도구 호출에 대한 세부 정보(도구 이름, 인수, 성공 여부, 기간 및 출력 등)가 포함된 세션 레코드입니다.
* **요약**: 시도한 도구 호출 수, 성공 또는 실패 횟수, 총 처리 시간 및 전체 상태를 포함한 세션의 합계입니다.
