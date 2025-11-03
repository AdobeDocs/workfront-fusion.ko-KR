---
title: Azure DevOps 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Azure DevOps]을(를) 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 0%

---

# [!DNL Azure DevOps]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Azure DevOps]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <p>작업 기반: Workfront Fusion 라이센스 요구 사항 없음</p>
   <p>커넥터 기반(레거시): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Azure DevOps] 모듈을 사용하려면 [!DNL Azure] DevOps 계정이 있어야 합니다.

## [!DNL Azure DevOps] API 정보

Azure DevOps 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Workfront Fusion에 [!DNL Azure DevOps] 연결 {#connect-azure-devops-to-workfront-fusion}

1. 시나리오에 [!DNL Azure DevOps] 모듈을 추가합니다.
1. **[!UICONTROL 연결]** 필드 옆에 있는 [!UICONTROL 추가]를 클릭합니다.
1. [!UICONTROL 연결 유형] 필드에서 사용할 연결 유형을 선택합니다.

   >[!NOTE]
   >
   >[!UICONTROL [!DNL Azure DevOps]&#x200B;(Entraapp)]을(를) 사용하면 연결에 대한 모든 범위를 요청할 수 있습니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL 연결 이름]</td>
            <td>생성 중인 연결의 이름을 입력합니다.</td>
      </tr>
      <tr>
            <td>[!UICONTROL 조직]</td>
            <td>[!DNL Azure DevOps] 응용 프로그램을 만든 조직의 이름을 입력하십시오.</td>
      </tr>
      <tr>
            <td>[!UICONTROL 앱 ID]</td>
            <td>연결 중인 DevOps 애플리케이션의 ID를 입력합니다.</td>
      </tr>
      <tr>
            <td>[!UICONTROL 클라이언트 암호]</td>
            <td>연결 중인 DevOps 응용 프로그램의 클라이언트 암호를 입력합니다.</td>
      </tr>
      <tr>
            <td>[!UICONTROL 모든 범위 요청]</td>
            <td>[!DNL Azure DevOps](EntraApp) 연결 유형을 사용하는 경우 이 옵션을 활성화하여 연결에 대한 모든 범위를 요청합니다.</td>
      </tr>
   </table>

1. Azure DevOps 앱 ID 또는 클라이언트 암호를 입력하려면 <b>고급 설정 표시</b>를 클릭하고 열려 있는 필드에 입력합니다.
1. 연결 설정을 완료하고 시나리오 만들기를 계속하려면 **[!UICONTROL 계속]**&#x200B;을(를) 클릭합니다.

## [!UICONTROL Azure DevOps] 모듈 및 해당 필드

[!DNL Azure DevOps] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Azure DevOps] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

#### [!UICONTROL 작업 항목 보기]

이 인스턴스 트리거 모듈은 [!UICONTROL Azure DevOps]에서 레코드를 추가, 업데이트 또는 삭제할 때 시나리오를 실행합니다.

모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>모듈에 대한 웹후크를 선택하거나 추가합니다.</p> <p>트리거 모듈의 웹후크에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">인스턴트 트리거(웹후크)</a>를 참조하십시오.</p> <p>웹후크를 만드는 방법에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">웹후크</a>를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [레코드 만들기](#create-a-record)
* [사용자 정의 API 호출](#custom-api-call)
* [첨부 파일 다운로드](#download-an-attachment)
* [작업 항목 연결](#link-work-items)
* [레코드 읽기](#read-record)
* [작업 항목 업데이트](#update-a-work-item)
* [[!UICONTROL 첨부 파일 업로드]](#upload-an-attachment)

#### [!UICONTROL 레코드 만들기]

이 작업 모듈은 새 프로젝트 또는 작업 항목을 만듭니다.

모듈은 새로 생성된 작업 항목에 대한 개체 ID나 새로 생성된 프로젝트의 URL 및 상태 코드를 출력합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>작업 항목을 만들지 프로젝트를 만들지 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 프로젝트]</strong> </p> <p>다음 필드를 채웁니다.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 이름]</strong>: 새 프로젝트의 이름을 입력하거나 매핑합니다.</p> </li> 
       <li> <p><strong>[!UICONTROL 설명]</strong>: 새 프로젝트에 대한 설명을 입력하거나 매핑합니다. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong>: 프로젝트를 public으로 할지 private으로 할지 선택합니다. 비공개 프로젝트와 상호 작용하려면 사용자에게 조직에 로그인하고 프로젝트에 대한 액세스 권한이 부여되어야 합니다. 조직에 로그인하지 않은 사용자가 공개 프로젝트를 볼 수 있습니다.</p> </li> 
       <li> <p><strong>[!UICONTROL Version control]</strong>: 프로젝트에서 버전 제어에 [!DNL Git] 또는 [!UICONTROL Team Foundation Version Control(TFCV)]을(를) 사용할지 여부를 선택합니다.</p> </li> 
       <li> <p><strong>[!UICONTROL 작업 항목 프로세스]</strong>: 프로젝트에 사용할 작업 프로세스를 선택합니다. 옵션은 [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration(CMMI)] 및 [!UICONTROL Agile]입니다.</p> <p>[!DNL Azure DevOps] 프로세스에 대한 자세한 내용은 <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process"> 설명서의 </a>기본 프로세스 및 프로세스 템플릿[!DNL Azure DevOps]을 참조하십시오.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL 작업 항목]</strong> </p> <p>다음 필드를 채웁니다.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 프로젝트]</strong>: 작업 항목을 만들 프로젝트를 선택하십시오.</p> </li> 
       <li> <p><strong>[!UICONTROL 작업 항목 형식]</strong>: 만들 작업 항목의 형식을 선택합니다.</p> </li> 
       <li> <p><strong>[!UICONTROL 기타 필드]</strong>: 이 필드에 주어진 속성에 대해 작업 항목에 사용할 값을 입력합니다. 사용 가능한 필드는 작업 항목 유형에 따라 다릅니다.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 지정 API 호출]

이 작업 모듈을 사용하면 [!DNL Azure DevOps] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Azure DevOps] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 기본 URL]</td> 
   <td> <p>[!DNL Azure DevOps] 계정에 연결하는 데 사용하는 기본 URL을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상대 URL]</td> 
   <td> <p>이 API 호출에 연결할 상대 URL을 입력합니다.</p> <p><b>예: </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>이 API 호출에 연결할 [!DNL Azure DevOps] API 버전을 선택하거나 매핑합니다. 버전을 선택하지 않으면 Workfront Fusion에서 [!DNL Azure DevOps] API 버전 5.1에 연결합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL 첨부 파일 다운로드]

이 작업 모듈은 첨부 파일을 다운로드합니다.

모듈은 첨부 파일의 내용을 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 첨부 파일 URL]</td> 
   <td> <p>다운로드하려는 첨부 파일의 URL을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 작업 항목 연결]

이 작업 모듈은 두 작업 항목을 연결하고 두 작업 항목 간의 관계를 정의합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 항목 ID]</td> 
   <td>다른 작업 항목을 연결할 기본 작업 항목 항목의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결된 작업 항목 ID]</td> 
   <td>기본 작업 항목에 연결할 작업 항목의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 링크 유형]</td> 
   <td> <p>연결할 작업 항목 간의 관계를 정의합니다.</p> <p>자세한 내용은 [!UICONTROL Azure DevOps] 설명서에서 <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">링크 유형에 대한 참조 안내서</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>댓글의 텍스트를 입력하거나 매핑합니다. 이는 링크의 추론이나 의도를 설명하는 데 유용하다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 읽기]

이 작업 모듈은 [!DNL Azure DevOps]의 단일 레코드에서 데이터를 읽습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>프로젝트를 읽을지 작업 항목을 읽을지 선택</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 프로젝트]</strong>: 읽을 프로젝트를 선택하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 작업 항목]</strong>: 읽을 작업 항목이 포함된 프로젝트를 선택한 다음 작업 항목 형식을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다. 사용 가능한 필드는 작업 항목 유형에 따라 다릅니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>읽으려는 레코드의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 작업 항목 업데이트]

이 작업 모듈은 해당 ID를 사용하여 기존 작업 항목을 업데이트합니다.

업데이트된 작업 항목의 ID가 반환됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트]</td> 
   <td>업데이트할 작업 항목이 포함된 프로젝트를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 항목 유형]</td> 
   <td> <p>업데이트할 작업 항목의 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other Fields]</td> 
   <td>이러한 각 필드에 주어진 속성에 대해 작업 항목에 지정할 값을 입력합니다. 사용 가능한 필드는 작업 항목 유형에 따라 다릅니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 항목 ID]</td> 
   <td>업데이트할 작업 항목의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 첨부 파일 업로드]

이 작업 모듈은 파일을 업로드하고 작업 항목에 첨부합니다.

모듈은 첨부 파일 ID 및 첨부 파일의 다운로드 URL을 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트] </td> 
   <td> <p>첨부 파일을 업로드할 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 항목 ID]</td> 
   <td> <p>첨부 파일을 업로드할 작업 항목의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>업로드한 첨부 파일에 추가할 댓글의 텍스트를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 파일] </td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 내용을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

#### [!UICONTROL 작업 항목 나열]

이 작업 모듈은 [!DNL Azure DevOps] 프로젝트에서 특정 형식의 모든 작업 항목을 검색합니다.

모듈은 기본 작업 항목의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Azure DevOps] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Azure DevOps] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트]</td> 
   <td>작업 항목을 검색할 프로젝트를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 항목 유형]</td> 
   <td> <p>검색할 작업 항목의 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>모듈의 출력에 표시할 속성을 선택합니다. 사용 가능한 필드는 검색할 작업 항목의 유형에 따라 다릅니다. 속성을 하나 이상 선택해야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td>Workfront Fusion이 한 실행 주기 동안 반환하는 최대 작업 항목 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>
