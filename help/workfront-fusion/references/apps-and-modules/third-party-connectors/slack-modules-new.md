---
title: Slack 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Slack을 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수도 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 4c14fa36-8333-40d6-bd0a-fc6b0d9f4410
source-git-commit: 88147d0305595e1d0d388f510ed43fc5beaa4b64
workflow-type: tm+mt
source-wordcount: '4581'
ht-degree: 12%

---

# [!DNL Slack] 모듈

>[!IMPORTANT]
>
>이 문서에서는 2025년 11월 17일에 릴리스된 새로운 Slack 커넥터에서 사용할 수 있는 모듈에 대해 설명합니다.
>
>기존 Slack 커넥터에 대한 자세한 내용은 [[!DNL Slack] 모듈(레거시)](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/slack-modules.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Slack]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 색인](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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
   <p>작업 기반: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

* [!DNL Slack] 모듈을 사용하려면 [!DNL Slack] 계정이 있어야 합니다.
* OAuth@ 연결을 만드는 경우 조직의 허용 목록에 추가하다에 다음 URL을 추가해야 합니다.
   * 봇 토큰: `https://oauth.app.workfrontfusion.com/oauth/cb/slack3`
   * 사용자 토큰:` https://oauth.app.workfrontfusion.com/oauth/cb/slack2`

## Slack API 정보

Slack 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>{{ifempty(parameters.domain, 'https://slack.com/api/')}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack] 모듈 및 해당 필드

[!DNL Slack] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL Slack] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [메시지](#messages)
* [파일](#files)
* [채널](#channels)
* [반응](#reactions)
* [별 개수](#stars)
* [저장된 항목](#saved-items)
* [고정 항목](#pins)
* [사용자](#users)
* [알림 메시지](#reminders)
* [이벤트](#events)
* [프로필](#profile)
* [기타](#other)

### 메시지

+++ **[!UICONTROL 메시지 만들기]**

이 작업 모듈은 새 메시지를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID 또는 이름 입력]</p> </td> 
   <td> <p>메시지를 만들 채널을 선택하는 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL 채널 ID 또는 이름]</strong> 필드에 메시지를 게시할 채널의 채널 ID 또는 이름을 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>채널 유형을 선택한 다음 채널을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 텍스트]</p> </td> 
   <td> <p>만들려는 메시지의 텍스트 콘텐츠를 입력합니다.</p> <p>참고: 텍스트 서식에 대한 자세한 내용은 <a href="https://api.slack.com/reference/surfaces/formatting"> 설명서에서 </a>앱 표면에 대한 텍스트 서식 지정[!DNL Slack]을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 블록]</td> 
   <td>블록은 메시지를 사용자 정의하고 구성하는 데 사용할 수 있는 재사용 가능한 구성 요소입니다. 블록에 대한 자세한 내용은 <a href="https://api.slack.com/block-kit"> 설명서의 </a>블록 키트[!DNL Slack]를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스레드 메시지 ID(타임스탬프)]</td> 
   <td>새 메시지가 회신인 경우 회신할 메시지의 타임스탬프를 입력합니다. 이미 회신한 메시지의 타임스탬프를 입력하지 마십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 회신 브로드캐스트]</td> 
   <td> <p>다음 두 가지가 모두 적용되는 경우 <strong>[!UICONTROL 예]</strong>를 선택하십시오.</p> 
    <ul> 
     <li> <p>새 메시지는 다른 메시지에 대한 회신입니다.</p> </li> 
     <li> <p>채널의 모든 사용자가 새 메시지를 볼 수 있도록 하려는 경우</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 링크 이름]</p> </td> 
   <td> <p>이름 및 채널에서 <code>@username</code> 또는 <code>#channel</code> 형식을 사용할 수 있도록 하려면 이 옵션을 활성화하십시오. </p> <p>자세한 내용은 <a href="https://api.slack.com/docs/formatting"> 설명서에서 </a>앱 표면에 대한 텍스트 서식 지정[!DNL Slack]을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 구문 분석 메시지 텍스트]</p> </td> 
   <td> <p>자동 구문 분석을 허용하려면 이 옵션을 활성화합니다. </p> <p>자세한 내용은 <a href="https://api.slack.com/docs/formatting"> 설명서에서 </a>앱 표면에 대한 텍스트 서식 지정[!DNL Slack]을 참조하십시오.</p> <p>참고: 원래 메시지에서 [!UICONTROL 링크 이름] 또는 [!UICONTROL 구문 분석 메시지 텍스트] 옵션을 사용한 경우 [!UICONTROL 메시지 업데이트] 모듈도 실행할 때 이 옵션을 지정해야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use Markdown]</p> </td> 
   <td> <p>[!DNL Slack]이(가) 텍스트에서 Markdown을 사용할 수 있도록 하려면 이 옵션을 사용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 주로 텍스트 기반 콘텐츠 펼치기]</p> </td> 
   <td> <p>주로 텍스트 기반 콘텐츠를 펼칠 수 있도록 하려면 이 옵션을 활성화합니다. </p> <p>[!DNL Slack]에서 연결 해제에 대한 자세한 내용은 <a href="https://api.slack.com/reference/messaging/link-unfurling"> 설명서에서 </a>메시지의 연결 해제[!DNL Slack]를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 미디어 콘텐츠 펼치기]</p> </td> 
   <td> <p>미디어 콘텐츠 풀기를 허용하려면 이 옵션을 활성화합니다. </p> <p>[!DNL Slack]에서 연결 해제에 대한 자세한 내용은 <a href="https://api.slack.com/reference/messaging/link-unfurling"> 설명서에서 </a>메시지의 연결 해제[!DNL Slack]를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 메시지 삭제]**

이 작업 모듈은 지정된 메시지를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>채널 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID(타임스탬프)]</td> 
   <td> <p> 삭제하려는 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 Watch Private Channel 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 개인 채널 메시지 가져오기]**

이 작업 모듈은 선택한 채널에서 메시지의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널]</p> </td> 
   <td> <p>메시지가 포함된 채널을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메시지 ID(타임스탬프)]</p> </td> 
   <td> <p> 정보를 검색할 메시지의 메시지 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Public Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 공개 채널 메시지 가져오기]**

이 작업 모듈은 지정된 공개 채널에서 지정된 ID의 메시지를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>메시지가 포함된 채널을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID(타임스탬프)]</td> 
   <td> <p> 정보를 검색할 메시지의 메시지 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Public Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 답글 나열]**

이 작업 모듈은 대화에 게시된 메시지 스레드를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>답글을 검색할 메시지가 포함된 채널 유형을 선택한 다음 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상위 메시지 ID(타임스탬프)]</td> 
   <td> <p> 회신을 검색할 메시지의 메시지 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Public Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 회신 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 메시지 검색]**

이 검색 모듈은 검색 쿼리와 일치하는 메시지를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>검색할 쿼리를 입력합니다. </p> <p>매핑 패널에서 수식을 만드는 방법에 대한 자세한 내용은 <a href="/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md" class="MCXref xref">[!DNL Adobe Workfront Fusion]</a>의 기본 제공 함수를 사용하여 항목 매핑을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 정렬 기준] </td> 
   <td> <p>반환된 메시지를 점수별로 정렬할지 아니면 타임스탬프별로 정렬할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>메시지를 오름차순으로 정렬할지 아니면 내림차순으로 정렬할지 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 메시지 업데이트]**

이 작업 모듈에서는 기존 메시지를 편집할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID 또는 이름 입력]</p> </td> 
   <td> <p>원하는 메시지를 선택하는 방법을 선택합니다 .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL 채널 ID 또는 이름]</strong> 필드에 메시지를 포함하는 채널의 채널 ID 또는 을 입력하거나 매핑한 다음 메시지의 <strong>[!UICONTROL 타임스탬프(메시지 ID)]</strong>을(를) 입력합니다. .</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>채널 유형을 선택한 다음 채널을 선택하고 메시지를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 텍스트]</p> </td> 
   <td> <p>업데이트하려는 메시지의 새 텍스트 콘텐츠를 입력합니다.</p> <p>자세한 내용은 <a href="https://api.slack.com/docs/formatting"> 설명서에서 </a>앱 표면에 대한 텍스트 서식 지정[!DNL Slack]을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 블록]</td> 
   <td>블록은 메시지를 사용자 정의하고 구성하는 데 사용할 수 있는 재사용 가능한 구성 요소입니다. 블록에 대한 자세한 내용은 <a href="https://api.slack.com/block-kit"> 설명서의 </a>블록 키트[!DNL Slack]를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 링크 이름]</p> </td> 
   <td> <p>이름 및 채널에서 <code>@username</code> 또는 <code>#channel</code> 형식을 사용할 수 있도록 하려면 이 옵션을 활성화하십시오. </p> <p>자세한 내용은 <a href="https://api.slack.com/docs/formatting"> 설명서에서 </a>앱 표면에 대한 텍스트 서식 지정[!DNL Slack]을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 구문 분석 메시지 텍스트]</p> </td> 
   <td> <p>자동 구문 분석을 허용하려면 이 옵션을 활성화합니다. </p> <p> 자세한 내용은 <a href="https://api.slack.com/docs/formatting"> 설명서에서 </a>앱 표면에 대한 텍스트 서식 지정[!DNL Slack]을 참조하십시오.</p> <p>참고: 원래 메시지에서 [!UICONTROL 링크 이름] 또는 [!UICONTROL 구문 분석 메시지 텍스트] 옵션을 사용한 경우 메시지 업데이트 모듈을 실행할 때도 이 옵션을 지정해야 합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 다이렉트 메시지 보기]**

이 트리거 모듈은 다이렉트 메시지에 새 메시지가 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널] </td> 
   <td> <p>새 메시지가 있는지 확인할 다이렉트 메시지 대화를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 메시지 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 다중 파티 다이렉트 메시지 보기]**

이 트리거 모듈은 새 메시지가 다중 당사자 다이렉트 메시지 채널에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널] </td> 
   <td> <p>새 메시지가 있는지 확인할 다이렉트 메시지 대화를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 메시지 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL 개인 채널 메시지 보기]**

이 트리거 모듈은 새 메시지가 개인 채널(그룹)에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널] </td> 
   <td> <p>새 메시지를 확인하려는 비공개 채널을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 메시지 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL 공개 채널 메시지 보기]**

이 트리거 모듈은 새 메시지가 공개 채널에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널] </td> 
   <td> <p>새 메시지를 확인하려는 공개 채널을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 메시지 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 파일

+++ **[!UICONTROL 파일 삭제]**

이 작업 모듈은 지정된 파일을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td> <p>삭제할 파일의 ID를 입력하거나 매핑합니다. </p> <p>참고: 파일 ID는 [!DNL Watch Files] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 파일 가져오기]**

이 작업 모듈은 지정된 파일에 대한 세부 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td> <p>검색할 파일의 ID를 입력하거나 매핑합니다. </p> <p>참고: 파일 ID는 [!DNL Watch Files] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 목록 파일]**

이 작업 모듈은 지정된 필터를 기반으로 파일 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 유형] </td> 
   <td> <p>검색할 파일 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 유형]</p> </td> 
   <td> <p>파일을 나열할 채널을 나타내는 채널 유형을 선택한 다음 채널을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작성자]</td> 
   <td> <p>지정된 사용자가 만든 파일만 반환할 사용자를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작 날짜]</td> 
   <td>파일을 반환할 가장 빠른 날짜를 입력합니다. 지원되는 날짜 및 시간 형식 목록을 보려면 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">의 [!DNL Adobe Workfront Fusion]</a>형식 변환을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 종료 날짜]</td> 
   <td>파일을 반환할 최신 날짜를 입력합니다. 지원되는 날짜 및 시간 형식 목록을 보려면 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">의 [!DNL Adobe Workfront Fusion]</a>형식 변환을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 파일 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Download a File]**

This action module downloads a file from a URL. It must follow the [!UICONTROL Slack] >[!UICONTROL Get a File] module in a scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL private download]</td> 
   <td> <p>Map the <b>[!UICONTROL URL Private download]</b> value from the [!DNL Slack] >[!UICONTROL Get a File] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL 파일 업로드]**

이 작업 모듈은 파일을 만들거나 [!DNL Slack]에 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널]</td> 
   <td> <p>파일을 업로드할 각 채널에 대해 <b>[!UICONTROL 항목 추가]</b>를 클릭한 다음 채널 유형 및 채널을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>업로드할 파일의 제목을 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스레드 ID(타임스탬프)]</td> 
   <td> <p>파일을 회신으로 업로드하는 경우 회신할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Initial Comment]</td> 
   <td> <p>파일을 소개하는 메시지 텍스트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 파일 보기]**

이 트리거 모듈은 새 파일이 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 유형]</td> 
   <td>모듈에서 조사할 파일 형식을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td> <p>파일에서 감시할 채널 유형을 선택한 다음 채널을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작성자]</td> 
   <td> <p>지정된 사용자가 만든 파일만 반환할 사용자를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 파일 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 채널

+++ **[!UICONTROL 채널 보관]**

이 작업 모듈은 채널을 보관합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>보관하려는 채널의 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널 만들기]**

이 작업 모듈은 새 채널을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이름]</p> </td> 
   <td> <p>새 채널의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Is private]</td> 
   <td>새 채널을 비공개로 설정하려면 이 옵션을 활성화하십시오.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널 가져오기]**

이 작업 모듈은 작업 영역 채널에 대한 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>정보를 검색할 채널의 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널 가입]**

이 작업 모듈은 사용자를 채널에 연결합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>가입하려는 채널의 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널 나가기]**

이 작업 모듈은 채널에서 사용자를 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>떠나려는 채널의 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널 나열]**

이 검색 모듈은 작업 영역의 모든 채널 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Exclude archived]</p> </td> 
   <td> <p>결과에서 보관된 채널을 제외하려면 [!UICONTROL 예]를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 유형] </td> 
   <td> <p>검색할 채널 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 채널 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널의 구성원 나열]**

이 검색 모듈은 선택한 채널의 사용자 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>나열할 멤버가 포함된 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private Channel]</td> 
   <td>구성원을 나열할 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 멤버 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널의 목적을 설정합니다]**

이 작업 모듈은 채널의 용도를 변경합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>용도를 변경할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / User / [!UICONTROL Multiple IM Channel]</td> 
   <td>목적을 변경할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Purpose]</td> 
   <td>채널의 새 용도를 입력하거나 매핑합니다. 이 필드는 서식 또는 링크를 지원하지 않습니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널의 주제를 설정합니다]**

이 작업 모듈은 채널의 주제를 변경합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>항목을 변경할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM Channel]</td> 
   <td>항목을 변경할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Topic]</td> 
   <td>채널의 새 주제를 입력하거나 매핑합니다. 이 필드는 서식 또는 링크를 지원하지 않습니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 채널 보관 해제]**

이 작업 모듈은 채널을 보관 해제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>보관을 해제할 채널의 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 반응

+++ **[!UICONTROL 반응 추가]**

이 작업 모듈은 항목에 반응을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>반응을 추가할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>반응을 추가할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID(타임스탬프)]</td> 
   <td> <p> 반응을 추가할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반응(이모지) 이름]</td> 
   <td>반응에 사용할 이모지의 이름을 입력하거나 매핑합니다. 예: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 반응 나열]**

이 작업 모듈은 사용자가 수행한 반응을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL User]</p> </td> 
   <td> <p>나열할 반응을 만든 사용자를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 반응 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 반응 제거]**

이 작업 모듈은 항목에서 반응을 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>반응을 제거할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>반응을 제거할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 반응을 제거할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반응(이모지) 이름]</td> 
   <td>메시지에서 제거할 이모지의 이름을 입력하거나 매핑합니다. 예: <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

### 별 개수

+++ **[!UICONTROL 별 추가]**

이 작업 모듈은 채널을 별표 채널로 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>별표를 추가하려는 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>별표를 추가할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 별 제거]**

이 작업 모듈은 별표가 표시된 채널에서 별표를 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>별표를 추가하려는 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>별표를 추가할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

### 저장된 항목

+++ **[!UICONTROL 저장된 항목 제거]**

이 작업 모듈은 저장된 항목에서 항목을 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID(타임스탬프)]</td> 
   <td> <p> 저장된 항목에서 제거할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td> <p>저장된 항목에서 제거할 파일을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 항목 저장]**

이 작업 모듈은 저장된 항목에 항목을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID(타임스탬프)]</td> 
   <td> <p> 저장할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td> <p>저장할 파일을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 고정 항목

+++ **[!UICONTROL 항목 고정]**

이 작업 모듈은 항목을 채널에 고정합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>항목을 고정할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL Multiple IM channel] / [!UICONTROL User]</td> 
   <td>항목을 고정할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 고정할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 항목 고정 해제]**

이 작업 모듈은 채널에서 항목을 고정 해제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>항목을 고정 해제할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL Multiple IM channel] / [!UICONTROL User]</td> 
   <td>항목을 고정 해제할 채널 또는 사용자를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 고정 해제할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 사용자

+++ **[!UICONTROL 사용자 가져오기]**

이 작업 모듈은 작업 영역 멤버에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 사용자 ID]</p> </td> 
   <td> <p>세부 정보를 검색할 사용자의 사용자 ID를 입력하거나 매핑합니다.</p> <p>참고: 사용자 ID는 [!DNL List Users] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 사용자 초대]**

이 작업 모듈은 1-30명의 사용자를 공개 또는 비공개 채널에 초대합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>사용자를 초대할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private channel]</td> 
   <td>사용자를 초대할 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사용자]</td> 
   <td> <p>채널에 추가할 사용자를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 사용자 시작]**

이 작업 모듈은 채널에서 사용자를 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널 유형]</td> 
   <td>사용자를 제거할 채널 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private channel]</td> 
   <td>사용자를 제거할 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사용자]</td> 
   <td> <p>채널에서 제거할 사용자를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 사용자 나열]**

이 작업 모듈은 작업 영역의 모든 사용자 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 제한]</p> </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 사용자 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 사용자 검색]**

이 작업 모듈은 이메일 주소를 사용하여 단일 사용자에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email] </p> </td> 
   <td> <p>세부 정보를 검색할 사용자의 이메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 사용자 보기]**

이 트리거 모듈은 새 사용자가 [!DNL Slack] 작업 영역에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 사용자 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 알림 메시지

<!--

+++ **[!UICONTROL List Reminders]**

This action module returns a list of all reminders created by or given to the currently authenticated user.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Enter or map the maximum number of reminders you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Reminder]**

This action module retrieves details about a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to retrieve details for.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL 미리 알림 만들기]**

이 작업 모듈은 미리 알림을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 텍스트]</td> 
   <td>미리 알림 콘텐츠 입력 또는 매핑</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Time]</td> 
   <td> <p>이 미리 알림이 발생해야 하는 날짜 및 시간을 입력하거나 매핑합니다. 다음 중 하나를 입력합니다. </p> 
    <ul> 
     <li> <p>Unix 타임스탬프(지금부터 최대 5년 후)</p> </li> 
     <li> <p>미리 알림까지의 시간(초)(24시간 이내인 경우) </p> </li> 
     <li> <p>자연어 설명(예: "15분 이내" 또는 "매주 목요일")</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL User] </p> </td> 
   <td> <p>미리 알림을 받는 사용자를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Complete a Reminder]**

This action module completes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to complete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Reminder]**

This action module deletes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to delete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

### 이벤트

+++ **[!UICONTROL 새 이벤트]**

이 즉시 트리거는 새 메시지나 다른 이벤트가 만들어질 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 웹후크]</p> </td> 
   <td> <p>사용할 웹후크를 선택합니다.</p> <p>또는</p> <p>새 웹후크를 만듭니다.</p> 
    <ol> 
     <li value="1"> <p><b>[!UICONTROL 추가]</b>를 클릭합니다.</p> </li> 
     <li value="2"> <p>이벤트 유형을 선택합니다.</p> </li> 
     <li value="3"> <p>연결을 선택하거나 추가합니다. [!DNL Slack] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!UICONTROL Adobe Workfront Fusion]에 대한 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </li> 
     <li value="4"> <p>메시지가 표시되면 보려는 채널을 선택합니다.</p> </li> 
     <li value="5"> <p><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 프로필

+++ **[!UICONTROL 상태 설정]**

이 작업 모듈은 사용자의 현재 상태를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 상태 텍스트]</p> </td> 
   <td> <p>상태 텍스트를 입력하거나 매핑합니다. 다음 사항을 고려하십시오.</p> 
    <ul> 
     <li> <p>최대 100자를 입력할 수 있습니다.</p> </li> 
     <li> <p>마크업이나 사용자 언급 같은 다른 서식을 사용할 수 있습니다.</p> </li> 
     <li> <p><code>:emojiname:</code> 형식을 사용하여 상태 텍스트에 이모지를 포함할 수 있습니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상태 이모지]</td> 
   <td> <p>상태를 표시하는 데 사용할 이모지를 입력하거나 매핑합니다. <code>:emojiname:</code> 형식을 사용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상태 만료]</td> 
   <td>상태를 만료하려는 날짜 및 시간을 입력하거나 매핑합니다. 지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">유형 강제 변환</a>을 참조하십시오.</td> 
  </tr> 
 </tbody> 
</table>

+++

### 기타

+++ **[!UICONTROL API 호출 만들기]**

이 액션 모듈을 사용하면 [!DNL Slack] API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Slack] 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://slack.com/api/</code>와 관련된 경로를 입력합니다. 예: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion]가 사용자에게 인증 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>예: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 기본 URL]</td> 
   <td>API 호출에 사용할 기본 URL을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

## Terminology

[!DNL Slack] 모듈을 구성할 때 다음 용어가 유용할 수 있습니다.

* **DM**: [!UICONTROL 다이렉트 메시지]
* **메신저**: [!UICONTROL 인스턴트 메시지]
* **개인 채널**: 이전 [!UICONTROL 그룹]
* **다이렉트 메시지**: 이전 [!UICONTROL IM]
* **채널**: API 설명서의 [!UICONTROL 대화], [!UICONTROL  앱의 ]채널[!DNL Slack].
