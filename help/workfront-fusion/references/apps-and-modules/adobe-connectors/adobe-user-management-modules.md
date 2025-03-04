---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe 사용자 관리 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Adobe 계정의 사용자를 관리하는 워크플로를 자동화할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: e8fe8ec4-4b00-4c9a-81a5-acb2039b153b
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '2374'
ht-degree: 2%

---

# Adobe 사용자 관리 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 Adobe 계정의 사용자를 관리하는 워크플로를 자동화할 수 있습니다.

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
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합의 경우 [!UICONTROL [!DNL Workfront Fusion], 작업 자동화의 경우 [!UICONTROL [!DNL Workfront Fusion]]</p>
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

+++

## Adobe 사용자 관리에 대한 연결 만들기

[!DNL Adobe User Management] 모듈에 대한 연결을 만들려면:

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

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
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>[!UICONTROL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS 조직 ID]</td>
        <td>[!DNL Adobe] IMS 자격 증명을 입력하십시오. 조직의 고유 식별자입니다. @ 앞에 오는 접두사가 16진수인 A495E53@AdobeOrg 형식의 문자열입니다. 이 값은 Admin Console 또는 사용자 관리 통합을 위한 adobe.io 콘솔에서 조직의 URL 경로의 일부로 찾을 수 있습니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 추가 범위]</td>
        <td>추가할 각 범위에 대해 <b>항목 추가</b>를 클릭하고 범위를 입력하십시오.</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.



## Adobe 사용자 관리 모듈 및 해당 필드

Adobe 사용자 관리 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Adobe 사용자 관리 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [검색 결과](#searches)
* [사용자 작업](#user-actions)
* [사용자 그룹 작업](#user-group-actions)
* [기타](#other)

### 검색 결과

* [사용자 그룹 및 제품 프로필 가져오기](#get-user-groups-and-product-profiles)
* [사용자 정보 가져오기](#get-user-information)
* [사용자 그룹 또는 제품 프로필에서 사용자 가져오기](#get-users-in-a-user-group-or-product-profile)
* [조직에서 사용자 가져오기](#get-users-in-an-organization)

#### 사용자 그룹 및 제품 프로필 가져오기

이 검색 모듈은 그룹 및 프로필에 대한 세부 정보와 함께 조직의 모든 사용자 그룹 및 제품 프로필 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 정보 가져오기

이 검색 모듈은 조직의 단일 사용자에 대한 세부 정보를 검색하고 이메일 주소로 식별합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이메일 주소</td> 
   <td>세부 정보를 반환할 사용자의 이메일 주소를 입력하거나 매핑합니다. AdobeID, Enterprise 및 이메일 페더레이션 사용자의 경우 도메인을 포함한 전체 이메일 주소여야 합니다. 모든 경우에 매개 변수는 대/소문자를 구분하지 않습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 그룹 또는 제품 프로필에서 사용자 가져오기

이 검색 모듈은 사용자에 대한 세부 정보와 함께 지정된 사용자 그룹 또는 제품 프로필의 모든 사용자 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 이름</td> 
   <td>사용자 그룹, 제품 프로필 이름 또는 관리 그룹. 관리 그룹의 경우 이름은 고정 그룹 <code>_org_admin</code>, <code>_deployment_admin</code> 또는 <code>_support_admin</code> 중 하나이거나 그룹별 관리 그룹일 수 있습니다. <code>_admin_groupName</code>, <code>_product_admin_productName</code> 또는 <code>_developer_groupName</code>과(와) 같은 그룹 이름 접두사로 식별됩니다. 그룹이 존재하지만 관리 그룹이 존재하지 않으면 빈 목록이 반환됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">직접 전용</td> 
   <td>반환된 사용자 구조의 그룹 필드에 해당 사용자가 직접 구성원인 제품 프로필만 포함할지 여부를 지정합니다. false인 경우 특정 제품 프로필에 대한 권한이 직접(사용자 할당을 통해) 또는 간접적으로(제품 프로필에 할당된 사용자를 포함하는 사용자 그룹을 통해) 들어오는지 여부에 관계없이 사용자가 포함된 모든 그룹(사용자 그룹, 제품 프로필 및 관리자 그룹)을 반환합니다. true면 은 사용자가 포함된 모든 사용자 그룹 및 관리 그룹을 반환하지만, 사용자가 명시적으로 권한을 할당한 제품 프로필만 반환합니다. 사용자는 제품 프로필의 직접 멤버이자 간접 멤버일 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 제외</td> 
   <td>응답이 각 개별 사용자에 대해 반환되는 그룹 배열을 제외할지 여부를 지정합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">상태</td> 
   <td>이 옵션은 제품 프로필에만 적용됩니다. 활성 을 선택하여 제품에 대해 프로비저닝되고 활성 라이센스가 있는 사용자를 나열합니다. 제품 프로필에 추가되었지만 활성 라이선스가 없는 사용자를 나열하려면 비활성 을 선택합니다. 비워 두면 모듈은 권한 상태에 관계없이 모든 구성원 사용자를 반환합니다.
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 조직에서 사용자 가져오기

이 검색 모듈은 연결과 연결된 조직의 모든 사용자를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 사용자 작업

* [사용자를 그룹의 구성원으로 추가](#add-a-user-as-a-member-of-a-group)
* [사용자 만들기](#create-a-user)
* [그룹에서 사용자 제거](#remove-a-user-from-groups)
* [사용자 업데이트](#update-a-user)

#### 사용자를 그룹의 구성원으로 추가

이 작업 모듈은 사용자를 지정된 그룹의 구성원으로 추가합니다. 이 모듈은 최대 4개의 그룹에 사용자를 추가할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자</td> 
   <td>그룹에 추가할 사용자를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">도메인</td> 
   <td>이메일 주소가 아닌 Federated ID의 경우 사용자가 속한 도메인을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹</td> 
   <td>사용자를 추가하려는 각 그룹에 대해 <b>항목 추가</b>를 클릭하고 그룹을 입력하거나 매핑하십시오. 최대 4개의 그룹을 입력할 수 있으며 최소 하나 이상의 그룹을 입력해야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID 사용</td> 
   <td>Enterprise 또는 Federated ID이 동일한 이름으로 존재하는 경우에도 사용자 ID가 기존 Adobe ID을 참조하도록 해석하려면 true를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 만들기

이 작업 모듈은 조직에서 새 사용자를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID 유형</td> 
   <td>Adobe ID, Enterprise ID 또는 Federated ID으로 사용자를 만들지 여부를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">로그인</td> 
   <td>Federated ID으로 사용자를 만드는 경우 로그인 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이메일</td> 
   <td>새 사용자의 이메일 주소를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">도메인</td> 
   <td>도메인 기반 로그인으로 Federated ID을 사용하는 사용자를 만드는 경우 도메인을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자</td> 
   <td>도메인 기반 로그인으로 Federated ID을 사용하는 사용자를 만드는 경우 이 새 사용자가 나타낼 사용자를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이름</td> 
   <td>사용자의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">성</td> 
   <td>사용자의 성을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">국가</td> 
   <td>두 문자 ISO 국가 코드를 입력하거나 매핑합니다. 사용자를 만든 후에는 변경할 수 없습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">옵션</td> 
   <td>사용자가 이미 조직에 있는 경우 수행할 작업을 선택합니다. 옵션을 선택하지 않았는데 사용자가 이미 있으면 모듈에서 오류를 반환합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID 사용</td> 
   <td>true인 경우 사용자 ID는 Enterprise 또는 Federated ID이 동일한 이름으로 존재하는 경우에도 기존 Adobe ID을 참조하는 것으로 해석됩니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 그룹에서 사용자 제거

이 작업 모듈은 지정된 그룹에서 사용자의 멤버십을 제거합니다. 한 번에 최대 4개의 그룹에서 사용자를 제거할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자</td> 
   <td>그룹에서 제거할 사용자를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">도메인</td> 
   <td>이메일 주소가 아닌 Federated ID의 경우 사용자가 속한 도메인을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹</td> 
   <td>사용자를 제거할 각 그룹에 대해 <b>항목 추가</b>를 클릭하고 그룹을 입력하거나 매핑하십시오. 최대 4개의 그룹을 입력할 수 있으며 최소 하나 이상의 그룹을 입력해야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID 사용</td> 
   <td>Enterprise 또는 Federated ID이 동일한 이름으로 존재하는 경우에도 사용자 ID가 기존 Adobe ID을 참조하도록 해석하려면 true를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>



#### 사용자 업데이트

이 작업 모듈은 기존 사용자를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자</td> 
   <td>업데이트할 사용자의 ID를 입력하거나 매핑합니다. 사용자 이메일 주소입니다. 예: <code>user@example.com</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">도메인</td> 
   <td>이메일 주소가 아닌 Federated ID으로 사용자를 업데이트하는 경우 사용자를 식별하기 위해 사용자가 속한 도메인을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이메일</td> 
   <td>사용자의 새 이메일 주소를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이름</td> 
   <td>사용자의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">성</td> 
   <td>사용자의 성을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 사용자 그룹 작업

* [사용자 그룹에 대한 멤버십 추가](#add-memberships-for-a-user-group)
* [사용자 그룹 만들기](#create-a-user-group)
* [사용자 그룹 삭제](#delete-a-user-group)
* [사용자 그룹에 대한 멤버십 제거](#remove-memberships-for-a-user-group)
* [사용자 그룹 업데이트](#update-a-user-group)

#### 사용자 그룹에 대한 멤버십 추가

이 작업 모듈은 사용자 및 제품 프로필을 사용자 그룹에 추가합니다. 사용자 그룹에 추가된 사용자는 사용자 그룹의 모든 제품 프로필에 대한 권한을 갖습니다. 제품 프로필을 추가하면 사용자 그룹의 사용자에게 해당 프로필에 대한 권한이 부여됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 이름</td> 
   <td>사용자 또는 프로필을 제거할 그룹의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자</td> 
   <td>추가하려는 각 사용자에 대해 <b>사용자 추가</b>를 클릭하고 사용자의 전자 메일 주소를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">프로필</td> 
   <td>그룹에 추가할 각 프로필에 대해 <b>사용자 추가</b>를 클릭하고 프로필 이름을 입력하십시오</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 그룹 만들기

이 작업 모듈은 새 사용자 그룹을 만듭니다. 지정된 이름의 그룹이 이미 있는 경우 모듈은 기존 그룹을 업데이트할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 이름</td> 
   <td>새 사용자 그룹의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">설명</td> 
   <td>새 사용자 그룹에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">옵션</td> 
   <td>사용자 그룹이 이미 조직에 있는 경우 수행할 작업을 선택합니다. 옵션을 선택하지 않았으며 사용자 그룹이 이미 존재하는 경우 모듈에서 오류를 반환합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 그룹 삭제

이 작업 모듈은 기존 사용자 그룹을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 이름</td> 
   <td>삭제할 그룹의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 그룹에 대한 멤버십 제거

이 작업 모듈은 사용자 그룹에서 사용자 또는 프로필을 제거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">그룹 이름</td> 
   <td>사용자 또는 프로필을 제거할 그룹의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자</td> 
   <td>제거할 각 사용자에 대해 <b>사용자 추가</b>를 클릭하고 사용자의 전자 메일 주소를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">프로필</td> 
   <td>그룹에서 제거할 각 프로필에 대해 <b>사용자 추가</b>를 클릭하고 프로필 이름을 입력하십시오</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe ID 사용</td> 
   <td>true인 경우 사용자 ID는 Enterprise 또는 Federated ID이 동일한 이름으로 존재하는 경우에도 기존 Adobe ID을 참조하는 것으로 해석됩니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 그룹 업데이트

이 작업 모듈은 기존 사용자 그룹을 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">원래 그룹 이름</td> 
   <td>업데이트할 그룹의 현재 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">새 그룹 이름</td> 
   <td>그룹에 지정할 새 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">원래 그룹 이름</td> 
   <td>업데이트된 그룹 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
 </table>

### 기타


#### 사용자 지정 API 호출 만들기

이 작업 모듈은 Adobe 사용자 관리 API에 대한 사용자 지정 호출을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">연결</td>
      <td>Adobe User Management에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Adobe User Management에 연결 만들기</a>를 참조하십시오.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>상대 경로 입력 <code>https://usermanagement.adobe.io/v2/usermanagement/</code></p>
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
        <p>[!DNL Workfront Fusion] 인증 헤더 및 x-api-key 헤더를 자동으로 추가합니다.</p>
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
