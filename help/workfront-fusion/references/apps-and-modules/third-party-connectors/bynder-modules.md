---
title: 바이더 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Bynder]을(를) 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1847'
ht-degree: 0%

---

# [!DNL Bynder]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Bynder]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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
   <p>현재: Workfront Fusion 라이선스 요구 사항 없음</p>
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Bynder] 모듈을 사용하려면 [!DNL Bynder] 계정이 있어야 합니다.

## Byender API 정보

Bynder 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL Bynder] 연결  {#connect-bynder-to-workfront-fusion}

>[!NOTE]
>
>Byender는 인증 코드/새로 고침 토큰 부여 유형을 사용합니다. 이는 Fusion Byender 커넥터가 사용하는 유일한 권한 부여 유형입니다.

* [Workfront Fusion에서  [!DNL Bynder] 에 대한 연결 만들기](#create-a-connection-to-bynder-from-workfront-fusion)
* [[!UICONTROL 에서 ]클라이언트 ID[!UICONTROL  및 ]클라이언트 암호 [!DNL Bynder]  생성(선택 사항)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### Workfront Fusion에서 [!DNL Bynder]에 대한 연결 만들기

[!DNL Bynder] 모듈 내에서 직접 Workfront Fusion과 [!DNL Bynder] 계정에 연결할 수 있습니다.

1. [!DNL Bynder] 모듈에서 **[!UICONTROL 연결]** 필드 옆에 있는 [!UICONTROL 추가]를 클릭합니다.
1. 연결할 [!DNL Bynder] 도메인을 선택하십시오.
1. (선택 사항) **[!UICONTROL 고급 설정]**&#x200B;을 클릭한 다음 [!UICONTROL 클라이언트 ID] 및 [!UICONTROL 클라이언트 암호]를 입력하십시오.

   클라이언트 ID 및 클라이언트 암호를 생성하는 방법에 대한 지침은 이 문서의 [클라이언트 ID 및 클라이언트 암호 생성 [!DNL Bynder] (선택 사항)](#generate-a-client-id-and-client-secret-in-bynder-optional)을 참조하십시오.

1. [!UICONTROL 로그인] 창에서 사용자 이름(전자 메일 주소)과 암호를 입력합니다.
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

### [!UICONTROL 에서 ]클라이언트 ID[!UICONTROL  및 ]클라이언트 암호[!DNL Bynder] 생성(선택 사항)

클라이언트 ID와 클라이언트 암호를 사용하여 연결을 만들려면 [!DNL Bynder] 계정에서 연결을 생성할 수 있습니다. 클라이언트 ID 및 클라이언트 암호는 [!DNL Bynder]에서 앱을 만들 때 생성됩니다.

[!DNL Bynder]에서 앱을 만드는 방법에 대한 지침은 [ 설명서의 ](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/)Oauth 2.0 앱[!DNL Bynder]을 참조하십시오.

>[!NOTE]
>
>* [!DNL Bynder]에서 앱을 만들 때 `redirect uri`(으)로 다음을 입력하십시오.
>
>   * 미국 클러스터: `https://app.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * EU 클러스터: `https://app-eu.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Azure 클러스터: `https://app-az.workfrontfusion.com/oauth/cb/workfront-bynder`
>* Byender는 인증 코드/새로 고침 토큰 부여 유형을 사용합니다. 이는 Fusion Byender 커넥터가 사용하는 유일한 권한 부여 유형입니다.

## [!DNL Bynder]개 모듈 및 해당 필드

[!DNL Bynder] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Bynder] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [검색 결과](#searches)
* [트리거](#triggers)

### 액션

* [[!UICONTROL 자산에 태그 추가]](#add-a-tag-to-assets)
* [[!UICONTROL 컬렉션에 에셋 추가]](#add-assets-to-a-collection)
* [[!UICONTROL 사용자 지정 API 호출]](#custom-api-call)
* [[!UICONTROL 에셋 다운로드]](#download-asset)
* [[!UICONTROL 자산 메타데이터 읽기]](#read-asset-metadata)
* [에셋에서 [!UICONTROL 태그 제거]](#remove-a-tag-from-assets)
* [[!UICONTROL 컬렉션에서 에셋 제거]](#remove-assets-from-collection)
* [[!UICONTROL 자산 메타데이터 업데이트]](#update-asset-metadata)
* [[!UICONTROL 자산 업로드]](#upload-asset)

#### [!UICONTROL 자산에 태그 추가]

이 작업 모듈은 하나 이상의 에셋에 태그를 추가합니다

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 태그 ID]</td> 
   <td> <p>에셋에 추가할 태그의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID]</td> 
   <td> <p>태깅할 각 에셋에 대해 <strong>[!UICONTROL 항목 추가]</strong>를 클릭한 다음 에셋 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL 컬렉션에 에셋 추가]

이 작업 모듈은 하나 이상의 에셋을 컬렉션에 추가합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 컬렉션 ID]</td> 
   <td> <p>자산을 추가할 컬렉션의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID]</td> 
   <td> <p>컬렉션에 추가할 각 자산에 대해 <strong>[!UICONTROL 항목 추가]</strong>를 클릭한 다음 자산 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 지정 API 호출]

이 작업 모듈을 사용하면 [!DNL Bynder] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Bynder] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

이 모듈은 API 호출의 헤더 및 본문과 함께 상태 코드를 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td><code>https://{your-bynder-domain}/api/{api-version}/</code>과(와) 관련된 경로를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
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

#### [!UICONTROL 에셋 다운로드]

이 작업 모듈은 단일 자산을 다운로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID]</td> 
   <td>다운로드하려는 에셋의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 버전]</td> 
   <td> <p>다운로드하려는 에셋의 버전을 입력하거나 매핑합니다. 최신 버전의 에셋을 다운로드하려면 필드를 비워 둡니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 자산 메타데이터 읽기]

이 작업 모듈은 에셋의 메타데이터를 읽습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID]</td> 
   <td>메타데이터를 검색할 에셋의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 에셋에서 태그 제거]

이 작업 모듈은 하나 이상의 에셋에서 태그를 제거합니다

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 태그 ID]</td> 
   <td> <p>에셋에서 제거할 태그의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID]</td> 
   <td> <p>태그를 제거할 각 에셋에 대해 <strong>[!UICONTROL 항목 추가]</strong>를 클릭한 다음 에셋 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 컬렉션에서 에셋 제거]

이 작업 모듈은 컬렉션에서 하나 이상의 자산을 제거합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 컬렉션 ID]</td> 
   <td> <p>자산을 제거할 컬렉션의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID]</td> 
   <td> <p>컬렉션에서 제거할 각 에셋에 대해 <strong>[!UICONTROL 항목 추가]</strong>를 클릭한 다음 에셋 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 자산 메타데이터 업데이트]

이 작업 모듈은 기존 에셋의 메타데이터를 업데이트합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID]</td> 
   <td>메타데이터를 업데이트할 에셋의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td> <p>정보를 입력할 필드를 선택한 다음 메타데이터를 업데이트할 정보를 해당 필드에 입력하거나 매핑합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>업데이트할 옵션을 선택한 다음 해당 속성에 정보를 입력하거나 매핑합니다. 메타속성은 에셋의 특정 필드를 나타내지 않는 에셋에 대한 정보입니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 자산 업로드]

이 작업 모듈은 단일 자산을 업로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 다른 이름으로 저장]</td> 
   <td> <p>업로드할 파일을 저장할 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 새 자산]</strong> </p> <p>정보를 입력할 필드 및 메타속성을 선택한 다음 해당 필드에 정보를 입력합니다.</p> <p>업로드한 자산에 사용할 브랜드의 ID를 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 새 자산 버전]</strong> </p> <p>새 버전을 업로드할 에셋의 ID를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 파일]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 비동기 파일 업로드]</td> 
   <td>대용량 파일을 업로드할 때 이 옵션을 활성화하십시오. 이렇게 하면 큰 파일이 시나리오 실행을 차단하지 않습니다.</td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL 레코드 나열]](#list-record)
* [[!UICONTROL Assets 검색]](#search-assets)

#### [!UICONTROL 레코드 나열]

이 검색 모듈은 특정 유형의 모든 항목을 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>나열할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 모든 컬렉션 읽기]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL 모든 태그에 대한 정보 읽기]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL 컬렉션의 모든 에셋 읽기]</strong> </p> <p>에셋을 나열할 컬렉션의 ID를 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Assets 검색]

이 검색 모듈은 사용자가 제공한 기준에 따라 자산을 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 검색 기준]</td> 
   <td> <p>검색 기준을 입력합니다. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 필드]</strong> </p> <p>검색에 사용할 필드를 선택합니다</p> </li> 
     <li> <p><strong>[!UICONTROL 논리 연산자]</strong> </p> <p>검색에 사용할 연산자를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 값]</strong> </p> <p>선택한 필드에서 찾을 값을 입력하거나 매핑합니다. 값 유형은 선택한 필드의 데이터 유형과 동일해야 합니다. </p> <p>데이터 형식에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">항목 데이터 형식</a>을 참조하세요.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 결과 집합]</td> 
   <td>첫 번째 일치하는 에셋을 반환할지 또는 모든 일치하는 에셋을 반환할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 정렬 기준]</td> 
   <td> <p>정렬할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 정렬 방향]</td> 
   <td> <p>오름차순 또는 내림차순 정렬 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 트리거

#### [!UICONTROL 자산 보기]

이 트리거 모듈은 자산이 생성되거나 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Bynder] 연결 </a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">이벤트 유형</td>
    <td>새 에셋이 생성될 때 또는 기존 에셋이 업데이트될 때 시나리오를 시작할지 여부를 선택합니다.</td>
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>새 자산에 대해 감시할 컬렉션을 선택합니다. 모든 컬렉션을 보려면 이 필드를 비워 두십시오.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">출력</td>
    <td>출력에 포함할 필드를 선택합니다.</td>
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 제한]</td>

<td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
