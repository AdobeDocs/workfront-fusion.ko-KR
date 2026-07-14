---
title: Adobe Workfront Planning 모듈
description: ' [!DNL Adobe Workfront Planning] 모듈을 사용하면  [!DNL Adobe] Workfront Planning 계정의 이벤트를 기반으로 Adobe Workfront Fusion 시나리오를 시작하고, 계약 및 기타 레코드를 만들거나 읽거나 업데이트하고, 설정한 기준을 사용하여 레코드를 검색하고, 문서를 업로드할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
TQID: https://experienceleague.adobe.com/QHOFWDOT-18-c0b3wLXsRV5cjGVxlcyLhvZdkev3GFg
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: f0e185778e01b71a91837531a082e88485e97ca2
workflow-type: tm+mt
source-wordcount: 6075
ht-degree: 34%

---


# Adobe Workfront Planning 모듈

[!DNL Adobe Workfront Planning] 모듈을 사용하면 Workfront Planning에서 이벤트가 발생할 때 시나리오를 트리거할 수 있습니다. 레코드를 만들고, 읽고, 업데이트하고 삭제하거나 [!DNL Adobe Workfront Planning] 계정에 대한 사용자 지정 API 호출을 수행할 수도 있습니다.

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

Workfront Planning에 액세스하려면 다음 항목이 있어야 합니다.

* 새로운 Workfront 패키지 및 라이선스. 기존 Workfront 패키지 또는 라이선스에는 Workfront Planning을 사용할 수 없습니다.
* Workfront Planning 패키지
* 조직의 Workfront 인스턴스는 Adobe 통합 경험에 온보딩되어야 합니다.

## Adobe Workfront Planning API 정보

Adobe Workfront Planning 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td><pre><code>https://&#123;&#123;connection.host&#125;&#125;/maestro/api/&#123;&#123;common.maestroApiVersion&#125;&#125;/</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Planning을 Workfront Fusion에 연결

Workfront Planning 커넥터는 OAuth 2.0을 사용하여 Workfront Planning에 연결합니다.

Workfront Planning Fusion 모듈 내에서 직접 Workfront Planning 계정에 대한 연결을 생성할 수 있습니다.

* [클라이언트 ID 및 클라이언트 암호를 사용하여 Workfront Planning에 연결](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [서버 간 연결을 사용하여 Workfront Planning에 연결](#connect-to-workfront--planning-using-a-server-to-server-connection)

### 클라이언트 ID 및 클라이언트 암호를 사용하여 Workfront Planning에 연결

1. Adobe Workfront Planning 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
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
          <p><b>Adobe Workfront 인증</b> 연결을 선택하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새로운 연결의 이름을 입력합니다.</p>
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
        <td role="rowheader">[!UICONTROL 인증 URL]</td>
        <td>이 값은 기본값으로 유지되거나 Workfront 인스턴스의 URL을 입력한 다음 <code>/integrations/oauth2</code>를 입력할 수 있습니다. <p>예: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 호스트 접두사]</td>
        <td>대부분의 경우 이 값은 <code>origin</code>이어야 합니다.
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   Workfront Planning에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인한 후 연결을 허용할 수 있습니다.

>[!NOTE]
>
>* OAuth 2.0의 Workfront API에 대한 연결은 더 이상 API 키에 사용하지 않습니다.
>* Workfront 샌드박스 환경에 연결하려면 해당 환경에서 OAuth2 애플리케이션을 만든 다음 해당 애플리케이션에서 생성한 클라이언트 ID와 클라이언트 암호를 연결에 사용해야 합니다.

### 서버 간 연결을 사용하여 Workfront Planning에 연결

1. Adobe Workfront Planning 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
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

   Workfront Planning에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인한 후 연결을 허용할 수 있습니다.

>[!NOTE]
>
>* OAuth 2.0의 Workfront API에 대한 연결은 더 이상 API 키에 사용하지 않습니다.
>* Workfront 샌드박스 환경에 연결하려면 해당 환경에서 OAuth2 애플리케이션을 만든 다음 해당 애플리케이션에서 생성한 클라이언트 ID와 클라이언트 암호를 연결에 사용해야 합니다.

## [!DNL Adobe Workfront Planning] 버전 2 모듈 및 해당 필드

>[!IMPORTANT]
>
>이 섹션의 모듈은 Workfront Planning V2 커넥터에 속합니다.Workfront Planning V1 커넥터의 모듈에 대해서는 [[!DNL Adobe Workfront Planning] 버전 1 모듈 및 해당 필드](#adobe-workfront-planning-version-1-modules-and-their-fields)를 참조하십시오.

Workfront Planning 모듈을 구성할 때 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 Workfront 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

* [작업 영역](#workspaces-v2)
* [레코드 유형](#record-types-v2)
* [레코드](#records-v2)
* [필드](#fields-v2)
* [보기 횟수](#views-v2)
* [권한](#permissions-v2)
* [기타](#other-v2)

### 작업 공간(V2)

* [작업 영역 만들기](#create-a-workspace-v2)
* [작업 영역 삭제](#delete-a-workspace-v2)
* [모든 작업 영역 가져오기](#get-all-workspaces-v2)
* [작업 영역 가져오기](#get-a-workspace-v2)
* [작업 공간 업데이트](#update-a-workspace-v2)

#### 작업 공간 만들기(V2)

이 작업 모듈은 Planning에서 새 작업 공간을 생성합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace 이름]</p>
      </td>
      <td>새 작업 공간의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>설명</p>
      </td>
      <td>새 작업 영역/td&gt;에 대한 설명 입력 또는 매핑 
    </tr>
    <tr>
      <td role="rowheader">
        <p>색상</p>
      </td>
      <td>새 레코드 종류를 나타내는 데 사용할 색을 선택합니다</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>아이콘</p>
      </td>
      <td>이 레코드 종류에 사용할 아이콘을 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>소유자</p>
      </td>
      <td>작업 영역을 소유하려는 사용자의 Adobe IMS 사용자 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 작업 영역 삭제(V2)

이 작업 모듈은 ID로 지정된 단일 작업 영역을 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 작업 영역 ID]</p>
      </td>
      <td>삭제할 작업 영역의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 모든 작업 영역 가져오기(V2)

이 모듈은 모든 작업 영역의 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 작업 영역 수]</p>
      </td>
      <td>한 실행 주기 동안 모듈이 반환할 최대 작업 공간 수를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 작업 공간(V2) 가져오기

이 모듈은 ID로 작업 영역을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 작업 영역 ID]</p>
      </td>
      <td>검색할 작업 영역의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 작업 공간 업데이트(V2)

이 작업 모듈은 Planning의 새 작업 영역을 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>업데이트할 작업공간을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace 이름]</p>
      </td>
      <td>새 작업 공간의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>설명</p>
      </td>
      <td>새 작업 영역/td&gt;에 대한 설명 입력 또는 매핑 
    </tr>
    <tr>
      <td role="rowheader">
        <p>색상</p>
      </td>
      <td>새 레코드 종류를 나타내는 데 사용할 색을 선택합니다</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>아이콘</p>
      </td>
      <td>이 레코드 종류에 사용할 아이콘을 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>소유자</p>
      </td>
      <td>작업 영역을 소유하려는 사용자의 Adobe IMS 사용자 ID를 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>레코드 유형 섹션</p>
      </td>
      <td>이 작업 영역에 추가할 각 레코드 종류 섹션에 대해 <b>항목 추가</b>를 클릭하고 섹션의 이름, 레코드 종류 ID 및 기존 레코드 종류 ID를 덮어쓸지 여부를 입력하십시오.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>레코드 유형 섹션 &gt; 덮어쓰기</p>
      </td>
      <td>기존 섹션을 모듈의 섹션으로 대체할지 여부를 선택합니다. 이 옵션이 없으면 모듈의 섹션이 기존 섹션 목록에 추가됩니다.</td> 
    </tr>
  </tbody>
</table>


### 레코드 유형(V2)

* [레코드 유형 만들기](#create-a-record-type-v2)
* [레코드 유형 삭제](#delete-a-record-type-v2)
* [글로벌 레코드 유형 가져오기](#get-global-record-types-v2)
* [레코드 유형 가져오기](#get-a-record-type-v2)
* [레코드 유형 가져오기](#get-record-types-v2)
* [레코드 유형 업데이트](#update-a-record-type-v2)

#### 레코드 유형 만들기(V2)

이 작업 모듈은 선택한 작업 영역에 새 레코드 유형을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>레코드 유형을 만들 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>표시 이름</p>
      </td>
      <td>새 레코드 유형의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>설명</p>
      </td>
      <td>새 레코드 유형에 대한 설명을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>아이콘</p>
      </td>
      <td>이 레코드 종류에 사용할 아이콘을 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>색상</p>
      </td>
      <td>새 레코드 종류를 나타내는 데 사용할 색을 선택합니다</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Source 레코드 유형</p>
      </td>
      <td>다른 레코드 유형을 사용하여 시작점으로 복사하는 경우 해당 레코드 유형을 선택합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 유형 삭제(V2)

이 작업 모듈은 ID로 지정된 단일 레코드 유형을 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형 ID]</p>
      </td>
      <td>삭제하려는 레코드 유형의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 글로벌 레코드 유형 가져오기(V2)

이 모듈은 Adobe Workfront Planning 계정의 레코드 유형 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>작업 영역을 선택합니다. 모듈은 이 작업 영역에 추가할 수 있는 글로벌 레코드 유형을 반환합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 레코드 유형 수]</p>
      </td>
      <td>한 실행 주기 동안 모듈이 반환할 최대 레코드 종류 수를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 유형 가져오기(V2)

이 모듈은 해당 ID로 레코드 유형을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형 ID]</p>
      </td>
      <td>검색할 레코드 유형의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 유형 가져오기(V2)

이 모듈은 특정 작업 영역에서 사용할 수 있는 레코드 유형 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>레코드 유형을 검색할 작업공간을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 레코드 유형 수]</p>
      </td>
      <td>한 실행 주기 동안 모듈이 반환할 최대 레코드 종류 수를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 유형 업데이트(V2)

이 모듈은 레코드 유형을 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>레코드 유형을 업데이트할 작업공간을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>레코드 유형을 업데이트할 작업공간을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>표시 이름</p>
      </td>
      <td>레코드 유형의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>설명</p>
      </td>
      <td>레코드 유형에 대한 설명을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>기본 필드 ID</p>
      </td>
      <td>레코드 유형의 제목으로 사용되는 필드의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>아이콘</p>
      </td>
      <td>이 레코드 종류에 사용할 아이콘을 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>색상</p>
      </td>
      <td>새 레코드 종류를 나타내는 데 사용할 색을 선택합니다</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Workspace ID로 연결 가능</p>
      </td>
      <td>이 레코드 종류를 연결할 각 작업 영역에 대해 <b>항목 추가</b>를 클릭하고 작업 영역의 ID를 입력하십시오.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Workspace ID &gt; 덮어쓰기로 연결 가능</p>
      </td>
      <td>기존 작업 공간을 모듈의 작업 공간으로 교체할지 여부를 선택합니다. 이 옵션이 없으면 모듈의 작업공간이 기존 작업공간 목록에 추가됩니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>동적 레코드 유형을 만들 수 있는 권한 부여</p>
      </td>
      <td>이 레코드 종류에서 동적 레코드 종류를 만들도록 승인된 각 주제에 대해 <b>항목 추가</b>를 클릭하고 제목의 종류와 ID를 입력하십시오.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>동적 레코드 유형을 만들 수 있는 권한이 부여됨 &gt; 덮어쓰기</p>
      </td>
      <td>기존 주제를 모듈의 주어로 바꾸는지 여부를 선택합니다. 아니요. 로 설정하면 모듈의 주체가 기존 주제 목록에 추가됩니다.</td> 
    </tr>
  </tbody>
</table>



### 레코드(V2)

* [레코드 만들기](#create-a-record-v2)
* [레코드 삭제](#delete-a-record-v2)
* [레코드 가져오기](#get-a-record-v2)
* [레코드 유형별 레코드 가져오기](#get-records-by-record-type-v2)
* [레코드 이동](#move-records-v2)
* [레코드 검색](#search-records-v2)
* [레코드 업데이트](#update-a-record-v2)

#### 레코드 만들기(V2)

이 작업을 수행하면 Workfront Planning에 단일 레코드가 만들어집니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>레코드를 만들 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>만들려는 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>기타 필드</p>
      </td>
      <td>새 레코드에 보유할 값을 입력합니다. 이러한 필드는 선택한 레코드 유형을 기반으로 하며 Workfront Planning 조직에 고유합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 삭제(V2)

이 작업 모듈은 ID로 지정된 단일 레코드를 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 ID]</p>
      </td>
      <td>삭제할 레코드의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 가져오기(V2)

이 작업 모듈은 해당 ID로 지정된 레코드를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 작업 영역 ID]</p>
      </td>
      <td>검색할 레코드의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 종류별 레코드 가져오기(V2)

이 모듈은 지정된 레코드 종류의 모든 레코드 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>검색할 레코드가 포함된 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>반환할 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 레코드 수]</p>
      </td>
      <td>한 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 이동(V2)

이 모듈은 배치할 위치를 지정하여 레코드 유형 내에서 하나 이상의 레코드를 재정렬합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>이동할 레코드가 포함된 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>이동할 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>이동할 레코드가 포함된 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>이동할 레코드가 포함된 작업 영역을 선택합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 검색(V2)

지정한 기준에 따라 레코드를 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>검색할 레코드가 포함된 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>검색할 레코드가 포함된 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 기타 필드]</p>
      </td>
      <td>필터링할 각 필드에 대해 해당 필드에 대한 연산자 및 값을 입력합니다. 이러한 필드는 선택한 레코드 유형을 기반으로 하며 Workfront Planning 조직에 고유합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 업데이트(V2)

이 모듈은 지정된 레코드를 업데이트합니다.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>업데이트할 레코드가 포함된 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형 ID]</p>
      </td>
      <td>업데이트할 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 ID]</p>
      </td>
      <td>업데이트할 레코드의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 기타 필드]</p>
      </td>
      <td>다른 필드에 대한 값을 입력합니다. 사용 가능한 필드는 선택한 레코드에 따라 다릅니다.</td> 
    </tr>
  </tbody>
</table>


### 필드(V2)

* [필드 만들기](#create-a-field-v2)
* [필드 삭제](#delete-a-field-v2)
* [필드 가져오기](#get-a-field-v2)
* [레코드 유형별 필드 가져오기](#get-fields-by-record-type-v2)
* [필드 업데이트](#update-a-field-v2)

#### 필드 만들기(V2)

이 작업 모듈은 지정된 레코드 종류에 새 필드를 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>필드를 만들 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>필드를 만들 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>표시 이름</p>
      </td>
      <td>새 필드의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>설명</p>
      </td>
      <td>새 필드에 대한 설명을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>필드 유형</p>
      </td>
      <td>필드에 대한 데이터 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>기타 필드</p>
      </td>
      <td>선택된 필드 유형에 특정한 다른 필드를 사용할 수 있습니다. 이 필드에 대한 값을 입력합니다.</td> 
    </tr>
  </tbody>
</table>

#### 필드 삭제(V2)

이 작업 모듈은 ID로 지정된 단일 필드를 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 필드 ID]</p>
      </td>
      <td>삭제할 필드의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 필드 가져오기(V2)

이 모듈은 ID로 필드를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 필드 ID]</p>
      </td>
      <td>검색할 필드의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 종류별 필드 가져오기(V2)

이 모듈은 특정 레코드 종류에 대한 필드 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>반환할 필드가 포함된 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>필드를 반환할 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 필드 수]</p>
      </td>
      <td>한 실행 주기 동안 모듈이 반환할 최대 필드 수를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 필드 업데이트(V2)

이 모듈은 ID로 필드를 부분적으로 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 유형]</p>
      </td>
      <td>업데이트할 필드가 포함된 리소스 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 필드 ID]</p>
      </td>
      <td>업데이트할 필드를 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 표시 이름]</p>
      </td>
      <td>필드의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 설명]</p>
      </td>
      <td>필드에 대한 설명을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 기타 매개 변수]</p>
      </td>
      <td>다른 필드 매개 변수의 값을 입력합니다. 사용 가능한 매개 변수는 선택한 필드에 따라 다릅니다.</td> 
    </tr>
  </tbody>
</table>


### 보기(V2)

* [보기 만들기](#create-a-view-v2)
* [보기 삭제](#delete-a-view-v2)
* [보기 가져오기](#get-a-view-v2)
* [레코드 유형별 보기 가져오기](#get-views-by-record-type-v2)
* [보기 업데이트](#update-a-view-v2)

#### 보기 만들기(V2)

이 작업 모듈은 선택한 레코드 종류에 대한 새 보기를 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>보기를 만들 작업 영역을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>보기를 만들 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>보기 이름</p>
      </td>
      <td>새 보기의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>보기 유형</p>
      </td>
      <td>새 보기가 테이블, 타임라인 또는 달력 보기인지 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>시작 일자 필드</p>
      </td>
      <td>보기가 타임라인 또는 달력 보기인 경우, 보기에서 레코드를 타임라인에 배치하는 데 사용할 필드를 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>종료 날짜 필드.</p>
      </td>
      <td>보기가 타임라인 또는 달력 보기인 경우, 보기에서 타임라인의 종료 날짜를 결정하는 데 사용할 필드를 선택합니다.</td> 
    </tr>
  </tbody>
</table>

#### 보기 삭제(V2)

이 작업 모듈은 ID로 지정된 단일 보기를 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 보기 ID]</p>
      </td>
      <td>삭제할 보기의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 보기 가져오기(V2)

이 모듈은 ID로 보기를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 보기 ID]</p>
      </td>
      <td>검색할 보기의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 레코드 종류별 보기 횟수(V2)

이 모듈은 특정 레코드 종류에 대한 보기 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>검색할 뷰가 포함된 작업공간을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>검색할 뷰가 포함된 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 보기 수]</p>
      </td>
      <td>한 실행 주기 동안 모듈이 반환할 최대 보기 수를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 보기 업데이트(V2)

이 작업 모듈은 지정된 보기를 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>보기를 업데이트할 작업공간을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>뷰를 갱신할 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID 보기</p>
      </td>
      <td>업데이트할 보기를 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>보기 이름</p>
      </td>
      <td>새 보기의 이름을 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

### 권한(V2)

* [액세스 요청 닫기](#dismiss-access-requests-v2)
* [리소스에 대한 모든 멤버 및 해당 역할 가져오기](#get-all-members-and-their-roles-for-a-resource-v2)
* [리소스에 대한 현재 사용자의 유효 권한 얻기](#get-the-current-users-effective-permissions-on-a-resource-v2)
* [리소스에 대해 보류 중인 액세스 요청 나열](#list-pending-access-requests-for-a-resource-v2)
* [리소스에 대한 액세스 권한 요청](#request-access-to-a-resource-v2)

#### 액세스 요청 취소(V2)

이 작업 모듈은 ID로 지정된 하나 이상의 액세스 요청을 무시합니다.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 유형]</p>
      </td>
      <td>삭제할 Workspace의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 ID]</p>
      </td>
      <td>액세스 요청을 취소할 리소스의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 요청 ID]</p>
      </td>
      <td>취소할 각 액세스 요청에 대해 <b>항목 추가</b>를 클릭하고 요청 ID를 입력하십시오.</td> 
    </tr>
  </tbody>
</table>

#### 리소스에 대한 모든 멤버 및 역할 가져오기(V2)

이 모듈에는 리소스에 대한 명시적 공유 관계가 있는 모든 사용자, 그룹 및 팀이 나열됩니다. 이 모듈에 대한 연결에 사용되는 자격 증명에는 리소스에 대한 관리 권한이 있어야 합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 유형]</p>
      </td>
      <td>정보를 검색할 리소스 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 ID]</p>
      </td>
      <td>정보를 검색할 리소스의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 리소스에 대한 현재 사용자의 유효 권한 얻기(V2)

이 모듈은 주어진 리소스에 대한 현재 사용자의 보기, 편집, 삭제 및 추가 권한을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 유형]</p>
      </td>
      <td>권한을 검색할 리소스 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 ID]</p>
      </td>
      <td>권한을 검색할 리소스의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 리소스에 대해 보류 중인 액세스 요청 나열(V2)

이 모듈은 지정된 리소스에 대해 보류 중인 모든 액세스 요청을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 유형]</p>
      </td>
      <td>정보를 검색할 리소스 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 ID]</p>
      </td>
      <td>정보를 검색할 리소스의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 리소스에 대한 액세스 요청(V2)

이 모듈은 지정된 리소스에 대한 현재 사용자에 대한 액세스 요청을 만들거나 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 유형]</p>
      </td>
      <td>액세스 요청을 만들거나 업데이트할 리소스 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 리소스 ID]</p>
      </td>
      <td>액세스 요청을 만들거나 업데이트할 리소스의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Message]</p>
      </td>
      <td>액세스 요청에 포함할 메시지 텍스트를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>



### 기타(V2)

* [Workfront ID에서 인증 ID 가져오기](#get-auth-id-from-workfront-id-v2)
* [사용자 정의 API 호출하기](#make-a-custom-api-call-v2)
* [이벤트 보기](#watch-events-v2)

#### Workfront ID(V2)에서 인증 ID 가져오기

이 모듈은 Workfront 사용자 ID를 가져와 Planning에서 사용하는 일치하는 인증 ID를 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workfront 사용자 ID]</p>
      </td>
      <td>인증 ID를 검색할 사용자의 Workfront ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 사용자 지정 API 호출 만들기(V2)&lt;표

이 모듈은 Workfront Planning API에 대한 사용자 정의 호출을 수행합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p><code> https://&lt;WORKFRONT_DOMAIN>/maestro/api/.</code>와 관련된 경로를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API 버전]</td> 
   <td>모듈에서 사용할 Workfront API 버전을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion의 HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다. 요청의 콘텐츠 유형을 결정합니다.</p> <p>예:<code> {"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>예: <code>{"name":"something-urgent"}</code></p> <p>팁: 쿼리 매개변수 대신 JSON 본문을 통해 정보를 전송하는 것이 좋습니다.</p> </td> 
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

#### 이벤트 보기(V2)

이 트리거 모듈은 기록, 레코드 유형 또는 작업 영역이 Workfront Planning에서 생성, 업데이트 또는 삭제될 때 시나리오를 시작합니다.

>[!IMPORTANT]
>
>이 모듈은 나중에 편집하여 웹후크를 편집할 수 있습니다.
>
>Webhook을 업데이트할 때에는 다음 사항을 고려하십시오.
>
>* 편집된 웹후크는 Workfront 이벤트 구독에서 새 구독으로 처리됩니다. 이전 웹후크 구성은 별도의 이벤트 구독으로 간주되므로 이벤트 구독 내역이 보존되지 않습니다.
>* 이전 이벤트 구독에서 새 이벤트 구독으로의 전환이 완벽하게 동기화되지 않을 수 있습니다. 따라서 이벤트를 두 번 받거나(새 구독이 이전 구독이 중지되기 전에 시작되는 경우) 이벤트를 놓칠 수 있습니다(새 구독이 시작되기 전에 이전 구독이 중지되는 경우).
>
>웹후크 편집에 대한 자세한 내용은 [웹후크 편집](/help/workfront-fusion/manage-scenarios/edit-webhooks.md)을 참조하십시오.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 웹후크]</td>
      <td>사용할 웹후크를 선택하거나 추가 를 클릭하여 새 웹후크를 만듭니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 오브젝트 유형]</td>
      <td>레코드, 레코드 종류 또는 작업 영역을 감시할지 여부를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>새 레코드, 업데이트된 레코드, 새 레코드와 업데이트된 레코드 모두 또는 삭제된 레코드를 볼지 여부를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 구성 유형]</td>
      <td>단순 구성 또는 고급 구성 중 어떤 것을 원하는지 선택합니다. <p>고급 구성에 대한 자세한 내용은 이 문서의 <a href="#example-of-advanced-logic-in-the-watch-events-module" class="MCXref xref" >이벤트 보기 모듈의 고급 논리 예제</a>를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 상태]</td>
      <td>이전 상태를 볼 것인지 새 상태를 볼 것인지 선택합니다.<ul><li><p><b>[!UICONTROL 새 상태]</b></p><p>레코드가 지정된 값<b>으로</b> 변경되면 시나리오를 트리거합니다.</p></li><li><p><b>[!UICONTROL 이전 상태]</b></p><p>레코드가 지정된 값<b>에서</b> 변경되면 시나리오를 트리거합니다.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>레코드를 보는 경우 레코드를 볼 Workspace을 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레코드 유형]</td>
      <td>레코드를 보는 경우 보려는 레코드 유형을 선택합니다.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 이벤트 필터]</p> </td> 
      <td> <p>선택한 기준을 충족하는 레코드만 보도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터가 평가할 필드, 연산자, 필터를 허용하기 원하는 값을 입력합니다. AND 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> <p>참고: 기존 Workfront 웹후크에서는 필터를 편집할 수 없습니다. Workfront 이벤트 구독에 대해 서로 다른 필터를 설정하려면 현재 웹후크를 제거하고 새 웹후크를 만듭니다.</p> <p>이벤트 필터에 대한 자세한 내용은 Workfront 모듈 문서의 Workfront &gt; [!UICONTROL Watch Events] 모듈에서 <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">이벤트 구독 필터</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>새로운 항목을 감시할지 여부를 선택합니다. 업데이트, 새 레코드 및 업데이트 또는 삭제된 레코드.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 이 연결에 의해 수행된 업데이트 제외]</p>
      </td>
      <td>이 모듈에서 사용한 연결에 의해 변경이 있을 때 시나리오가 트리거되지 않도록 하려면 이 옵션을 활성화합니다. 이렇게 하면 이 시나리오가 트리거 작업을 수행하는 경우 시나리오의 다른 인스턴스가 트리거되지 않습니다.</td> 
    </tr>
  </tbody>
</table>

이 모듈에서 고급 로직을 사용하는 예는 [이벤트 보기 모듈의 고급 로직 예제](#example-of-advanced-logic-in-the-watch-events-module)를 참조하십시오.






## [!DNL Adobe Workfront Planning] 버전 1 모듈 및 해당 필드

>[!IMPORTANT]
>
>이 섹션의 모듈은 Workfront Planning V1 커넥터에 속합니다.Workfront Planning V2 커넥터의 모듈에 대해서는 [[!DNL Adobe Workfront Planning] 버전 2 모듈 및 해당 필드](#adobe-workfront-planning-version-2-modules-and-their-fields)를 참조하십시오.

Workfront Planning 모듈을 구성할 때 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 Workfront 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.


![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)
* [미분류](#uncategorized)

### 트리거

#### 이벤트 보기

이 트리거 모듈은 기록, 레코드 유형 또는 작업 영역이 Workfront Planning에서 생성, 업데이트 또는 삭제될 때 시나리오를 시작합니다.

>[!IMPORTANT]
>
>이 모듈은 나중에 편집하여 웹후크를 편집할 수 있습니다.
>
>Webhook을 업데이트할 때에는 다음 사항을 고려하십시오.
>
>* 편집된 웹후크는 Workfront 이벤트 구독에서 새 구독으로 처리됩니다. 이전 웹후크 구성은 별도의 이벤트 구독으로 간주되므로 이벤트 구독 내역이 보존되지 않습니다.
>* 이전 이벤트 구독에서 새 이벤트 구독으로의 전환이 완벽하게 동기화되지 않을 수 있습니다. 따라서 이벤트를 두 번 받거나(새 구독이 이전 구독이 중지되기 전에 시작되는 경우) 이벤트를 놓칠 수 있습니다(새 구독이 시작되기 전에 이전 구독이 중지되는 경우).
>
>웹후크 편집에 대한 자세한 내용은 [웹후크 편집](/help/workfront-fusion/manage-scenarios/edit-webhooks.md)을 참조하십시오.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 웹후크]</td>
      <td>사용할 웹후크를 선택하거나 추가 를 클릭하여 새 웹후크를 만듭니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 오브젝트 유형]</td>
      <td>레코드, 레코드 종류 또는 작업 영역을 감시할지 여부를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 상태]</td>
      <td>이전 상태를 볼 것인지 새 상태를 볼 것인지 선택합니다.<ul><li><p><b>[!UICONTROL 새 상태]</b></p><p>레코드가 지정된 값<b>으로</b> 변경되면 시나리오를 트리거합니다.</p></li><li><p><b>[!UICONTROL 이전 상태]</b></p><p>레코드가 지정된 값<b>에서</b> 변경되면 시나리오를 트리거합니다.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>레코드를 보는 경우 레코드를 볼 Workspace을 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레코드 유형]</td>
      <td>레코드를 보는 경우 보려는 레코드 유형을 선택합니다.</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 이벤트 필터]</p> </td> 
      <td> <p>선택한 기준을 충족하는 레코드만 보도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터가 평가할 필드, 연산자, 필터를 허용하기 원하는 값을 입력합니다. AND 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> <p>참고: 기존 Workfront 웹후크에서는 필터를 편집할 수 없습니다. Workfront 이벤트 구독에 대해 서로 다른 필터를 설정하려면 현재 웹후크를 제거하고 새 웹후크를 만듭니다.</p> <p>이벤트 필터에 대한 자세한 내용은 Workfront 모듈 문서의 Workfront &gt; [!UICONTROL Watch Events] 모듈에서 <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">이벤트 구독 필터</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>새로운 항목을 감시할지 여부를 선택합니다. 업데이트, 새 레코드 및 업데이트 또는 삭제된 레코드.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 이 연결에 의해 수행된 업데이트 제외]</p>
      </td>
      <td>이 모듈에서 사용한 연결에 의해 변경이 있을 때 시나리오가 트리거되지 않도록 하려면 이 옵션을 활성화합니다. 이렇게 하면 이 시나리오가 트리거 작업을 수행하는 경우 시나리오의 다른 인스턴스가 트리거되지 않습니다.</td> 
    </tr>
  </tbody>
</table>

이 모듈에서 고급 로직을 사용하는 예는 [이벤트 보기 모듈의 고급 로직 예제](#example-of-advanced-logic-in-the-watch-events-module)를 참조하십시오.

### 액션

* [레코드 유형 삭제](#delete-a-record-type)
* [사용자 정의 AI 호출 만들기](#make-a-custom-api-call)

#### 레코드 유형 삭제

이 작업 모듈은 해당 ID로 Workfront Planning에서 단일 레코드 유형을 삭제합니다.

>[!WARNING]
>
>Workfront Planning에서 레코드 유형을 삭제하면 레코드 유형 테이블의 모든 레코드도 삭제됩니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형 ID]</p>
      </td>
      <td>삭제하려는 레코드 유형의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

#### 사용자 정의 API 호출하기

이 모듈은 [!DNL Adobe Workfront Planning] API에 대한 사용자 지정 API 호출을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>상대 경로 입력 <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
      </td>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 헤더]</td>
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


### 검색 결과

#### 레코드 검색

이 작업 모듈은 지정한 조건에 따라 레코드 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>검색할 레코드가 포함된 Workspace을 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형]</p>
      </td>
      <td>검색할 레코드 유형을 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 필드]</p>
      </td>
      <td>검색할 각 필드에 대해 해당 필드를 찾아 연산자를 선택한 다음 검색할 값을 입력하거나 매핑합니다. 필드는 선택한 레코드 유형에 따라 사용할 수 있습니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Condition for filters]</p>
      </td>
      <td>필터 조건 선택:<ul><li><b>및</b><p>모듈이 사용자가 선택한 필드 값의 <b>모두</b>를 충족하는 레코드를 반환합니다.</p></li><li><b>또는</b><p>모듈은 선택한 필드 값의 <b>any</b>을(를) 충족하는 레코드를 반환합니다.</p></li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 제한]</p>
      </td>
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
    </tr>
  </tbody>
</table>


### 미분류


#### 레코드 만들기

이 작업을 수행하면 Workfront Planning에 단일 레코드가 만들어집니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 유형 ID]</p>
      </td>
      <td>생성할 레코드 유형을 입력하거나 매핑합니다. 사용 가능한 레코드 유형은 Workfront Planning 계정을 기반으로 합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>기타 필드</p>
      </td>
      <td>새 레코드에 보유할 값을 입력합니다. 이 필드는 선택한 레코드 종류를 기반으로 합니다.</td> 
    </tr>
    <tr>
  </tbody>
</table>

### 레코드 삭제

이 작업 모듈은 Workfront Planning에서 지정된 레코드를 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 ID]</p>
      </td>
      <td>삭제할 레코드의 ID를 입력하거나 매핑합니다.</td> 
    </tr>
  </tbody>
</table>

### 레코드 가져오기

이 작업 모듈은 ID로 지정된 [!DNL Adobe Workfront Planning]에서 단일 레코드를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레코드 ID]</td>
      <td>검색할 레코드의 ID를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

### 레코드 유형별 레코드 가져오기

이 작업 모듈은 지정된 유형의 모든 레코드를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>검색할 레코드가 포함된 작업 영역을 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레코드 유형]</td>
      <td>검색할 레코드 유형을 선택합니다.</td>
    </tr>
    <!--
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
    -->
  </tbody>
</table>

### 레코드 유형 가져오기

이 작업 모듈은 [!DNL Adobe Workfront Planning] 계정의 레코드 종류 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>검색할 레코드 유형이 포함된 작업 영역을 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

### 레코드 업데이트

이 작업은 Workfront Planning의 단일 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Workfront Planning]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >[!DNL Adobe Workfront Planning]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레코드 ID]</p>
      </td>
      <td>업데이트할 레코드 유형을 입력하거나 매핑합니다. 사용 가능한 레코드 유형은 Workfront Planning 계정을 기반으로 합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>기타 필드</p>
      </td>
      <td>레코드에 보유할 새 값을 입력합니다. 이 필드는 선택한 레코드 종류를 기반으로 합니다.</td> 
    </tr>
    <tr>
  </tbody>
</table>


## 읽을 수 있는 `record-types` 분류에 JSONata 사용

다음 JSONata 표현식은 레코드 유형 분류를 제공하는 Planning 쿼리의 사람이 읽을 수 있는 출력을 생성합니다. 이렇게 하면 레코드 유형 이름, 필드 이름 및 필드 옵션 이름(해당하는 경우)을 사람이 이름으로 읽을 수 있도록 하고 나머지 구조는 그대로 유지합니다.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

JSONata 모듈 사용에 대한 자세한 내용은 [JSONata 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md)을 참조하십시오.

## 이벤트 보기 모듈의 고급 논리 예

다음은 Workfront Planning > 이벤트 보기 모듈을 사용할 때 고급 로직에서 사용하는 형식의 예입니다.

```
[
  {
    "fieldName": "recordTypeId",
    "fieldValue": "Rt68c886502d4b5554ee80896b",
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "planning"
    },
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "active"
    },
    "comparison": "eq",
    "state": "newState"
  }
]
```

이벤트 보기 모듈에서 고급 로직을 사용할 때 다음 사항을 고려하십시오.

* 첫 번째 `"fieldvalue":` 항목은 URL에서 가져온 계획 레코드 유형 ID입니다. 이 예제에서 Planning 레코드 유형 ID는 `Rt68c886502d4b5554ee80896b`입니다.
* Planning 데이터가 `data `(이 예제에 `"fieldName": "data"`(으)로 표시됨) 배열 내에서 반환됩니다.
* Planning fieldNames는 `F`(으)로 시작하는 ID로 반환됩니다.
* 이 예제는 `OR` 필터 커넥터에 대해 평가 중이므로 동일한 필드(`F68c886502d4b5554eec808975`)에 대해 두 개의 항목이 있습니다.  모듈이 필터링하는 두 가지 드롭다운 옵션은 `"planning"` 및 `"active"`입니다.

