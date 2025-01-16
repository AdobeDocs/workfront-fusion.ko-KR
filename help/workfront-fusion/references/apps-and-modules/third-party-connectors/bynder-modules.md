---
title: 바이더 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는  [!DNL Bynder]을(를) 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Bynder]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Bynder]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

* [ [!DNL Workfront Fusion]에서  [!DNL Bynder] 에 연결 만들기](#create-a-connection-to-bynder-from-workfront-fusion)
* [ [!DNL Bynder] 에서 [!UICONTROL Client ID] 및 [!UICONTROL Client Secret] 생성(선택 사항)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### [!DNL Workfront Fusion]에서 [!DNL Bynder]에 연결 만들기

[!DNL Bynder] 모듈 내에서 직접 [!DNL Workfront Fusion]에서 [!DNL Bynder] 계정에 연결할 수 있습니다.

1. [!DNL Bynder] 모듈에서 [!UICONTROL Connection] 필드 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 연결할 [!DNL Bynder] 도메인을 선택하십시오.
1. (선택 사항) **[!UICONTROL Advanced settings]**&#x200B;을(를) 클릭한 다음 [!UICONTROL Client ID] 및 [!UICONTROL Client Secret]을(를) 입력합니다.

   클라이언트 ID 및 클라이언트 암호를 생성하는 방법에 대한 지침은 이 문서의 [클라이언트 ID 및 클라이언트 암호 생성 [!DNL Bynder] (선택 사항)](#generate-a-client-id-and-client-secret-in-bynder-optional)을 참조하십시오.

1. [!UICONTROL login] 창에서 사용자 이름(이메일 주소)과 암호를 입력합니다.
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

### [!DNL Bynder]에서 [!UICONTROL Client ID] 및 [!UICONTROL Client Secret] 생성(선택 사항)

클라이언트 ID와 클라이언트 암호를 사용하여 연결을 만들려면 [!DNL Bynder] 계정에서 연결을 생성할 수 있습니다. 클라이언트 ID 및 클라이언트 암호는 [!DNL Bynder]에서 앱을 만들 때 생성됩니다.

[!DNL Bynder]에서 앱을 만드는 방법에 대한 지침은 [!DNL Bynder] 설명서의 [Oauth 2.0 앱](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/)을 참조하십시오.

>[!NOTE]
>
>[!DNL Bynder]에서 앱을 만들 때 `redirect uri`(으)로 다음을 입력하십시오.
>
>`https://app.workfrontfusion.com/oauth/cb/workfront-bynder`

## [!DNL Bynder]개 모듈 및 해당 필드

[!DNL Bynder] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Bynder] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [검색 결과](#searches)
* [트리거](#triggers)

### 액션

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read asset metadata]](#read-asset-metadata)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Add assets to a collection]](#add-assets-to-a-collection)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Add a tag to assets]](#add-a-tag-to-assets)
* [자산의 [!UICONTROL Remove a tag]](#remove-a-tag-from-assets)
* [[!UICONTROL Download asset]](#download-asset)
* [[!UICONTROL Upload asset]](#upload-asset)

#### [!UICONTROL Custom API Call]

이 작업 모듈을 사용하면 [!DNL Bynder] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Bynder] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

이 모듈은 API 호출의 헤더 및 본문과 함께 상태 코드를 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td><code>https://{your-bynder-domain}/api/{api-version}/</code>과(와) 관련된 경로를 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL Read asset metadata]

이 작업 모듈은 에셋의 메타데이터를 읽습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>메타데이터를 검색할 에셋의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

이 작업 모듈은 기존 에셋의 메타데이터를 업데이트합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>메타데이터를 업데이트할 에셋의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>정보를 입력할 필드를 선택한 다음 메타데이터를 업데이트할 정보를 해당 필드에 입력하거나 매핑합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>업데이트할 옵션을 선택한 다음 해당 속성에 정보를 입력하거나 매핑합니다. 메타속성은 에셋의 특정 필드를 나타내지 않는 에셋에 대한 정보입니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add assets to a collection]

이 작업 모듈은 하나 이상의 에셋을 컬렉션에 추가합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>자산을 추가할 컬렉션의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>컬렉션에 추가할 각 에셋에 대해 <strong>[!UICONTROL Add item]</strong>을(를) 클릭한 다음 에셋 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

이 작업 모듈은 컬렉션에서 하나 이상의 자산을 제거합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>자산을 제거할 컬렉션의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>컬렉션에서 제거할 각 에셋에 대해 <strong>[!UICONTROL Add item]</strong>을(를) 클릭한 다음 에셋 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add a tag to assets]

하나 이상의 에셋에 태그 추가

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>에셋에 추가할 태그의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>태깅할 각 에셋에 대해 <strong>[!UICONTROL Add item]</strong>을(를) 클릭한 다음 에셋 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a tag from assets]

하나 이상의 에셋에서 태그 제거

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>에셋에서 제거할 태그의 ID를 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>태그를 제거할 각 에셋에 대해 <strong>[!UICONTROL Add item]</strong>을(를) 클릭한 다음 에셋 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download asset]

이 작업 모듈은 단일 자산을 다운로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>다운로드하려는 에셋의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset version]</td> 
   <td> <p>다운로드하려는 에셋의 버전을 입력하거나 매핑합니다. 최신 버전의 에셋을 다운로드하려면 필드를 비워 둡니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload asset]

이 작업 모듈은 단일 자산을 업로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save as]</td> 
   <td> <p>업로드할 파일을 저장할 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL New asset]</strong> </p> <p>정보를 입력할 필드 및 메타속성을 선택한 다음 해당 필드에 정보를 입력합니다.</p> <p>업로드한 자산에 사용할 브랜드의 ID를 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL New asset version]</strong> </p> <p>새 버전을 업로드할 에셋의 ID를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL List record]](#list-record)
* [[!UICONTROL Search for assets]](#search-for-assets)

#### [!UICONTROL List record]

이 검색 모듈은 특정 유형의 모든 항목을 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>나열할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Read all collections]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read information about all tags]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read all assets of a collection]</strong> </p> <p>에셋을 나열할 컬렉션의 ID를 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for assets]

이 검색 모듈은 사용자가 제공한 기준에 따라 자산을 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criteria]</td> 
   <td> <p>검색 기준을 입력합니다. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>검색에 사용할 필드를 선택합니다</p> </li> 
     <li> <p><strong>[!UICONTROL Logical Operator]</strong> </p> <p>검색에 사용할 연산자를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>선택한 필드에서 찾을 값을 입력하거나 매핑합니다. 값 유형은 선택한 필드의 데이터 유형과 동일해야 합니다. </p> <p>데이터 형식에 대한 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>의 <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">항목 데이터 형식을 참조하십시오.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>첫 번째 일치하는 에셋을 반환할지 또는 모든 일치하는 에셋을 반환할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>정렬할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort Direction]</td> 
   <td> <p>오름차순 또는 내림차순 정렬 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>모듈의 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 트리거

#### [!UICONTROL Watch assets]

이 트리거 모듈은 자산이 생성되거나 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>[!DNL Bynder] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">[!DNL Bynder]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> <!--
    <td role="rowheader">Event type</td>
   --> <!--
    <td>Select whether you want to start the scenario when a new asset is created or when an existing asset is updated.</td>
   --> 
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>새 자산에 대해 감시할 컬렉션을 선택합니다. 모든 컬렉션을 보려면 이 필드를 비워 두십시오.</p> </td> 
  </tr> 
  <tr> <!--
    <td role="rowheader">Outputs</td>
   --> <!--
    <td>Select the fields that you want to include in the output.</td>
   --> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
