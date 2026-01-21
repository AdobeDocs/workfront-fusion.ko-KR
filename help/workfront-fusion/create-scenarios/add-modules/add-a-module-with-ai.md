---
title: AI를 사용하여 시나리오 세그먼트 생성
description: AI를 사용하여 시나리오의 세그먼트가 수행해야 할 작업을 설명하는 텍스트 프롬프트를 입력할 수 있습니다. 그런 다음 Fusion은 해당 작업을 수행하는 하나 이상의 모듈을 생성하며, 이 모듈은 시나리오에서 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: 2bec2607d55e4ba2ffd6ddcae6daa51071b204c4
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 19%

---

# AI를 사용하여 시나리오 세그먼트 생성

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

AI를 사용하여 시나리오의 세그먼트가 수행해야 할 작업을 설명하는 텍스트 프롬프트를 입력할 수 있습니다. 그런 다음 Fusion은 해당 작업을 수행하는 하나 이상의 모듈을 생성하며, 이 모듈은 시나리오에서 사용할 수 있습니다.

생성된 시나리오 세그먼트에는 단일 커넥터에 대한 모듈이 포함되어 있습니다. 다른 커넥터에 대한 모듈을 생성하려면 별도의 프롬프트를 생성한 다음 시나리오에서 시나리오 세그먼트를 조인합니다.

AI에서 생성된 모든 것과 마찬가지로 생성된 모듈을 두 번 확인하고 테스트하여 의도한 대로 작동하는지 확인하는 것이 좋습니다.

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

## 전제 조건

이 기능을 사용하려면 조직에서 다음 전제 조건을 충족해야 합니다.

* 귀사는 Workfront AI Assistant Beta 프로그램에 참여했어야 합니다.
* Adobe은 조직의 파일에 대해 서명된 Adobe Gen AI 계약이 있어야 합니다.

  계약 서명에 대한 자세한 내용은 Workfront 설명서의 AI Assistant 개요에서 [Adobe Gen AI 계약 서명](https://experienceleague.adobe.com/ko/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement)을 참조하십시오.

## 현재 지원되는 AI 모듈 애플리케이션

Fusion AI는 현재 다음 애플리케이션에 연결하는 모듈을 생성할 수 있습니다.

* Adobe Firefly
* Azure OpenAI
* Microsoft 그래프
* Adobe Workfront 계획 수립
* Adobe Analytics
* Adobe PDF Services
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* NetSuite
* Google 캘린더
* 아틀라시안 지라
* GitLab
* 스포티파이
* Bitbucket
* 오픈에이아이
* Slack

## 모듈 생성

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 모듈을 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 화면 오른쪽 상단 근처에 있는 **AI Assistant** 아이콘 ![AI Assistant 아이콘](assets/ai-assistant-icon.png)을 클릭합니다.
1. AI 지원 패널에 텍스트 프롬프트를 입력합니다.

   프롬프트에 대한 팁은 이 문서에서 [시나리오 세그먼트에 대한 프롬프트 작성 팁](#tips-for-creating-prompts-for-scenario-segments)을 참조하십시오.

   AI Assistant는 모듈 또는 모듈 세트를 생성합니다.
1. (조건부) 필요한 경우 애플리케이션에 대한 API 토큰을 모듈에 추가합니다.
1. 모듈을 확인하여 적절한 애플리케이션 및 작업에 맞게 구성되었는지 확인하십시오.
1. (조건부) 생성된 시나리오 섹션이 시나리오에 첨부되지 않은 경우 시나리오에 적절히 드래그합니다.

모듈을 테스트하여 의도한 대로 작동하는지 확인하는 것이 좋습니다.

## 시나리오 세그먼트에 대한 프롬프트를 만들기 위한 팁

텍스트 프롬프트에 최소한 다음 정보가 포함되어야 합니다.

* 연결 중인 응용 프로그램
* 수행할 작업

>[!IMPORTANT]
>
>한 번에 두 개 이상의 모듈을 생성할 수 있지만 한 번에 한 애플리케이션에 대한 모듈만 생성할 수 있습니다.

>[!BEGINSHADEBOX]

**예**:

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
여기에는 `Workfront Planning` 응용 프로그램과 `delete records` 작업이 포함됩니다. 이 프롬프트는 삭제할 각 레코드에 대해 하나씩, 세 개의 모듈을 만듭니다.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
여기에는 `Workfront Planning` 응용 프로그램과 `change campaign summary` 작업이 포함됩니다.
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
여기에는 `Workfront Planning` 응용 프로그램과 `get field details` 작업이 포함됩니다.

다음 예는 올바르지 않습니다.

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  이 예제는 두 개 이상의 애플리케이션을 포함하므로 올바르지 않습니다

>[!ENDSHADEBOX]

텍스트 프롬프트를 생성할 때 다음 사항을 고려하십시오.

* 직접적이고 간단한 언어를 사용하십시오.
* 시나리오 세그먼트를 확인하고 테스트합니다. 예상대로 수행되지 않으면 프롬프트를 세분화하고 다시 시도하십시오.
