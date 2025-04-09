---
title: Slack 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Slack을 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수도 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: eb0518ba0d1a0c758cb547e362c722f4be3674c7
workflow-type: tm+mt
source-wordcount: '1954'
ht-degree: 0%

---

# [!DNL Slack]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Slack]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

## 전제 조건

[!DNL Slack] 모듈을 사용하려면 [!DNL Slack] 계정이 있어야 합니다.

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

## [!DNL Slack]개 모듈 및 해당 필드

[!DNL Slack] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Slack] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [메시지](#messages)
* [대화](#channels)
* [기타](#other)

### 메시지

* [메시지 보내기 만들기](#create-a-message)
* [메시지 삭제](#delete-a-message)
* [비공개 채널 메시지 보내기 받기](#get-a-private-channel-message)
* [공개 채널 메시지 보내기 받기](#get-a-public-channel-message)
* [메시지 업데이트](#update-a-message)
* [비공개 채널 메시지 보기](#watch-private-channel-messages)
* [공개 채널 메시지 보기](#watch-public-channel-messages)

### [!UICONTROL 메시지 만들기]

이 작업 모듈은 새 메시지를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
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
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>만들려는 메시지의 텍스트 콘텐츠를 입력합니다.</p> <p>참고: 텍스트 서식에 대한 자세한 내용은 [!DNL Slack] 설명서에서 <a href="https://api.slack.com/reference/surfaces/formatting">앱 표면에 대한 텍스트 서식 지정</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As User]</td> 
   <td>이 모듈의 연결에 사용된 자격 증명을 소유한 사용자로 메시지를 게시하려면 이 옵션을 활성화하십시오.</td> 
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
   <td role="rowheader">[!UICONTROL 첨부 파일]</td> 
   <td>메시지에 첨부할 각 항목에 대해 <b>항목 추가</b>를 클릭하고 항목의 세부 정보를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 아이콘 이모지]</td> 
   <td>이 메시지의 아이콘으로 사용할 이모지를 <code>:icon-name:</code> 형식으로 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 아이콘 URL]</td> 
   <td>이 메시지의 아이콘으로 사용할 이미지의 URL을 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 링크 이름]</p> </td> 
   <td> <p>이름 및 채널에서 <code>@username</code> 또는 <code>#channel</code> 형식을 사용할 수 있도록 하려면 이 옵션을 활성화하십시오. </p> <p>자세한 내용은 [!DNL Slack] 설명서에서 <a href="https://api.slack.com/docs/formatting">앱 표면에 대한 텍스트 서식 지정</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 구문 분석 메시지 텍스트]</p> </td> 
   <td> <p>자동 구문 분석을 허용하려면 이 옵션을 활성화합니다. </p> <p>자세한 내용은 [!DNL Slack] 설명서에서 <a href="https://api.slack.com/docs/formatting">앱 표면에 대한 텍스트 서식 지정</a>을 참조하십시오.</p> <p>참고: 원래 메시지에서 [!UICONTROL 링크 이름] 또는 [!UICONTROL 구문 분석 메시지 텍스트] 옵션을 사용한 경우 [!UICONTROL 메시지 업데이트] 모듈도 실행할 때 이 옵션을 지정해야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use Markdown]</p> </td> 
   <td> <p>[!DNL Slack]이(가) 텍스트에서 Markdown을 사용할 수 있도록 하려면 이 옵션을 사용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 주로 텍스트 기반 콘텐츠 펼치기]</p> </td> 
   <td> <p>주로 텍스트 기반 콘텐츠를 펼칠 수 있도록 하려면 이 옵션을 활성화합니다. </p> <p>[!DNL Slack]에서 연결 해제에 대한 자세한 내용은 [!DNL Slack] 설명서에서 <a href="https://api.slack.com/reference/messaging/link-unfurling">메시지의 연결 해제</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 미디어 콘텐츠 펼치기]</p> </td> 
   <td> <p>미디어 콘텐츠 풀기를 허용하려면 이 옵션을 활성화합니다. </p> <p>[!DNL Slack]에서 연결 해제에 대한 자세한 내용은 [!DNL Slack] 설명서에서 <a href="https://api.slack.com/reference/messaging/link-unfurling">메시지의 연결 해제</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사용자 이름]</td> 
   <td>메시지를 게시하는 데 사용되는 사용자 이름을 지정합니다. 사용자 이름을 지정하지 않으면 "보트"라는 이름이 사용됩니다.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 메시지 삭제]

이 작업 모듈은 지정된 메시지를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>채널 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 삭제하려는 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 개인 채널 메시지 보기 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As User]</td> 
   <td> <p> 연결에 사용된 자격 증명을 사용하여 사용자로 메시지를 삭제하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 개인 채널 메시지 가져오기]

이 작업 모듈은 선택한 채널에서 메시지의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>채널 ID를 입력(매핑)합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메시지 ID(타임스탬프)]</p> </td> 
   <td> <p> 정보를 검색할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Private Channel Messages] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 공개 채널 메시지 가져오기]**

이 작업 모듈은 지정된 공개 채널에서 지정된 ID의 메시지를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>채널 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID(타임스탬프)]</td> 
   <td> <p> 정보를 검색할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Public Channel Messages] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 업데이트]

이 작업 모듈에서는 기존 메시지를 편집할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>업데이트하려는 메시지가 포함된 채널의 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메시지 ID(타임스탬프)]</p> </td> 
   <td> <p> 정보를 검색할 메시지의 타임스탬프를 입력하거나 매핑합니다.</p> <p>참고: 타임스탬프는 [!UICONTROL Watch Public Channel Messages] 모듈과 같은 다른 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>업데이트하려는 메시지의 새 텍스트 콘텐츠를 입력합니다.</p> <p>자세한 내용은 [!DNL Slack] 설명서에서 <a href="https://api.slack.com/docs/formatting">앱 표면에 대한 텍스트 서식 지정</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As User]</td> 
   <td>이 모듈 연결에 사용되는 신임 정보를 소유하는 사용자 메시지를 업데이트하려면 이 옵션을 사용하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL 첨부 파일]</td> 
   <td>메시지에 첨부할 각 항목에 대해 항목</b> 추가를 클릭하고 <b>항목의 세부 정보를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! UICONTROL 링크 이름]</p> </td> 
   <td> <p>이 옵션을 활성화하여 이름 및 채널의 사용 <code>@username</code> 또는 포맷 지정을 <code>#channel</code> 허용합니다. </p> <p>자세한 내용은 설명서에서 앱 화면에</a> 대한 텍스트 서식 지정을 [!DNL Slack] 참조하세요<a href="https://api.slack.com/docs/formatting">.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[! UICONTROL 구문 분석 메시지 텍스트]</p> </td> 
   <td> <p>자동 구문 분석을 허용하려면 이 옵션을 활성화하십시오. </p> <p> 자세한 내용은 [!DNL Slack] 설명서에서 <a href="https://api.slack.com/docs/formatting">앱 표면에 대한 텍스트 서식 지정</a>을 참조하십시오.</p> <p>참고: 원래 메시지에서 [!UICONTROL 링크 이름] 또는 [!UICONTROL 구문 분석 메시지 텍스트] 옵션을 사용한 경우 메시지 업데이트 모듈을 실행할 때도 이 옵션을 지정해야 합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 개인 채널 메시지 보기]

이 트리거 모듈은 새 메시지가 개인 채널(그룹)에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널] </td> 
   <td> <p>새 메시지를 확인하려는 비공개 채널을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 메시지 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 공개 채널 메시지 보기]

이 트리거 모듈은 새 메시지가 공개 채널에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널] </td> 
   <td> <p>새 메시지를 확인하려는 공개 채널을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 메시지 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>



### 대화

* [채널 받기](#get-a-channel)
* [채널 나열](#list-channels)
* [채널의 구성원 나열](#list-members-in-channel)

#### [!UICONTROL 채널 가져오기]

이 작업 모듈은 작업 영역 채널에 대한 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Slack] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 채널 ID]</p> </td> 
   <td> <p>정보를 검색할 채널의 ID를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL 채널 나열]

이 검색 모듈은 작업 영역의 모든 채널 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
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
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 채널 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL 채널의 구성원 나열]

이 검색 모듈 은 선택한 채널의 사용자 목록을 리턴합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! UICONTROL 연결] </td> 
   <td> <p>계정 연결 [!DNL Slack] 방법에 [!DNL Workfront Fusion]대한 자세한 내용은 에 대한 연결 [!DNL Adobe Workfront Fusion] 만들기 - 기본 지침을</a> 참조하세요<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">.</p> </td> 
  </tr> 
<tr> 
   <td role="rowheader"> <p>[! UICONTROL 채널 ID 또는 이름 입력]</p> </td> 
   <td> <p>할 메시지를 선택하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL 채널 ID 또는 이름]</strong> 필드에 사용자를 나열할 채널의 채널 ID 또는 를 입력하거나 매핑합니다.</p> <p>참고: 채널 ID는 [!UICONTROL 목록 채널] 모듈을 사용하여 검색할 수 있습니다.</p> </li> 
     <li> <p><strong>[! UICONTROL 목록에서 선택]</strong> </p> <p>채널 유형을 선택한 다음 채널을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr>
  <tr> 
   <td role="rowheader">[! UICONTROL 제한] </td> 
   <td> <p>한 실행 주기 동안 반환되는 최대 멤버 [!DNL Workfront Fusion] 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>


### 기타

#### [!UICONTROL API 호출하기]

이 작업 모듈 사용하면 API에 대해 인증된 사용자 지정 호출을 [!DNL Slack] 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Slack] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[! UICONTROL 연결] </td> 
   <td> <p>계정 연결 [!DNL Slack] 방법에 [!DNL Workfront Fusion]대한 자세한 내용은 에 대한 연결 [!DNL Adobe Workfront Fusion] 만들기 - 기본 지침을</a> 참조하세요<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL URL]</td> 
   <td>에 상대 <code>https://slack.com/api/</code>적인 경로를 입력합니다. 예: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion]이 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 기본 URL]</td> 
   <td>API 호출에 사용할 기본 URL을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 전송 액세스 토큰]</td> 
   <td>액세스 토큰을 헤더로 전송할지 또는 쿼리 매개 변수로 전송할지를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

## Terminology

[!DNL Slack] 모듈을 구성할 때 다음 용어가 유용할 수 있습니다.

* **DM**: [!UICONTROL 다이렉트 메시지]
* **메신저**: [!UICONTROL 인스턴트 메시지]
* **개인 채널**: 이전 [!UICONTROL 그룹]
* **다이렉트 메시지**: 이전 [!UICONTROL IM]
* **채널**: API 설명서의 [!UICONTROL 대화], [!DNL Slack] 앱의 [!UICONTROL 채널].
