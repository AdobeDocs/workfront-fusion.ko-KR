---
title: Gmail 모듈
description: Adobe Workfront Fusion 시나리오에서는 Gmail을 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1852'
ht-degree: 0%

---

# [!DNL Gmail]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Gmail]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오. 모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Gmail] 모듈을 사용하려면 [!DNL Gmail] 계정이 있어야 합니다.

## Workfront Fusion에 [!DNL Gmail] 연결 {#connect-gmail-to-workfront-fusion}

* [&#x200B; [!DNL Gmail] 을(를) 사용하여  [!DNL Google Workspace]Workfront Fusion 연결](#connect-gmail-to-workfront-fusion-usinggoogle-workspace)
* [&#x200B; [!DNL Gmail] or [!DNL gmail.com] .com을 사용하여  [!DNL googlemail]Workfront Fusion에 연결](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### [!DNL Gmail]을(를) 사용하여 [!DNL &#x200B; Google Workspace]을(를) Workfront Fusion에 연결

[!DNL Google Workspace] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

### [!DNL Gmail] 또는 [!DNL gmail.com].com을 사용하여 [!DNL googlemail]을(를) Workfront Fusion에 연결

[!DNL @gmail.com] 또는 [!DNL @googlemail.com] 사용자인 경우 [클라이언트 ID [!DNL Google Cloud Platform] 및 &#x200B;](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project)클라이언트 암호[!UICONTROL 를 가져오려면 &#x200B;]the에 OAuth 클라이언트를 만들어야 합니다.

OAuth 클라이언트를 만들고 [!UICONTROL 클라이언트 ID] 및 [!UICONTROL 클라이언트 암호]를 얻는 방법에 대한 단계별 지침은 [사용자 지정 OAuth 클라이언트를 사용하여 Adobe Workfront Fusion을 Google Services에 연결](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)을 참조하십시오.

## [!DNL Gmail]개 모듈 및 해당 필드

[!DNL Gmail] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Gmail] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [반복기](#iterators)

### 트리거

#### [!UICONTROL 전자 메일 보기]

이 트리거 모듈은 처리할 새 이메일이 수신되면 시나리오를 실행합니다.

모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드 또는 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>보려는 전자 메일 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 필터 유형] </td> 
   <td> <p>전자 메일 시청에 사용할 필터 유형 선택</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 단순 필터]</strong> </p> <p>[!UICONTROL Criteria], [!UICONTROL 발신자 이메일 주소], [!UICONTROL 제목] 및 [!UICONTROL 검색 구문] 필드를 채웁니다.</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail 필터]</strong> </p> <p>[!UICONTROL 쿼리] 필드에 이메일을 필터링하는 데 사용할 쿼리를 입력합니다.</p> <p>[!DNL Gmail] 필터에 대한 자세한 내용은 <a href="https://support.google.com/mail/answer/7190"> 설명서에서 </a>검색 구체화[!DNL Gmail]를 참조하십시오.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 기준]</td> 
   <td>[!UICONTROL all email], [!UICONTROL only read emails] 또는 [!UICONTROL only unread] 이메일을 시청할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 발신자 이메일 주소]</td> 
   <td> <p> 해당 주소에서 전송된 이메일만 시청하려면 이메일 주소를 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>제목에서 해당 텍스트 문자열이 있는 이메일만 보려면 텍스트 문자열을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>이메일의 어디에나 해당 텍스트 문자열이 있는 이메일만 보려면 텍스트 문자열을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 이메일 메시지를 가져올 때 읽음으로 표시]</td> 
   <td> <p> 검색된 이메일을 읽은 것으로 표시하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 최대 결과 수]</td> 
   <td> <p> 한 주기 동안 Workfront Fusion이 사용할 최대 결과 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

<!--* [Add labels](#add-labels)-->
* [[!UICONTROL 전자 메일 복사]](#copy-an-email)
* [[!UICONTROL 초안 만들기]](#create-a-draft)
* [[!UICONTROL 전자 메일 삭제]](#delete-an-email)
  <!--* [Delete labels](#delete-labels)-->
* [[!UICONTROL 전자 메일을 읽은 상태로 표시]](#mark-an-email-as-read)
* [[!UICONTROL 메일을 읽지 않음으로 표시]](#mark-an-email-as-unread)
* [[!UICONTROL 전자 메일 이동]](#move-an-email)
* [[!UICONTROL 전자 메일 레이블 수정]](#modify-email-labels)
* [[!UICONTROL 전자 메일 보내기]](#send-an-email)
  <!--* [Set labels](#set-labels)-->

<!--#### Add labels-->

#### [!UICONTROL 전자 메일 복사]

이 작업 모듈은 이메일 또는 이메일 초안을 사용자가 지정하는 폴더로 복사합니다.

폴더, 대상 폴더 및 전자 메일의 ID를 지정합니다.

모듈은 전자 메일의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>복사할 전자 메일이 포함된 [!DNL Gmail] 원본 폴더를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 대상 폴더]</td> 
   <td> <p>전자 메일을 복사할 대상 폴더 [!DNL Gmail]을(를) 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 이메일 ID (UID)]</td> 
   <td> <p>복사할 이메일의 이메일 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 초안 만들기]

이 작업 모듈은 새 이메일 초안을 만들어 지정한 폴더에 추가합니다.

초안을 생성할 폴더를 지정합니다.

모듈은 연결이 액세스하는 사용자 지정 필드 및 값과 함께 이메일 초안의 ID와 관련 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>초안을 만들 [!DNL Gmail] 폴더를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p><strong>[!UICONTROL 추가]</strong>를 클릭한 다음 각 수신자의 전자 메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>이메일 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>이메일 콘텐츠(메시지 본문)를 입력하거나 매핑합니다. HTML 태그가 허용됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 첨부 파일] </td> 
   <td> <p>첨부 파일을 추가하려면 <strong>[!UICONTROL 추가]</strong>를 클릭하십시오. 이전 모듈에서 파일을 매핑할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> <strong>[!UICONTROL 추가]</strong>를 클릭한 다음 각 복사 수신자의 전자 메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> <strong>[!UICONTROL Add]</strong>을(를) 클릭한 다음 각 Blind Copy 받는 사람의 전자 메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 전자 메일 삭제]

이 작업 모듈은 지정한 폴더에서 이메일 또는 이메일 초안을 제거합니다.

모듈은 전자 메일의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] 메시지 ID]</p> </td> 
   <td> <p>삭제하려는 이메일의 이메일 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>모듈이 이메일을 휴지통 폴더로 이동하는 대신 영구적으로 삭제할 수 있도록 하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Delete labels-->



#### [!UICONTROL 전자 메일을 읽은 상태로 표시]

이 작업 모듈은 이메일을 읽은 것으로 표시합니다.

이메일과 해당 폴더의 ID를 지정합니다.

모듈은 전자 메일의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>전자 메일이 포함된 [!DNL Gmail] 폴더를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 이메일 ID (UID)]</td> 
   <td> <p> 이메일 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메일을 읽지 않음으로 표시]

이 작업 모듈은 이메일 또는 이메일 초안을 읽지 않음으로 표시합니다.

이메일과 해당 폴더의 ID를 지정합니다.

모듈은 전자 메일의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>전자 메일이 포함된 [!DNL Gmail] 폴더를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 이메일 ID (UID)] </td> 
   <td> <p>읽지 않음으로 표시할 전자 메일의 전자 메일 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 전자 메일 레이블 수정]

이 작업 모듈은 지정한 이메일 메시지의 레이블을 수정합니다.

모듈은 전자 메일의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] 메시지 ID]</td> 
   <td> <p> 삭제하려는 이메일의 이메일 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>추가할 [!UICONTROL 레이블]</p> </td> 
   <td> <p>추가할 레이블을 선택한 이메일 메시지에 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>제거할 [!UICONTROL 레이블]</td> 
   <td> <p> 선택한 이메일 메시지에서 제거할 레이블을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL 추가할 레이블] 및 [!UICONTROL 제거할 레이블] 필드는 사용자가 만든 레이블만 로드합니다.

#### [!UICONTROL 전자 메일 이동]

이 작업 모듈은 이메일 또는 이메일 초안을 사용자가 지정하는 폴더로 이동합니다.

폴더, 대상 폴더 및 전자 메일의 ID를 지정합니다.

모듈은 전자 메일의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>이동할 전자 메일이 포함된 [!DNL Gmail] 원본 폴더를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 대상 폴더]</td> 
   <td> <p> 전자 메일을 이동할 [!DNL Gmail] 대상 폴더를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 이메일 ID (UID)]</td> 
   <td> <p> 이동할 전자 메일의 전자 메일 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 전자 메일 보내기]

이 작업 모듈은 새 이메일을 전송합니다.

전자 메일 수신자를 지정합니다.

모듈은 전자 메일의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Gmail] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Gmail] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>발신자 이메일 주소를 입력하거나 매핑합니다.</p> <p>참고: 잘못된 이메일 주소를 입력하면 계정에 내 주소가 아닌 다른 주소에서 이메일을 보낼 수 있는 권한이 없을 수 있으므로 메시지를 보낼 때 오류가 발생할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p><strong>[!UICONTROL 추가]</strong>를 클릭한 다음 각 수신자의 전자 메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>이메일 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>이메일 콘텐츠(메시지 본문)를 입력하거나 매핑합니다. HTML 태그가 허용됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 첨부 파일] </td> 
   <td> <p>첨부 파일을 추가하려면 <strong>[!UICONTROL 추가]</strong>를 클릭하십시오. 이전 모듈에서 파일을 매핑할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> <strong>[!UICONTROL 추가]</strong>를 클릭한 다음 각 복사 수신자의 전자 메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> <strong>[!UICONTROL Add]</strong>을(를) 클릭한 다음 각 Blind Copy 받는 사람의 전자 메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Set labels-->

### 반복기

#### [!UICONTROL 첨부 파일 반복]

이메일 첨부 파일을 반복할 수 있습니다. 각 첨부 파일은 모듈의 출력에 있는 별도의 번들입니다. 자세한 내용은 [반복자 모듈](/help/workfront-fusion/references/modules/iterator-module.md)을 참조하세요.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source 모듈] </td> 
   <td> <p>첨부 파일을 반복할 모듈을 선택합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
