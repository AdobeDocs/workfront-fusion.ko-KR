---
title: Adobe Workfront 컨텐츠 및 승인 모듈
description: Adobe Workfront 컨텐츠 및 승인 모듈을 사용하면 승인 세부 정보를 가져오고, 자산에 대한 결정을 내리고, 승인 참여자를 추가 또는 삭제하고, 승인 단계를 추가 또는 업데이트하고, 단계를 잠금 또는 잠금 해제하고, 사용자 지정 API를 호출할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 56b4c0736c60131ed83635a55cd4a86a35759586
workflow-type: tm+mt
source-wordcount: '5202'
ht-degree: 11%
---
# Adobe Workfront 통합 검토 및 승인 모듈

Adobe Workfront 통합 검토 및 승인 모듈을 사용하면 승인 세부 정보를 가져오고, 에셋에 대한 결정을 내리고, 승인 참가자를 추가 또는 삭제하고, 승인 단계를 추가 또는 업데이트하고, 단계를 잠금 또는 잠금 해제하고, 사용자 지정 API를 호출할 수 있습니다.

Workfront 통합 검토 및 승인에 대한 자세한 내용은 Workfront 설명서에서 [통합 검토 및 승인 개요](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/document-approvals-overview)를 참조하십시오.

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
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 전제 조건

Workfront 컨텐츠 및 승인에 액세스하려면 다음 항목이 있어야 합니다.

* Adobe 클라우드 스토리지를 지원하는 Workfront 버전을 사용해야 합니다. 조직이 이미 지원되는 버전을 사용하고 있지 않은 경우 Adobe 계정 담당자에게 문의하십시오.

## Adobe Workfront 통합 검토 및 승인에 연결


1. Adobe Workfront 통합 검토 및 승인 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 유형]</td>
        <td>
          <p><b>Adobe Workfront 서버 간 연결</b>을 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새로운 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인스턴스 이름]</td>
        <td>
          <p>인스턴스 이름(도메인이라고도 함)을 입력합니다.</p><p>예: URL이 <code>https://example.my.workfront.com</code>인 경우 <code>example</code>을(를) 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인스턴스 레인]</td>
        <td>
          <p>이 연결이 연결될 환경 유형을 입력합니다.</p><p>예: URL이 <code>https://example.my.workfront.com</code>인 경우 <code>my</code>을(를) 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>Workfront 클라이언트 ID를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. 연결할 특정 애플리케이션을 열어 클라이언트 ID를 확인합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>Workfront 클라이언트 암호를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. Workfront에 OAuth2 애플리케이션에 대한 클라이언트 암호가 없는 경우 다른 애플리케이션을 생성할 수 있습니다. 자세한 내용은 Workfront 설명서를 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 범위]</td>
        <td>이 연결에 적용할 수 있는 범위를 입력합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 호스트 접두사]</td>
        <td>대부분의 경우 이 값은 <code>origin</code>이어야 합니다.
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   Workfront Unified Review and Approvals에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인한 후 연결을 허용할 수 있습니다.

## Adobe Workfront 통합 검토 및 승인 모듈

Workfront 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 Workfront 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.


![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [검색 결과](#searches)
* [기타](#other)

### 액션

* [참가자 추가 또는 업데이트](#add-or-update-participants)
* [템플릿 일괄 삭제](#bulk-delete-templates)
* [템플릿 만들기](#create-a-template)
* [그룹화된 승인 만들기](#create-grouped-approval)
* [단계 만들기](#create-stages)
* [스테이지 잠금](#lock-a-stage)
* [결정](#make-a-decision)
* [스테이지에서 결정](#make-a-decision-on-a-stage)
* [그룹화된 승인에서 에셋 관리](#manage-assets-on-a-grouped-approval)
* [스테이지 참가자 관리](#manage-stage-participants)
* [그룹화된 승인에서 단계 관리](#manage-stages-on-a-grouped-approval)
* [스테이지의 참가자에게 알림](#remind-a-participant-on-a-stage)
* [참가자 알림](#remind-participant)
* [결정되지 않은 참가자에게 알림 전송](#remind-undecided-participants)
* [무대에서 미결정 참가자에게 알림](#remind-undecided-participants-on-a-stage)
* [단계 잠금 해제](#unlock-a-stage)
* [단계 업데이트](#update-a-stage)
* [템플릿 업데이트](#update-a-template)
* [모든 단계 업데이트](#update-all-stages)
* [그룹화 승인 업데이트(전체 상태)](#update-grouped-approval-full-state)


#### 참가자 추가 또는 업데이트

이 작업 모듈은 승인 시 기본 단계의 참가자를 추가하거나 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>문서 ID</p>
      </td>
      <td>참가자를 추가하거나 업데이트할 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계에 참가자 추가</p>
      </td>
      <td>참가자를 추가하려는 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계를 입력합니다.<p> 그런 다음 단계에 추가하려는 각 참가자에 대해 <b>항목 추가</b>를 클릭하고 참가자 세부 정보를 입력합니다.</p>
      <ul>
      <li><b>참가자 ID</b><p>참여자의 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>참가자 유형</b><p>참가자가 사용자인지 또는 티인지 선택합니다.</p></li>
      <li><b>참가자 역할</b><p>참여자가 승인자인지 검토자인지 선택합니다.</p></li>
      </ul> 
      </td> 
      </tr>
  </tbody>
</table>

#### 템플릿 일괄 삭제

이 모듈은 지정된 승인 템플릿을 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>템플릿 ID</p></td>
      <td>삭제할 각 템플릿에 대해 <b>항목 추가</b>를 클릭하고 템플릿 ID를 입력하십시오.</td> 
      </tr>
  </tbody>
</table>

#### 템플릿 만들기

이 작업 모듈은 승인 템플릿을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>이름</p></td>
      <td>템플릿의 이름을 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>회사 ID</p></td>
      <td>템플릿에 회사 범위를 추가하려면 회사 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계</p>
      </td>
      <td>추가할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 데이터를 입력하십시오.<p>자세한 내용은 이 문서에서 <a href="#stages-fields" class="MCXref xref" >단계 필드</a>를 참조하십시오. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>다음 사용자와 공유:</p></td>
      <td>템플릿을 공유할 각 사용자에 대해 <b>항목 추가</b> 및 사용자 ID와 원하는 액세스 수준을 클릭합니다.</td> 
      </tr>
  </tbody>
</table>

#### 그룹화된 승인 만들기

이 작업 모듈은 그룹화된 승인, 즉 하나 이상의 승인 경로를 통해 함께 이동하는 문서 버전 세트를 만듭니다. 각 문서 버전은 자체 참여자가 포함된 순서가 지정된 스테이지 시퀀스를 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>이름</p></td>
      <td>그룹화된 승인에 대한 표시 이름을 입력하거나 매핑합니다. 이름은 1~255자 사이여야 합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>자산</p></td>
      <td>그룹에 포함할 각 문서 버전에 대해 <b>항목 추가</b>를 클릭하고 문서 버전(DOCV) ID를 입력하십시오.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>경로</p></td>
      <td>추가할 각 승인 경로에 대해 <b>항목 추가</b>를 클릭하고 경로 ID, 이름 및 단계를 입력하십시오. 각 경로에는 순서가 지정된 스테이지 시퀀스가 포함됩니다. 각 단계에 대해 단계 필드에서 <b>항목 추가</b>를 클릭하고 다음 데이터를 입력합니다.
      <ul>
      <li><b>단계 ID</b><p>모든 경로에서 고유한 단계에 대해 클라이언트가 할당한 식별자를 입력합니다. 영숫자이고 밑줄 또는 하이픈이 허용되며 64자 이하여야 합니다.</p></li>
      <li><b>단계 이름</b><p>단계 이름을 입력하거나 매핑합니다.</p></li>
      <li><b>상위 단계 ID</b><p>단계에 추가하려는 각 상위 단계에 대해 <b>항목 추가</b>를 클릭하고 상위 ID를 입력하십시오.</p></li>
      <li><b>참가자</b><p>단계에 추가하려는 각 참가자에 대해 <b>항목 추가</b>를 클릭하고 참가자 세부 정보를 입력하십시오.
      <ul>
      <li><b>참가자 ID</b><p>참여자의 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>참가자 유형</b><p>참여자가 사용자인지 팀인지 선택합니다.</p></li>
      <li><b>참가자 역할</b><p>참여자가 승인자인지 검토자인지 선택합니다.</p></li>
      </ul>
      </p></li>
      <li><b>기한 일자</b><p>기한이 특정 날짜인 경우 날짜를 입력하거나 매핑합니다.</p></li>
      <li><b>마감까지 영업일</b><p>기한이 특정 영업일 수 이후인 경우 일 수를 입력하거나 매핑합니다.</p></li>
      <li><b>기한 시간: 시간</b><p>기한(0~23)의 시간을 입력하거나 매핑합니다. 기한 시간과 연결: 분.</p></li>
      <li><b>기한 시간: 분</b><p>기한(0~59)의 분을 입력하거나 매핑합니다. 기한 시간과 연결: 시간.</p></li>
      <li><b>사용자 정의 메시지</b><p>단계에 대한 사용자 지정 메시지를 입력하거나 매핑합니다.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>상위 개체 ID</p></td>
      <td>그룹화된 승인과 연결할 Workfront 상위 개체(예: 프로젝트 또는 작업)의 ID를 입력하거나 매핑합니다. 이 필드를 사용하는 경우 개체 코드도 입력해야 합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>오브젝트 코드</p></td>
      <td>부모 개체에 대한 Workfront 개체 유형 코드를 입력하거나 매핑합니다(예: <code>PROJ</code> 또는 <code>TASK</code>). 상위 개체 ID를 입력하는 경우 필수입니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>템플릿 ID</p></td>
      <td>(선택 사항) 추적성을 위해 그룹화된 승인에 기록할 템플릿 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 단계 만들기

이 작업 모듈은 주어진 단계 데이터로 승인을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>단계를 생성하거나 업데이트할 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계</p>
      </td>
      <td>추가할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 데이터를 입력하십시오.<p>자세한 내용은 이 문서에서 <a href="#stages-fields" class="MCXref xref" >단계 필드</a>를 참조하십시오. </p> </td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>템플릿 ID</p></td>
      <td>단계를 생성할 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

<!-- BECKY CHECK ME: The following block of Delete-prefixed Actions modules (Delete a decision on a stage, Delete a stage, Delete a template, Delete an approval, Delete decisions, Delete grouped approval, Delete participants) is not confirmed to be current in the live connector as of this update - status uncertain. Commented out for now; restore (and remove this comment) once confirmed, or delete for good if confirmed removed.

#### Delete a decision on a stage

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
   </tbody>
</table>


#### Delete a stage

This action module deletes the specified stage from the approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a stage from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete a template

This module deletes the specified approval template.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Template ID</p></td>
      <td>Enter or map the ID of the template that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete an approval

This action module deletes the approval for the given document.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete an approval from.</td> 
      </tr>
  </tbody>
</table>

#### Delete decisions

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
  </tbody>
</table>

#### Delete grouped approval

This action module deletes a grouped approval, cascading to its child asset approvals and paths.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Group GUID</p></td>
      <td>Enter or map the GUID of the grouped approval that you want to delete.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limit</p></td>
      <td>Enter or map the maximum number of results you want the module to work with during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

#### Delete participants

This action module deletes participants from an approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to delete participants from.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant type</p>
      </td>
      <td>Select whether the participants is a user or a team.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant ID</p>
      </td>
      <td>Enter or map the ID of the participant.</td> 
      </tr>
  </tbody>
</table>
-->

#### 스테이지 잠금

이 작업 모듈은 지정된 승인 단계를 잠그고 단계를 비활성으로 설정합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>잠그려는 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계 ID</p>
      </td>
      <td>잠그려는 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 결정

이 작업 모듈은 승인 또는 승인 단계에 결정을 적용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>잠그려는 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>결정</p></td>
      <td>승인 또는 단계에 적용할 결정을 선택합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계 ID</p>
      </td>
      <td>결정을 적용할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 ID를 입력하십시오.</td> 
      </tr>
  </tbody>
</table>

#### 스테이지에서 결정

이 모듈은 지정된 단계에 결정을 적용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>결정을 내릴 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 ID</p></td>
      <td>결정을 내릴 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
    <tr>
      <td role="rowheader"><p>결정</p></td>
      <td>이 단계에 적용할 결정을 선택합니다.</td> 
      </tr>
  </tbody>
</table>

#### 그룹화된 승인에서 에셋 관리

이 작업 모듈은 그룹화된 승인에서 문서 버전을 추가 및/또는 제거합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>그룹화된 승인 ID</p></td>
      <td>자산을 관리할 그룹화된 승인의 GUID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Assets 추가</p></td>
      <td>그룹에 추가할 각 문서 버전에 대해 <b>항목 추가</b>를 클릭하고 문서 버전(DOCV) ID를 입력하십시오.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Assets 제거</p></td>
      <td>그룹에서 제거할 각 문서 버전에 대해 <b>항목 추가</b>를 클릭하고 문서 버전(DOCV) ID를 입력하십시오.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 스테이지 참가자 관리

이 작업 모듈은 그룹화된 승인의 특정 단계에서 참가자를 추가, 업데이트 및/또는 제거합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>그룹화된 승인 ID</p></td>
      <td>그룹화된 승인의 GUID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 ID</p></td>
      <td>참가자를 관리할 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>참가자 추가</p></td>
      <td>단계에 추가하려는 각 참가자에 대해 <b>항목 추가</b>를 클릭하고 다음 세부 정보를 입력하십시오.
      <ul>
      <li><b>참가자 유형</b><p>참여자가 사용자인지 팀인지 선택합니다.</p></li>
      <li><b>참가자</b><p>참여자의 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>역할</b><p>참여자가 승인자인지 검토자인지 선택합니다.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>참가자 업데이트</p></td>
      <td>단계에서 업데이트할 각 참가자에 대해 <b>항목 추가</b>를 클릭하고 다음 세부 정보를 입력하십시오.
      <ul>
      <li><b>참가자 유형</b><p>참여자가 사용자인지 팀인지 선택합니다.</p></li>
      <li><b>참가자</b><p>참여자의 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>역할</b><p>참여자가 승인자인지 검토자인지 선택합니다.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>참가자 제거</p></td>
      <td>단계에서 제거할 각 참가자에 대해 <b>항목 추가</b>를 클릭하고 다음 세부 정보를 입력하십시오.
      <ul>
      <li><b>참가자 유형</b><p>참여자가 사용자인지 팀인지 선택합니다.</p></li>
      <li><b>참가자</b><p>참여자의 ID를 입력하거나 매핑합니다.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 그룹화된 승인에서 단계 관리

이 작업 모듈은 그룹화된 승인의 단계를 추가, 업데이트 및/또는 제거합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>그룹화된 승인 ID</p></td>
      <td>그룹화된 승인의 GUID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 추가</p></td>
      <td>추가할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 다음 세부 정보를 입력하십시오.
      <ul>
      <li><b>단계 ID</b><p>단계에 대한 식별자를 입력하거나 매핑합니다.</p></li>
      <li><b>단계 이름</b><p>단계 이름을 입력하거나 매핑합니다.</p></li>
      <li><b>기한 일자</b><p>기한이 특정 날짜인 경우 날짜를 입력하거나 매핑합니다.</p></li>
      <li><b>마감까지 영업일</b><p>기한이 특정 영업일 수 이후인 경우 일 수를 입력하거나 매핑합니다.</p></li>
      <li><b>사용자 정의 메시지</b><p>단계에 대한 사용자 지정 메시지를 입력하거나 매핑합니다.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 업데이트</p></td>
      <td>업데이트할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 다음 세부 정보를 입력하십시오.
      <ul>
      <li><b>단계 ID</b><p>업데이트할 단계의 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>단계 이름</b><p>단계 이름을 입력하거나 매핑합니다.</p></li>
      <li><b>기한 일자</b><p>기한이 특정 날짜인 경우 날짜를 입력하거나 매핑합니다.</p></li>
      <li><b>마감까지 영업일</b><p>기한이 특정 영업일 수 이후인 경우 일 수를 입력하거나 매핑합니다.</p></li>
      <li><b>사용자 정의 메시지</b><p>단계에 대한 사용자 지정 메시지를 입력하거나 매핑합니다.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 제거</p></td>
      <td>제거할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 ID를 입력하십시오.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 스테이지의 참가자에게 알림

이 모듈은 특정 단계의 특정 참가자에게 미리 알림을 보냅니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>미리 알림을 보낼 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계 ID</p>
      </td>
      <td>미리 알림을 보낼 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>참가자 ID</p></td>
      <td>미리 알림을 보낼 참여자의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 참가자 알림

이 모듈은 지정된 참가자에게 미리 알림을 보냅니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>미리 알림을 보낼 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>참가자 ID</p>
      </td>
      <td>알림을 보내려는 참가자의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
      <tr>
      <td role="rowheader">
        <p>참가자 유형</p>
      </td>
      <td>알림을 보낼 참여자의 유형을 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>참가자 역할</p>
      </td>
      <td>알림을 받을 참가자의 역할을 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 결정되지 않은 참가자에게 알림 전송

이 모듈은 지정된 승인 시 결정되지 않은 모든 참가자에게 미리 알림을 보냅니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>미리 알림을 보낼 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 무대에서 미결정 참가자에게 알림

이 모듈은 스테이지의 결정되지 않은 모든 참가자에게 미리 알림 을 보냅니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>미리 알림을 보낼 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계 ID</p>
      </td>
      <td>미리 알림을 보낼 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 단계 잠금 해제

이 작업 모듈은 지정된 승인 단계를 잠금 해제하고 단계를 활성으로 설정합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>잠금을 해제할 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계 ID</p>
      </td>
      <td>잠그려는 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>


#### 단계 업데이트

이 작업 모듈은 지정된 단계의 필드를 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>결정을 내릴 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 ID</p></td>
      <td>결정을 내릴 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 이름</p></td>
      <td>템플릿의 이름을 입력하거나 매핑합니다.</td> 
      </tr>
      <td role="rowheader">
        <p>기타 필드</p>
      </td>
      <td>단계 필드에 데이터를 입력합니다.<p>자세한 내용은 이 문서에서 <a href="#stages-fields" class="MCXref xref" >단계 필드</a>를 참조하십시오. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>다음 사용자와 공유:</p></td>
      <td>템플릿을 공유할 각 사용자에 대해 <b>항목 추가</b> 및 사용자 ID와 원하는 액세스 수준을 클릭합니다.</td> 
      </tr>
  </tbody>
</table>

#### 템플릿 업데이트

이 모듈은 지정된 승인 템플릿의 필드를 업데이트합니다.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>템플릿 ID</p></td>
      <td>템플릿의 이름을 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>이름</p></td>
      <td>업데이트할 템플릿의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>회사 ID</p></td>
      <td>템플릿에 회사 범위를 추가하려면 회사 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계</p>
      </td>
      <td>추가할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 데이터를 입력하십시오.<p>자세한 내용은 이 문서에서 <a href="#stages-fields" class="MCXref xref" >단계 필드</a>를 참조하십시오. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>다음 사용자와 공유:</p></td>
      <td>템플릿을 공유할 각 사용자에 대해 <b>항목 추가</b> 및 사용자 ID와 원하는 액세스 수준을 클릭합니다.</td> 
      </tr>
  </tbody>
</table>

#### 모든 단계 업데이트

이 모듈은 기존 승인의 모든 단계를 지정된 단계 데이터로 대체합니다. 문서는 편집 가능한 상태여야 합니다.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>단계를 업데이트할 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계</p>
      </td>
      <td>업데이트할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 데이터를 입력하십시오.<p>자세한 내용은 이 문서에서 <a href="#stages-fields" class="MCXref xref" >단계 필드</a>를 참조하십시오. </p> </td> 
      </tr>
  </tbody>
</table>

#### 그룹화 승인 업데이트(전체 상태)

이 작업 모듈은 전체 상태 업데이트를 그룹화된 승인에 적용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>그룹화된 승인 ID</p></td>
      <td>업데이트할 그룹화된 승인의 GUID를 입력하거나 매핑합니다. 예: <code>9f8b60820000462ecf66c409d1248fa9</code>.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>경로</p></td>
      <td>그룹화된 승인을 받을 각 승인 경로에 대해 <b>항목 추가</b>를 클릭하고 경로 ID, 이름 및 단계를 입력하십시오. Fusion은 현재 상태와 비교하여 경로를 추가, 업데이트 및 제거하여 전송한 내용과 일치하도록 합니다. 각 경로에는 순서가 지정된 스테이지 시퀀스가 포함됩니다. 각 단계에 대해 단계 필드에서 <b>항목 추가</b>를 클릭하고 다음 데이터를 입력합니다.
      <ul>
      <li><b>단계 ID</b><p>모든 경로에서 고유한 단계에 대해 클라이언트가 할당한 식별자를 입력합니다. 영숫자이고 밑줄 또는 하이픈이 허용되며 64자 이하여야 합니다.</p></li>
      <li><b>단계 이름</b><p>단계 이름을 입력하거나 매핑합니다.</p></li>
      <li><b>상위 단계 ID</b><p>단계에 추가하려는 각 상위 단계에 대해 <b>항목 추가</b>를 클릭하고 상위 ID를 입력하십시오.</p></li>
      <li><b>참가자</b><p>단계에 추가하려는 각 참가자에 대해 <b>항목 추가</b>를 클릭하고 참가자 세부 정보를 입력하십시오.
      <ul>
      <li><b>참가자 ID</b><p>참여자의 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>참가자 유형</b><p>참여자가 사용자인지 팀인지 선택합니다.</p></li>
      <li><b>참가자 역할</b><p>참여자가 승인자인지 검토자인지 선택합니다.</p></li>
      </ul>
      </p></li>
      <li><b>기한 일자</b><p>기한이 특정 날짜인 경우 날짜를 입력하거나 매핑합니다.</p></li>
      <li><b>마감까지 영업일</b><p>기한이 특정 영업일 수 이후인 경우 일 수를 입력하거나 매핑합니다.</p></li>
      <li><b>기한 시간: 시간</b><p>기한(0~23)의 시간을 입력하거나 매핑합니다. 기한 시간과 연결: 분.</p></li>
      <li><b>기한 시간: 분</b><p>기한(0~59)의 분을 입력하거나 매핑합니다. 기한 시간과 연결: 시간.</p></li>
      <li><b>사용자 정의 메시지</b><p>단계에 대한 사용자 지정 메시지를 입력하거나 매핑합니다.</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>자산</p></td>
      <td>(선택 사항) 그룹에 포함할 각 문서 버전에 대해 <b>항목 추가</b>를 클릭하고 문서 버전(DOCV) ID를 입력하십시오. 이 필드를 생략하면 현재 에셋은 변경되지 않습니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>관념화 키</p></td>
      <td>(선택 사항) 재시도 요청을 안전하게 만드는 클라이언트 제공 키(최대 128자)를 입력하거나 매핑합니다. 동일한 키를 다시 보내면 모듈이 업데이트를 두 번 적용하지 않습니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

### 검색 결과

* [템플릿 가져오기](#get-a-template)
* [승인 세부 정보 가져오기](#get-approval-details)
* [그룹화된 승인에서 승인 받기](#get-approvals-in-a-grouped-approval)
* [그룹화된 승인 세부 정보 가져오기](#get-grouped-approval-details)
* [여러 승인 받기](#get-multiple-approvals)
* [제안된 승인 받기](#get-suggested-approvals)
* [제안된 참가자 가져오기](#get-suggested-participants)
* [보트 나열](#list-bots)
* [상위 항목별로 그룹화된 승인 나열](#list-grouped-approvals-by-parent)
* [목록 템플릿](#list-templates)
* [AI 브랜드 리뷰 검색](#search-ai-brand-reviews)
* [그룹화된 승인 검색](#search-grouped-approvals)


#### 템플릿 가져오기

이 모듈은 지정된 승인 템플릿을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>템플릿 ID</p></td>
      <td>제안 승인 참여자를 받을 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           반환되는 최대 템플릿 수
         </td>
         <td>
              각 시나리오 실행 주기 동안 모듈이 반환할 최대 템플릿 수를 입력하거나 매핑합니다. 
         </td>
       </tr>
  </tbody>
</table>

#### 승인 세부 정보 가져오기

이 검색 모듈은 자산에 대한 승인 세부 정보를 검색합니다.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>문서</p>
      </td>
      <td>승인 세부 정보를 검색할 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 그룹화된 승인에서 승인 받기

이 검색 모듈은 그룹화된 승인을 구성하는 개별 자산 승인을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>그룹 GUID</p></td>
      <td>승인을 받을 그룹화된 승인의 GUID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>문서 버전 데이터</p></td>
      <td>Redrock documentVersion 레코드를 각 문서 버전(DOCV) 승인에 첨부할지 여부를 선택합니다. </td>
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 그룹화된 승인 세부 정보 가져오기

이 검색 모듈은 GUID별로 그룹화된 승인을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>그룹 GUID</p></td>
      <td>세부 정보를 가져올 그룹화된 승인의 GUID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 여러 승인 받기

이 모듈은 특정 유형의 문서 목록에 대한 승인 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>승인 세부 정보를 검색할 각 문서에 대해 <b>항목 추가</b>를 클릭하고 문서 ID를 입력하십시오.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           반환된 최대 결과 수
         </td>
         <td>
              각 시나리오 실행 주기 동안 모듈이 반환할 최대 결과 수를 입력하거나 매핑합니다. 
         </td>
       </tr>
  </tbody>
</table>

#### 제안된 승인 받기

이 모듈은 이전 문서 버전에서 제안된 승인 페이로드를 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>제안된 승인을 받을 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           반환된 최대 승인 수
         </td>
         <td>
              각 시나리오 실행 주기 동안 모듈이 반환할 최대 승인 수를 입력하거나 매핑합니다. 
         </td>
       </tr>
  </tbody>
</table>

#### 제안된 참가자 가져오기

이 모듈은 이전 문서 승인에 대한 승인에서 참가자 제안을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>문서 ID</p></td>
      <td>제안 승인 참여자를 받을 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           반환된 최대 참가자 수
         </td>
         <td>
              각 시나리오 실행 주기 동안 모듈이 반환할 최대 참여자 수를 입력하거나 매핑합니다. 
         </td>
       </tr>
  </tbody>
</table>

#### 보트 나열

이 모듈은 보트 계정의 페이지 매김된 목록을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>페이지</p></td>
      <td>반환할 결과 페이지를 입력하거나 매핑합니다.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           반환된 최대 결과 수
         </td>
         <td>
              각 시나리오 실행 주기 동안 모듈이 반환할 최대 결과 수를 입력하거나 매핑합니다. 
         </td>
       </tr>
  </tbody>
</table>

#### 상위 항목별로 그룹화된 승인 나열

이 검색 모듈은 Workfront 상위 개체와 연결된 그룹화된 승인을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>상위 ID</p></td>
      <td>그룹화된 승인을 받을 Workfront 상위 개체(예: 프로젝트 또는 작업)의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>개체 코드</p></td>
      <td>(선택 사항) 부모 개체에 대한 Workfront 개체 유형 코드를 입력하거나 매핑합니다(예: <code>PROJ</code> 또는 <code>TASK</code>).</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 목록 템플릿

이 모듈은 현재 사용자가 사용할 수 있는 모든 승인 템플릿 목록을 반환합니다. 현재 사용자는 이 모듈에 사용된 연결에 사용되는 자격 증명의 사용자입니다.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
   </tbody>
</table>

#### AI 브랜드 리뷰 검색

이 모듈은 승인의 일부로 문서 버전에 대해 생성된 AI 브랜드 검토 결과를 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>봇 사용자 ID</p></td>
      <td>리뷰를 검색할 보트의 사용자 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>상위 문서 ID</p></td>
      <td>검토를 검색할 상위 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>문서 버전 ID</p></td>
      <td>미리 알림을 보낼 에셋의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 ID</p></td>
      <td>단계 ID를 입력하거나 매핑하여 결과를 승인의 특정 단계로 제한합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>페이지</p></td>
      <td>결과를 해당 페이지로 제한하려면 페이지 번호를 입력하거나 매핑하십시오.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           반환된 최대 리뷰 수
         </td>
         <td>
              각 시나리오 실행 주기 동안 모듈이 반환할 최대 검토 수를 입력하거나 매핑합니다. 
         </td>
       </tr>
  </tbody>
</table>

#### 그룹화된 승인 검색

이 검색 모듈은 명명된 보기를 사용하여 그룹화된 승인을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>보기</p></td>
      <td>(선택 사항) 응답의 모양을 결정하는 명명된 보기를 선택하거나 매핑합니다. 현재 대기 중인 승인만 지원됩니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>(선택 사항) 결과의 첫 페이지에 대한 페이지 크기를 입력하거나 매핑합니다. 최대값은 100이고 기본값은 20입니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>커서</p></td>
      <td>(선택 사항) 이전 응답의 불투명 커서를 입력하거나 매핑하여 다음 결과 페이지를 가져옵니다. 커서를 제공하면 모듈은 제한 필드를 무시합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>팀 ID</p></td>
      <td>(선택 사항) 그룹화된 승인을 일치시키려는 각 팀에 대해 <b>항목 추가</b>를 클릭하고 팀 ID를 입력합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>제한</p></td>
      <td>각 시나리오 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

<!-- BECKY CHECK ME: the screenshot shows two separate fields both labeled "Limit" - an optional pagination page-size field (max 100, default 20, ignored if Cursor is set) and a required general execution-cycle limit, matching the Limit field used in every other module in this article. Confirm this isn't a UI labeling issue before publishing, and that both rows are needed/correctly distinguished. -->

### 기타

* [사용자 정의 API 호출하기](#make-a-custom-api-call)
* [단계 필드](#stages-fields)


#### 사용자 정의 API 호출하기

이 모듈은 Adobe Workfront 통합 검토 및 승인 API에 대한 사용자 지정 API 호출을 수행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe Workfront 통합 검토 및 승인에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Adobe Workfront 통합 검토 및 승인에 연결</a>을 참조하십시오.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>상대 경로</p>
      </td>
      <td>
        <p><code>https://workfront.adobe.io</code>과 관련된 경로를 입력합니다. 예: <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
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
        <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p>
        <p>예: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>쿼리 문자열에 추가할 각 키/값 쌍에 대해 <b>항목 추가</b>를 클릭하고 키와 값을 입력하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 본문]</td>
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>



#### 단계 필드

단계를 구성할 때 다음 필드를 사용할 수 있습니다. 모든 모듈에 일부 필드를 사용할 수 있는 것은 아닙니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">단계 이름</td>
      <td>단계 이름을 입력하거나 매핑합니다.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>기한 일자</p></td>
      <td>기한이 특정 날짜인 경우 날짜를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
     <tr>
      <td role="rowheader"><p>마감 영업일</p></td>
      <td>기한이 특정 영업일 수 이후인 경우 일 수를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>기한 시간</p></td>
      <td>기한이 특정 시간인 경우 시간을 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>참가자</p></td>
      <td>단계에 추가하려는 각 참가자에 대해 <b>항목 추가</b>를 클릭하고 참가자 세부 정보를 입력하십시오.      
      <ul>
      <li><b>참가자 ID</b><p>참여자의 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>참가자 유형</b><p>참여자가 사용자인지 팀인지 선택합니다.</p></li>
      <li><b>참가자 역할</b><p>참여자가 승인자인지 검토자인지 선택합니다.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>자동 잠금 활성화됨</p></td>
      <td>스테이지를 자동으로 잠글 것인지 지정합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>결정 규칙</p></td>
      <td>단계에 대해 하나의 결정만 요구할지 여부를 선택합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>상위 ID / 상위 단계 ID</p></td>
      <td>단계에 추가하려는 각 상위 단계에 대해 <b>항목 추가</b>를 클릭하고 상위 ID를 입력하십시오.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>트리거</p></td>
      <td>이 승인 단계에 대한 트리거를 구성하려면 <b>항목 추가</b>를 클릭하고 트리거 세부 정보를 입력하십시오.      <ul>
      <li><b>유형</b><p><b>활성화</b> 선택</p></li>
      <li><b>조건</b><p>승인이 생성될 때 또는 다른 단계가 완료될 때 단계를 트리거할지 여부를 선택합니다.</p></li>
      <li><b>단계</b><p>트리거에 추가할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 ID를 입력하거나 매핑합니다.</p></li>
      <li><b>결정</b><p>트리거에 추가할 각 결정에 대해 <b>항목 추가</b>를 클릭하고 결정을 입력하거나 매핑합니다.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>사용자 정의 메시지</p></td>
      <td>단계에 대한 사용자 지정 메시지를 입력하거나 매핑합니다.</td> 
      </tr>
</table>
