---
title: Azure DevOps 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Azure DevOps]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
TQID: https://experienceleague.adobe.com/RFI6MFgF-C1Cnn0bvjOLVf3qahyRblEp4dtypNrxqzE
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 0b7298ce53bf59695ce52cb46cb8d25b6ede5fc8
workflow-type: tm+mt
source-wordcount: 2646
ht-degree: 23%

---

# [!DNL Azure DevOps] 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Azure DevOps]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

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
   <p>운영 기반: 운영 기반 라이센스가 있는 조직에서 사용 가능</p>
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

## [!DNL Azure DevOps]를 Workfront Fusion에 연결 {#connect-azure-devops-to-workfront-fusion}

* [EntraApp을 사용하여 Azure DevOps를 Workfront Fusion에 연결](#connect-azure-devops-to-workfront-fusion-using-entraapp)
* [서비스 주체를 사용하여 Azure DevOps를 Workfront Fusion에 연결](#connect-azure-devops-to-workfront-fusion-using-a-service-principal)

### EntraApp을 사용하여 Azure DevOps를 Workfront Fusion에 연결

1. 시나리오에 [!DNL Azure DevOps] 모듈을 추가합니다.
1. [!UICONTROL 연결] 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
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
            <td>[!DNL Azure DevOps] (EntraApp) 연결 유형을 사용하는 경우 이 옵션을 활성화하여 연결에 대한 모든 범위를 요청합니다.</td>
      </tr>
   </table>

1. Azure DevOps 앱 ID 또는 클라이언트 암호를 입력하려면 <b>고급 설정 표시</b>를 클릭하고 열려 있는 필드에 해당 ID를 입력합니다.
1. 연결 설정을 완료하고 시나리오 만들기를 계속하려면 **[!UICONTROL 계속]**&#x200B;을(를) 클릭합니다.

### 서비스 주체를 사용하여 Azure DevOps를 Workfront Fusion에 연결

개인 계정 대신 서비스 주체(애플리케이션 API 연결)를 사용하는 연결을 만들 수 있습니다. 이 기능은 연결을 특정 사용자가 아닌 응용 프로그램 또는 서비스 ID로 실행하려는 경우에 유용합니다. 이 기능은 예를 들어 해당 사용자가 회사를 퇴사하거나 암호를 변경하는 경우 통합이 중단되지 않도록 유용할 수 있습니다.

이 연결 유형은 모든 Azure DevOps 모듈에서 사용할 수 있습니다.

>[!NOTE]
>
>서비스 주체 인증이 모든 Azure DevOps 기능을 지원하는 것은 아닙니다. 사용자 라이선스 관리와 같은 소수의 관리자 수준 작업에는 여전히 개인 계정 연결이 필요합니다. 작업 항목, 보드, 저장소 또는 파이프라인에 대해서만 필요한 경우 서비스 주체 인증을 사용합니다.

* [서비스 주체를 사용하여 Azure DevOps를 Workfront Fusion에 연결하기 위한 사전 요구 사항](#prerequisites-to-connecting-azure-devops-to-workfront-fusion-using-a-service-principal)
* [Microsoft Entra ID에서 앱 등록 만들기](#create-the-app-registration-in-microsoft-entra-id)
* [클라이언트 암호 만들기](#create-a-client-secret)
* [연결 세부 정보 수집](#collect-your-connection-details)
* [Azure DevOps 조직에 서비스 주체 추가](#add-the-service-principal-to-your-azure-devops-organization)
* [연결 만들기](#create-the-connection)

#### 서비스 주체를 사용하여 Azure DevOps를 Workfront Fusion에 연결하기 위한 사전 요구 사항

이 연결을 만들려면 다음이 필요합니다.

* **전역 관리자** 또는 **응용 프로그램 관리자**&#x200B;가 앱을 등록하기 위해 Microsoft Entra ID에 액세스합니다. 이 액세스 권한이 없는 경우 IT 또는 ID 팀의 사용자에게 해당 단계를 완료하도록 요청하십시오.
* **프로젝트 컬렉션 관리자** Azure DevOps 조직의 액세스 권한을 부여하여 서비스 주체를 구성원으로 추가합니다. 이 사용자는 Microsoft Entra ID를 관리하는 사용자와 다른 경우가 많습니다.
* Azure DevOps 조직의 이름입니다. Azure DevOps URL `dev.azure.com/<your organization name>`에서 찾을 수 있습니다.

#### Microsoft Entra ID에서 앱 등록 만들기

1. [!DNL Microsoft Entra] 관리 센터에 로그인합니다.
1. **[!UICONTROL 앱 등록]** > **[!UICONTROL 새 등록]**(으)로 이동합니다.
1. 앱에 인식할 수 있는 명확한 이름을 지정합니다. 예: `Workfront Fusion Azure DevOps Integration`.
1. **[!UICONTROL 리디렉션 URI]**&#x200B;을 비워 둡니다. 이 연결은 브라우저를 통한 로그인을 포함하지 않습니다.
1. **[!UICONTROL 등록]**&#x200B;을 선택하세요.
1. [클라이언트 암호를 만드세요](#create-a-client-secret).

#### 클라이언트 암호 만들기

1. 새 앱 등록에서 **[!UICONTROL 인증서 및 암호]**(으)로 이동합니다.
1. **[!UICONTROL 새 클라이언트 암호]**&#x200B;를 선택하고 설명을 추가한 다음 만료 기간을 선택하십시오.
1. **[!UICONTROL 추가]**&#x200B;를 선택합니다.
1. 암호의 **[!UICONTROL 값]**&#x200B;을(를) 즉시 복사합니다. 한 번만 표시됩니다. 복사하기 전에 다른 곳으로 이동하면 새 파일을 만들어야 합니다.
1. [연결 세부 정보 수집](#collect-your-connection-details)을 계속합니다.

#### 연결 세부 정보 수집

1. 앱 등록의 **[!UICONTROL 개요]** 페이지에서 다음 값을 참고하십시오. 모듈에서 연결을 만들 때 이를 입력합니다.

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL 테넌트 ID]</td>
      <td>개요 페이지에서 <b>디렉터리(테넌트) ID</b> 레이블이 지정되었습니다.</td>
      </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
      <td>개요 페이지에서 <b>응용 프로그램(클라이언트) ID</b> 레이블이 지정되었습니다.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
      <td><a href="#create-a-client-secret" class="MCXref xref">클라이언트 암호 만들기</a>에서 복사한 값입니다.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 조직]</td>
      <td>Azure DevOps 조직 이름입니다. 예를 들어 URL이 <code>dev.azure.com/yourorg</code>인 경우 <code>yourorg</code>을(를) 입력하십시오.</td>
     </tr>
    </tbody>
   </table>

   >[!NOTE]
   >
   >앱 등록의 **API 권한** 영역을 건너뛸 수 있습니다. Azure DevOps를 추가하면 **위임된 권한**&#x200B;만 사용할 수 있습니다. **응용 프로그램 권한**&#x200B;이 회색으로 표시됩니다. Azure DevOps에서는 이러한 방식으로 액세스 권한을 부여할 수 없기 때문에 예상된 결과입니다. 대신 다음 부분에서 액세스 권한이 Azure DevOps 내에서 직접 부여됩니다.

1. [Azure DevOps 조직에 서비스 주체를 추가](#add-the-service-principal-to-your-azure-devops-organization)합니다.

#### Azure DevOps 조직에 서비스 주체 추가

Microsoft Entra ID에서 앱을 등록하면 해당 ID만 생성됩니다. 아직 앱에 Azure DevOps 데이터에 대한 액세스 권한을 부여하지 않습니다. 이 절차에서는 해당 액세스 권한을 부여합니다.

1. `dev.azure.com/<your organization name>`에서 Azure DevOps 조직에 로그인합니다.
1. 왼쪽 아래에서 **[!UICONTROL 조직 설정]**&#x200B;을 선택한 다음 **[!UICONTROL 사용자]**&#x200B;를 선택합니다.
1. **[!UICONTROL 사용자 추가]**&#x200B;를 선택합니다.
1. 검색 상자에서 앱 표시 이름으로 검색합니다. 이 이름은 앱을 등록할 때 지정한 이름입니다. 클라이언트 ID로 검색하지 마십시오.
1. 액세스 수준 선택:

   * **[!UICONTROL 기본]**&#x200B;은(는) 일반적으로 작업 항목, 게시판 및 보고서를 읽고 쓰는 데 충분합니다.
   * 워크플로우가 설정의 일부로 애자일, 스크럼 또는 사용자 지정 템플릿과 같은 사용 가능한 프로세스를 검색해야 하는 경우 대신 **[!UICONTROL 프로젝트 컬렉션 관리자]** 그룹에 서비스 사용자를 추가하십시오. 이는 더 광범위한 액세스 수준이므로 해당 기능이 필요한 경우에만 부여합니다.

1. 조직의 일반적인 액세스 사례에 따라 필요한 특정 프로젝트 또는 프로젝트에 서비스 사용자를 할당합니다.
1. **[!UICONTROL 추가]**&#x200B;를 선택합니다.
1. [연결 만들기](#create-the-connection)를 계속합니다.

#### 연결 만들기

1. 모듈의 연결 설정 화면에서 **[!UICONTROL 서비스 사용자]** 연결 유형을 선택합니다.
1. 다음을 입력하십시오.

   * [!UICONTROL 테넌트 ID]
   * [!UICONTROL 클라이언트 ID]
   * [!UICONTROL 클라이언트 암호]
   * [!UICONTROL 조직]

1. 연결을 저장합니다.

   모든 것이 올바르게 설정되면 연결이 성공적으로 검증됩니다.

## [!UICONTROL Azure DevOps] 모듈 및 해당 필드

[!DNL Azure DevOps] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL Azure DevOps] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

#### [!UICONTROL 작업 항목 보기]

이 인스턴트 트리거 모듈은 [!UICONTROL Azure DevOps]에서 레코드를 추가, 업데이트 또는 삭제할 때 시나리오를 실행합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 웹후크]</td> 
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
   <td role="rowheader">[!UICONTROL 연결]</td> 
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
       <li> <p><strong>[!UICONTROL 작업 항목 프로세스]</strong>: 프로젝트에 사용할 작업 프로세스를 선택합니다. 옵션은 [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration(CMMI)] 및 [!UICONTROL Agile]입니다.</p> <p>[!DNL Azure DevOps] 프로세스에 대한 자세한 내용은 [!DNL Azure DevOps] 설명서의 <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&tabs=basic-process">기본 프로세스 및 프로세스 템플릿</a>을 참조하십시오.</p> </li> 
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

#### [!UICONTROL 사용자 정의 API 호출]

이 액션 모듈을 사용하면 [!DNL Azure DevOps] API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Azure DevOps] 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
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
   <td role="rowheader">[!UICONTROL API 버전]</td> 
   <td>이 API 호출에 연결할 [!DNL Azure DevOps] API 버전을 선택하거나 매핑합니다. 버전을 선택하지 않으면 Workfront Fusion에서 [!DNL Azure DevOps] API 버전 5.1에 연결합니다.</td> 
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

#### [!UICONTROL 첨부 파일 다운로드]

이 작업 모듈은 첨부 파일을 다운로드합니다.

모듈은 첨부 파일의 내용을 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
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
   <td role="rowheader">[!UICONTROL 연결]</td> 
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

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
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
   <td>이 모듈의 출력 번들에 포함할 정보를 선택합니다. 사용 가능한 필드는 작업 항목 유형에 따라 다릅니다.</td> 
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
   <td role="rowheader">[!UICONTROL 연결]</td> 
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
   <td role="rowheader">[!UICONTROL 연결]</td> 
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
   <td role="rowheader">[!UICONTROL 소스 파일] </td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 내용을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

#### [!UICONTROL 작업 항목 나열]

이 작업 모듈은 [!DNL Azure DevOps] 프로젝트에서 특정 형식의 모든 작업 항목을 검색합니다.

모듈은 기본 작업 항목의 ID 및 연결된 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
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
