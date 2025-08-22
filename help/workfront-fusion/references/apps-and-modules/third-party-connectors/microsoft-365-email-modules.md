---
title: Microsoft Office 365 전자 메일
description: Adobe Workfront Fusion 시나리오에서는 Microsoft Office 365 이메일을 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 5d4072ba-c598-4347-a42f-c59c7add0a1b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2915'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Email]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!UICONTROL Microsoft Office 365 이메일]을 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

[!DNL Microsoft Office 365 Email] 모듈을 사용하려면 [!DNL Microsoft Office 365 Email] 계정이 있어야 합니다.

## Microsoft Office 365 이메일 API 정보

Microsoft Office 365 이메일 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v2.6.5</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL Office 365 Email] 서비스 연결

[!DNL Office 365 Email] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion에 연결 만들기] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.

## [!DNL Microsoft Office 365 Email]개 모듈 및 해당 필드

[!DNL Microsoft Office 365 Email] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Microsoft Office 365 Email] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [메시지](#message)
* [초안 메시지](#draft-message)
* [첨부 파일](#attachment)
* [기타](#other)

### 메시지

* [[!UICONTROL 메시지 만들기 및 보내기(레거시)]](#create-and-send-a-message)
* [[!UICONTROL 메시지 삭제]](#delete-a-message)
* [[!UICONTROL 메시지 가져오기]](#get-a-message)
* [[!UICONTROL 메시지 이동]](#move-a-message)
* [[!UICONTROL 메시지 검색]](#search-messages)
* [[!UICONTROL 메시지 보기]](#watch-messages)



#### [!UICONTROL 메시지 만들기 및 보내기(레거시)]

이 작업 모듈은 이메일 메시지를 만들고 전송합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>메시지의 제목 줄을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>이메일의 메시지 본문 텍스트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 중요도]</td> 
   <td> <p>이메일의 중요도 선택</p> 
    <ul> 
     <li>[!UICONTROL 낮음]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL 높음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>전자 메일을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>전자 메일 복사본을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>전자 메일 복사본을 보내려는 각 받는 사람의 이름이나 전자 메일 주소를 다른 받는 사람이 볼 수 없도록 하려면 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 첨부 파일]</p> </td> 
   <td> <p>전자 메일에 추가할 각 첨부 파일에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source 파일]</strong> </p> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 인터넷 메시지 헤더]</td> 
   <td> <p>전자 메일에 추가할 각 헤더에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>헤더 이름 입력</p> </li> 
     <li> <p><strong>[!UICONTROL 값]</strong> </p> <p>헤더 값을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 삭제]

이 작업 모듈은 기존 이메일 메시지를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 삭제하려는 메시지의 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 가져오기]

이 작업 모듈은 특정 메시지의 메타데이터를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 메타데이터를 검색할 메시지의 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME 콘텐츠 가져오기]</td> 
   <td>메시지의 MIME 콘텐츠에 대한 데이터를 검색하려면 이 옵션을 활성화하십시오. [!UICONTROL MIME] 컨텐츠에는 이미지, 오디오, 비디오 또는 기타 유형의 파일이 포함될 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 이동]

이 작업 모듈은 전자 메일 메시지를 사서함의 선택한 폴더로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 다른 폴더로 이동할 메시지의 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메일 폴더] </td> 
   <td> <p>메시지를 이동할 폴더의 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 검색]

이 검색 모듈은 특정 기준에 따라 메시지를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL 메일 폴더]</td> 
   <td> <p>검색할 메시지가 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>검색 쿼리를 입력합니다. 검색 쿼리를 작성하는 방법에 대한 자세한 내용은 [!DNL Microsoft] 지원 문서 <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&rs=en-us&ad=us">메일 및 사람 검색 [!DNL Outlook.com]</a>을(를) 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>결과 정렬 방법을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 제목(오름차순 또는 내림차순)]</li> 
     <li>[!UICONTROL 생성된 날짜 시간(오름차순 또는 내림차순)]</li> 
     <li>[!UICONTROL 마지막 수정 날짜 시간(오름차순 또는 내림차순)]</li> 
     <li>[!UICONTROL 받은 날짜 시간(오름차순 또는 내림차순)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>한 시나리오 실행 주기 동안 Workfront Fusion이 반환해야 하는 최대 메시지 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 보기]

이 트리거 모듈은 새 이메일 메시지를 보내거나 받을 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 시청 메시지]</p> </td> 
   <td> <p>보려는 메시지 선택:</p> 
    <ul> 
     <li>[!UICONTROL 읽지 않은 항목만]</li> 
     <li>[!UICONTROL 읽기 전용]</li> 
     <li>[!UICONTROL All]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메일 폴더]</td> 
   <td> <p>보려는 메시지가 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>검색 쿼리를 입력합니다. 이 모듈은 이 쿼리와 일치하는 메시지를 반환합니다. 검색 쿼리를 작성하는 방법에 대한 자세한 내용은 [!DNL Microsoft] 지원 문서 <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&rs=en-us&ad=us">메일 및 사람 검색 [!DNL Outlook.com]</a>을(를) 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>한 시나리오 실행 주기 동안 Workfront Fusion이 반환해야 하는 최대 메시지 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 초안 메시지

* [초안 메시지 만들기](#create-a-draft-message)
* [초안 메시지 보내기](#send-a-draft-message)
* [메시지 업데이트](#update-a-message)

#### [!UICONTROL 초안 메시지 만들기]

이 작업 모듈은 새 이메일 메시지를 초안으로 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>메시지의 제목 줄을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문 컨텐츠 유형]</td> 
   <td>메시지의 본문 내용이 HTML인지 텍스트인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>이메일의 메시지 본문 텍스트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 중요도]</td> 
   <td> <p>이메일의 중요도 선택</p> 
    <ul> 
     <li>[!UICONTROL 낮음]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL 높음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>전자 메일을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>전자 메일 복사본을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>전자 메일 복사본을 보내려는 각 받는 사람의 이름이나 전자 메일 주소를 다른 받는 사람이 볼 수 없도록 하려면 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 첨부 파일]</p> </td> 
   <td> <p>전자 메일에 추가할 각 첨부 파일에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source 파일]</strong> </p> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 초안 메시지 보내기]

이 작업 모듈은 현재 초안 상태인 이메일 메시지를 보냅니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 초안 메시지 ID]</td> 
   <td> <p> 보낼 초안의 메시지 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 업데이트]

이 작업 모듈은 기존 메시지를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID 입력]</td> 
   <td> <p>업데이트할 메시지를 식별하는 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter Manually]</strong> </p> <p>메시지 ID를 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>업데이트할 메시지가 포함된 폴더를 선택한 다음 메시지를 선택합니다</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>메시지의 제목 줄을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>이메일의 메시지 본문 텍스트를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 중요도]</td> 
   <td> <p>이메일의 중요도 선택</p> 
    <ul> 
     <li>[!UICONTROL 낮음]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL 높음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>전자 메일을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>전자 메일 복사본을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>전자 메일 복사본을 보내려는 각 받는 사람의 이름이나 전자 메일 주소를 다른 받는 사람이 볼 수 없도록 하려면 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 첨부 파일]</p> </td> 
   <td> <p>전자 메일에 추가할 각 첨부 파일에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source 파일]</strong> </p> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 읽음으로 표시]</td> 
   <td>업데이트된 메시지를 읽은 상태로 표시하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 첨부 파일

* [[!UICONTROL 첨부 파일 다운로드]](#download-an-attachment)
* [[!UICONTROL 첨부 파일 나열]](#list-attachments)

#### [!UICONTROL 첨부 파일 다운로드]

이 모듈은 지정된 첨부 파일을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 다운로드하려는 첨부 파일이 포함된 메시지의 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 첨부 파일 ID]</td> 
   <td> <p>다운로드하려는 첨부 파일의 ID를 입력하거나 매핑합니다. 첨부 파일 목록 모듈을 사용하여 이 아이디어를 찾을 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 첨부 파일 나열]

이 모듈은 지정된 메시지에 속하는 첨부 파일 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 첨부 파일을 가져올 메시지의 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 첨부 파일 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [[!UICONTROL 첨부 파일 추가]](#add-an-attachment)
* [메시지 만들기 및 보내기](#create-and-send-a-message)
* [[!UICONTROL API 호출 만들기]](#make-an-api-call)

#### [!UICONTROL 첨부 파일 추가]

이 모듈은 메시지에 큰 첨부 파일을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 ID]</td> 
   <td> <p> 첨부 파일을 추가할 메시지의 ID를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 파일]</td> 
   <td> <p>이전 모듈에서 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메시지 만들기 및 보내기]

이 작업 모듈은 이메일 메시지를 만들고 전송합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>메시지의 제목 줄을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>이메일의 메시지 본문 텍스트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 중요도]</td> 
   <td> <p>이메일의 중요도 선택</p> 
    <ul> 
     <li>[!UICONTROL 낮음]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL 높음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>전자 메일을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>전자 메일 복사본을 보낼 각 받는 사람에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>전자 메일 복사본을 보내려는 각 받는 사람의 이름이나 전자 메일 주소를 다른 받는 사람이 볼 수 없도록 하려면 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>연락처의 이메일 주소를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>연락처의 이름을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 첨부 파일]</p> </td> 
   <td> <p>전자 메일에 추가할 각 첨부 파일에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source 파일]</strong> </p> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 인터넷 메시지 헤더]</td> 
   <td> <p>이메일에 대한 메시지 헤더를 추가합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 이름]</strong> </p> <p>헤더 이름 입력</p> </li> 
     <li> <p><strong>[!UICONTROL 전자 메일 주소]</strong> </p> <p>헤더 값을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL 보내는 사람 이메일 주소]</td> 
   <td> <p> 공유 전자 메일 주소를 사용하려면 여기에 주소를 입력하십시오. 이 모듈에 사용되는 연결에 자격 증명을 사용하는 사용자는 공유 폴더에 액세스할 수 있어야 합니다.<p>연결 소유자의 전자 메일 주소를 사용하려면 이 필드를 비워 둡니다.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL API 호출 만들기]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Office 365] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code>https://graph.microsoft.com</code>과(와) 관련된 경로를 입력하십시오. 예:<code> /v1.0/me/messages</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메서드]</p> </td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 예, <code>{"Content-type":"application/json"}</code>. Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p> 표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
