---
title: Adobe Experience Manager Mcp 모듈
description: Adobe Experience Manager MCP 모듈을 사용하면 Adobe Experience Manager의 MCP 서버에 일반 영어 프롬프트를 보내고 AI 모델이 요청을 수행하도록 할 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 4c23409465b4be9fd10ff6938a750bc662ba2fe4
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 11%

---

# Adobe Experience Manager Mcp 모듈

Adobe Experience Manager MCP 커넥터는 Adobe Experience Manager의 자체 MCP(Model Context Protocol) 서버를 위한 전용 Fusion 통합입니다. 각 모듈이 하나의 고정된 작업을 수행하는 일반적인 커넥터와 달리 이 커넥터에는 개방형 일반 영어 지침을 수락하는 단일 모듈이 있어 AI 모델이 사이트, 디지털 에셋, 콘텐츠 조각, 폴더, 콘텐츠 저장소 및 콘텐츠 AI와 같은 영역 전반에서 이를 수행하는 데 필요한 Adobe Experience Manager 작업을 결정할 수 있도록 합니다.

이 커넥터는 Adobe Experience Manager 자체 MCP 서버 전용입니다. 다른 관련 없는 MCP 서버는 지원하지 않습니다. 커넥터의 경우 대신 MCP 서버를 지정할 수 있으며 MCP 에이전트 커넥터를 사용합니다.

MCP 에이전트 커넥터에 대한 자세한 내용은 [MCP 에이전트 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md)을 참조하세요.

>[!NOTE]
>
>이 모듈의 응답은 AI에서 생성되며 사용 가능한 모든 안전 장치가 있더라도 때때로 완벽하지 않을 수 있습니다. 이 모듈은 사람이 모든 실행을 실시간으로 검토하지 않는 자동화에 적합하지만, 기존 Adobe Experience Manager 모듈에서 얻을 수 있는 결정론적 동작을 보장하는 것은 아닙니다.

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

* 이 모듈을 사용하려면 Adobe Experience Manager 계정이 있어야 합니다.

## Adobe Experience Manager MCP를 Workfront Fusion에 연결 {#connect-adobe-experience-manager-mcp-to-workfront-fusion}

Adobe Experience Manager MCP 커넥터는 OAuth를 사용하여 Adobe Experience Manager에 연결합니다. 사용자 이름, 암호 또는 API 키와 같이, 수동으로 입력할 연결 필드가 없습니다.

연결을 만들려면 다음 작업을 수행하십시오.

1. Adobe Experience Manager MCP 모듈에서 연결 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.
1. 서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택
1. **계속**&#x200B;을 클릭합니다.

   Adobe의 로그인 페이지로 리디렉션됩니다.
1. Adobe 로그인 페이지에서 로그인하고 액세스를 승인합니다.

Workfront Fusion으로 다시 리디렉션되고 새 연결은 모듈에서 사용할 수 있습니다.

## Adobe Experience Manager MCP 모듈 및 해당 필드

현재 Adobe Experience Manager MCP 커넥터에는 모듈이 하나뿐이다.

### 사용자 프롬프트 처리

이 액션 모듈은 Adobe Experience Manager의 MCP 서버로 평이한 영어 지침을 보내고 AI의 대답을 반환합니다.

이 모듈의 각 실행은 라이브 대화가 아닌 이메일 전송과 유사한 독립적인 단일 실행입니다. AI가 후속 질문을 할 수 없고 답변을 기다릴 수 없다. 대신 최선의 판단을 내리고 완전한 답을 반환합니다. 귀하의 프롬프트가 모호한 경우, AI는 명확한 답변을 요청하기 위해 멈추기 보다는 답변의 일부로 만들어진 모든 가정을 명시합니다.

>[!IMPORTANT]
>
>이 모듈은 프롬프트가 실제로 쓰기 또는 삭제 작업을 요청할 때만 실행됩니다. 요청하지 않은 추가 작업은 수행하지 않습니다. 심지어 요청했던 다른 작업을 수행하는 동일한 실행에서도 마찬가지입니다.

각 실행은 독립적이므로 모듈에는 이전 실행의 메모리가 자체적으로 없습니다. 여러 번의 실행에 걸쳐 다중 전환, 대화 경험을 만들려면 이전 질문과 답변을 저장합니다. 이에 대해 데이터 저장소를 사용한 다음 다음 새 질문이 시작될 때 해당 기록을 텍스트로 포함할 수 있습니다.

데이터 저장소에 대한 자세한 내용은 [데이터 저장소](/help/workfront-fusion/create-scenarios/data-stores/data-store-overview.md)를 참조하십시오.

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
   <td><p>Adobe Experience Manager 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-adobe-experience-manager-mcp-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager MCP를 Workfront Fusion에 연결</a>을 참조하십시오.</p></td>
  </tr>
  <tr>
   <td role="rowheader">사용자 프롬프트</td>
   <td><p>AI가 수행할 지침을 일반 영어로 입력하거나 매핑합니다.</p><p>예: <i>90일 동안 업데이트되지 않은 모든 자산을 마케팅 폴더에서 찾습니다.</i></p></td>
  </tr>
  <tr>
   <td role="rowheader">읽기 전용 도구 <i>(선택 사항)</i></td>
   <td><p>AI가 호출할 수 있는 읽기 전용 Adobe Experience Manager 작업(에셋 찾기 또는 페이지 콘텐츠 읽기와 같이 검색만 하고 아무것도 변경하지 않는 작업)을 제한합니다.</p><p>이 필드를 비워 두면 모든 읽기 전용 작업이 허용됩니다.</p></td>
  </tr>
  <tr>
   <td role="rowheader">쓰기/삭제 도구 <i>(선택 사항)</i></td>
   <td><p>AI가 호출할 수 있는 Adobe Experience Manager 작업(페이지 업데이트, 콘텐츠 게시 또는 에셋 삭제 등)을 제한합니다.</p><p>이 필드를 비워 두면 모든 쓰기 및 삭제 작업이 허용됩니다. 무인 시나리오가 파괴적인 작업을 수행하지 않도록 하려면 이 필드를 제한 없이 두지 않고 의도적으로 빈 선택 항목으로 설정하는 것이 좋습니다.</p></td>
  </tr>
 </tbody>
</table>

이 모듈은 어떤 도구가 호출되었는지, 각 호출이 성공했는지, 처리 시간이 얼마나 걸렸는지 등 해당 답변을 생성하는 과정에서 무슨 일이 있었는지 기록과 함께 AI의 최종 답변을 텍스트로 반환합니다.
