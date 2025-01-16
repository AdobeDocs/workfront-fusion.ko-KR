---
title: Frame.io 모듈
description: ' [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] 계정입니다.'
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1969'
ht-degree: 0%

---

# [!DNL Frame.io]개 모듈

[!DNL Adobe Workfront Fusion] [!DNL Frame.io] 모듈을 사용하면 [!DNL Frame.io] 계정의 자산 및 주석을 모니터링, 만들기, 업데이트, 검색 또는 삭제할 수 있습니다.

Frame.io 커넥터에 대한 비디오 소개는 다음을 참조하십시오.

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

[!DNL Frame.io] 모듈을 사용하려면 [!DNL Frame.io] 계정이 있어야 합니다.

## Frame.io API 정보

Frame.io 커넥터에서는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://api.frame.io/v2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Frame.io]을(를) [!UICONTROL Adobe Workfront Fusion]에 연결

API 토큰을 사용하거나 OAuth 2.0을 사용하여 [!DNL Frame.io]에 연결할 수 있습니다.

[API 토큰을 사용하여  [!DNL Frame.io] 에 연결](#connect-to-frameio-using-an-api-token)

[OAuth 2.0 PKCE를 사용하여  [!DNL Frame.io] 에 연결](#connect-to-frameio-using-oauth-20-pkce)

### API 토큰을 사용하여 [!DNL Frame.io]에 연결

API 토큰을 사용하여 [!DNL Frame.io] 계정을 [!DNL Workfront Fusion]에 연결하려면 [!DNL Frame.io] 계정에서 API 토큰을 만든 후 [!DNL Workfront Fusion] [!DNL Frame.io] [!UICONTROL Create a connection] 대화 상자에 삽입해야 합니다.

1. [!DNL Frame.io] 계정에 로그인합니다.
1. [!DNL Frame.io] 개발자의 **[!UICONTROL Tokens]** 페이지로 이동합니다.
1. **[!UICONTROL New]**&#x200B;을(를) 클릭합니다.
1. 토큰 이름을 입력하고 사용할 범위를 선택한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.
1. 제공된 토큰을 복사합니다.
1. [!DNL Workfront Fusion](으)로 이동하여 [!DNL Frame.io] 모듈의 **[!UICONTROL Create a connection]** 대화 상자를 엽니다.
1. **[!UICONTROL Connection type]** 필드에서 **[!DNL Frame.io]**&#x200B;을(를) 선택합니다.
1. 5단계에서 복사한 토큰을 **[!UICONTROL Your [!DNL Frame.io] API Key]** 필드에 입력하고 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하여 연결을 설정합니다.

연결이 설정되었습니다. 모듈 설정을 진행할 수 있습니다.

### OAuth 2.0 PKCE를 사용하여 [!DNL Frame.io]에 연결

선택적 클라이언트 ID가 있는 OAuth 2.0 PKCE를 사용하여 [!DNL Frame.io]에 연결할 수 있습니다. 연결에 클라이언트 ID를 포함하려면 [!DNL Frame.io] 계정에 OAuth 2.0 앱을 만들어야 합니다.

* [OAuth 2.0 PKCE(클라이언트 ID 없음)를 사용하여  [!DNL Frame.io] 에 연결](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [OAuth 2.0 PKCE(클라이언트 ID 포함)를 사용하여  [!DNL Frame.io] 에 연결](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### OAuth 2.0 PKCE(클라이언트 ID 없음)를 사용하여 [!DNL Frame.io]에 연결

1. [!DNL Workfront Fusion](으)로 이동하여 [!DNL Frame.io] 모듈의 **[!UICONTROL Create a connection]** 대화 상자를 엽니다.
1. **[!UICONTROL Connection type]** 필드에서 **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Connection name]** 필드에 새 연결의 이름을 입력하십시오.
1. 연결을 설정하려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

연결이 설정되었습니다. 모듈 설정을 진행할 수 있습니다.

#### OAuth 2.0 PKCE(클라이언트 ID 포함)를 사용하여 [!DNL Frame.io]에 연결

1. [!DNL Frame.io]에서 OAuth 2.0 앱을 만듭니다. 지침은 [!UICONTROL OAuth 2.0 Code Authorization Flow]의 [!DNL Frame.io] 설명서를 참조하십시오.

   >[!IMPORTANT]
   >
   >[!DNL Frame.io]에서 OAuth 2.0 앱을 만들 때:
   >
   >* 리디렉션 URI로 다음을 입력합니다.
   >   
   >  아메리카/APAC `https://app.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >  EMEA `https://app-eu.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >* PCKE 옵션을 활성화합니다.


1. 제공된 `client_id`을(를) 복사합니다.
1. [!DNL Workfront Fusion](으)로 이동하여 [!DNL Frame.io] 모듈의 **[!UICONTROL Create a connection]** 대화 상자를 엽니다.
1. **[!UICONTROL Connection type]** 필드에서 **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Connection name]** 필드에 새 연결의 이름을 입력하십시오.
1. **[!UICONTROL Show advanced settings]**&#x200B;을(를) 클릭합니다.
1. 2단계에서 복사한 `client_id`을(를) **[!UICONTROL Client ID]** 필드에 입력합니다.
1. 연결을 설정하려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

연결이 설정되었습니다. 모듈 설정을 진행할 수 있습니다.

## [!DNL Frame.io]개 모듈 및 해당 필드

[!DNL Frame.io] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Frame.io] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [자산](#assets)
* [댓글](#comments)
* [프로젝트](#projects)
* [기타](#other)

### 자산

* [[!UICONTROL Create an Asset]](#create-an-asset)
* [[!UICONTROL Delete an Asset]](#delete-an-asset)
* [[!UICONTROL Get an Asset]](#get-an-asset)
* [[!UICONTROL List Assets]](#list-assets)
* [[!UICONTROL Update an Asset]](#update-an-asset)
* [[!UICONTROL Watch Asset Deleted]](#watch-asset-deleted)
* [[!UICONTROL Watch Asset Label Updated]](#watch-asset-label-updated)
* [[!UICONTROL Watch New Asset]](#watch-new-asset)

#### [!UICONTROL Create an Asset]

이 작업 모듈은 새 자산을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>에셋을 만들 프로젝트를 소유하고 있는 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>프로젝트를 선택하거나 자산을 만들 프로젝트 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>폴더를 선택하거나 자산을 만들 폴더의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>폴더 또는 파일 생성 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>새 파일 또는 폴더의 이름을 입력합니다.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">File Type </td> 
    <td> <p>Select the type of file you want to upload.</p> </td> 
   </tr>
  --> <!--
   <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>The file size in bytes.</p> </td> 
   </tr>
  --> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>업로드할 파일의 URL을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>자산에 대한 간단한 설명을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Asset]

이 작업 모듈은 지정된 에셋을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>삭제하려는 에셋이 포함된 프로젝트를 소유하는 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> 삭제할 자산을 포함하는 또는 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>삭제할 자산이 포함된 폴더를 선택합니다</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>삭제할 자산을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Asset]

이 작업 모듈은 자산 세부 사항을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>세부 정보를 검색할 에셋이 포함된 프로젝트를 소유하는 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> 세부 정보를 검색할 에셋이 포함된 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>세부 정보를 검색할 에셋이 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>에셋을 선택하거나 세부 정보를 검색할 에셋의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Assets]

이 검색 모듈은 지정된 프로젝트의 폴더에 있는 모든 에셋을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>자산을 검색할 폴더가 포함된 프로젝트를 소유하는 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> 자산을 검색할 폴더가 포함된 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>에셋을 나열할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 자산 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### `[!UICONTROL Update an Asset]`

이 작업 모듈에서는 기존 에셋의 이름, 설명 또는 사용자 지정 필드를 업데이트할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>에셋을 업데이트할 프로젝트를 소유한 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>프로젝트를 선택하거나 자산을 업데이트할 프로젝트의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>폴더를 선택하거나 자산을 업데이트할 폴더의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>업데이트된 파일의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>업데이트된 자산에 대한 간단한 설명을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Deleted]

이 트리거 모듈은 자산이 삭제되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> 웹후크의 이름을 입력합니다(예: 에셋 삭제됨).</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>이 웹후크를 만들 팀을 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Label Updated]

이 트리거 모듈은 에셋의 상태가 설정, 변경 또는 제거되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> 웹후크의 이름(예: 에셋 상태 업데이트됨)을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>이 웹후크를 만들 팀을 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Asset]

이 트리거 모듈은 새 에셋이 생성될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> 웹후크의 이름(예: 생성된 에셋)을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>이 웹후크를 만들 팀을 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 댓글

* [[!UICONTROL Create a Comment]](#create-a-comment)
* [[!UICONTROL Delete a Comment]](#delete-a-comment)
* [[!UICONTROL Get a Comment]](#get-a-comment)
* [[!UICONTROL List Comments]](#list-comments)
* [[!UICONTROL Update a Comment]](#update-a-comment)
* [[!UICONTROL Watch Comment Updated]](#watch-comment-updated)
* [[!UICONTROL Watch New Comment]](#watch-new-comment)

#### [!UICONTROL Create a Comment]

이 작업 모듈은 자산에 새 댓글 또는 회신을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>댓글을 작성할지 댓글에 답글을 달지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>댓글을 추가할 에셋이 포함된 프로젝트를 소유한 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>프로젝트를 선택하거나 댓글을 추가할 자산이 포함된 프로젝트의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>폴더를 선택하거나 댓글을 추가할 자산이 포함된 폴더의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>댓글을 추가할 에셋을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>회신을 추가할 댓글을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> 댓글이나 답글의 텍스트 내용을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>댓글이 연결되어야 하는 비디오 프레임 번호를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Comment]

이 작업 모듈은 기존 주석을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID]</td> 
   <td> <p> 댓글을 삭제할 에셋이 포함된 프로젝트를 소유한 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> 프로젝트를 선택하거나 댓글을 삭제할 자산이 포함된 프로젝트의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p> 댓글을 삭제할 에셋이 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>삭제할 댓글이 포함된 자산을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>삭제할 주석을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Comment]

이 작업 모듈은 지정된 주석의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>자산을 검색할 폴더가 포함된 프로젝트를 소유하는 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>자산을 검색할 폴더가 포함된 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>에셋을 나열할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>검색할 주석이 포함된 자산을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>세부 정보를 가져올 주석을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Comments]

이 검색 모듈은 지정된 자산의 모든 주석을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>주석을 검색할 폴더가 포함된 프로젝트를 소유하는 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>주석을 가져올 폴더가 포함된 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>설명을 나열할 에셋이 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>설명을 나열할 자산을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 댓글 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Comment]

이 작업 모듈은 기존 주석을 편집합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>댓글을 업데이트할 에셋이 포함된 프로젝트를 소유한 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>댓글을 업데이트할 에셋이 포함된 프로젝트 \ 를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>댓글을 업데이트할 에셋이 포함된 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>댓글을 업데이트할 에셋을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>업데이트할 주석을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> 주석의 텍스트 콘텐츠를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>댓글이 연결된 비디오의 프레임 번호를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comment Updated]

이 트리거 모듈은 댓글을 편집할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>웹후크의 이름을 입력합니다(예: Comment Edited).</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>이 웹후크를 만들 팀을 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Comment]

이 트리거 모듈은 새 댓글 또는 답글이 작성되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>웹후크의 이름을 입력합니다(예: ). 새 댓글.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>이 웹후크를 만들 팀을 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 프로젝트

#### [!UICONTROL List Projects]

이 검색 모듈은 지정된 팀의 모든 프로젝트를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>프로젝트를 검색할 팀을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 프로젝트 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

#### [!UICONTROL Make an API Call]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code>https://api.frame.io</code>과(와) 관련된 경로를 입력하십시오. 예: <code> /v2/teams</code></p> <p>참고: 사용 가능한 끝점 목록은 [!DNL Frame.io] API 참조를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 인증 헤더를 자동으로 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>요청 쿼리 문자열을 입력합니다. 쿼리 문자열에 포함할 각 매개 변수에 대해 <b>[!UICONTROL Add item]</b>을(를) 클릭하고 필드 이름과 원하는 값을 입력합니다.</p> </td> 
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

**예:** 다음 API 호출은 [!DNL Frame.io] 계정에 있는 모든 팀과 세부 정보를 반환합니다.

URL: `/v2/teams`

메서드: `GET`

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

결과는 번들 > 본문 아래의 모듈 출력에서 확인할 수 있습니다.

이 예에서는 1개 팀의 세부 정보가 반환되었습니다.

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)
