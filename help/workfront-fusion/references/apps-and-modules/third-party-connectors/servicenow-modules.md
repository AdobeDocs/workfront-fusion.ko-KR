---
title: ServiceNow 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는  [!DNL ServiceNow]을(를) 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 0%

---

# [!DNL ServiceNow]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL ServiceNow]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 플랜*</td>
  <td> <p>[!UICONTROL Pro] 이상</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재 라이선스 요구 사항: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합을 위한 [!UICONTROL [!DNL Workfront Fusion]] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>현재 제품 요구 사항: [!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Adobe Workfront] 플랜이 있는 경우 조직에서 이 문서에 설명된 기능을 사용하려면 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다. [!DNL Workfront Fusion]이(가) [!UICONTROL Ultimate] [!DNL Workfront] 계획에 포함되어 있습니다.</p>
   <p>또는</p>
   <p>레거시 제품 요구 사항: 이 문서에 설명된 기능을 사용하려면 조직에서 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

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
   <td>https://{{connection.instance}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL ServiceNow]을(를) [!DNL Workfront Fusion]에 연결

[!DNL ServiceNow] 모듈에 대한 연결을 만들려면:

1. 첫 번째 [!DNL ServiceNow] 모듈 구성을 시작할 때 [!UICONTROL Connection] 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 다음을 입력합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>새 [!DNL ServiceNow] 연결의 이름 입력</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Username]</p> </td> 
      <td>[!DNL ServiceNow] 사용자 이름을 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>ServiceNow 암호를 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instance]</p> </td> 
      <td> <p><code>https://</code> 없이 [!DNL ServiceNow] 계정의 주소를 입력하십시오(일반적으로 <code>&lt;company>.service-now.com</code>).</p> </td> 
     </tr> 
    </tbody> 
   </table>

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow]개 모듈 및 해당 필드

[!DNL ServiceNow] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL ServiceNow] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>&quot;[!UICONTROL Record type]&quot; 필드에서 사용자 지정 레코드를 선택한 경우 사용자 지정 필드를 로드하는 데 시간이 걸릴 수 있습니다.
>
>사용자 지정 레코드가 없으면 드롭다운이 비어 있습니다.

* [[!UICONTROL Watch records]](#watch-records)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Deactivate a User]](#deactivate-a-user)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Search for records]](#search-for-records)

### [!UICONTROL Watch records]

이 트리거 모듈은 레코드가 생성되거나 업데이트될 때 시나리오를 활성화합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>보려는 테이블이 사용자 지정 테이블인지 표준 테이블인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>보려는 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>표시할 값 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈에서 출력할 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>새 레코드와 업데이트된 레코드 중 어느 것을 보려는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Custom API Call]

이 작업 모듈을 사용하면 [!DNL ServiceNow] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL ServiceNow] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> <p>모듈이 상호 작용할 웹 서버의 주소를 입력합니다.</p> <p>상대 URL을 입력할 수 있습니다. 즉, 처음부터 프로토콜을 포함할 필요가 없습니다(예: <code>http://</code>). 이것은 상호작용이 서버에서 발생하고 있음을 웹 서버에 시사한다.</p> <p>For example: <code>[!DNL /api/conversations].create</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
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

### [!UICONTROL Read a record]

이 작업 모듈은 시스템 ID를 사용하여 [!DNL ServiceNow] 레코드를 읽습니다.

모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>모듈에서 읽을 레코드의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>읽으려는 레코드가 사용자 지정 테이블에 있는지 아니면 표준 테이블에 있는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>모듈에서 읽을 [!DNL ServiceNow] 레코드의 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>표시할 값 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈에서 출력할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Deactivate a User]

이 작업 모듈은 시스템 ID를 사용하여 [!DNL ServiceNow]의 사용자를 비활성화합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User System ID]</td> 
   <td> 모듈을 비활성화하려는 사용자의 고유한 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Download an attachment]

이 작업 모듈은 [!DNL ServiceNow] 레코드의 첨부 파일을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment System ID]</td> 
   <td> 모듈에서 다운로드할 첨부 파일의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Upload an attachment]

이 작업 모듈은 첨부 파일을 [!DNL ServiceNow] 레코드로 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table name]</td> 
   <td>첨부 파일을 업로드할 테이블의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>첨부 파일을 업로드할 시스템의 고유한 [!DNL ServiceNow] ID를 입력하거나 매핑하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>첨부 파일 이름 입력 또는 매핑</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File content]</td> 
   <td>[!DNL ServiceNow]에 업로드할 파일을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create a record]

이 작업 모듈은 새 [!DNL ServiceNow] 레코드를 만듭니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>사용자 지정 테이블에 레코드를 만들지 아니면 표준 테이블에 레코드를 만들지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>모듈을 만들 [!DNL ServiceNow] 레코드 형식을 선택하십시오. 그런 다음 이 레코드 종류에 사용 가능한 필드를 채울 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a record]

이 작업 모듈은 새 [!DNL ServiceNow] 레코드를 만듭니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>모듈을 업데이트할 레코드의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>업데이트할 레코드가 사용자 지정 테이블에 있는지 아니면 표준 테이블에 있는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>모듈을 업데이트할 [!DNL ServiceNow] 레코드의 형식을 선택하십시오. 그런 다음 이 레코드 종류에 사용 가능한 필드를 채울 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a record]

이 작업 모듈은 문제 또는 사용자를 삭제합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>인시던트를 삭제할지 사용자를 삭제할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>모듈에서 삭제할 레코드의 고유 [!DNL ServiceNow] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search for records]

이 모듈은 사용자가 선택한 기준을 사용하여 레코드를 검색합니다.

모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>ServiceNow 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">[!DNL ServiceNow]을(를) [!UICONTROL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>검색할 테이블이 사용자 지정 테이블인지 표준 테이블인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>검색할 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>모듈이 기준과 일치하는 모든 레코드를 반환할지 또는 기준에 일치하는 첫 번째 레코드만 반환할지 여부를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search type]</td> 
   <td> <p>모듈을 실행할 검색 유형을 선택합니다</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Advanced query]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Query]</p> <p>사용자 지정 검색 쿼리를 입력합니다. [!DNL ServiceNow] 사용자 지정 검색 쿼리에 대한 자세한 내용은 <a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow 쿼리 설명서</a>를 참조하세요.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Criteria]</p> <p>모듈에서 검색할 기준을 입력합니다. <!--For more information on setting up search filters, see <a href="." class="MCXref xref">Add a filter to a scenario in Adobe Workfront Fusion</a>.</p>--> </li> 
       <li> <p>[!UICONTROL Sort by]</p> <p>모듈에서 결과를 정렬할 기준 필드와 오름차순 또는 내림차순 정렬 여부를 나타냅니다.</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>표시할 값 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈에서 출력할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>
