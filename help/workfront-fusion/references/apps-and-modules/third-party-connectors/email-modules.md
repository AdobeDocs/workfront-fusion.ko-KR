---
title: 이메일 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 전자 메일 계정을 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.이렇게 하면 IMAP을 통해 전자 메일을 다운로드하고, SMTP를 통해 전자 메일을 보내고, 새 초안을 만들고, 한 폴더에서 다른 폴더로 전자 메일을 이동 및 복사하고, 전자 메일을 읽음 또는 읽지 않음으로 표시하고, 전자 메일을 삭제할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2460'
ht-degree: 0%

---

# 이메일 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 전자 메일 계정을 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.이렇게 하면 IMAP을 통해 전자 메일을 다운로드하고, SMTP를 통해 전자 메일을 보내고, 새 초안을 만들고, 한 폴더에서 다른 폴더로 전자 메일을 이동 및 복사하고, 전자 메일을 읽음 또는 읽지 않음으로 표시하고, 전자 메일을 삭제할 수 있습니다.

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

## 이메일을 Workfront Fusion에 연결 {#connect-your-email-to-workfront-fusion}

* [Google에 연결](#connect-to-google)
* [다른 전자 메일 서비스(IMAP)에 연결](#connect-to-other-email-services-smap)

### [!DNL Google]에 연결

[!DNL Google] 계정에 연결해야 하는 이메일 모듈로 시나리오를 만들려면 이 옵션을 사용하십시오. 범위가 제한된 계정입니다.

전자 메일 모듈 내에서 직접 [!DNL Google] 계정에 연결할 수 있습니다.

1. 전자 메일 모듈에서 [!UICONTROL 연결] 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 연결 유형으로 **[!DNL Google]**&#x200B;을(를) 선택하십시오.
1. 연결의 이름을 입력합니다.
1. (선택 사항) [!UICONTROL [!DNL Google] 클라이언트 ID] 및 [!UICONTROL 클라이언트 암호]를 입력합니다.
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

### 다른 전자 메일 서비스(IMAP)에 연결

IMAP 연결을 사용하면 사서함에 원격으로 액세스하고 사서함에서 메시지를 읽거나 조작할 수 있습니다. 대부분의 이메일 모듈에서 IMAP 연결을 사용합니다.

1. 전자 메일 모듈에서 [!UICONTROL 연결] 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 연결 유형으로 **[!UICONTROL 기타(SMTP)]**&#x200B;을(를) 선택하십시오.
1. 연결을 위한 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.
1. 목록에서 **[!UICONTROL 전자 메일 공급자]**&#x200B;를 선택하십시오. 이메일 공급자가 목록에 없는 경우 기타를 선택합니다.
1. 전자 메일 계정의 **[!UICONTROL 사용자 이름]** 및 **[!UICONTROL 암호]**&#x200B;를 입력하세요.
1. (조건부) 공급자가 목록에 없으면 **[!UICONTROL SMTP 서버]** 및 **[!UICONTROL 포트]**&#x200B;를 입력하고 **[!UICONTROL TLS(보안 연결)를 사용할지 여부를 지정]**&#x200B;합니다. 이 정보를 찾으려면 사서함의 [!UICONTROL 도움말] 섹션을 확인하십시오. 이 정보를 사용할 수 없는 경우 이메일 서비스 공급자에게 문의하십시오.
1. 자체 서명된 인증서를 사용하려면 **허가되지 않은 인증서 거부** 옵션을 활성화하고 자체 서명된 인증서를 업로드하십시오. 자세한 내용은 [자체 서명된 인증서 업로드](#upload-a-self-signed-certificate)를 참조하세요.
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

#### 자체 서명된 인증서 업로드

자체 서명된 인증서를 추가하려면 다음을 수행하십시오.

1. **추출**&#x200B;을 클릭합니다.
1. 추출 중인 파일 유형을 선택합니다.
1. 또는 인증서가 포함된 파일을 선택합니다.
1. 파일의 암호를 입력합니다.
1. **저장**&#x200B;을 클릭하여 파일을 추출하고 모듈 설정으로 돌아갑니다.

## [!UICONTROL 전자 메일] 모듈 및 해당 필드

[!UICONTROL 전자 메일] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준과 같은 요소에 따라 추가 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

시나리오의 다른 모듈에서 사용했으므로 일부 이메일 필드에 데이터가 이미 포함되어 있을 수 있습니다. 이에 대한 정보가 필요한 경우 이메일 도움말 설명서를 참조하십시오.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>&#39;[!UICONTROL 전자 메일 ID(UID)]&#39;(으)로 알려진 고유한 전자 메일 ID가 전자 메일의 식별자입니다. 이메일 ID는 각 이메일 폴더에 대해 고유합니다.

* [트리거](#triggers)
* [액션](#actions)
* [반복기](#iterators)

### 트리거

#### [!UICONTROL 전자 메일 보기]

이 트리거 모듈은 지정된 기준에 따라 처리를 위해 새 이메일이 수신되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더] </td> 
   <td> <p>보려는 전자 메일이 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 기준]</p> </td> 
   <td> <p>전자 메일을 볼 기준을 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL 모든 이메일]</li> 
     <li>[!UICONTROL 읽기 전용 이메일]</li> 
     <li>[!UICONTROL 읽지 않은 이메일만]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 발신자 이메일 주소] </td> 
   <td> <p>보려는 이메일을 보낸 사람의 이메일 주소를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>보려는 전자 메일의 제목을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>키워드를 입력하여 해당 키워드가 포함된 이메일만 시청합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 가져올 때 읽은 상태로 메시지 표시]</td> 
   <td> <p>세부 정보를 검색한 후 읽지 않은 이메일을 읽은 상태로 표시하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 최대 결과 수]</td> 
   <td> <p> 시나리오 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환해야 하는 최대 전자 메일 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 전자 메일 복사]](#copy-an-email)
* [[!UICONTROL 초안 만들기]](#create-a-draft)
* [[!UICONTROL 전자 메일 삭제]](#delete-an-email)
* [[!UICONTROL 전자 메일 가져오기]](#get-emails)
* [[!UICONTROL 이메일을 읽은 상태로 표시]](#mark-an-email-as-read)
* [[!UICONTROL 메일을 읽지 않음으로 표시]](#mark-an-email-as-unread)
* [[!UICONTROL 전자 메일 이동]](#move-an-email)
* [[!UICONTROL 전자 메일 보내기]](#send-an-email)

#### [!UICONTROL 전자 메일 복사]

이 작업 모듈은 이메일 또는 초안을 선택한 폴더로 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 폴더]</td> 
   <td>이메일을 복사할 폴더를 선택합니다. 예: 기본.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 대상 폴더]</td> 
   <td> <p> 이메일을 복사할 폴더를 선택합니다. 예: 작업.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이메일 ID (UID)]</p> </td> 
   <td> <p>대상 폴더로 복사할 이메일의 이메일 UID을 입력합니다.</p> <p>[!UICONTROL Email] &gt; [!UICONTROL Watch Email] 모듈 또는 [!UICONTROL Search Email] 모듈을 사용하여 이메일의 UID을 가져올 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 초안 만들기]

이 작업 모듈은 선택한 폴더에 새 초안을 만들어 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더]</td> 
   <td>초안 이메일을 만들 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>이메일을 보낼 이메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>이메일의 제목 줄을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>HTML 태그를 사용하여 HTML 형식 또는 일반 텍스트로 이메일 콘텐츠를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 첨부 파일]</p> </td> 
   <td> <p>추가할 각 첨부 파일에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 파일 이름]</strong> </p> <p>확장자를 포함하여 파일 이름을 입력합니다. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>첨부 파일을 업로드할 폴더의 경로를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>콘텐츠에 첨부 파일(이미지)을 삽입하려면 콘텐츠 ID를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사본 수신자] </td> 
   <td> <p>이 전자 메일의 복사본을 보낼 각 전자 메일 주소에 대해 <b>항목 추가</b>를 클릭하고 전자 메일 주소를 입력하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> 전자 메일 주소가 전자 메일에 표시되지 않고 이 전자 메일 복사본을 보낼 각 전자 메일 주소에 대해 <b>항목 추가</b>를 클릭하고 전자 메일 주소를 입력하십시오.</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, [!DNL Workfront Fusion] uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL 전자 메일 삭제]

이 작업 모듈은 선택한 폴더에서 이메일 또는 초안을 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더]</td> 
   <td>삭제하려는 이메일이 포함된 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이메일 ID (UID)]</p> </td> 
   <td> <p>삭제하려는 이메일의 이메일 UID을 입력합니다.</p> <p>이메일 &gt; 이메일 보기 모듈 또는 [!UICONTROL 검색 이메일] 모듈을 사용하여 이메일의 UID을 가져올 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Exponge]</td> 
   <td> <p>현재 열려 있는 사서함에서 [!UICONTROL Deleted](으)로 플래그가 지정된 모든 메시지를 영구적으로 제거하려면 이 옵션을 활성화합니다.</p> <p>참고: [!DNL Gmail]에서 이 동작은 [!UICONTROL 설정] &gt;[!UICONTROL Forwarding POP/IMAP in IMAP access] 섹션의 설정에 의해 결정됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 전자 메일 가져오기]

이 모듈은 지정된 기준과 일치하는 이메일을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더] </td> 
   <td> <p>검색할 이메일이 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 가져올 때 읽은 상태로 메시지 표시] </td> 
   <td> <p>세부 정보를 검색한 후 읽지 않은 이메일을 읽은 상태로 표시하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 기준]</p> </td> 
   <td> <p>검색할 이메일의 기준을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 모든 이메일]</li> 
     <li>[!UICONTROL 읽기 전용 이메일]</li> 
     <li>[!UICONTROL 읽지 않은 이메일만]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 발신자 이메일 주소] </td> 
   <td> <p>이메일을 검색할 발신자의 이메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 수신자 이메일]</td> 
   <td> <p> 검색할 이메일의 수신자 이메일 주소를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작 날짜] </td> 
   <td> <p>지정된 날짜 또는 그 이후에 처리된 이메일을 검색할 날짜를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before date]</td> 
   <td> <p> 지정된 날짜 이전에 처리된 이메일을 검색하려면 날짜를 입력하거나 매핑하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>검색할 이메일의 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>키워드를 입력하거나 매핑하여 해당 키워드가 포함된 이메일만 검색하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이메일 ID (UID)]</td> 
   <td> <p> 세부 정보를 검색할 이메일의 이메일 ID(UID)를 입력합니다.</p> <p>[!DNL Workfront Fusion]의[!UICONTROL 시계 이메일] 모듈 또는 [!UICONTROL 검색 이메일] 모듈을 사용하여 이메일의 UID을 가져올 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 최대 결과 수]</td> 
   <td> <p> 시나리오 실행 주기 동안 최대 [!DNL Workfront Fusion] 전자 메일 수가 반환되어야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모듈이 결과를 반환하지 않더라도 라우트 실행을 계속합니다.]</td> 
   <td> <p> 반환된 결과가 없더라도 모듈을 계속 실행하려면 를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 이메일을 읽은 상태로 표시]

이 작업 모듈은 [!UICONTROL 읽기] 플래그를 설정하여 선택한 폴더의 전자 메일 또는 초안을 읽은 것으로 표시합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더]</td> 
   <td>읽음으로 표시할 이메일이 포함된 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이메일 ID (UID)]</p> </td> 
   <td> <p>읽음으로 표시할 이메일의 이메일 UID을 입력합니다.</p> <p>이메일 &gt; 이메일 보기 모듈 또는 [!UICONTROL 검색 이메일] 모듈을 사용하여 이메일의 UID을 가져올 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 메일을 읽지 않음으로 표시]

읽지 않음 플래그를 설정하여 선택한 폴더의 전자 메일 또는 초안을 읽지 않음으로 표시합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더]</td> 
   <td>읽지 않음으로 표시할 전자 메일이 포함된 폴더를 선택합니다. 예: 기본.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이메일 ID (UID)]</p> </td> 
   <td> <p>읽지 않음으로 표시할 전자 메일의 전자 메일 UID을 입력합니다.</p> <p>이메일 &gt; 이메일 보기 모듈 또는 [!UICONTROL 검색 이메일] 모듈을 사용하여 이메일의 UID을 가져올 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 전자 메일 이동]

선택한 이메일 또는 초안을 선택한 폴더로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!UICONTROL Workfront Fusion]에 전자 메일 계정을 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 폴더]</td> 
   <td>이동할 전자 메일이 포함된 폴더를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 대상 폴더]</td> 
   <td> <p> 이메일을 추가할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이메일 ID (UID)]</p> </td> 
   <td> <p>대상 폴더로 이동할 이메일의 이메일 UID을 입력합니다.</p> <p>이메일 &gt; 이메일 보기 모듈 또는 [!UICONTROL 검색 이메일] 모듈을 사용하여 이메일의 UID을 가져올 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 전자 메일 보내기]

새 이메일을 전송합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>전자 메일 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 전자 메일 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 전송 후 메시지 저장]</td> 
   <td>전자 메일 메시지가 전송되면 사서함에 저장됩니다. [!DNL Workfront Fusion]을(를) 사용하여 보낸 전자 메일을 사서함의 <i>[!UICONTROL 보낸 메일]</i> 폴더 또는 다른 폴더에 저장하려면 이 옵션을 활성화합니다. [!DNL Gmail]과(와) 같은 일부 이메일 서비스는 보낸 메시지를 자동으로 저장합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>이메일을 보낼 이메일 주소를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>이메일의 제목 줄을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 콘텐츠 유형]</p> </td> 
   <td> <p>이메일에 대한 [!UICONTROL content] 유형을 선택합니다.</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL 일반 텍스트]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>[!UICONTROL 콘텐츠 유형] 필드에서 선택한 내용에 따라 HTML 태그를 사용하여 HTML 형식이나 일반 텍스트로 이메일 콘텐츠를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 첨부 파일]</p> </td> 
   <td> <p>추가할 각 첨부 파일에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 파일 이름]</strong> </p> <p>확장자를 포함하여 파일 이름을 입력합니다. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>첨부 파일을 업로드할 폴더의 경로를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>콘텐츠에 첨부 파일(이미지)을 삽입하려면 콘텐츠 ID를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사본 수신자] </td> 
   <td> <p>이 전자 메일의 복사본을 보낼 각 전자 메일 주소에 대해 <b>항목 추가</b>를 클릭하고 전자 메일 주소를 입력하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> 전자 메일 주소가 전자 메일에 표시되지 않고 이 전자 메일 복사본을 보낼 각 전자 메일 주소에 대해 <b>항목 추가</b>를 클릭하고 전자 메일 주소를 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>이메일의 [!UICONTROL Sender] 필드에 표시되는 이메일 주소를 입력하거나 매핑합니다.</p> <p>팁: 이 필드를 사용할지 또는 부터 필드를 사용할지 확실하지 않은 경우 부터 필드를 선택하는 것이 좋습니다.</p> <p>중요: 올바른 구문 사용: <code>name@email.com</code> 또는 <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 회신 주소]</td> 
   <td> <p> 이 전자 메일에 대한 회신을 "보낸 사람" 주소가 아닌 다른 주소로 보내려면 이 전자 메일에 회신할 전자 메일 주소를 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> 특정 전자 메일에 회신하는 경우 회신하는 전자 메일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 참조] </td> 
   <td> <p>스레드에 있는 모든 응답의 메시지 ID를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 우선 순위]</p> </td> 
   <td> <p>이메일의 우선 순위 선택:</p> 
    <ul> 
     <li>[!UICONTROL 높음]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL 낮음]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>헤더를 추가합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 키]</strong> </p> <p>키를 추가합니다. 예: [!UICONTROL Sender], [!UICONTROL Date], [!UICONTROL To] 등.</p> </li> 
     <li> <p><strong>[!UICONTROL 값]</strong> </p> <p>키 값을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>이메일의 [!UICONTROL From] 필드에 표시되는 이메일 주소(및 필요한 경우 이름)를 입력하거나 매핑합니다. </p> <p>중요: 올바른 구문(<code>name@email.com</code> 또는 <code>"Name" name@email.com</code>)을 사용하십시오.</p> <p>참고: 일반적으로 [!DNL Workfront Fusion]은(는) 연결을 만들 때 입력한 전자 메일 주소를 보낸 사람 주소로 사용합니다. 다른 이메일 주소를 입력하면 계정에 내 주소가 아닌 다른 주소에서 이메일을 보낼 수 있는 권한이 없을 수 있으므로 메시지를 보낼 때 오류가 발생할 수 있습니다. 예: <code>test@mail.com</code> 또는 "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 반복기

#### [!UICONTROL 첨부 파일 반복]

수신한 첨부 파일을 하나씩 반복합니다.

이메일 반복기 모듈을 사용하면 이메일 첨부 파일을 별도로 관리할 수 있습니다. 예를 들어 이메일이 첨부 파일이 있는 이메일을 반복하고 경고를 수신하도록 설정할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 모듈]</td> 
   <td> <p>반복할 첨부 파일이 있는 전자 메일을 출력하는 모듈을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

반복기에 대한 자세한 내용은 [반복기 모듈](/help/workfront-fusion/references/modules/iterator-module.md)을 참조하세요.
