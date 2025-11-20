---
title: Frame.io 모듈
description: ' [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] 계정'
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 52dbf75ebb65a1de1a7a86619af4c7633e0cbe03
workflow-type: tm+mt
source-wordcount: '4399'
ht-degree: 87%

---

# [!DNL Frame.io] V4 모듈

>[!IMPORTANT]
>
>본 문서는 Frame.io 커넥터의 신규 버전에 대해 설명합니다. 이 커넥터는 Frame.io 버전 4에 연결하는 데 사용됩니다.
>
>Frame.io 커넥터의 이전 버전에 대한 지침은 [Frame.io 이전 커넥터](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)를 참조하십시오.

Adobe Workfront Fusion [!DNL Frame.io] 모듈을 사용하면 [!DNL Frame.io] 계정의 에셋과 댓글을 모니터링, 생성, 업데이트, 가져오기 또는 삭제할 수 있습니다.

Workfront은 연결 중인 Frame.io 버전에 따라 두 개의 Frame.io 커넥터를 제공합니다.

| 커넥터 | Frame.io 버전 |
|---|---|
| Frame.io | V4 |
| Frame.io(기존) | V3 |

Frame.io 커넥터의 이전 버전에 대한 지침은 [Frame.io 이전 커넥터](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)를 참조하십시오.


Frame.io 커넥터에 대한 비디오 소개는 다음을 참조하십시오.

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>작업 기반: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Frame.io] 모듈을 사용하려면 [!DNL Frame.io] 계정이 있어야 합니다.

## Frame.io API 정보

Frame.io 커넥터는 다음을 사용합니다.

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

## [!DNL Frame.io]를 [!UICONTROL Adobe Workfront Fusion]에 연결

사용자 자격 증명으로 자동 연결하거나, 사용자 자격 증명 연결을 수동으로 만들거나 서버 간 연결을 만들 수 있습니다.

* [사용자 자격 증명으로 자동 연결](#connect-automatically-with-user-credentials#)
* [사용자 자격 증명 연결을 수동으로 만들기](#create-a-user-credentials-connection-manually)
* [서버 간 연결 만들기](#create-a-server-to-server-connection)

### 사용자 자격 증명으로 자동 연결

이 메서드는 Frame.io에 로그인하는 경우 자동으로 연결을 만들거나 Frame.io 로그인 페이지에 연결하여 로그인할 수 있도록 합니다.

1. Frame.io 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 연결의 이름을 입력합니다.
1. **계속**&#x200B;을 클릭합니다.
1. Frame.io 계정에 로그인하라는 메시지가 표시되면 로그인합니다.
1. 둘 이상의 Frame.io 조직에 속해 있는 경우 이 연결에 사용할 조직을 선택합니다.

연결이 생성되었습니다.

### 사용자 자격 증명 연결을 수동으로 만들기

Frame.io에 로그인하거나 클라이언트 ID 또는 클라이언트 암호를 제공하여 사용자 자격 증명 연결을 만들 수 있습니다.

서버 간 연결을 만들려면 먼저 Adobe Developer Console에서 애플리케이션을 구성해야 합니다.

* [Adobe Developer Console에서 사용자 자격 증명 만들기](#create-user-credentials-in-the-adobe-developer-console)
* [사용자 인증 연결 구성](#configure-a-user-authentication-connection)

#### Adobe Developer Console에서 사용자 자격 증명 만들기

Adobe Developer Console 프로젝트에 서버 간 자격 증명이 없는 경우 사용자 자격 증명을 만들 수 있습니다.

1. [Adobe Developer Console](https://developer.adobe.com/)을 엽니다.
1. Adobe Developer Console에서 이 연결에 사용할 기존 프로젝트를 선택

   또는

   Adobe Developer Console에서 새 프로젝트를 만듭니다. 관련 지침은 [빈 프로젝트 만들기](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)를 참조하십시오.

1. 프로젝트 개요 페이지 또는 새 프로젝트 시작 페이지에서 **API 추가**&#x200B;를 클릭합니다.
1. 열린 페이지에서 **Frame.io API**&#x200B;를 찾아 클릭합니다.
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

   여기에서 클라이언트 ID와 클라이언트 암호를 확인할 수 있습니다.

>[!NOTE]
>
> Adobe Workfront Fusion에서 연결 구성을 시작할 때 이 창을 열어 두는 것이 좋습니다. 이 페이지에서 클라이언트 ID를 복사하고 클라이언트 암호를 가져오기 및 복사하여 연결 필드에 붙여넣을 수 있습니다.


#### 사용자 인증 연결 구성

1. Frame.io 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
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
            <p>이 연결의 이름을 입력합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 사용자 자격 증명 만들기</a>를 참조하십시오.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 사용자 자격 증명 만들기</a>를 참조하십시오.</p>
        </tr>
       </tbody>
    </table>
1. Frame.io 계정에 로그인하라는 메시지가 표시되면 로그인합니다.
1. 둘 이상의 Frame.io 조직에 속해 있는 경우 이 연결에 사용할 조직을 선택합니다.

연결이 생성되었습니다.


### 서버 간 연결 만들기

서버 간 연결을 만들려면 먼저 Adobe Developer Console에서 애플리케이션을 구성해야 합니다.

* [Adobe Developer Console에서 서버 간 자격 증명 만들기](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [서버 간 연결 구성](#configure-a-server-to-server-connection)

#### Adobe Developer Console에서 서버 간 자격 증명 만들기

Adobe Developer Console 프로젝트에 서버 간 자격 증명이 없는 경우 사용자 자격 증명을 만들 수 있습니다.

1. [Adobe Developer Console](https://developer.adobe.com/)을 엽니다.
1. Adobe Developer Console에서 이 연결에 사용할 기존 프로젝트를 선택

   또는

   Adobe Developer Console에서 새 프로젝트를 만듭니다. 관련 지침은 [빈 프로젝트 만들기](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)를 참조하십시오.

1. 프로젝트 개요 페이지 또는 새 프로젝트 시작 페이지에서 **API 추가**&#x200B;를 클릭합니다.
1. 열린 페이지에서 **Frame.io API**&#x200B;를 찾아 클릭합니다.
1. 인증 유형 선택 페이지에서 **서버 간 인증**&#x200B;을 선택하고 **다음**&#x200B;을 클릭합니다.
1. 자격 증명의 이름을 입력합니다. 이렇게 하면 나중에 Adobe Admin Console의 API 자격 증명 영역에서 자격 증명을 식별할 수 있습니다.
1. **다음**&#x200B;을 클릭합니다.
1. 제품 프로필 선택 페이지에서 연결할 Frame.io 계정이 포함된 제품 프로필을 선택합니다.
1. **구성된 API 저장**&#x200B;을 클릭합니다.
1. 제품 페이지에서 방금 만든 자격 증명에 대한 카드를 클릭합니다.

   여기에서 클라이언트 ID와 클라이언트 암호를 확인할 수 있습니다.

>[!NOTE]
>
> Adobe Workfront Fusion에서 연결 구성을 시작할 때 이 창을 열어 두는 것이 좋습니다. 이 페이지에서 클라이언트 ID를 복사하고 클라이언트 암호를 가져오기 및 복사하여 연결 필드에 붙여넣을 수 있습니다.


#### 서버 간 연결 구성

1. Frame.io 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

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
            <p><b>IMS 서버 간</b>을 선택합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 연결 이름]</td>
          <td>
            <p>이 연결의 이름을 입력합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 서버 간 자격 증명 만들기</a>를 참조하십시오.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력합니다. 해당 ID는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Adobe Developer Console에서 서버 간 자격 증명 만들기</a>를 참조하십시오.</p>
        </tr>
       </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.




## [!DNL Frame.io] 모듈 및 해당 필드

[!DNL Frame.io] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 수준과 같은 요인에 따라 추가적인 [!DNL Frame.io] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 토글](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [에셋](#assets)
* [댓글](#comments)
* [폴더](#folders)
* [프로젝트](#projects)
* [공유](#shares)
* [작업 영역](#workspaces)
* [메타데이터](#metadata)
* [기타](#other)

### 에셋

* [[!UICONTROL 에셋 만들기]](#create-an-asset)
* [[!UICONTROL 에셋 삭제]](#delete-an-asset)
* [[!UICONTROL 에셋 가져오기]](#get-an-asset)
* [[!UICONTROL 에셋 나열]](#list-assets)
* [삭제된 에셋 보기](#watch-asset-deleted)
* [새 에셋 보기](#watch-new-asset)

#### [!UICONTROL 에셋 만들기]<!--different for v4-->

이 작업 모듈은 새 자산을 만듭니다. 로컬 파일을 업로드하거나 원격 파일의 URL을 제공하여 자산을 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 에셋을 만들 프로젝트가 포함된 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
   <td> <p>작업 영역을 선택하거나 에셋을 만들 프로젝트가 포함된 작업 영역의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>프로젝트를 선택하거나 에셋을 만들 프로젝트 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>에셋을 만들 경로를 선택합니다.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Enter the name of the file that you want to use for this asset.</p> </td> 
  </tr> -->
    <tr> 
    <td role="rowheader">업로드 유형 </td> 
    <td> <p>로컬 파일에서 자산을 만드는지 아니면 원격 삶에서 자산을 만드는지 선택합니다.</p> </td> 
   </tr>
    <tr> 
    <td role="rowheader">파일 크기 </td> 
    <td> <p>로컬 파일을 업로드하는 경우 파일 크기를 바이트 단위로 입력하거나 매핑합니다.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 URL] </td> 
   <td> <p>원격 파일에서 자산을 만드는 경우 업로드할 파일의 URL을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름을 매핑합니다.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> -->
  </tbody> 
</table>

#### [!UICONTROL 에셋 만들기(레거시)] <!--different for v4-->

이 액션 모듈은 새 에셋을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 에셋을 만들 프로젝트가 포함된 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
   <td> <p>작업 영역을 선택하거나 에셋을 만들 프로젝트가 포함된 작업 영역의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>프로젝트를 선택하거나 에셋을 만들 프로젝트 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>에셋을 만들 경로를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 이름] </td> 
   <td> <p>이 에셋에 사용할 파일의 이름을 입력합니다.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">파일 크기 </td> 
    <td> <p>파일 크기를 바이트 단위로 입력하거나 매핑합니다.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 URL] </td> 
   <td> <p>파일을 만드는 경우 업로드할 파일의 URL을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 미디어 유형] </td> 
   <td> <p>이 에셋에 대한 미디어 유형을 선택합니다.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL 에셋 삭제]

이 액션 모듈은 지정된 에셋을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 삭제할 에셋을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 에셋 ID] </td> 
   <td> <p>삭제할 에셋을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 에셋 가져오기]

이 액션 모듈은 에셋 세부 정보를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 가져올 에셋을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 에셋 ID] </td> 
   <td> <p>가져올 에셋을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 에셋 나열]

이 검색 모듈은 지정된 프로젝트의 폴더에 있는 모든 에셋을 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 나열할 에셋을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 에셋 수] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 에셋 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 에셋 보기 삭제됨

이 트리거 모듈은 에셋이 삭제되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 웹후크 이름] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 삭제된 에셋을 확인하려는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 새 에셋 보기

이 트리거 모듈은 새 에셋이 생성될 때 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 웹후크 이름] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 새 에셋을 확인하려는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 댓글

* [[!UICONTROL 댓글 작성]](#create-a-comment)
* [[!UICONTROL 댓글 삭제]](#delete-a-comment)
* [[!UICONTROL 댓글 가져오기]](#get-a-comment)
* [[!UICONTROL 댓글 나열]](#list-comments)
* [[!UICONTROL 댓글 업데이트]](#update-a-comment)
* [업데이트된 댓글 보기](#watch-comment-updated)
* [새 댓글 보기](#watch-new-comment)

#### [!UICONTROL 댓글 작성]

이 액션 모듈은 에셋에 새 댓글 또는 답글을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 댓글을 추가할 에셋을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
   <td> <p>계정을 선택하거나 댓글을 추가할 에셋을 포함하는 작업 영역의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>프로젝트를 선택하거나 댓글을 추가할 에셋을 포함하는 프로젝트의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>댓글을 추가할 에셋의 경로를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 텍스트]</td> 
   <td> <p> 댓글이나 답글의 텍스트 내용을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 타임스탬프] </td> 
   <td> <p>댓글이 연결되어야 하는 비디오의 프레임 번호를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지] </td> 
   <td> <p>에셋이 PDF인 경우 댓글을 첨부해야 하는 페이지를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 삭제]

이 액션 모듈은 기존 댓글을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 삭제할 댓글을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 댓글 ID] </td> 
   <td> <p>삭제할 댓글의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 가져오기]

이 액션 모듈은 지정된 댓글의 세부 정보를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 세부 정보를 가져올 댓글을 포함하는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 댓글 ID] </td> 
   <td> <p>세부 정보를 가져올 댓글을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 나열]

이 검색 모듈은 지정된 에셋의 모든 댓글을 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>댓글을 가져올 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
   <td> <p>댓글을 가져올 에셋이 포함된 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>댓글을 가져올 에셋이 포함된 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 경로] </td> 
   <td> <p>댓글을 나열할 에셋으로 연결되는 경로를 선택합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 댓글 수] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 댓글 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 업데이트]

이 액션 모듈은 기존 댓글을 수정합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>댓글을 업데이트할 에셋이 포함된 프로젝트가 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 댓글 ID] </td> 
   <td> <p>업데이트할 댓글을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 텍스트]</td> 
   <td> <p> 댓글의 텍스트 내용을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 타임스탬프] </td> 
   <td> <p>댓글이 연결되어 있는 비디오의 프레임 번호를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지] </td> 
   <td> <p>에셋이 PDF인 경우 댓글이 첨부된 페이지를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 업데이트된 댓글 보기

이 트리거 모듈은 댓글이 업데이트되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 웹후크 이름] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 업데이트된 댓글을 확인하려는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 새 댓글 보기

이 트리거 모듈은 댓글이 생성되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 웹후크 이름] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>계정을 선택하거나 새 댓글을 확인하려는 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 폴더

#### 폴더 만들기

이 액션 모듈은 Frame.io에 새 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>폴더를 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
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

이 액션 모듈은 Frame.io에 새 프로젝트를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>프로젝트를 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
   <td> <p>프로젝트를 만들 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>새 프로젝트의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Frame.io 프로젝트에 사용자 초대

이 액션 모듈은 지정된 Frame.io 프로젝트에 사용자를 초대합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>사용자를 초대하려는 프로젝트가 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
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

이 검색 모듈은 지정된 팀의 모든 프로젝트를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>프로젝트를 가져올 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
   <td> <p>프로젝트를 가져올 에셋이 포함된 작업 영역을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 프로젝트 수] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할
   최대 프로젝트 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 공유

* [공유 링크에 에셋 추가](#add-an-asset-to-a-share-link)
* [공유 링크 만들기](#create-a-share-link)

#### 공유 링크에 에셋 추가

이 액션 모듈은 Frame.io의 공유 링크에 에셋을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
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
   <td role="rowheader">[!UICONTROL 에셋 ID] </td> 
   <td> <p>공유 링크에 추가할 에셋의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 공유 링크 만들기

이 액션 모듈은 Frame.io에 새 공유 링크를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>공유 링크를 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
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
   <td role="rowheader">에셋 </td> 
   <td> <p>공유 링크에 추가하려는 각 에셋에 대해 <b>항목 추가</b>를 클릭하고 에셋의 ID를 입력합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">설명 </td> 
   <td> <p>공유 링크에 대한 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>공유 링크의 만료 일자를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>새 공유 링크에 대한 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>공유 링크에 대한 암호문구를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 작업 영역

#### 작업 영역 만들기

이 액션 모듈은 Frame.io에 새 작업 영역을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>작업 영역을 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이름] </td> 
   <td> <p>작업 영역의 새 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 작업 영역 나열

이 모듈은 계정의 모든 작업 영역을 나열합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>작업 영역을 가져올 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 작업 영역 수] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할
   최대 작업 영역 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 메타데이터

* [계정 수준 필드 만들기](#create-an-account-level-field)
* [계정 수준 필드 삭제](#delete-an-account-level-field)
* [메타데이터 가져오기](#get-metadata)
* [계정 수준 필드 나열](#list-account-level-fields)
* [계정 수준 필드 정의 업데이트](#update-an-account-level-field-definition)
* [여러 파일에 걸친 메타데이터 업데이트](#update-metadata-across-multiple-files)

#### 계정 수준 필드 만들기

이 작업 모듈은 새 계정 수준 메타데이터 필드를 만들고 구성합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>메타데이터를 만들려는 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">필드 유형 </td> 
   <td> <p>만들려는 메타데이터 필드의 유형을 선택한 다음 해당 필드에 대한 옵션을 구성합니다.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>새 필드의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 계정 수준 필드 삭제

이 작업 모듈은 단일 계정 수준 메타데이터 필드를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>삭제하려는 메타데이터 필드가 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">필드 정의 ID </td> 
   <td> <p>삭제하려는 필드의 ID를 입력하거나 매핑합니다. 목록 계정 수준 필드 모듈로 필드 ID를 찾을 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 메타데이터 가져오기

이 작업 모듈은 Frame.io의 파일에 대한 메타데이터를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>메타데이터를 검색할 파일이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">파일 ID </td> 
   <td> <p>메타데이터를 검색할 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">null 표시 </td> 
   <td> <p>이 옵션을 활성화하여 출력 시 null 값이 포함된 필드를 포함할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 계정 수준 필드 나열

이 모듈은 지정된 계정에 대한 계정 수준 메타데이터 필드 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>필드를 나열할 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 계약 수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 필드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 계정 수준 필드 정의 업데이트

이 모듈은 하나의 기존 메타데이터 필드에 대한 정의를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>메타데이터를 만들려는 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">필드 정의 ID </td> 
   <td> <p>업데이트할 필드의 ID를 입력하거나 매핑합니다. 목록 계정 수준 필드 모듈로 필드 ID를 찾을 수 있습니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">필드 유형 </td> 
   <td> <p>필드의 필드 유형을 변경하려면 만들 메타데이터 필드 유형을 선택한 다음, 해당 필드에 대한 옵션을 구성합니다.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">이름 </td> 
   <td> <p>필드에 대한 새 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 여러 파일에 걸친 메타데이터 업데이트

이 모듈은 사용자가 지정한 값으로 하나 이상의 파일에 대한 메타데이터 필드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>메타데이터를 업데이트할 파일이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL 작업 영역 ID] </td> 
   <td> <p>작업 영역을 선택하거나 에셋을 만들 프로젝트가 포함된 작업 영역의 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로젝트 ID] </td> 
   <td> <p>프로젝트를 선택하거나 에셋을 만들 프로젝트 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID] </td> 
   <td> <p>메타데이터를 업데이트할 각 파일에 대해 <b>항목 추가</b>를 클릭하고 파일의 ID를 입력하거나 매핑하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 값] </td> 
   <td> <p>메타데이터를 업데이트할 각 필드에 대해 <b>항목 추가</b>를 클릭하고 필드 정의의 ID와 해당 필드에 입력할 값을 입력하거나 매핑합니다. 파일 ID 필드에 지정된 모든 파일은 이 필드 값으로 업데이트됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [사용자 정의 API 호출 만들기](#make-a-custom-api-call)
* [업데이트된 메타데이터 값 보기](#watch-metadata-value-updated)


#### [!UICONTROL 사용자 정의 API 호출 만들기]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code>https://api.frame.io</code>와 관련된 경로를 입력합니다. 예: <code> /v4/me</code></p> <p>참고: 사용 가능한 엔드포인트 목록은 [!DNL Frame.io] API 참조를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 방법]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 방법을 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 방법</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열] </td> 
   <td> <p>요청 쿼리 문자열을 입력합니다. 쿼리 문자열에 포함할 각 매개 변수에 대해 <b>[!UICONTROL 항목 추가]</b>를 클릭하고 필드 이름과 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 내용을 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 업데이트된 메타데이터 값 보기

이 트리거 모듈은 댓글이 업데이트되면 시나리오를 시작합니다.

이 모듈에 사용할 웹후크를 선택하거나 웹후크 필드 옆에 있는 추가를 클릭하고 다음 정보를 입력합니다.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 웹후크 이름] </td> 
   <td> <p>새 웹후크의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법을 안내하는 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]를 Adobe Workfront Fusion에 연결</a>을 확인하십시오.</td> 
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
