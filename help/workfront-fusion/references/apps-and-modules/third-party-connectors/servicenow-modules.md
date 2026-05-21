---
title: ServiceNow 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL ServiceNow]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
TQID: https://experienceleague.adobe.com/cIq5yfUbJsb3v8DbVjWv7hCP6kOkTbGmGouBirjETpo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1643
ht-degree: 43%

---

# [!DNL ServiceNow] 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL ServiceNow]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

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

[!DNL ServiceNow] 모듈을 사용하려면 [!DNL ServiceNow] 계정이 있어야 합니다.

## ServiceNow API 정보

ServiceNow 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td><pre><code>https://&#123;&#123;connection.instance&#125;&#125;/api</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL ServiceNow]를 Workfront Fusion에 연결

사용자의 [!DNL ServiceNow] 모듈에 연결하려면:

1. 첫 번째 [!DNL ServiceNow] 모듈 구성을 시작할 때 [!UICONTROL 연결] 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 다음을 입력하십시오.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 이름]</p> </td> 
      <td>새 [!DNL ServiceNow] 연결의 이름을 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 환경]</p> </td> 
      <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 암호]</p> </td> 
      <td>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 사용자 이름]</p> </td> 
      <td>[!DNL ServiceNow] 사용자 이름을 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 암호]</p> </td> 
      <td>ServiceNow 암호를 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 인스턴스]</p> </td> 
      <td> <p><code>https://</code> 없이 [!DNL ServiceNow] 계정의 주소를 입력하십시오(일반적으로 <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 저장하고 모듈로 돌아가려면 **계속**&#x200B;을 클릭합니다.

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow] 모듈 및 해당 필드

[!DNL ServiceNow] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL ServiceNow] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* &quot;[!UICONTROL 레코드 종류]&quot; 필드에서 사용자 지정 레코드를 선택한 경우 사용자 지정 필드를 로드하는 데 시간이 걸릴 수 있습니다.
>
>* 사용자 지정 레코드가 없으면 &quot;레코드 유형&quot; 필드 드롭다운이 비어 있습니다.

### 트리거

#### [!UICONTROL 레코드 보기]

이 트리거 모듈은 레코드가 생성되거나 업데이트될 때 시나리오를 활성화합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 유형]</td> 
   <td>보려는 테이블이 사용자 지정 테이블인지 표준 테이블인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td>보려는 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>표시할 값 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>모듈에서 출력할 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필터]</td> 
   <td>새 레코드와 업데이트된 레코드 중 어느 것을 보려는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 레코드 만들기]](#create-a-record)
* [[!UICONTROL 사용자 정의 API 호출]](#custom-api-call)
* [[!UICONTROL 사용자 비활성화]](#deactivate-a-user)
* [[!UICONTROL 레코드 삭제]](#delete-a-record)
* [[!UICONTROL 첨부 파일 다운로드]](#download-an-attachment)
* [[!UICONTROL 레코드 읽기]](#read-a-record)
* [[!UICONTROL 첨부 파일 업로드]](#upload-an-attachment)
* [[!UICONTROL 레코드 업데이트]](#update-a-record)

#### [!UICONTROL 레코드 만들기]

이 작업 모듈은 새 [!DNL ServiceNow] 레코드를 만듭니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 유형]</td> 
   <td>사용자 지정 테이블에 레코드를 만들지 아니면 표준 테이블에 레코드를 만들지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td>모듈을 만들 [!DNL ServiceNow] 레코드 형식을 선택하십시오. 그런 다음 이 레코드 종류에 사용 가능한 필드를 채울 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 정의 API 호출]

이 액션 모듈을 사용하면 [!DNL ServiceNow] API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL ServiceNow] 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상대 URL]</td> 
   <td> <code>https://&ltinstance_url&gt/api/</code>과 관련된 경로를 입력합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL 사용자 비활성화]

이 작업 모듈은 시스템 ID를 사용하여 [!DNL ServiceNow]의 사용자를 비활성화합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사용자 시스템 ID]</td> 
   <td> 모듈을 비활성화하려는 사용자의 고유한 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 삭제]

이 작업 모듈은 문제 또는 사용자를 삭제합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td>인시던트를 삭제할지 사용자를 삭제할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시스템 ID]</td> 
   <td>모듈에서 삭제할 레코드의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 첨부 파일 다운로드]

이 작업 모듈은 [!DNL ServiceNow] 레코드의 첨부 파일을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 첨부 파일 시스템 ID]</td> 
   <td> 모듈에서 다운로드할 첨부 파일의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 읽기]

이 작업 모듈은 시스템 ID를 사용하여 [!DNL ServiceNow] 레코드를 읽습니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 시스템 ID]</td> 
   <td>모듈에서 읽을 레코드의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 유형]</td> 
   <td>읽으려는 레코드가 사용자 지정 테이블에 있는지 아니면 표준 테이블에 있는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td>모듈에서 읽을 [!DNL ServiceNow] 레코드의 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>표시할 값 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>모듈에서 출력할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 업데이트]

이 작업 모듈은 새 [!DNL ServiceNow] 레코드를 만듭니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 시스템 ID]</td> 
   <td>모듈을 업데이트할 레코드의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 유형]</td> 
   <td>업데이트할 레코드가 사용자 지정 테이블에 있는지 아니면 표준 테이블에 있는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td>모듈을 업데이트할 [!DNL ServiceNow] 레코드의 형식을 선택하십시오. 그런 다음 이 레코드 종류에 사용 가능한 필드를 채울 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 첨부 파일 업로드]

이 작업 모듈은 첨부 파일을 [!DNL ServiceNow] 레코드로 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 이름]</td> 
   <td>첨부 파일을 업로드할 테이블의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시스템 ID]</td> 
   <td>첨부 파일을 업로드할 항목의 고유한 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

#### [!UICONTROL 레코드 검색]

이 모듈은 사용자가 선택한 기준을 사용하여 레코드를 검색합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>ServiceNow 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL ServiceNow] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 테이블 유형]</td> 
   <td>검색할 테이블이 사용자 지정 테이블인지 표준 테이블인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td>검색할 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 결과 집합]</td> 
   <td>모듈이 기준과 일치하는 모든 레코드를 반환할지 또는 기준에 일치하는 첫 번째 레코드만 반환할지 여부를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드의 최대 개수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 검색 유형]</td> 
   <td> <p>모듈을 실행할 검색 유형을 선택합니다</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 고급 쿼리]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL 검색 쿼리]</p> <p>사용자 지정 검색 쿼리를 입력합니다. [!DNL ServiceNow] 사용자 지정 검색 쿼리에 대한 자세한 내용은 <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow 쿼리 설명서</a>를 참조하세요.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL 검색 기준]</p> <p>모듈에서 검색할 기준을 입력합니다. </li> 
       <li> <p>[!UICONTROL 정렬 기준]</p> <p>모듈에서 결과를 정렬할 기준 필드와 오름차순 또는 내림차순 정렬 여부를 나타냅니다.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>표시할 값 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>모듈에서 출력할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>
