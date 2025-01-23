---
title: 모듈 확장
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 [!UICONTROL Widen]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 1%

---

# [!DNL Widen]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!UICONTROL Widen]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

[!UICONTROL Widen] 모듈을 사용하려면 [!UICONTROL Widen] 계정이 있어야 합니다.

## API 정보 확장

확장 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.10.11</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Widen]을(를) [!DNL Workfront Fusion]에 연결 {#connect-widen-to-workfront-fusion}

[!DNL Widen] 모듈 내에서 직접 [!DNL Widen] 계정에 연결할 수 있습니다.

1. [!DNL Widen] 모듈에서 [!UICONTROL Connection] 필드 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 연결할 [!DNL Widen] 도메인을 선택하십시오.
1. [!DNL Widen] 계정에 대한 토큰을 입력하십시오. 이 토큰을 찾는 방법에 대한 지침은 [[!DNL Widen] API FAQ](https://community.widen.com/collective/s/article/API-FAQs)를 참조하십시오.
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## [!DNL Widen]개 모듈 및 해당 필드

[!DNL Widen] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Widen] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거 모듈](#trigger-modules)
* [작업 모듈](#action-modules)
* [모듈 검색](#search-modules)

### 트리거 모듈

#### [!UICONTROL Watch assets]

이 트리거 모듈은 자산이 생성되거나 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p>새 에셋 또는 업데이트된 에셋을 시청할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>에셋 필드 외에 모듈 출력에 포함할 속성을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈 출력에 포함할 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 사용할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 작업 모듈

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read asset info]](#read-asset-info)
* [[!UICONTROL Add assets to collections]](#add-assets-to-collections)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Download File]](#download-file)
* [[!UICONTROL Upload] 파일](#upload-a-file)

#### [!UICONTROL Custom API Call]

이 작업 모듈을 사용하면 [!DNL Widen] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Widen] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>최신 버전의 [!DNL Widen] API를 사용할지 또는 버전 1.0을 사용할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>API 호출에 대한 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] 인증 헤더를 추가합니다.</p> </td> 
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

#### [!UICONTROL Read asset info]

이 작업 모듈은 고유 ID로 개별 자산을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>정보를 읽을 자산의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>에셋 필드 외에 모듈 출력에 포함할 속성을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈 출력에 포함할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add assets to collections]

이 작업 모듈은 컬렉션에 하나 이상의 에셋을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td> <p>에셋을 추가할 각 컬렉션에 대해:</p> 
    <ol> 
     <li value="1"> <p> <strong>[!UICONTROL Add]</strong>을(를) 클릭합니다.</p> </li> 
     <li value="2"> <p>[!UICONTROL Collection ID]을(를) 입력하거나 매핑합니다.</p> </li> 
     <li value="3"> <p><strong>[!UICONTROL Add item]</strong>을(를) 클릭합니다.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> <p>컬렉션에 추가할 각 에셋에 대해 다음 작업을 수행하십시오.</p> 
    <ol> 
     <li value="1"> <p> <strong>[!UICONTROL Add]</strong>을(를) 클릭합니다.</p> </li> 
     <li value="2"> <p>자산 ID를 입력하거나 매핑합니다.</p> </li> 
     <li value="3"> <p><strong>[!UICONTROL Add item]</strong>을(를) 클릭합니다.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 사용할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collections ID]</td> 
   <td> <p>에서 에셋을 제거할 각 컬렉션에 대해:</p> 
    <ol> 
     <li value="1"> <p> <strong>[!UICONTROL Add]</strong>을(를) 클릭합니다.</p> </li> 
     <li value="2"> <p>컬렉션 ID를 입력하거나 매핑합니다.</p> </li> 
     <li value="3"> <p><strong>[!UICONTROL Add item]</strong>을(를) 클릭합니다.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ASSETS ID</td> 
   <td> <p>컬렉션에서 제거할 각 에셋에 대해 다음 작업을 수행하십시오.</p> 
    <ol> 
     <li value="1"> <p> <strong>[!UICONTROL Add]</strong>을(를) 클릭합니다.</p> </li> 
     <li value="2"> <p>자산 ID를 입력하거나 매핑합니다.</p> </li> 
     <li value="3"> <p><strong>[!UICONTROL Add item]</strong>을(를) 클릭합니다.</p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 사용할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

이 작업 모듈은 자산의 메타데이터 필드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>메타데이터를 업데이트할 에셋의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata type]</td> 
   <td> <p>업데이트할 메타데이터의 메타데이터 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>업데이트할 메타데이터 필드를 선택합니다. 각 필드에 대해 새 필드 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 사용할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download File]

이 작업 모듈은 [!DNL Widen] 계정에서 자산을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>다운로드하려는 에셋의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

이 작업 모듈은 파일을 [!DNL Widen] 계정으로 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Profile]</td> 
   <td> <p>모듈에서 사용할 업로드 프로필을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload Method]</td> 
   <td> <p>파일 업로드 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL From File]</strong> </p> <p>이전 모듈에서 소스 파일을 선택하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL By URL]</strong> </p> <p>업로드할 파일의 URL을 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>업로드한 파일의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata Type]</td> 
   <td>업로드할 파일의 메타데이터 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>파일 업로드에 포함할 메타데이터 필드를 선택합니다. 각 필드에 대해 필드에 [!UICONTROL value]을(를) 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 모듈 검색

* [[!UICONTROL Read collection assets]](#read-collection-assets)
* [[!UICONTROL Search assets]](#search-assets)

#### [!UICONTROL Read collection assets]

이 작업 모듈은 컬렉션 내의 자산 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>읽을 자산을 포함하는 컬렉션의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>나열할 첫 번째 항목의 번호를 입력하거나 매핑합니다. 이것은 레코드에 페이지를 매기는 방법입니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>에셋을 정렬할 속성을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>에셋을 오름차순으로 정렬할지 아니면 내림차순으로 정렬할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈 출력에 포함할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search assets]

이 검색 모듈은 특정 검색 기준과 일치하는 에셋 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>[!DNL Widen] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-widen-to-workfront-fusion" class="MCXref xref">[!DNL Widen]을(를) [!DNL Workfront Fusion] </a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search query]</td> 
   <td> <p>에셋을 검색할 기준을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort By]</td> 
   <td> <p>에셋을 정렬할 방법을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order]</td> 
   <td>에셋을 오름차순으로 정렬할지 아니면 내림차순으로 정렬할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include deleted]</td> 
   <td>삭제된 에셋을 검색에 포함하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Include archived]</p> </td> 
   <td> <p>보관된 자산을 검색에 포함하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search document text]</td> 
   <td>이 옵션을 활성화하면 검색에 문서 텍스트가 포함되고, false를 활성화하면 검색 기준과 일치하는 제목이 있는 자산만 포함됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Offset]</td> 
   <td>세부 정보를 검색할 첫 번째 항목의 번호를 입력하거나 매핑합니다. 이것은 레코드에 페이지를 매기는 방법입니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scroll]</td> 
   <td>스크롤을 허용하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand]</td> 
   <td> <p>에셋 필드 외에 모듈 출력에 포함할 속성을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈 출력에 포함할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>
