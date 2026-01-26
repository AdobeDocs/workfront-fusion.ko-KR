---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: 템플릿을 사용하여 Adobe Workfront Fusion 및 Jira 연결
description: 이러한 템플릿을 사용하여 Adobe Workfront Fusion과 Jira 간에 워크플로우를 자동화합니다.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ede5c7a75725a6540d6a8ff9cd056e6147d5c55
workflow-type: tm+mt
source-wordcount: '4171'
ht-degree: 3%

---

# 템플릿을 사용하여 Adobe Workfront Fusion 및 Jira 연결

Adobe workfront Fusion은 Fusion과 Jira 간의 공통 워크플로를 자동화할 수 있는 템플릿을 제공합니다.

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
   <p>Workfront: 조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p><p>Jira: Jira Cloud에 대한 라이선스가 있어야 합니다.</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">액세스 수준 구성</td> 
   <td> <p>Workfront: 사용자, 사용자 정의 양식 및 사용자 정의 필드를 만들 수 있는 권한.</p> <p>Jira: 사용자 및 사용자 정의 필드를 만들고 화면 및 웹후크를 수정할 수 있는 권한.</td> 
  </tr> 
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## 전제 조건

### Workfront

* Adobe Developer Console에 대한 기술 계정이 있어야 합니다.

  자세한 내용 및 지침은 Adobe 설명서에서 [기술 계정 설정](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup)을 참조하세요.
* Adobe Admin Console 제품 프로필 영역의 기술 계정에 시스템 관리자 권한을 적용해야 합니다.

  자세한 내용 및 지침은 [Adobe Admin Console을 사용하여 Workfront에서 시스템 관리자 만들기](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console)를 참조하십시오.

### Jira

Jira에 대해 OAuth2 인증을 사용하는 경우(권장) [https://developer.atlassian.com/console](https://developer.atlassian.com/console)에서 OAuth2 애플리케이션을 설정해야 합니다. 자세한 내용 및 지침은 문서 Jira 모듈에서 [Jira에 대한 OAuth2 연결 만들기](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#create-an-oauth2-connection-to-jira)를 참조하십시오.

<!--

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

-->

## 가정

이러한 모듈은 다음과 같이 가정합니다.

* Workfront은 전체 마케팅 캠페인 프로젝트의 진실 소스입니다.
* Jira는 Workfront에서 시작된 프로젝트의 일부를 이행하며 기술 팀에서 사용되고 있습니다.
* 모든 Jira 사용자가 Workfront에 액세스하거나 그 반대로 액세스할 수 있는 것은 아닙니다.
* Workfront 및 Jira는 클라우드에서 호스팅됩니다.

## 데이터 모델(필드 매핑)


| Workfront | Jira | 방향 | 참고 |
|---|---|---|---|
| ObjId | WF ID * | → 히라 | Jira 문제 생성 시 |
| Jira 키 * | 문제 키 | → | Jira 문제 생성 시 |
| Jira URL * | - | → | WF에서 Jira로의 사용자 클릭 가능 링크 |
| - | WF 링크 * | → 히라 | WF에 대한 Jira의 사용자 클릭 가능 링크 |
| 이름 | 요약 | → 히라 |  |
| 설명 | 설명 | → 히라 |  |
| 상태 | WF 상태 | → 히라 | WF 상태 |
| Jira 상태 * | 상태 | → | Jira 상태 |
| 계획된 완료 일자 기준 | 기한 | → 히라 | 계획된 완료 일자 기준 |
| 참고 | 댓글 | ↔ 히라 | 양방향 복제 |
| 문서 | 첨부 파일 | → 히라 | 문제 작성에 대한 첨부 파일 및 작성 후 새 문서에 대한 주석으로 사용됩니다. |

\* 이러한 필드는 이 통합 설정의 일부로 구성됩니다. 지침은 [Workfront, Jira 및 Workfront Fusion에서 필수 구성 요소 구성](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion)을 참조하십시오.

## Workfront, Jira 및 Workfront Fusion의 사전 요구 사항 구성

Jira 통합 템플릿을 사용하려면 다음 구성을 수행해야 합니다.

* [Jira 구성](#configure-jira)
* [Workfront 구성](#configure-workfront)
* [Workfront Fusion에서 연결 구성](#configure-connections-in-workfront-fusion)

### Jira 구성

이러한 모듈을 사용하려면 Jira에서 다음을 만들어야 합니다.

* 시스템 통합 사용자
* 세 개의 특정 사용자 정의 필드

#### Jira에서 시스템 통합 사용자 만들기

1. Jira에서 System Integration User라는 특정 사용자를 생성합니다. 이 사용자는 Workfront Fusion에서만 사용해야 하며 일반 사용자를 나타내서는 안 됩니다. 이 사용자의 자격 증명은 Workfront Fusion 연결에 사용됩니다.

#### Jira에서 필요한 사용자 정의 필드 만들기

이 통합에는 연결되는 Jira 계정에 세 개의 특정 필드가 필요합니다. 이러한 필드가 없으면 통합에 실패합니다

1. Jira에서 **설정**(톱니바퀴 아이콘)으로 이동하여 **작업 항목**&#x200B;을 선택합니다.
1. 왼쪽 탐색에서 **사용자 지정 필드**&#x200B;를 선택합니다.
1. 화면 오른쪽 상단에서 **사용자 지정 필드 만들기**&#x200B;를 클릭합니다.
1. 다음 필드를 만듭니다.

   | 필드 이름 | 필드 유형 |
   |---|---|
   | WF ID | 텍스트 필드(한 줄) |
   | WF 상태 | 텍스트 필드(한 줄) |
   | WF 링크 | URL 필드 |

   Jira에서 링크를 만드는 방법에 대한 자세한 내용은 필드 만들기에 대한 Jira 설명서를 참조하십시오.
1. 새로 만든 필드를 Jira 프로젝트와 관련된 화면에 추가합니다.

   Jira의 화면에 대한 자세한 내용은 작업 항목 화면 설정에 대한 Jira 설명서를 참조하십시오.


### Workfront 구성

이러한 모듈을 사용하려면 Workfront에서 다음을 만들어야 합니다.

* 시스템 통합 사용자
* 특정 사용자 정의 양식

#### Workfront에서 시스템 통합 사용자 만들기

1. Workfront에서 시스템 통합 사용자를 만듭니다. 이 사용자는 Workfront Fusion에서만 사용되며 사람 사용자를 나타내지는 않습니다. 이 사용자에게 할당된 작업은 Workfront을 Jira와 동기화하는 시나리오를 트리거합니다.

   지침은 Workfront 설명서에서 [사용자 추가](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users)를 참조하십시오.

#### Workfront에서 사용자 정의 양식 만들기

1. Workfront에서 사용자 정의 양식을 만들기 시작합니다.

   자세한 내용은 Workfront 설명서에서 [사용자 정의 양식 만들기](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form)를 참조하십시오.
1. 양식 이름을 &quot;**JIRA 필드**&quot;로 지정합니다.
1. 사용자 정의 양식에 다음 필드를 포함합니다.

| 필드 이름 | 필드 유형 |
|---|---|
| Jira 키 | 한 줄 텍스트 필드 |
| Jira URL | 한 줄 텍스트 필드 |
| Jira 상태 | 한 줄 텍스트 필드 |

1. Jira와 Workfront 간에 매핑할 추가 필드를 추가합니다.
1. 사용자 정의 양식을 저장합니다.

>[!NOTE]
>
>다른 사용자가 이 양식을 편집할 수 없도록 제한하는 것이 좋습니다. 사용자 정의 양식에 추가된 모든 사용자에게 보기 액세스만 허용하면 됩니다.
>
>자세한 내용은 Workfront 설명서에서 [사용자 정의 양식 공유](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form)를 참조하십시오.

### Workfront Fusion에서 연결 구성

연결을 만들려면 먼저 Jira 및 Workfront에서 System Integration 사용자를 만들어야 합니다.

이러한 연결을 만들 때는 만든 System Integration 사용자의 자격 증명을 사용해야 합니다.

원하는 경우 템플릿 구성의 일부로 이러한 연결을 만들 수 있습니다.

* Workfront에 연결하는 방법에 대한 지침은 Workfront 모듈 문서에서 [Workfront을 Workfront Fusion에 연결](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion)을 참조하십시오.
* Jira에 연결하는 방법에 대한 지침은 Jira 소프트웨어 모듈 문서에서 [Workfront Fusion에 Jira 연결](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion)을 참조하십시오.


## 시나리오

Jira용 8개의 즉시 사용 가능한 템플릿은 일반적인 워크플로를 복제하고 구현을 가속화하는 데 도움이 됩니다. 템플릿은 특정 비즈니스 요구 사항을 충족하도록 완전히 맞춤화할 수 있으며 요구 사항이 발전함에 따라 확장될 수 있습니다.

모든 시나리오를 구현할 필요는 없습니다. 최소 구현에는 Workfront의 할당에서 JIRA 문제에 대한 단일 방향 통합을 만드는 시나리오 1이 필요합니다.  추가 시나리오를 추가하여 Workfront과 JIRA 간의 견고성과 더 양방향 상호 연결을 추가할 수 있습니다.  추가적인 시나리오를 만들어 Workfront 문제 또는 작업에 대한 프로젝트-epic 통합 또는 JIRA 문제와 같은 사례를 처리할 수도 있습니다.

이러한 템플릿 또는 이러한 템플릿의 확장을 사용하는 것은 모두 사용자 지정 구성으로 간주되며 지원 및 구현을 위해 Adobe Professional Services 또는 Adobe 파트너를 활용하는 것이 좋습니다.

* **[Workfront에서 Jira로: Workfront 작업 또는 문제 할당에서 JIRA 문제 만들기](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)**
* [JIRA에서 Workfront으로: JIRA에서 Workfront으로: 문제에 대한 업데이트 및 주석을 Jira에서 Workfront으로 다시 보냅니다.](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront to Jira: Workfront 작업의 JIRA 문제 변경](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* [Workfront to Jira: Workfront 문제가 JIRA 문제로 변경되었습니다.](#scenario-4-workfront-to-jira-changes-to-workfront-issue-to-jira-issue)
* [Workfront에서 Jira로: Workfront 작업 또는 문제에 대한 새 메모가 있을 때 JIRA에서 주석 만들기](#scenario-5-workfront-to-jira-create-comment-in-jira-when-new-note-on-workfront-task-or-issue)
* [Workfront에서 Jira로: Workfront 작업 또는 문제에 대해 삭제된 노트에 JIRA에 댓글 만들기](#scenario-6-workfront-to-jira-create-comment-in-jira-on-deleted-note-on-workfront-task-or-issue)
* [Workfront to Jira: Workfront 작업 또는 문제에 대한 새 문서가 있을 때 JIRA에서 주석 만들기](#scenario-7-workfront-to-jira-create-comment-in-jira-when-new-document-on-workfront-task-or-issue)
* [Workfront에서 Jira로: Workfront 작업 또는 문제에 대해 삭제된 문서에 대해 JIRA에 댓글 만들기](#scenario-8-workfront-to-jira-create-comment-in-jira-on-deleted-document-on-workfront-task-or-issue)

### 일반 매개 변수

이러한 템플릿을 구성할 때는 다음의 일반 매개 변수를 사용하십시오.

* **JiraBaseURL**: Jira 인스턴스의 기본 URL입니다. 예: `https://myjira.atlassian.net/`
* **wfBaseURL**: Workfront 인스턴스의 기본 URL.  일반적으로 `https://<domain>.my.workfront.com`입니다. 여기서 `<domain>`은(는) 특정 Workfront 도메인 이름입니다.
* **defaultJIRAReporterID**: 문제를 만드는 JIRA의 사용자 ID입니다. (예: `557058:5aedf933-2312-40bc-b328-0c21314167f0`)
다음 중 하나를 수행하여 이 ID를 가져올 수 있습니다.
   * JIRA에서 사용자 프로필을 클릭하고 브라우저에서 URL을 확인합니다.
(예`https://myjira.atlassian.net/jira/people/<JiraUserID>`)
   * JIRA 인스턴스에서 다음 API 호출을 실행하여 JIRA의 특정 계정에 대한 ID를 가져옵니다.
     `GET /rest/api/3/user/search?query=email@example.com`


### 시나리오 1: Workfront에서 Jira로: Workfront 작업 또는 문제 할당에서 JIRA 문제 만들기

이 시나리오는 Workfront 작업 또는 문제가 System Integration 사용자에게 할당될 때 Jira 문제를 생성합니다. 시나리오는 요약, 설명, 기한, WF 상태 및 WF ID 필드를 채웁니다. 문제가 생성되면 이 시나리오에서는 첨부 파일 목록과 Workfront의 원래 작업 또는 문제와 관련된 메모의 기록도 업로드합니다.

Workfront 작업이 할당되면 Jira의 문제는 작업입니다. Workfront 문제가 할당되면 Jira 문제는 버그입니다.

+++**확장하여 Jira에 시나리오 1 구성 지침 보기:Workfront: Workfront 작업 또는 문제 할당에서 JIRA 문제 만들기**

#### 트리거 모듈 구성

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **Workfront to Jira: Workfront 작업 또는 문제 할당에서 JIRA 문제 만들기** 템플릿을 클릭합니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. [Workfront Fusion에서 연결 구성](#configure-connections-in-workfront-fusion)에서 만든 Workfront 연결을 선택합니다.
1. **레코드 종류** 필드에서 `Assignment`을(를) 선택합니다.
1. **상태** 필드에서 `New state`을(를) 선택합니다.
1. **And** 옵션을 사용하여 다음 작업으로 필터를 구성합니다.

   | 필드 | 연산자 | 값 |
   |---|---|---|
   | assignedToID | 다음과 같음 | (System Integration 사용자의 Workfront ID 입력) |
   | 작업 ID | 있음 |  |
   | projectID | 다음과 같음 | (웹후크에서 볼 프로젝트의 ID를 입력하십시오.) |

1. **이 연결에서 수행한 업데이트 제외** 옵션을 사용하도록 설정합니다.
1. **레코드 원본** 필드에서 새 레코드만 선택합니다.
1. **저장**&#x200B;을 클릭하여 웹후크를 저장한 다음 **확인**&#x200B;을 클릭하여 트리거 모듈을 저장합니다.
1. [템플릿 모듈을 Workfront 및 Jira에 연결](#connect-template-modules-to-workfront-and-jira)을 계속합니다.

#### 템플릿 모듈을 Workfront 및 Jira에 연결

1. **각** Workfront 모듈의 연결 필드에서 [Workfront Fusion에서 연결 구성](#configure-connections-in-workfront-fusion)에서 만든 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 해당 모듈에 대한 연결을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 [Workfront Fusion에서 연결 구성](#configure-connections-in-workfront-fusion)에서 만든 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 해당 모듈에 대한 연결을 저장합니다.
1. [일반 매개 변수 모듈 업데이트](#update-the-general-parameters-module)를 계속합니다.

#### 일반 매개변수 모듈 업데이트

1. 템플릿의 두 번째 모듈(환경 세부 정보 설정)에서 다음 각 변수에 대해 **항목 추가**&#x200B;를 클릭하고 변수의 이름과 값을 입력합니다

   | 변수 이름 | 변수 값 |
   |---|---|
   | defaultJiraReporterID | 작성자 사용자가 Jira에 존재하지 않는 경우 기본 사용자의 ID를 입력합니다. 사용자 프로필을 클릭하고 브라우저의 URL을 확인하여 이 사용자 ID를 찾을 수 있습니다. 예: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 연결 중인 Jira 계정의 기본 URL을 입력합니다. |
   | wfBaseURL | 연결 중인 Workfront 계정의 기본 URL을 입력합니다. |

1. [Jira의 사용자 지정 필드 매핑](#map-custom-fields-in-jira)을 계속합니다.

<!--#### Map custom fields in Jira. 

Awaiting feedback-->

+++

### 시나리오 2: JIRA에서 Workfront으로: 문제에 대한 업데이트 및 주석을 Jira에서 Workfront으로 다시 전송

이 시나리오는 Jira에서 문제가 생성되면 Workfront 작업 또는 문제를 생성합니다.

>[!NOTE]
>
>이 시나리오에는 Jira에 대한 OAuth2 연결이 필요합니다.
>Jira에 대해 OAuth2 인증을 사용하려면 [https://developer.atlassian.com/console](https://developer.atlassian.com/console)에서 OAuth2 애플리케이션을 설정해야 합니다. 자세한 내용 및 지침은 Jira 설명서를 참조하십시오.

+++**시나리오 2 구성에 대한 지침을 보려면 확장: JIRA에서 Workfront으로: 문제에 대한 업데이트 및 주석을 Jira에서 Workfront으로 다시 보내기**

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **파트2: JIRA에서 Workfront으로 보내기: 문제에 대한 업데이트와 의견을 Jira** 템플릿에서 Workfront으로 다시 보냅니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. System Integration 사용자에 대한 자격 증명을 사용하는 연결을 선택하거나 System Integration 자격 증명으로 Jira에 대한 연결을 만듭니다.

* Jira에 연결하는 방법에 대한 지침은 Jira 소프트웨어 모듈 문서에서 [Workfront Fusion에 Jira 연결](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion)을 참조하십시오.

1. 웹후크 필터 구성

1. [Jira에서 웹후크 구성](#configure-a-webhook-in-jira)을 계속합니다.

#### Jira에서 웹후크 구성

1. Jira에서 웹후크를 생성합니다.

   자세한 내용은 Jira 설명서의 [Webhooks](https://developer.atlassian.com/server/jira/platform/webhooks/)을(를) 참조하십시오.

1. Webhook을 구성할 때는 다음 값을 사용합니다.

   * **JQL**: project = &quot;yourProjectName&quot;(여기서 yourProjectName = your JIRA project의 이름)
   * **문제**: 생성됨, 업데이트됨
   * **댓글**: 생성, 삭제됨


1. [템플릿 모듈을 Workfront 및 Jira에 연결(모듈 2)](#connect-template-modules-to-workfront-and-jira-module-2)로 계속

#### 템플릿 모듈을 Workfront 및 Jira에 연결(모듈 2)

1. **각** Workfront 모듈의 연결 필드에서 [Workfront Fusion에서 연결 구성](#configure-connections-in-workfront-fusion)에서 만든 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 해당 모듈에 대한 연결을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 [Workfront Fusion에서 연결 구성](#configure-connections-in-workfront-fusion)에서 만든 Workfront 연결을 선택한 다음 **확인**을 클릭하여 해당 모듈에 대한 연결을 저장합니다.
   <!--#### Map custom fields-->

+++

### 시나리오 3: Workfront에서 Jira로: Workfront 작업에서 JIRA 문제로 변경

+++**시나리오 3: WF-Jira 변경(작업) 구성에 대한 지침을 보려면 확장**

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **파트3: Workfront to Jira: Workfront 작업의 변경 사항을 JIRA 문제로 클릭** 서식 파일입니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.

1. 템플릿을 클릭하여 편집기로 들어갑니다.
1. 이 시나리오를 소유할 조직 및 팀을 선택하십시오.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. 연결 필드에서 System Integration 자격 증명을 사용하는 Workfront 연결을 선택합니다.
1. **레코드 종류** 필드에서 `Task`을(를) 선택합니다.
1. **상태** 필드에서 `New state`을(를) 선택합니다.
1. **And** 옵션을 사용하여 다음 작업으로 필터를 구성합니다.

   | 필드 | 연산자 | 값 |
   |---|---|---|
   | assignedToID | 다음과 같음 | System Integration 사용자의 Workfront ID 입력 |
   | projectID | 다음과 같음 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |
   | DE: Jira 키 | 있음 |  |

1. **이 연결에서 수행한 업데이트 제외** 옵션을 사용하도록 설정합니다.
1. **원본 기록** 필드에서 `Updated record only`을(를) 선택합니다.
1. **저장**&#x200B;을 클릭하여 웹후크를 저장한 다음 **확인**&#x200B;을 클릭하여 트리거 모듈을 저장합니다.
1. **JIRA 변수 설정** 모듈에서 다음 변수를 설정한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

   | 변수 이름 | 변수 값 |
   |---|---|
   | defaultJiraReporterID | 작성자 사용자가 Jira에 없는 경우 기본 사용자의 ID입니다. 사용자 프로필을 클릭하고 브라우저의 URL을 확인하여 이 사용자 ID를 찾을 수 있습니다. 예: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 연결 중인 Jira 계정의 기본 URL입니다. |
   | wfBaseURL | 연결 중인 Workfront 계정의 기본 URL입니다. |

1. **각** Workfront 모듈의 연결 필드에서 시스템 통합 자격 증명을 사용하는 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 System Integration 자격 증명을 사용하는 Jira 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

+++

### 시나리오 4: Workfront에서 Jira로: Workfront 문제가 JIRA 문제로 변경됨

이 시나리오는 Workfront 문제에서 이전에 연결된 JIRA 문제로 업데이트를 전송합니다.

+++**를 확장하여 시나리오 4: Workfront에서 Jira로 구성: Workfront 문제의 변경 사항을 JIRA 문제로 구성**&#x200B;하기 위한 지침을 봅니다.

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **시나리오 4: WF-Jira 변경(문제)** 템플릿을 클릭합니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.

1. 템플릿을 클릭하여 편집기로 들어갑니다.
1. 이 시나리오를 소유할 조직 및 팀을 선택하십시오.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. 연결 필드에서 System Integration 자격 증명을 사용하는 Workfront 연결을 선택합니다.
1. **레코드 종류** 필드에서 `Issues`을(를) 선택합니다.
1. **상태** 필드에서 `New state`을(를) 선택합니다.
1. **And** 옵션을 사용하여 다음 작업으로 필터를 구성합니다.

   | 필드 | 연산자 | 값 |
   |---|---|---|
   | assignedToID | 다음과 같음 | System Integration 사용자의 Workfront ID 입력 |
   | projectID | 다음과 같음 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |
   | DE: Jira 키 | 있음 |  |

1. **이 연결에서 수행한 업데이트 제외** 옵션을 사용하도록 설정합니다.
1. **원본 기록** 필드에서 `Updated record only`을(를) 선택합니다.
1. **저장**&#x200B;을 클릭하여 웹후크를 저장한 다음 **확인**&#x200B;을 클릭하여 트리거 모듈을 저장합니다.
1. **JIRA 변수 설정** 모듈에서 다음 변수를 설정한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

   | 변수 이름 | 변수 값 |
   |---|---|
   | defaultJiraReporterID | 작성자 사용자가 Jira에 없는 경우 기본 사용자의 ID입니다. 사용자 프로필을 클릭하고 브라우저의 URL을 확인하여 이 사용자 ID를 찾을 수 있습니다. 예: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 연결 중인 Jira 계정의 기본 URL입니다. |
   | wfBaseURL | 연결 중인 Workfront 계정의 기본 URL입니다. |

1. **각** Workfront 모듈의 연결 필드에서 시스템 통합 자격 증명을 사용하는 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 System Integration 자격 증명을 사용하는 Jira 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

+++

### 시나리오 5: Workfront에서 Jira로: Workfront 작업 또는 문제에 대한 새 메모가 있을 때 JIRA에서 주석 만들기

+++**시나리오 5: Workfront에서 Jira로: Workfront 작업 또는 문제에 대한 새 메모가 있을 때 JIRA에서 주석을 만들기**&#x200B;을 구성하는 지침을 보려면 확장하십시오.

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **시나리오 5: WF-to-Jira 새 메모(작업 및 문제)** 템플릿을 클릭합니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. 연결 필드에서 System Integration 자격 증명을 사용하는 Workfront 연결을 선택합니다.
1. **레코드 종류** 필드에서 `Note`을(를) 선택합니다.
1. **상태** 필드에서 `New state`을(를) 선택합니다.
1. 다음 작업을 사용하여 필터를 구성합니다.

   | 필드 | 연산자 | 값 |
   |---|---|---|
   | projectID<br>AND<br>TaskID | 같음<br><br>존재함 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |
   | 또는 |  |  |
   | projectID<br>AND<br>OpTaskID | 같음<br><br>존재함 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |

1. **이 연결에서 수행한 업데이트 제외** 옵션을 사용하도록 설정합니다.
1. **원본 기록** 필드에서 `New record only`을(를) 선택합니다.
1. **저장**&#x200B;을 클릭하여 웹후크를 저장한 다음 **확인**&#x200B;을 클릭하여 트리거 모듈을 저장합니다.
1. **변수 설정** 모듈에서 다음 변수를 설정한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

   | 변수 이름 | 변수 값 |
   |---|---|
   | defaultJiraReporterID | 작성자 사용자가 Jira에 없는 경우 기본 사용자의 ID입니다. 사용자 프로필을 클릭하고 브라우저의 URL을 확인하여 이 사용자 ID를 찾을 수 있습니다. 예: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 연결 중인 Jira 계정의 기본 URL입니다. |
   | wfBaseURL | 연결 중인 Workfront 계정의 기본 URL입니다. |

1. **각** Workfront 모듈의 연결 필드에서 시스템 통합 자격 증명을 사용하는 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 System Integration 자격 증명을 사용하는 Jira 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

+++

### 시나리오 6: Workfront에서 Jira로: Workfront 작업 또는 문제에 대해 삭제된 노트에 JIRA에 댓글 만들기

+++**를 확장하여 시나리오 6: Workfront에서 Jira로 구성: Workfront 작업 또는 문제에 대해 삭제된 노트에 대한 JIRA의 댓글 만들기**&#x200B;을 구성하는 방법에 대한 지침을 봅니다.

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **시나리오 6: WF-to-Jira 메모(작업 및 문제) 제거** 템플릿을 클릭합니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. 연결 필드에서 System Integration 자격 증명을 사용하는 Workfront 연결을 선택합니다.
1. **레코드 종류** 필드에서 `Note`을(를) 선택합니다.
1. **상태** 필드에서 `New state`을(를) 선택합니다.
1. 다음 작업을 사용하여 필터를 구성합니다.

   | 필드 | 연산자 | 값 |
   |---|---|---|
   | projectID<br>AND<br>TaskID | 같음<br><br>존재함 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |
   | 또는 |  |  |
   | projectID<br>AND<br>OpTaskID | 같음<br><br>존재함 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |

1. **이 연결에서 수행한 업데이트 제외** 옵션을 사용하도록 설정합니다.
1. **원본 기록** 필드에서 `Deleted record only`을(를) 선택합니다.
1. **저장**&#x200B;을 클릭하여 웹후크를 저장한 다음 **확인**&#x200B;을 클릭하여 트리거 모듈을 저장합니다.
1. 두 번째 모듈에서 다음 변수를 설정한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

   | 변수 이름 | 변수 값 |
   |---|---|
   | defaultJiraReporterID | 작성자 사용자가 Jira에 없는 경우 기본 사용자의 ID입니다. 사용자 프로필을 클릭하고 브라우저의 URL을 확인하여 이 사용자 ID를 찾을 수 있습니다. 예: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 연결 중인 Jira 계정의 기본 URL입니다. |
   | wfBaseURL | 연결 중인 Workfront 계정의 기본 URL입니다. |

1. **각** Workfront 모듈의 연결 필드에서 시스템 통합 자격 증명을 사용하는 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 System Integration 자격 증명을 사용하는 Jira 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

+++

### 시나리오 7: Workfront에서 Jira로: Workfront 작업 또는 문제에 대한 새 문서가 있을 때 JIRA에서 주석 만들기

+++**시나리오 7을 구성하는 지침을 보려면 확장: Workfront에서 Jira로: Workfront 작업 또는 문제에 대한 새 문서가 있을 때 JIRA에서 주석 만들기**

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **시나리오 7: WF-Jira의 새 첨부 파일(작업 및 문제)** 템플릿을 클릭합니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. 연결 필드에서 System Integration 자격 증명을 사용하는 Workfront 연결을 선택합니다.
1. **레코드 종류** 필드에서 `Document`을(를) 선택합니다.
1. **상태** 필드에서 `New state`을(를) 선택합니다.
1. **And** 옵션을 사용하여 다음 작업으로 필터를 구성합니다.

   | 필드 | 연산자 | 값 |
   |---|---|---|
   | assignedToID | 다음과 같음 | System Integration 사용자의 Workfront ID 입력 |
   | projectID | 다음과 같음 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |

1. 두 번째 모듈에서는 다음 변수를 설정합니다.

   | 변수 이름 | 변수 값 |
   |---|---|
   | defaultJiraReporterID | 작성자 사용자가 Jira에 없는 경우 기본 사용자의 ID입니다. 사용자 프로필을 클릭하고 브라우저의 URL을 확인하여 이 사용자 ID를 찾을 수 있습니다. 예: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 연결 중인 Jira 계정의 기본 URL입니다. |
   | wfBaseURL | 연결 중인 Workfront 계정의 기본 URL입니다. |

1. **이 연결에서 수행한 업데이트 제외** 옵션을 사용하도록 설정합니다.
1. **원본 기록** 필드에서 `New record only`을(를) 선택합니다.
1. **저장**&#x200B;을 클릭하여 웹후크를 저장한 다음 **확인**&#x200B;을 클릭하여 트리거 모듈을 저장합니다.
1. **각** Workfront 모듈의 연결 필드에서 시스템 통합 자격 증명을 사용하는 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 System Integration 자격 증명을 사용하는 Jira 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.

+++

### 시나리오 8: Workfront에서 Jira로: Workfront 작업 또는 문제에 대해 삭제된 문서의 JIRA에 댓글 만들기

+++**시나리오 8을 구성하는 방법에 대한 지침을 보려면 확장: Workfront에서 Jira로: Workfront 작업 또는 문제에 대해 삭제된 문서의 JIRA에 댓글 만들기**

1. 왼쪽 탐색 패널에서 **템플릿** 탭 ![템플릿 아이콘](assets/templates-icon.png)을 클릭합니다.
1. 화면의 왼쪽 상단 모서리 근처에 있는 검색 막대를 사용하여 템플릿을 검색합니다. 템플릿 이름 또는 포함된 애플리케이션별로 검색할 수 있습니다.
1. **시나리오 8: WF-To-Jira 첨부 파일 제거(작업 및 문제)** 템플릿을 클릭합니다.

   템플릿 보기가 열리고 정보 및 데이터 흐름의 애니메이션이 표시됩니다.
1. 첫 번째 모듈에서 웹후크 추가를 시작합니다.
1. 연결 필드에서 System Integration 자격 증명을 사용하는 Workfront 연결을 선택합니다.
1. **레코드 종류** 필드에서 `Document`을(를) 선택합니다.
1. **상태** 필드에서 `New state`을(를) 선택합니다.
1. 다음 작업을 사용하여 필터를 구성합니다.

   | 필드 | 연산자 | 값 |
   |---|---|---|
   | projectID<br>AND<br>TaskID | 같음<br><br>존재함 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |
   | 또는 |  |  |
   | projectID<br>AND<br>OpTaskID | 같음<br><br>존재함 | Webhook에서 볼 프로젝트의 ID를 입력합니다. |

1. **변수 설정** 모듈에서 다음 변수를 설정합니다.

   | 변수 이름 | 변수 값 |
   |---|---|
   | defaultJiraReporterID | 작성자 사용자가 Jira에 없는 경우 기본 사용자의 ID입니다. 사용자 프로필을 클릭하고 브라우저의 URL을 확인하여 이 사용자 ID를 찾을 수 있습니다. 예: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 연결 중인 Jira 계정의 기본 URL입니다. |
   | wfBaseURL | 연결 중인 Workfront 계정의 기본 URL입니다. |

1. **이 연결에서 수행한 업데이트 제외** 옵션을 사용하도록 설정합니다.
1. **원본 기록** 필드에서 `Deleted record only`을(를) 선택합니다.
1. **저장**&#x200B;을 클릭하여 웹후크를 저장한 다음 **확인**&#x200B;을 클릭하여 트리거 모듈을 저장합니다.
1. **각** Workfront 모듈의 연결 필드에서 시스템 통합 자격 증명을 사용하는 Workfront 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.
1. **각** Jira 모듈의 연결 필드에서 System Integration 자격 증명을 사용하는 Jira 연결을 선택한 다음 **확인**&#x200B;을 클릭하여 모듈을 저장합니다.


+++

