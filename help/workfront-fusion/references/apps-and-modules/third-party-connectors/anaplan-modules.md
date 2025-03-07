---
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Anaplan을 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: defc5aa9b2e3ffa5c698c5a19dd8d9d8768d72c2
workflow-type: tm+mt
source-wordcount: '1983'
ht-degree: 1%

---

# [!DNL Anaplan]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Anaplan]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
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

[!DNL Anaplan] 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 [!UICONTROL Anaplan] 계정이 있어야 합니다.
* [!DNL Workfront Fusion]이(가) 작업 공간, 모델 및 [!UICONTROL Anaplan] 계정에서 다른 [!DNL Anaplan] 개체와 상호 작용하려면 먼저 해당 개체를 구성해야 합니다.

## Anaplan API 정보

Anaplan 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>https://api.anaplan.com/2/0/
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.11.5</td> 
 </tbody> 
</table>

## [!DNL Anaplan]을(를) [!DNL Workfront Fusion]에 연결 {#connect-anaplan-to-workfront-fusion}

[!DNL Anaplan] 모듈에 대한 연결을 만들려면:

1. [!UICONTROL 연결] 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>
          <p>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>
          <p>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL email]</td>
        <td>
          <p>이 Anaplan 계정의 이메일 주소를 입력하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Password]</td>
        <td>이 Anaplan 계정의 암호를 입력합니다.</td>
      </tr>
     </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

<!--1. Click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box.
1. Select the connection type.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL Basic] connection requires only an email address and password to create the connection. </p> <p>Enter a name for the connection, then enter your email address and the password of your [!DNL Anaplan] account.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL CA Certificate] connection requires a [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data]. You can generate these in your [!DNL Anaplan] account. For instructions, see the [!DNL Anaplan] documentation.</p> <p>Enter a name for the connection, then enter the [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data] that you generated in your [!DNL Anaplan] account.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.-->

## [!DNL Anaplan]개 모듈 및 해당 필드

[!DNL Anaplan] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Anaplan] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

#### [!DNL Watch records]

이 트리거 모듈은 선택한 유형의 레코드가 생성되거나 업데이트될 때 시나리오를 시작합니다.

>[!NOTE]
>
>이 모듈은 새 레코드의 데이터를 반환합니다. 수정된 기존 레코드의 데이터는 반환하지 않습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">조사할 오브젝트 유형</td> 
   <td>보려는 항목의 유형을 선택합니다. 이 유형의 레코드가 생성되거나 업데이트되면 시나리오가 시작됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">&lt;개체&gt; ID</td> 
   <td>Anaplan에서 보려는 객체와 연관된 모델 또는 모듈 등의 객체 ID를 입력합니다</td> 
  </tr> 
  <tr> 
   <td role="rowheader">제한</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 목록 항목 만들기]](#create-a-list-item)
* [레코드 삭제](#delete-a-record)
* [데이터 내보내기](#export-data)
* [데이터 가져오기](#import-data)
* [[!UICONTROL 사용자 지정 API 호출 만들기]](#make-a-custom-api-call)
* [[!UICONTROL 레코드 읽기]](#read-a-record)
* [[!UICONTROL 작업 실행]](#run-an-action)
* [[!UICONTROL 레코드 업데이트]](#update-a-record)
* [[!UICONTROL 파일 업로드]](#upload-a-file)

#### [!UICONTROL 목록 항목 만들기]

이 작업 모듈은 Anaplan의 목록에 새 항목을 추가합니다.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Connection]</td>
        <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Workspace ID]</td>
        <td>항목을 추가하려는 목록이 포함된 Anaplan Workspace의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 모델 ID]</td>
        <td>항목을 추가하려는 목록이 포함된 모델의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 목록 ID]</td>
        <td>항목을 만들 목록의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 이름]</td>
        <td>새 항목의 이름을 입력합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Code]</td>
        <td>새 항목에 대한 코드를 입력합니다. 코드는 사용자가 생성한 코드로서 동일한 이름의 라인 항목을 구분할 수 있습니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 상위]</td>
        <td>아래에서 새 항목을 생성할 상위 항목의 이름을 입력합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 속성]</td>
        <td>항목을 추가할 목록에 사용자 지정 속성이 있으면 값을 추가할 속성을 선택한 다음 값을 추가합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 하위 집합]</td>
        <td>항목을 추가할 목록에 사용자 정의 하위 집합이 있는 경우 항목을 추가할 하위 집합을 선택합니다.</td>
    </tr>
</table>

#### [!UICONTROL 레코드 삭제]

이 작업 모듈은 기존 레코드를 삭제합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>삭제하려는 개체가 포함된 Anaplan Workspace의 ID를 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델 ID]</td> 
   <td>삭제하려는 개체가 포함된 모델의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>삭제할 오브젝트의 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><b>작업</b> </p> <p>삭제할 작업을 선택하거나 매핑합니다.</p> </li> 
     <li> <p><b>목록 항목</b> </p> <p>항목을 삭제할 목록을 선택한 다음 삭제할 항목의 ID 또는 코드를 입력하거나 매핑합니다</p>  </li> 
     <li> <p><b>[!UICONTROL 파일]</b> </p> <p>삭제할 파일을 선택하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL 데이터 내보내기]

이 작업 모듈은 내보내기 정의 를 사용하여 Anaplan에서 데이터를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>내보내려는 데이터가 포함된 Anaplan Workspace의 ID를 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델 ID]</td> 
   <td>내보낼 데이터가 포함된 모델의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">내보내기 정의 ID</td> 
   <td> <p>사용하려는 Anaplan 내보내기 정의의 ID를 입력하거나 매핑합니다.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### 데이터 가져오기

이 작업 모듈은 데이터를 Anaplan으로 가져옵니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>데이터를 가져올 Anaplan Workspace의 ID를 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델 ID]</td> 
   <td>데이터를 가져올 모델의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">내보내기 정의 ID</td> 
   <td> <p>사용하려는 Anaplan 가져오기 정의의 ID를 입력하거나 매핑합니다.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 지정 API 호출 만들기]

이 모듈에서는 [!DNL Anaplan] API에 대한 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>상대 경로 입력 <code>https://api.anaplan.com/2/0/</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메서드]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 인증 헤더를 자동으로 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열] </td> 
   <td> <p>요청 쿼리 문자열을 입력합니다.</p> </td> 
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

#### [!UICONTROL 레코드 읽기]

이 작업 모듈은 단일 레코드를 읽습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>읽을 레코드 종류를 선택하십시오.</p> 
    <ul> 
     <li> <p><b>모델</b> </p> <p>읽으려는 모델의 ID를 선택하거나 매핑합니다.</p> </li> 
     <li> <p><b>모델 목록</b> </p> <p>읽을 목록을 포함하는 Workspace 및 모델의 ID를 선택하거나 매핑한 다음 목록을 선택합니다. [!UICONTROL 데이터 유형] 필드에서 데이터를 읽을지 아니면 메타데이터를 읽을지 선택합니다.</p> </li> 
     <li> <p><b>모델 버전</b> </p> <p>읽으려는 모델의 ID를 선택하거나 매핑합니다.</p> </li> 
     <li> <p><b>사용자</b> </p> <p>사용 중인 계정 소유자에 대한 데이터를 반환할지 또는 다른 사용자에 대한 데이터를 반환할지 여부를 선택합니다. 다른 사용자를 선택하는 경우 해당 사용자의 이름을 선택합니다.</p> </li> 
     <li> <p><b>Workspace</b> </p> <p>읽으려는 Workspace의 ID를 선택하거나 매핑합니다.</p> </li> 
     <li> <p><b>보기</b> </p> <p>읽으려는 뷰가 포함된 모델의 ID를 선택하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 작업 실행]

이 작업 모듈은 작업을 가져오기, 내보내기, 삭제 또는 처리합니다.

<table style="table-layout:auto"> 
     <col/>
     <col/>
     <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection]</td>
        <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#Connect" class="MCXref xref" >[!UICONTROL Anaplan을 Workfront Fusion에 연결]</a>을 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Workspace ID]</td>
        <td>작업을 수행할 [!DNL Anaplan] Workspace의 ID를 선택하거나 매핑합니다.</td>
      </tr>
      <tr >
        <td role="rowheader">[!UICONTROL 모델 ID]</td>
        <td>작업을 수행할 모델의 ID를 선택하거나 매핑합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 작업 유형]</td>
        <td>
          <p>수행할 작업을 선택합니다</p>
            <ul>
              <li>
                <p><b>[!UICONTROL Delete]</b>
                </p>
                <p>삭제할 작업의 ID를 입력하거나 매핑합니다.</p>
              </li>
              <li>
                <p><b>[!UICONTROL Export]</b>
                </p>
                <p>사용할 내보내기 정의의 ID를 입력하거나 매핑합니다. 다음과 같은 파일 형식으로 내보낼 수 있습니다.</p>
                  <ul>
                    <li>
                      <p>XLS</p>
                    </li>
                    <li>
                      <p>XLSX</p>
                    </li>
                    <li>
                      <p>CSV</p>
                    </li>
                  </ul>
                </li>
                <li>
                  <p><b>[!UICONTROL 가져오기] </b>
                  </p>
                  <p style="font-weight: normal;">사용할 가져오기 정의의 ID를 입력하거나 매핑합니다.</p>
                </li>
                <li>
                 <p><b>[!UICONTROL 프로세스]</b>
                 </p>
                  <p>사용할 프로세스의 ID를 입력하거나 매핑합니다. </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL 레코드 업데이트]

이 작업 모듈은 [!UICONTROL Anaplan]의 단일 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>업데이트할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL 목록 항목]</b> </p> <p>필드의 경우 이 문서에서 <a href="#create-a-list-item" class="MCXref xref">목록 항목 만들기</a>를 참조하십시오.</p> </li> 
     <li> <p><b>[!UICONTROL 모듈 셀 데이터]</b> </p> <p>셀 데이터를 업데이트하면 해당 데이터를 사용하는 모든 다운스트림 계산도 업데이트됩니다.</p> <p>다음 필드를 채웁니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL 모델 ID]</b> </p> <p>업데이트할 셀이 포함된 모델을 선택하거나 매핑합니다.</p> </li> 
       <li> <p><b>[!UICONTROL 모듈 ID]</b> </p> <p>업데이트할 셀이 포함된 모듈을 선택하거나 매핑합니다.</p> </li> 
       <li> <p><b>[!UICONTROL 라인 항목 이름]</b> </p> <p>업데이트할 셀의 라인 항목을 선택하거나 매핑합니다.</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>라인 항목에 있는 차원을 선택하거나 매핑합니다.</p> 
       <p><b>참고: </b> 
       <ul>
       <li> Dimension 키(값)는 <code>dimensionName</code>(다음) 또는 <code>dimensionId</code>(ID)이어야 합니다.</li>
       <li>항목 키(값)는 <code>itemName</code>(텍스트), <code>itemCode</code>(텍스트) 또는 <code>itemId</code>(ID)여야 합니다.</li>
       <li>Dimension 및 항목 키는 동일한 유형(텍스트 또는 ID)이어야 합니다.
       </ul>
        </p> 
        <p>차원에 대한 자세한 내용을 보려면 [!DNL Anaplan Anapedia]에서 차원을 검색하십시오.</p> </li> 
       <li> <p><b>[!UICONTROL 값]</b> </p> <p>셀의 새 값을 입력하거나 매핑합니다.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL 모델 현재 회계 연도]</b> </p> <p>회계 연도를 갱신할 모델의 Workspace ID 및 모델 ID를 입력한 다음 모델에 대한 새 연도를 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 작업에 대한 파일 업로드]

이 작업 모듈은 Anaplan의 기존 파일을 Anaplan 내의 추가 위치로 업로드합니다.
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL Connection]</td>
<td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Workspace ID]</td>
<td>파일을 업로드할 [!DNL Anaplan] Workspace의 ID를 선택하거나 매핑합니다.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL 모델 ID]</td>
<td>파일을 업로드할 모델의 ID를 선택하거나 매핑합니다.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL 파일 ID]</td>
<td>업로드할 파일의 ID를 선택하거나 매핑합니다.</td>
</tr>
</tbody>
</table>
</div>

### 검색 결과

#### [!UICONTROL 레코드 가져오기]

이 검색 모듈은 선택한 유형의 액세스 가능한 모든 레코드를 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Anaplan]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">[!DNL Anaplan]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>검색할 레코드 유형을 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Workspaces]</b> </p> </li> 
       <li> <p><b>[!UICONTROL 모델]</b> </p> </li> 
       <li> <p><b>[!UICONTROL 라인 항목]</b> </p> <p>검색할 [!DNL line] 항목이 포함된 모델의 ID를 선택하거나 매핑합니다.</p> </li> 
       <li> <p><b>[!UICONTROL 모델 목록]</b> </p> <p>검색할 모델 목록이 포함된 Workspace의 ID와 모델 ID를 선택하거나 매핑합니다.</p> </li> 
       <li> <p><b>[!UICONTROL 모델 달력]</b> </p> <p>검색할 모델 캘린더가 포함된 Workspace의 ID를 선택하거나 매핑합니다.</p> </li> 
       <li> <p><b>[!UICONTROL 모델 버전]</b> </p> </li> 
       <li> <p>검색할 모델 버전이 포함된 모델 ID를 선택하거나 매핑합니다.</p> </li> 
       <li> <p><b>[!UICONTROL 사용자]</b> </p> </li> 
       <li> <p><b>[!UICONTROL 보기]</b> </p> <p>모듈별 뷰를 선택할지 모델별 뷰를 선택할지 선택한 다음 검색할 뷰가 포함된 모듈이나 모델의 ID를 선택하거나 매핑합니다.</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 공간 크기 반환]</td> 
   <td>작업 영역의 현재 크기 예상치를 반환하려면 이 옵션을 활성화합니다. 이 예상 값은 작업 영역에 포함된 모든 모듈의 크기를 기반으로 합니다.</td> 
  </tr> 
 </tbody> 
</table>
