---
title: Split.io 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는  [!DNL Split.io]을(를) 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1493'
ht-degree: 0%

---

# [!DNL Split.io]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Split.io]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

[!DNL Split.io] 모듈을 사용하려면 [!DNL Split.io] 계정이 있어야 합니다.

## Split.io API 정보

Split.io 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://api.split.io/internal/api</td>
   </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.34.1</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Split.io]을(를) [!DNL Workfront Fusion]에 연결 {#connect-split-io-to-workfront-fusion}

[!DNL Split.io] 모듈 내에서 직접 [!DNL Split.io] 계정에 연결할 수 있습니다.

1. [!DNL Split.io] 모듈에서 [!UICONTROL Connection] 필드 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 연결의 이름을 입력합니다.
1. [!DNL Split.io] API 키를 입력하십시오.

   [!DNL Split.io] API 키에 대한 자세한 내용은 [!DNL Split.io] 설명서의 [API 키](https://help.split.io/hc/en-us/articles/360019916211-API-keys)를 참조하십시오.

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## [!DNL Split.io]개 모듈 및 해당 필드

[!DNL split.io] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL split.io] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [검색 결과](#searches)

### 액션

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Get Split]](#get-split)
* [[!UICONTROL Get Split Definition in Environment]](#get-split-definition-in-environment)
* [[!UICONTROL Create Split]](#create-split)
* [[!UICONTROL Delete Split]](#delete-split)
* [[!UICONTROL Create Split Definition in Environment]](#create-split-definition-in-environment)
* [[!UICONTROL Remove Split Definition from Environment]](#remove-split-definition-from-environment)
* [[!UICONTROL Partial Update Split Definition in Environment]](#partial-update-split-definition-in-environment)
* [[!UICONTROL Associate Tags]](#associate-tags)

#### [!UICONTROL Custom API Call]

이 작업 모듈을 사용하면 [!DNL split.io] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL split.io] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://api.split.io/internal/api/v2/</code>과(와) 관련된 경로를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 사용할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split]

이 작업 모듈은 분할을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>검색할 분할이 포함된 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>검색할 분할 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split Definition in Environment]

이 작업 모듈은 지정된 환경에서 특정 분할 정의를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>검색할 분할 정의가 포함된 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>검색할 분할 정의가 포함된 환경을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>분할 정의를 검색할 분할 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split]

이 작업 모듈은 트래픽 유형이 지정된 경우 조직에서 새 분할을 생성합니다.

>[!NOTE]
>
>API는 어떤 환경에서도 분할을 구성하지 않습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>분할을 생성할 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Traffic Type ID or Name]</td> 
   <td>분할을 만드는 데 사용할 트래픽 유형을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>생성할 분할의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Description]</td> 
   <td>만들려는 분할에 대한 [!UICONTROL split] 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Split]

이 작업 모듈은 조직에서 분할을 삭제합니다. 이렇게 하면 모든 환경에서 분할 정의를 자동으로 구성 해제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>분할을 삭제할 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>삭제할 분할 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split Definition in Environment]

이 작업 모듈은 특정 환경에 대한 분할 정의를 구성합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>분할 정의를 생성할 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>분할 정의를 생성할 환경을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>정의를 생성할 분할의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>분할 정의에 추가할 주석을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rules]</td> 
   <td> <p>정의에 추가하려는 각 타겟팅 규칙에 대해 <b>[!UICONTROL Add item]</b>을(를) 클릭한 다음 규칙을 입력하거나 매핑합니다.</p> <p>타깃팅 규칙에 대한 자세한 내용은 [!DNL Split.io] 설명서의 <a href="https://docs.split.io/reference#create-split-definition-in-environment">환경에서 분할 정의 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default rule]</td> 
   <td> <p>다른 규칙의 사양을 충족하지 않는 트래픽에 대해 분할에서 사용할 규칙을 입력하거나 매핑합니다.</p> <p>타깃팅 규칙에 대한 자세한 내용은 [!DNL Split.io] 설명서의 <a href="https://docs.split.io/reference#create-split-definition-in-environment">환경에서 분할 정의 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default treatment]</td> 
   <td> <p>분할이 종료되거나 고객이 트래픽 할당에 포함되지 않은 경우 분할에서 사용할 처리를 입력하거나 매핑합니다.</p> <p>처리에 대한 자세한 내용은 [!DNL Split.io] 설명서의 <a href="https://docs.split.io/reference#create-split-definition-in-environment">환경에서 분할 정의 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Treatments]</td> 
   <td> <p>정의에 추가할 각 처리에 대해 <b>[!UICONTROL Add item]</b>을(를) 클릭한 다음 처리를 입력하거나 매핑합니다.</p> <p>처리에 대한 자세한 내용은 [!DNL Split.io] 설명서의 <a href="https://docs.split.io/reference#create-split-definition-in-environment">환경에서 분할 정의 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Split Definition from Environment]

이 작업 모듈은 특정 환경에 대한 분할 정의의 구성을 해제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>분할 정의를 제거할 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>분할 정의를 제거할 환경을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>정의를 제거할 분할의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>분할 정의에 추가할 주석을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Partial Update Split Definition in Environment]

이 작업 모듈은 특정 환경에 대한 분할 정의를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>분할 정의를 업데이트할 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>분할 정의를 업데이트할 환경을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>정의를 갱신할 분할의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update content]</td> 
   <td> <p>업데이트할 분할의 각 특성에 대해 <b>[!UICONTROL Add item]</b>을(를) 클릭하고 원하는 변경 내용을 입력하거나 매핑합니다.</p> <p>자세한 내용은 [!DNL Split.io] 설명서의 <a href="https://docs.split.io/reference#partial-update-split-definition-in-environment">환경의 분할 정의 부분 업데이트</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>분할 정의에 추가할 주석을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Associate Tags]

이 작업 모듈은 지정된 개체에 태그를 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>태그를 추가할 작업 영역을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Name]</td> 
   <td>태그를 추가할 개체의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type]</td> 
   <td> <p>태그를 추가할 개체 유형을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> <p>추가할 각 태그에 대해 <b>[!UICONTROL Add item]</b>을(를) 클릭하고 태그를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL Get Workspaces]](#get-workspaces)
* [[!UICONTROL Get Environments]](#get-environments)
* [[!UICONTROL Get Splits]](#get-splits)
* [[!UICONTROL List Split Definitions in an Environment]](#list-split-definitions-in-an-environment)
* [[!UICONTROL Get Traffic Types]](#get-traffic-types)

#### [!UICONTROL Get Workspaces]

이 검색 모듈은 조직의 작업 공간을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 검색할 최대 작업 공간 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Environments]

이 검색 모듈은 환경 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>나열할 환경이 포함된 작업 영역을 선택하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Splits]

이 검색 모듈은 분할 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>나열할 분할이 포함된 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 검색할 최대 분할 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Split Definitions in an Environment]

이 검색 모듈은 주어진 환경에서 분할 정의 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>나열할 분할 정의가 포함된 작업공간을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>나열할 분할 정의가 포함된 환경을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 검색할 분할 정의의 최대 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Traffic Types]

이 검색 모듈은 트래픽 유형 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Split.io] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">[!DNL Split.io]을(를) [!UICONTROL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>나열할 트래픽 유형이 포함된 작업 영역을 선택하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>
