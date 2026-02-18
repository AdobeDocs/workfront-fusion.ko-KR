---
title: MCP(Model Context Protocol) 모듈
description: MCP(Model Context Protocol) 모듈은 MCP를 사용하여 사용자 프롬프트를 처리할 수 있도록 해줍니다.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
source-git-commit: 5dfca593b17a234c80c807470026a7b192cbf7fa
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 23%

---

# Model Context Protocol(MCP) 모듈

<!--SET UP REDIRECTS-->

모델 컨텍스트 프로토콜(MCP)은 AI 언어 모델을 다른 애플리케이션과 안전하게 연결하는 방법입니다. AI 모델이 애플리케이션에 액세스할 수 있도록 MCP 서버를 구성합니다. 그런 다음 AI 모델에 프롬프트를 보내고 애플리케이션에서 정보를 반환할 수 있습니다.

예를 들어 AI 모델을 Gmail과 연결하도록 MCP 서버를 구성할 수 있습니다. &quot;Gmail에서 최근 5개의 이메일 보내기&quot;라는 메시지를 보낼 때 Gmail에 액세스하고 이메일을 반환할 수 있습니다.

MCP(Model Context Protocol) 모듈은 언어 모델 및 MCP 서버를 사용하여 사용자 프롬프트를 처리할 수 있도록 해줍니다.

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





## 모델 컨텍스트 프로토콜 모듈 및 해당 필드

MCP 모듈을 구성하면 Adobe Workfront Fusion에 아래 나열된 필드가 표시됩니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

### 사용자 프롬프트 처리

이 작업 모듈은 사용자가 지정하는 언어 모델 및 MCP 서버를 사용하여 프롬프트를 처리합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM 키</td> 
   <td> 기존 LLM 키를 선택하거나 <b>추가</b>를 클릭하고 다음 정보를 입력하여 새 키를 만드십시오. 
     <ul>
       <li><b>키 이름</b>: 새 키의 이름을 입력하십시오.</li>
       <li><b>LLM</b>: 이 키와 연결된 큰 언어 모델을 선택하십시오.</li>
       <li><b>키</b>: 선택한 모델의 API 키를 입력하거나 매핑합니다.</li>
       <li><b>모델</b>: 키에 사용할 LLM 모델을 선택하십시오.</li>
       <li><b>최대 토큰</b>: LLM이 응답에서 생성할 수 있는 최대 토큰 수를 입력하거나 매핑합니다.<p>한 토큰은 보통 4자, 즉 영어에서 한 단어의 .75와 같다. "Hello world"는 2개의 토큰과 같으며 "Authentication"은 1개와 2개의 토큰으로 같습니다.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>MCP 서버</td> 
   <td> <p>연결할 각 MCP 서버에 대해 <b>추가</b>를 클릭하고 다음 정보를 입력하십시오. </p> 
     <ul>
       <li><b>연결</b>: Fusion에서 MCP 서버에 연결하는 데 사용할 연결을 선택하십시오.</li>
       <li><b>MCP 서버 호스트</b>: MCP 서버의 URL을 입력하십시오.</li>
       <li><b>MCP 서버 이름</b>: 이 MCP 서버의 이름을 입력하거나 매핑합니다.</li>
       <li><b>헤더</b>: 적용 가능한 헤더를 추가합니다.</li>
       <li><b>MCP 서버 유형</b>: 서버 유형을 선택합니다.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>프롬프트 입력 </td> 
   <td> <p>처리할 프롬프트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>


