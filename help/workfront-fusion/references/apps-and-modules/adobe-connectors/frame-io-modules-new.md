---
title: Frame.io(Beta) 모듈
description: ' [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] 계정입니다.'
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '3559'
ht-degree: 1%

---

# [!DNL Frame.io] V4 모듈

>[!IMPORTANT]
>
>이 문서에서는 Frame.io 커넥터의 새 버전에 대해 설명합니다. 이 커넥터는 Frame.io 버전 4에 연결하는 데 사용됩니다.
>
>Frame.io 커넥터의 레거시 버전에 대한 지침은 [Frame.io 레거시 커넥터](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)를 참조하십시오.

Adobe Workfront Fusion [!DNL Frame.io] 모듈을 사용하면 [!DNL Frame.io] 계정의 에셋 및 주석을 모니터링, 만들기, 업데이트, 검색 또는 삭제할 수 있습니다.

Workfront은 연결 중인 Frame.io 버전에 따라 두 개의 Frame.io 커넥터를 제공합니다.

| 커넥터 | Frame.io 버전 |
|---|---|
| Frame.io | V4 |
| Frame.io(기존) | V3 |

Frame.io 커넥터의 레거시 버전에 대한 지침은 [Frame.io 레거시 커넥터](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)를 참조하십시오.


Frame.io 커넥터에 대한 비디오 소개는 다음을 참조하십시오.

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>작업 기반: Workfront Fusion 라이센스 요구 사항 없음</p>
   <p>커넥터 기반(레거시): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

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
   <td> https://api.frame.io/v4</td> 
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

사용자 자격 증명으로 자동으로 연결하거나, 사용자 자격 증명 연결을 수동으로 만들거나, 서버 간 연결을 만들 수 있습니다.

* [사용자 자격 증명으로 자동 연결](#connect-automatically-with-user-credentials#)
* [사용자 자격 증명 연결을 수동으로 만듭니다.](#create-a-user-credentials-connection-manually)
* [서버 간 연결 만들기](#create-a-server-to-server-connection)

### 사용자 자격 증명으로 자동 연결

이 메서드는 Frame.io에 로그인하는 경우 자동으로 연결을 만들거나 로그인할 수 있도록 Frame.io 로그인 페이지에 연결합니다.

1. Frame.io Beta 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 연결의 이름을 입력합니다.
1. **계속**&#x200B;을 클릭합니다.
1. Frame.io 계정에 로그인하라는 메시지가 표시되면 로그인합니다.
1. 둘 이상의 Frame.io 조직에 속해 있는 경우 이 연결에 사용할 조직을 선택합니다.

연결이 만들어집니다.

### 사용자 자격 증명 연결을 수동으로 만듭니다.

Frame.io에 로그인하거나 클라이언트 ID 또는 클라이언트 암호를 제공하여 사용자 자격 증명 연결을 만들 수 있습니다.

서버 간 연결을 만들려면 먼저 Adobe Developer Console에서 애플리케이션을 구성해야 합니다.

* [Adobe Developer Console에서 사용자 자격 증명 만들기](#create-user-credentials-in-the-adobe-developer-console)
* [사용자 인증 연결 구성](#configure-a-user-authentication-connection)

#### Adobe Developer Console에서 사용자 자격 증명 만들기

Adobe Developer Console 프로젝트에 서버 간 자격 증명이 없는 경우 만들 수 있습니다.

1. [Adobe Developer Console](https://developer.adobe.com/)을 엽니다.
1. 이 연결에 사용할 Adobe Developer Console의 기존 프로젝트 선택

   또는

   Adobe Developer Console에서 새 프로젝트를 만듭니다. 지침은 [빈 프로젝트 만들기](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)를 참조하십시오.

1. 프로젝트 개요 페이지 또는 새 프로젝트 시작 페이지에서 **API 추가**&#x200B;를 클릭합니다.
1. 열리는 페이지에서 **Frame.io API**&#x200B;를 찾아 클릭합니다.
1. 인증 유형 선택 페이지에서 **사용자 인증**&#x200B;을 선택하고 **다음**&#x200B;을 클릭합니다.
1. 사용자 인증 자격 증명 추가 페이지에서 **OAuth 웹 앱**&#x200B;을 선택하고 **다음**&#x200B;을 클릭합니다.
1. OAuth 웹 앱 자격 증명 구성 페이지에서 다음을 입력합니다.   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 기본 리디렉션 URI]</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 리디렉션 URI 패턴]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. **다음**&#x200B;을 클릭합니다.
1. **구성된 API 저장**&#x200B;을 클릭합니다.
1. 제품 페이지에서 방금 만든 자격 증명에 대한 카드를 클릭합니다.

   여기에서 클라이언트 ID와 클라이언트 암호를 찾을 수 있습니다.

>[!NOTE]
>
> Adobe Workfront Fusion에서 연결 구성을 시작할 때 이 창을 열어 두는 것이 좋습니다. 이 페이지에서 클라이언트 ID를 복사하고 클라이언트 암호를 검색 및 복사하여 연결 필드에 붙여넣을 수 있습니다.


#### 사용자 인증 연결 구성

1. Frame.io Beta 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 연결 만들기 상자에서 **고급 설정 표시**&#x200B;를 클릭합니다.

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
            <p><b>IMS 사용자 인증</b>을 선택합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 연결 이름]</td>
          <td>
            <p>이 연결의 이름을 입력하십시오.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 ID]를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 사용자 자격 증명 만들기</a>를 참조하십시오.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 사용자 자격 증명 만들기</a>를 참조하십시오.</p>
        </tr>
       </tbody>
    </table>
1. Frame.io 계정에 로그인하라는 메시지가 표시되면 로그인합니다.
1. 둘 이상의 Frame.io 조직에 속해 있는 경우 이 연결에 사용할 조직을 선택합니다.

연결이 만들어집니다.


### 서버 간 연결 만들기

서버 간 연결을 만들려면 먼저 Adobe Developer Console에서 애플리케이션을 구성해야 합니다.

* [Adobe Developer Console에서 서버 간 자격 증명 만들기](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [서버 간 연결 구성](#configure-a-server-to-server-connection)

#### Adobe Developer Console에서 서버 간 자격 증명 만들기

Adobe Developer Console 프로젝트에 서버 간 자격 증명이 없는 경우 만들 수 있습니다.

1. [Adobe Developer Console](https://developer.adobe.com/)을 엽니다.
1. 이 연결에 사용할 Adobe Developer Console의 기존 프로젝트 선택

   또는

   Adobe Developer Console에서 새 프로젝트를 만듭니다. 지침은 [빈 프로젝트 만들기](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)를 참조하십시오.

1. 프로젝트 개요 페이지 또는 새 프로젝트 시작 페이지에서 **API 추가**&#x200B;를 클릭합니다.
1. 열리는 페이지에서 **Frame.io API**&#x200B;를 찾아 클릭합니다.
1. 인증 유형 선택 페이지에서 **서버 간 인증**&#x200B;을 선택하고 **다음**&#x200B;을 클릭합니다.
1. 자격 증명의 이름을 입력합니다. 이렇게 하면 나중에 Adobe Admin Console의 API 자격 증명 영역에서 자격 증명을 식별할 수 있습니다.
1. **다음**&#x200B;을 클릭합니다.
1. 제품 프로필 선택 페이지에서 연결할 Frame.io 계정이 포함된 제품 프로필을 선택합니다.
1. **구성된 API 저장**&#x200B;을 클릭합니다.
1. 제품 페이지에서 방금 만든 자격 증명에 대한 카드를 클릭합니다.

   여기에서 클라이언트 ID와 클라이언트 암호를 찾을 수 있습니다.

>[!NOTE]
>
> Adobe Workfront Fusion에서 연결 구성을 시작할 때 이 창을 열어 두는 것이 좋습니다. 이 페이지에서 클라이언트 ID를 복사하고 클라이언트 암호를 검색 및 복사하여 연결 필드에 붙여넣을 수 있습니다.


#### 서버 간 연결 구성

1. Frame.io Beta 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

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
            <p><b>서버에 대한 IMS 서버</b>를 선택하십시오.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 연결 이름]</td>
          <td>
            <p>이 연결의 이름을 입력하십시오.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 ID]를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 서버 간 자격 증명 만들기</a>를 참조하십시오.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 서버 간 자격 증명 만들기</a>를 참조하십시오.</p>
        </tr>
       </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.




## [!DNL Frame.io]개 모듈 및 해당 필드

[!DNL Frame.io] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Frame.io] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [자산](#assets)
* [댓글](#comments)
* [폴더](#folders)
* [프로젝트](#projects)
* [공유](#shares)
* [작업 영역](#workspaces)
* [기타](#other)

### 자산

* [[!UICONTROL 자산 만들기]](#create-an-asset)
* [[!UICONTROL 자산 삭제]](#delete-an-asset)
* [[!UICONTROL 자산 가져오기]](#get-an-asset)
* [[!UICONTROL 자산 나열]](#list-assets)
* [자산 보기 삭제됨](#watch-asset-deleted)
* [새 자산 보기](#watch-new-asset)

#### [!UICONTROL 자산 만들기] <!--different for v4-->

이 작업 모듈은 새 자산을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 자산을 만들 프로젝트가 포함된 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>작업 영역을 선택하거나 자산을 만들려는 프로젝트가 포함된 작업 영역의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>프로젝트를 선택하거나 자산을 만들 프로젝트 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>자산을 만들 경로를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 이름] </td> 
   <td> <p>이 자산에 사용할 파일의 이름을 입력합니다.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">파일 크기 </td> 
    <td> <p>파일 크기를 바이트 단위로 입력하거나 매핑합니다.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>파일을 만드는 경우 업로드할 파일의 URL을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>이 자산에 대한 미디어 유형을 선택합니다.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL 자산 삭제]

이 작업 모듈은 지정된 에셋을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 삭제할 자산을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID] </td> 
   <td> <p>삭제할 자산을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 자산 가져오기]

이 작업 모듈은 자산 세부 사항을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 검색할 자산을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID] </td> 
   <td> <p>검색할 자산을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 자산 나열]

이 검색 모듈은 지정된 프로젝트의 폴더에 있는 모든 에셋을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 나열할 자산을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 자산 수] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 자산 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 자산 보기 삭제됨

이 트리거 모듈은 자산이 삭제되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가 를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 삭제된 자산을 확인하려는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 새 자산 보기

이 트리거 모듈은 새 에셋이 생성될 때 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가 를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 새 자산을 확인하려는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 댓글

* [[!UICONTROL 댓글 만들기]](#create-a-comment)
* [[!UICONTROL 댓글 삭제]](#delete-a-comment)
* [[!UICONTROL 댓글 가져오기]](#get-a-comment)
* [[!UICONTROL 댓글 나열]](#list-comments)
* [[!UICONTROL 댓글 업데이트]](#update-a-comment)
* [업데이트된 댓글 보기](#watch-comment-updated)
* [새 댓글 보기](#watch-new-comment)

#### [!UICONTROL 댓글 만들기]

이 작업 모듈은 자산에 새 댓글 또는 회신을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 댓글을 추가할 자산이 포함된 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>계정을 선택하거나 댓글을 추가할 에셋이 포함된 작업 공간 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>프로젝트를 선택하거나 댓글을 추가할 자산이 포함된 프로젝트의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>댓글을 추가할 에셋의 경로를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> 댓글이나 답글의 텍스트 내용을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 타임스탬프] </td> 
   <td> <p>댓글이 연결되어야 하는 비디오 프레임 번호를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>자산이 PDF인 경우 댓글을 첨부해야 하는 페이지를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 삭제]

이 작업 모듈은 기존 주석을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 삭제하려는 주석이 포함된 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 주석 ID] </td> 
   <td> <p>삭제할 댓글의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 가져오기]

이 작업 모듈은 지정된 주석의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 세부 정보를 검색할 주석이 포함된 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 주석 ID] </td> 
   <td> <p>세부 정보를 가져올 주석을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 나열]

이 검색 모듈은 지정된 자산의 모든 주석을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>댓글을 검색할 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>주석을 검색할 에셋이 포함된 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>댓글을 검색할 에셋이 포함된 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>설명을 나열할 에셋으로 연결되는 경로를 선택합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 주석 수] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 주석 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 업데이트]

이 작업 모듈은 기존 주석을 편집합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>댓글을 업데이트할 에셋이 포함된 프로젝트가 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 주석 ID] </td> 
   <td> <p>업데이트할 주석을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> 주석의 텍스트 콘텐츠를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 타임스탬프] </td> 
   <td> <p>댓글이 연결된 비디오의 프레임 번호를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>자산이 PDF인 경우 댓글이 첨부된 페이지를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 업데이트된 댓글 보기

이 트리거 모듈은 댓글이 업데이트되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가 를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 업데이트된 댓글이 있는지 확인할 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 새 댓글 보기

이 트리거 모듈은 댓글이 작성되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가 를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 새 댓글이 있는지 확인할 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 폴더

#### 폴더 만들기

이 작업 모듈은 Frame.io에 새 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>폴더를 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>폴더를 만들 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>폴더를 만들 위치를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>폴더를 만들 경로를 선택합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>새 폴더의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 프로젝트

* [프로젝트 만들기](#create-a-project)
* [Frame.io 프로젝트에 사용자 초대](#invite-users-to-frameio-project)
* [프로젝트 나열](#list-projects)

#### 프로젝트 만들기

이 작업 모듈은 Frame.io에서 새 프로젝트를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>프로젝트를 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>프로젝트를 만들 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>새 프로젝트의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Frame.io 프로젝트에 사용자 초대

이 작업 모듈은 지정된 Frame.io 프로젝트에 사용자를 초대합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>사용자를 초대하려는 프로젝트가 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>사용자를 초대하려는 프로젝트가 포함된 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">프로젝트 ID </td> 
   <td> <p>사용자를 초대할 프로젝트를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">사용자 ID </td> 
   <td> <p>프로젝트에 초대할 사용자를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 프로젝트 나열]

이 검색 모듈은 지정된 팀의 모든 프로젝트를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>프로젝트를 검색할 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>프로젝트를 검색할 에셋이 포함된 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 프로젝트 수] </td> 
   <td> <p>최대 프로젝트 수 입력 또는 매핑
   각 시나리오 실행 주기 동안 모듈이 반환되도록 합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 공유

* [공유 링크에 자산 추가](#add-an-asset-to-a-share-link)
* [공유 링크 만들기](#create-a-share-link)

#### 공유 링크에 자산 추가

이 작업 모듈은 Frame.io의 공유 링크에 자산을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>에셋을 추가할 공유 링크가 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 공유 링크 ID] </td> 
   <td> <p>에셋을 추가할 공유 링크를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 자산 ID] </td> 
   <td> <p>공유 링크에 추가할 자산의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 공유 링크 만들기

이 작업 모듈은 Frame.io에 새 공유 링크를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>공유 링크를 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>공유 링크를 만들 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>공유 링크를 만들 프로젝트를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">액세스 </td> 
   <td> <p>이 링크에 공개 또는 제한된 액세스 권한이 있는지 선택합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">자산 </td> 
   <td> <p>공유 링크에 추가하려는 각 에셋에 대해 <b>항목 추가</b>를 클릭하고 에셋의 ID를 입력합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">설명 </td> 
   <td> <p>공유 링크에 대한 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>공유 링크의 만료 날짜를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>새 공유 링크의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>공유 링크에 대한 암호를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 작업 영역

#### 작업 영역 만들기

이 작업 모듈은 Frame.io에 새 작업 영역을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>작업 영역을 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이름] </td> 
   <td> <p>작업 공간에 대한 새 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 작업 영역 나열

이 모듈에는 계정의 모든 작업 영역이 나열됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>작업 영역을 검색할 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 작업 영역 수] </td> 
   <td> <p>최대 작업 공간 수 입력 또는 매핑
   각 시나리오 실행 주기 동안 모듈이 반환되도록 합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [사용자 지정 API 호출 만들기](#make-a-custom-api-call)
* [업데이트된 메타데이터 값 보기](#watch-metadata-value-updated)


#### [!UICONTROL 사용자 지정 API 호출 만들기]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code>https://api.frame.io</code>과(와) 관련된 경로를 입력하십시오. 예: <code> /v4/me</code></p> <p>참고: 사용 가능한 끝점 목록은 [!DNL Frame.io] API 참조를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메서드]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 인증 헤더를 자동으로 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열] </td> 
   <td> <p>요청 쿼리 문자열을 입력합니다. 쿼리 문자열에 포함할 각 매개 변수에 대해 <b>[!UICONTROL 항목 추가]</b>를 클릭하고 필드 이름과 원하는 값을 입력합니다.</p> </td> 
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

#### 업데이트된 메타데이터 값 보기

이 트리거 모듈은 댓글이 업데이트되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가 를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Adobe Workfront Fusion에 [!DNL Frame.io] 연결</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 업데이트된 메타데이터 값을 확인하려는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
