---
title: MCP(Model Context Protocol) 모듈
description: MCP(Model Context Protocol) 모듈은 MCP를 사용하여 사용자 프롬프트를 처리할 수 있도록 해줍니다.
author: Becky
feature: Workfront Fusion
source-git-commit: d8ae176db714d2b9f041b74a62e8276171745c4b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# MCP(Model Context Protocol) 모듈

모델 컨텍스트 프로토콜(MCP)은 AI 언어 모델을 다른 애플리케이션과 안전하게 연결하는 방법입니다. AI 모델이 애플리케이션에 액세스할 수 있도록 MCP 서버를 구성합니다. 그런 다음 AI 모델에 프롬프트를 보내고 애플리케이션에서 정보를 반환할 수 있습니다.

예를 들어 AI 모델을 Gmail과 연결하도록 MCP 서버를 구성할 수 있습니다. &quot;Gmail에서 최근 5개의 이메일 보내기&quot;라는 메시지를 보낼 때 Gmail에 액세스하고 이메일을 반환할 수 있습니다.

MCP(Model Context Protocol) 모듈은 언어 모델 및 MCP 서버를 사용하여 사용자 프롬프트를 처리할 수 있도록 해줍니다.

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
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>또는</p>
   <p>레거시: 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 모델 컨텍스트 프로토콜 모듈 및 해당 필드

MCP 모듈을 구성할 때 [!DNL Adobe Workfront Fusion]은(는) 아래 나열된 필드를 표시합니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

### 사용자 프롬프트 처리

이 작업 모듈은 사용자가 지정하는 언어 모델 및 MCP 서버를 사용하여 프롬프트를 처리합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL LLM(Large Language Model) key]</td> 
   <td> <p>이 프롬프트에 사용할 대형 언어 모델의 API 키를 입력하거나 매핑합니다. </p> <p>현재 Anthropic API 키만 지원됩니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MCP 서버]</td> 
   <td> <p>이 프롬프트에 사용할 수 있게 하려는 각 MCP 서버에 대해 <b>항목 추가</b>를 클릭하고 서버의 이름과 호스트를 입력합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프롬프트 입력]</td> 
   <td> <p>대형 언어 모델의 프롬프트를 입력하거나 매핑합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
