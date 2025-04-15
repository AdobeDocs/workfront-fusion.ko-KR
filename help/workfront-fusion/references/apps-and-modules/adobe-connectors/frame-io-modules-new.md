---
title: Frame.io 모듈
description: ' [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] 계정입니다.'
author: Becky
feature: Workfront Fusion
source-git-commit: c0b08b206f69d6af3b629c5d31cc0b840edea766
workflow-type: tm+mt
source-wordcount: '2167'
ht-degree: 1%

---

# [!DNL Frame.io]개의 Beta(V4) 모듈

>[!IMPORTANT]
>
>이 문서에서는 Frame.io 커넥터의 새(베타) 버전에 대해 설명합니다. 이 커넥터는 Frame.io 버전 4에 연결하는 데 사용됩니다.
>
>Frame.io 커넥터의 레거시 버전에 대한 지침은 [Frame.io 레거시 커넥터](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)를 참조하십시오.

[!DNL Adobe Workfront Fusion] [!DNL Frame.io] 모듈을 사용하면 [!DNL Frame.io] 계정의 자산 및 주석을 모니터링, 만들기, 업데이트, 검색 또는 삭제할 수 있습니다.

Workfront은 연결 중인 Frame.io 버전에 따라 두 개의 Frame.io 커넥터를 제공합니다.

| 커넥터 | Frame.io 버전 |
|---|---|
| Frame.io (Beta) | V4 |
| Frame.io(기존) | V3 |

Frame.io 커넥터의 레거시 버전에 대한 지침은 [Frame.io 레거시 커넥터](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)를 참조하십시오.


Frame.io 커넥터에 대한 비디오 소개는 다음을 참조하십시오.

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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
   <p>Current: Workfront Fusion 라이센스 요구 사항 없음</p>
   <p>또는</p>
   <p>레거시: 업무 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>새로운:</p> <ul><li>Workfront 패키지 선택 또는 프라임 구성: 조직에서 반드시 Adobe Systems Workfront Fusion을 구입해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

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

연결 프로세스는 기존 Frame.io 커넥터 또는 Beta Frame.io 커넥터를 사용하는지에 따라 다릅니다.

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
            <p>IMD 사용자 인증 연결을 만들지 IMS 서버 대 서버 연결을 만들지 선택합니다.</p>
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
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 ID]를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
          <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.<p>자격 증명을 찾는 방법에 대한 지침은 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >자격 증명</a>을 참조하십시오.</p>
        </tr>
       </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## [!DNL Frame.io]개 모듈 및 해당 필드

[!DNL Frame.io] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Frame.io] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

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
* [[!UICONTROL 자산 업데이트]](#update-an-asset)

#### [!UICONTROL 자산 만들기] <!--different for v4-->

이 작업 모듈은 새 자산을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>에 대한 연결을 [!DNL Frame.io]만드는 방법에 대한 지침은 이 문서의 연결 [!DNL Frame.io] 대상 [!DNL Adobe Workfront Fusion]</a> 을 참조하세요<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL 계정 ID] </td> 
   <td> <p>계정 선택하거나 자산 만들려는 프로젝트가 포함된 계정의 ID를 매핑합니다.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[! UICONTROL 작업 영역 ID] </td> 
   <td> <p>작업 영역 선택하거나 자산 만들려는 프로젝트가 포함된 작업 영역의 ID를 매핑합니다.</p> </td> 
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

이 작업 모듈은 지정된 자산을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[! UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
    <td role="rowheader">[! UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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

### 댓글

* [[!UICONTROL 댓글 만들기]](#create-a-comment)
* [[!UICONTROL 댓글 삭제]](#delete-a-comment)
* [[!UICONTROL 댓글 가져오기]](#get-a-comment)
* [[!UICONTROL 댓글 나열]](#list-comments)
* [[!UICONTROL 댓글 업데이트]](#update-a-comment)

#### [!UICONTROL 댓글 만들기]

이 작업 모듈은 자산에 새 주석 또는 답글을 추가합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[! UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
   <td role="rowheader">[! UICONTROL 타임스탬프] </td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL 계정 ID] </td> 
   <td> <p>계정 선택하거나 세부 정보를 검색할 주석이 포함된 계정의 ID를 매핑합니다.</p> </td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>댓글을 검색할 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL 작업 영역 ID] </td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
   <td role="rowheader">[! UICONTROL 텍스트]</td> 
   <td> <p> 주석의 텍스트 콘텐츠를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 타임스탬프] </td> 
   <td> <p>댓글이 연결된 비디오의 프레임 번호를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL 페이지] </td> 
   <td> <p>자산이 PDF인 경우 주석이 첨부된 페이지를 입력하거나 매핑합니다.</p> </td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
* [프로젝트 나열](#list-projects)

#### 프로젝트 만들기

이 작업 모듈은 Frame.io에서 새 프로젝트를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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

#### [!UICONTROL 프로젝트 나열]

이 검색 모듈은 지정된 팀에 대한 모든 프로젝트를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[! UICONTROL 연결] </td> 
   <td>에 대한 연결을 [!DNL Frame.io]만드는 방법에 대한 지침은 이 문서의 연결 [!DNL Frame.io] 대상 [!DNL Adobe Workfront Fusion]</a> 을 참조하세요<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">.</td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>공유 링크를 만들 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[! UICONTROL 작업 영역 ID] </td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 계정 ID] </td> 
   <td> <p>작업 영역을 검색할 에셋이 포함된 계정을 선택하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 작업 영역 수] </td> 
   <td> <p>최대 작업 공간 수 입력 또는 매핑
   각 시나리오 실행 주기 동안 모듈 반환을 원합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

#### [!UICONTROL 사용자 지정 API 호출 만들기]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[! UICONTROL 연결] </td> 
   <td>[!DNL Frame.io]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">[!DNL Frame.io]을(를) [!DNL Adobe Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
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
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 인증 헤더를 자동으로 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열] </td> 
   <td> <p>요청 쿼리 문자열을 입력합니다. 쿼리 문자열에 포함할 각 매개 변수에 대해 <b>[!UICONTROL 항목 추가]</b>를 클릭하고 필드 이름과 원하는 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>API 호출에 대한 본문 컨텐츠 내용을 표준 JSON 개체 양식으로 추가합니다.</p> <p>메모:  <p>JSON에서와 같이 <code>if</code> 조건문을 사용할 때는 조건문 밖에 따옴표를 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
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
