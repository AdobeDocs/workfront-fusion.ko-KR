---
title: Adobe Workfront 컨텐츠 및 승인 모듈
description: Adobe Workfront 컨텐츠 및 승인 모듈을 사용하면 승인 세부 정보를 가져오고, 자산에 대한 결정을 내리고, 승인 참여자를 추가 또는 삭제하고, 승인 단계를 추가 또는 업데이트하고, 단계를 잠금 또는 잠금 해제하고, 사용자 지정 API를 호출할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: e9ea91840c9be594e98b97202cb46dfa009349a9
workflow-type: tm+mt
source-wordcount: 3743
ht-degree: 15%

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
* [승인 만들기](#create-an-approval)
* [단계 만들기](#create-stages)
* [스테이지에서 결정 삭제](#delete-a-decision-on-a-stage)
* [단계 삭제](#delete-a-stage)
* [템플릿 삭제](#delete-a-template)
* [승인 삭제](#delete-an-approval)
* [결정 삭제](#delete-decisions)
* [참가자 삭제](#delete-participants)
* [스테이지 잠금](#lock-a-stage)
* [결정](#make-a-decision)
* [스테이지에서 결정](#make-a-decision-on-a-stage)
* [스테이지의 참가자에게 알림](#remind-a-participant-on-a-stage)
* [참가자 알림](#remind-participant)
* [결정되지 않은 참가자에게 알림 전송](#remind-undecided-participants)
* [무대에서 미결정 참가자에게 알림](#remind-undecided-participants-on-a-stage)
* [단계 잠금 해제](#unlock-a-stage)
* [단계 업데이트](#update-a-stage)
* [템플릿 업데이트](#update-a-template)
* [모든 단계 업데이트](#update-all-stages)


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

#### 승인 만들기

이 작업 모듈은 단계 데이터 또는 템플릿을 포함하여 Adobe 클라우드 스토리지에 있는 문서에 대한 승인을 생성합니다.

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
      <td>승인을 생성할 자산의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>단계</p>
      </td>
      <td>추가할 각 단계에 대해 <b>항목 추가</b>를 클릭하고 단계 데이터를 입력하십시오.<p>자세한 내용은 이 문서에서 <a href="#stages-fields" class="MCXref xref" >단계 필드</a>를 참조하십시오. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>템플릿 ID</p></td>
      <td>이 승인에 사용할 템플릿의 ID를 입력하거나 매핑합니다.</td> 
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

#### 스테이지에서 결정 삭제

이 모듈은 지정된 단계에서 현재 사용자의 결정을 제거합니다. 현재 사용자는 이 모듈에 사용된 연결에 사용되는 자격 증명의 사용자입니다.

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
      <td>결정을 삭제할 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 ID</p></td>
      <td>삭제하려는 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
   </tbody>
</table>


#### 단계 삭제

이 작업 모듈은 승인에서 지정된 단계를 삭제합니다.

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
      <td>단계를 삭제할 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>단계 ID</p></td>
      <td>삭제하려는 단계의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 템플릿 삭제

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
      <td>삭제할 템플릿의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 승인 삭제

이 작업 모듈은 특정 문서에 대한 승인을 삭제합니다.

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
      <td>승인을 삭제할 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 결정 삭제

이 모듈은 지정된 단계에서 현재 사용자의 결정을 제거합니다. 현재 사용자는 이 모듈에 사용된 연결에 사용되는 자격 증명의 사용자입니다.

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
      <td>결정을 삭제할 문서의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

#### 참가자 삭제

이 작업 모듈은 승인에서 참여자를 삭제합니다.

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
      <td>참여자를 삭제할 자산의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>참가자 유형</p>
      </td>
      <td>참여자가 사용자인지 팀인지를 선택합니다.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>참가자 ID</p>
      </td>
      <td>참여자의 ID를 입력하거나 매핑합니다.</td> 
      </tr>
  </tbody>
</table>

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

### 검색 결과

* [템플릿 가져오기](#get-a-template)
* [승인 세부 정보 가져오기](#get-approval-details)
* [여러 승인 받기](#get-multiple-approvals)
* [제안된 승인 받기](#get-suggested-approvals)
* [제안된 참가자 가져오기](#get-suggested-participants)
* [보트 나열](#list-bots)
* [목록 템플릿](#list-templates)
* [AI 브랜드 검토자 검색](#search-ai-brand-reviews)


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
        <p><code>https://workfront.adobe.io</code>와 관련된 경로를 입력합니다. 예: <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
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

