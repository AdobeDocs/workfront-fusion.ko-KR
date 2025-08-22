---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe 스토리지 모듈
description: Adobe Workfront Fusion 시나리오에서는 Adobe Admin Console에서 프로젝트를 만들고 관리할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 78ee905f-4713-44a4-bffb-c64cdb3665c2
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1400'
ht-degree: 3%

---

# Adobe 스토리지 모듈

Adobe Workfront Fusion 시나리오에서는 Adobe Admin Console에서 프로젝트를 만들고 관리할 수 있습니다.

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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## Adobe 스토리지에 대한 연결 만들기

Adobe 스토리지에 대한 연결을 만들려면 Adobe Developer Console과 Fusion에서 일부 구성이 필요합니다.

### Adobe Developer Console에서 프로젝트 구성

Adobe Developer Console에서 프로젝트에 API를 추가해야 합니다.

1. Adobe Developer Console에서 프로젝트를 엽니다.
1. **프로젝트에 추가**&#x200B;를 클릭하고 **API**&#x200B;을(를) 선택합니다.
1. 사용 가능한 API 목록에서 **Adobe Cloud Platform 및 Collaboration API**&#x200B;를 선택합니다.
1. 인증 유형 선택 화면에서 **OAuth 서버 간**&#x200B;을 선택하고 **다음**&#x200B;을 클릭합니다.
1. 자격 증명의 이름을 추가합니다.
1. **다음**&#x200B;을 클릭한 다음 **구성된 API 저장**&#x200B;을 클릭합니다.
1. Workfront Fusion에서 연결을 구성할 때 사용할 제공된 자격 증명을 메모하십시오.
1. 계속 [기술 계정을 Adobe Admin Console의 관리자로 지정](#make-your-technical-account-an-admin-in-the-adobe-admin-console)합니다.

### Adobe Admin Console에서 기술 계정을 관리자로 지정

Adobe Admin Console 페이지에서 상단 탐색 막대의 제품 탭을 선택한 다음 Workfront Fusion 을 선택합니다

1. 조직 내 기술 계정 사용자의 이메일 주소를 찾아 복사합니다.
1. 목록이 표시되면 맨 위에 있는 링크를 선택합니다.
1. 사용자가 작업하는 프로덕션 인스턴스입니다.
1. 표시되는 목록에서 제품 프로필 탭을 선택한 상태로 Workfront 제품 프로필 링크의 이름을 클릭합니다.

   이 목록에는 Workfront의 프로덕션 인스턴스에 이미 할당된 모든 사용자가 포함됩니다.

1. 사용자 목록 위에 있는 **관리자** 탭을 선택하십시오.
1. **관리자 추가**&#x200B;를 선택합니다.
1. 제품 프로필 관리자 추가 상자에서 기술 계정의 전자 메일 주소를 입력한 다음 **저장**&#x200B;을 선택합니다.

   기술 계정은 관리자가 됩니다.

1. [Workfront Fusion에서 연결 만들기](#create-the-connection-in-workfront-fusion)를 계속합니다.

### Workfront Fusion에서 연결 만들기

[!DNL Adobe Storage] 모듈에 대한 연결을 만들려면:

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL 연결 유형]</td>
        <td><code>Server to server</code>를 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>[!UICONTROL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. [!DNL Adobe Developer Console]에 있는 프로젝트의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. [!DNL Adobe Developer Console]에 있는 프로젝트의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS 조직 ID]</td>
        <td>Adobe IMS 조직 ID를 입력하거나 매핑합니다. <code> 123abc@AdobeOrg</code> 형식의 문자열입니다. 여기서 @ 앞의 섹션은 16진수입니다. 이 값은 Adobe Admin Console 또는 사용자 관리 통합을 위한 Adobe.IO 콘솔에서 조직의 URL 경로의 일부로 찾을 수 있습니다.</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## Adobe 스토리지 모듈 및 해당 필드

Adobe 사용자 관리 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Adobe 사용자 관리 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [ESM 스토어](#esm-stores)
* [초대](#invitations)
* [기타](#other)

### ESM 스토어

* [ESM 스토어 만들기](#create-an-esm-store)
* [ESM 스토어 삭제](#delete-an-esm-store)
* [ESM 스토어 버리기](#discard-an-esm-store)
* [ESM 저장소 복원](#restore-an-esm-store)

#### ESM 스토어 만들기

이 작업 모듈은 비즈니스 크리티컬한 자산을 구성하고 관리할 수 있도록 새로운 ESM(엔터프라이즈 스토리지 관리) 스토어를 설정합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe 저장소에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Adobe 저장소에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">프로젝트 이름</td> 
   <td>새 프로젝트의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### ESM 스토어 삭제

이 작업 모듈은 기존 ESM 저장소 및 모든 관련 데이터를 영구적으로 제거합니다. 이 작업은 실행 취소할 수 없습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe 저장소에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Adobe 저장소에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토어 ID</td> 
   <td>삭제하려는 스토어의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### ESM 스토어 버리기

이 작업 모듈은 영구적으로 제거하기 전에 유예 기간을 허용하면서 EMS 스토어에 삭제를 표시합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe 저장소에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Adobe 저장소에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토어 ID</td> 
   <td>삭제할 스토어의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### ESM 저장소 복원

이 작업 모듈은 이전에 삭제된 ESM 스토어를 복구하고 해당 데이터 및 구성에 대한 액세스를 복원합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe 저장소에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Adobe 저장소에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토어 ID</td> 
   <td>복원할 저장소의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 초대

#### 사용자 초대

이 작업 모듈은 새 사용자에게 특정 ESM 스토어에 대한 액세스 권한을 부여하는 초대를 보내어 공동 작업 및 파일 관리를 가능하게 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe 저장소에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Adobe 저장소에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이메일 주소</td> 
   <td>스토어에 초대하려는 사용자의 이메일 주소를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">자산 ID</td> 
   <td>사용자를 초대하려는 에셋의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">역할</td> 
   <td>새로 초대된 사용자가 에셋에 대해 가질 역할을 선택합니다.<ul><li>소유자</li><li>편집자</li><li>뷰어</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">댓글 작성 가능</td> 
   <td>이 옵션을 활성화하면 사용자가 에셋에 댓글을 달 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">공유 가능</td> 
   <td>사용자가 자산을 다른 사용자와 공유할 수 있도록 하려면 이 옵션을 활성화하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">수락 필요</td> 
   <td>이 옵션을 활성화하면 에셋에 대해 공동 작업을 수행하기 전에 사용자가 초대를 수락해야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">마운트 사용</td> 
   <td>초대받은 사람에 대해 리소스에 대한 마운트 지점을 만들어야 하는 경우 이 옵션을 활성화합니다. 이 옵션을 활성화하려면 수락 필수 옵션을 활성화해야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">알림 유형</td> 
   <td>사용자에게 초대에 대해 알리는 데 사용할 Adobe 알림 유형을 입력하거나 매핑합니다. 비워 두면 알림 유형은 자산의 mimetype을 기반으로 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">템플릿 이름</td> 
   <td>초대 이메일에 사용할 템플릿의 Adobe Post Office ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">로케일</td> 
   <td>언어 코드와 국가 코드 형태로 사용자 로케일을 입력합니다. <p>예: <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">외부</td> 
   <td>Adobe 초대 서비스 외부의 시스템을 사용하여 알림을 전송하려면 이 옵션을 true로 설정합니다. 외부 알림은 수락이 필요하지 않은 경우에만 지원됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 유형</td> 
   <td>에셋 유형을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">메시지</td> 
   <td>초대 이메일에 포함할 메시지를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">대상 URL</td> 
   <td>초대자가 자산을 보는 데 사용할 수 있는 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 기타

#### 사용자 지정 API 호출 만들기

이 작업 모듈은 Adobe 스토리지 API에 대한 사용자 지정 HTTP 요청을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
   <td>Adobe 저장소에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Adobe 저장소에 대한 연결 만들기</a>를 참조하십시오.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>상대 경로 입력 <code>https://ccprojects.adobe.io/api/v3/.</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>메서드</p>
      </td>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">헤더</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 인증 헤더와 x-api-key 헤더를 자동으로 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">쿼리 문자열  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">본문</td>
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
