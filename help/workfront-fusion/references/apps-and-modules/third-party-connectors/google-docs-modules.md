---
title: Google Docs 모듈
description: Adobe Workfront Fusion [!DNL Google Docs] 모듈을 사용하면  [!DNL Google Docs] 및 [!DNL Google Docs] ( [!DNL Google Workspace] 사용자용)에서 문서를 모니터링, 만들기, 편집 및 검색할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: cd44250d-c2cd-46b2-8773-15b30472a8d8
source-git-commit: 2af808aaf8136253c623ee65641d0e57d4f6cf10
workflow-type: tm+mt
source-wordcount: '4045'
ht-degree: 0%

---

# [!DNL Google Docs]개 모듈

[!DNL Adobe Workfront Fusion] [!DNL Google Docs] 모듈을 사용하면 [!DNL Google Docs] 및 [!DNL Google Docs]의 문서를 모니터링, 만들기, 편집 및 검색할 수 있습니다([!DNL Google Workspace] 사용자용).

[!DNL Adobe Workfront Fusion]에 [!DNL Google Docs]을(를) 사용하려면 [!DNL Google] 계정이 있어야 합니다. 아직 [!DNL Google] 계정이 없는 경우 [!DNL Google] 계정 도움말 페이지에서 계정을 만들 수 있습니다.

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

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 전제 조건

[!DNL Google Docs] 모듈을 사용하려면 Google 계정이 있어야 합니다.

## Google Docs API 정보

Google Docs 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://docs.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.4.13</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Docs]개 모듈 및 해당 필드

[!DNL Google Docs] 모듈을 구성할 때 [!UICONTROL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Docs] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 문서

* [[!UICONTROL 문서 만들기]](#create-a-document)
* [[!UICONTROL 템플릿에서 문서 만들기]](#create-a-document-from-a-template)
* [[!UICONTROL 문서 삭제]](#delete-a-document)
* [[!UICONTROL 문서 다운로드]](#download-a-document)
* [[!UICONTROL 문서 내용 가져오기]](#get-content-of-a-document)
* [[!UICONTROL 문서에 단락 삽입]](#insert-a-paragraph-to-a-document)
* [[!UICONTROL 문서에 이미지 삽입]](#insert-an-image-to-a-document)
* [[!UICONTROL 문서 나열]](#list-documents)
* [[!UICONTROL 문서의 텍스트 바꾸기]](#replace-text-in-a-document)
* [[!UICONTROL 이미지를 새 이미지로 바꾸기]](#replace-an-image-with-a-new-image)
* [[!UICONTROL 문서 보기]](#watch-documents)

#### [!UICONTROL 문서 만들기]

이 작업 모듈에서는 선택한 폴더에 새 문서를 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이름] </td> 
   <td> <p>문서의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td> <p>문서의 내용을 입력합니다. HTML을 포함하여 문서의 서식을 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>문서를 만들 드라이브 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>새 문서의 위치 필드에서 문서를 만들 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>새 문서의 위치 필드에서 문서를 만들 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>문서를 만들 공유 드라이브를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더 삽입]</td> 
   <td> <p> 이 옵션을 활성화하여 문서에 헤더를 삽입한 다음 헤더의 텍스트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 바닥글 삽입] </td> 
   <td> <p>이 옵션을 활성화하여 문서에 바닥글을 삽입한 다음 머리글의 텍스트를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 템플릿에서 문서 만들기]

이 작업 모듈은 기존 템플릿 문서의 복사본을 만들고 태그를 대체합니다. 또한 이 모듈에서는 URL을 사용하여 이미지를 새 이미지로 바꿀 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 템플릿으로 문서 만들기]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>문서 템플릿을 매핑하려면 이 옵션을 선택하십시오.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>드롭다운 메뉴에서 문서 템플릿을 선택하려면 이 옵션을 선택하십시오.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>템플릿이 있는 드라이브 유형을 선택합니다. 이 옵션은 이전 필드에서 [!UICONTROL By Dropdown]을 선택한 경우 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p>  </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>템플릿이 있는 공유 드라이브를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p>매핑별 로 를 선택한 경우 템플릿의 ID를 매핑하거나 템플릿 및 템플릿에 대한 경로를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 값]</p> </td> 
   <td> <p>값을 입력하려는 각 태그에 대해 <b>항목 추가</b>를 클릭하고 태그를 입력한 다음 새 문서에 태그 대신 입력할 값을 입력합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL 태그]</strong> <br>문서 템플릿에 포함된 태그를 입력합니다. <code>&#123;&#123;&#125;&#125;</code>을(를) 사용하지 마십시오. 예: <code>&#123;&#123;name&#125;&#125;</code> 대신 <code>name</code> 사용.</li> 
     <li><strong>[!UICONTROL 이 값을 대체했습니다]</strong><br>태그의 값을 입력하십시오.</li> 
    </ul> <p>예를 들어 소스 문서의 <code> &#123;&#123;name&#125;&#125;</code> 변수는 <code>John</code>과 같이 값을 삽입할 수 있는 여기에서 이름 필드로 표시됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이미지 대체]</p> </td> 
   <td> <p>&gt;값을 입력하려는 각 태그에 대해 <b>항목 추가</b>를 클릭한 다음 현재 이미지를 대체할 [!UICONTROL 이미지 개체 ID] 및 [!UICONTROL 이미지 URL]에 대한 링크를 입력합니다.</p> <p>참고: ID가 배열 [!UICONTROL Inline Object Array]에 포함되어 있는 [!UICONTROL Get a Document] 모듈을 사용하여 이미지 ID를 검색할 수 있습니다.</p> <p>[!DNL Google] 문서의 이미지에 대체 텍스트를 추가하는 것이 좋습니다. </p> <p>[!DNL Google Docs] 이미지에 대체 텍스트를 추가하려면:</p> 
    <ol> 
     <li value="1">이미지를 마우스 오른쪽 단추로 클릭합니다.</li> 
     <li value="2">[!UICONTROL ALT TEXT] 옵션을 선택합니다.</li> 
     <li value="3">[!UICONTROL Title] 필드에 [!UICONTROL ALT TEXT]를 입력하고 [!UICONTROL OK]를 클릭합니다.</li> 
    </ol> <p>이미지에 대체 텍스트가 추가되면 필드 이름에 대체 텍스트가 괄호 안에 표시됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>새 문서의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>템플릿이 있는 드라이브 유형을 선택합니다. 이 옵션은 이전 필드에서 [!UICONTROL By Dropdown]을 선택한 경우 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>문서를 만들 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>문서를 만들 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>문서를 만들 공유 드라이브를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문서 삭제]

이 작업 모듈은 문서를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>삭제하려는 문서가 있는 드라이브 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>삭제할 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>삭제할 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>삭제할 문서가 있는 공유 드라이브를 선택한 다음 문서를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 공유 드라이브]</td> 
   <td> <p>다운로드할 문서가 포함된 드라이브를 선택한 다음 문서를 선택합니다. [!UICONTROL 드라이브 선택] 필드에서 [!DNL My Drive]을(를) 선택한 경우 이 옵션을 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p> 삭제할 문서를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문서 다운로드]

이 작업 모듈은 선택한 문서를 변환하고 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>다운로드할 문서가 있는 드라이브 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>문서 ID 필드에서 다운로드할 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>문서 ID 필드에서 다운로드할 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>다운로드할 문서가 있는 공유 드라이브를 선택한 다음 문서를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 유형] </p> </td> 
   <td> <p>다운로드한 문서의 대상 파일 형식을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문서 내용 가져오기]

이 작업 모듈은 지정된 문서를 검색합니다.

권한을 확장해야 할 수도 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 컨텐트 가져오기]</td> 
   <td> <p>문서의 문서 ID를 매핑할지 또는 드롭다운 메뉴에서 문서를 수동으로 선택할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>검색할 문서가 포함된 드라이브 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>검색할 문서가 포함된 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>검색할 문서가 포함된 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>검색할 문서가 포함된 공유 드라이브를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p>검색할 문서를 입력하거나 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>모듈의 출력에서 반환할 개체를 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL Image] (기본값)</li> 
     <li>[!UICONTROL 드로잉]</li> 
     <li>[!UICONTROL 차트]</li> 
    </ul> <p>참고:  <p>이러한 개체를 추가로 매핑하려면 이 모듈의 출력에 있는 [!UICONTROL InlineObjects] 값([!UICONTROL inlineObjects] 대신)을 사용하십시오.</p> <p>[!UICONTROL Inline Objects Array] 개체는 문서에 나타나는 순서와 동일한 순서로 정렬됩니다. 이를 통해 더 이상의 처리가 더 쉬워집니다.</p> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문서에 단락 삽입]

이 작업 모듈은 기존 문서에 새 단락을 추가하거나 삽입합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 문서 선택]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>문서를 매핑하려면 이 옵션을 선택하십시오.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> 드롭다운 메뉴에서 문서를 선택하려면 이 옵션을 선택하십시오.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>단락을 추가할 문서가 있는 드라이브 유형을 선택합니다. 이 옵션은 이전 필드에서 [!UICONTROL By Dropdown]을 선택한 경우 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>단락을 추가할 문서가 있는 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>단락을 추가할 문서가 있는 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>단락을 추가할 문서가 있는 공유 드라이브를 선택한 다음 문서를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p>텍스트를 삽입할 문서를 매핑하거나 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 단락 삽입]</p> </td> 
   <td> <p>문서에 새 텍스트를 삽입할 방법을 선택합니다.</p> 
    <ul> 
     <li> <p>위치 지정별 <strong></strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL By index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL 인덱스]</strong> </p> <p>텍스트를 삽입할 색인 번호를 입력합니다. [!UICONTROL Get a Document] 모듈을 사용하여 인덱스 번호를 검색할 수 있습니다.</p> </li> 
         <li> <p><strong>[!UICONTROL 삽입된 텍스트]</strong> </p> <p>문서에 삽입할 텍스트를 입력합니다.</p> </li> 
        </ul> </li> 
       <li> <p>세그먼트 ID별 <strong></strong> </p> <p>텍스트 내용을 삽입할 머리글과 바닥글을 선택하고 해당 필드에 삽입할 텍스트를 입력합니다.</p> <p>머리글이나 바닥글에 이미 텍스트가 포함되어 있으면 새 텍스트가 기존 텍스트 앞에 추가됩니다.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL 문서 본문에 추가]</strong> </p> <p>문서의 본문 내용 끝에 입력한 텍스트를 추가합니다.</p> <p>새 단락의 스타일은 목록 및 글머리 기호를 포함하여 현재 삽입 색인의 단락에서 복사됩니다.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL By appending to end of segment (Header and Footer)]</strong> </p> <p>텍스트 내용을 삽입할 머리글과 바닥글을 선택하고 해당 필드에 삽입할 텍스트를 입력합니다.</p> <p>머리글이나 바닥글에 이미 텍스트가 포함되어 있으면 기존 텍스트 뒤에 새 텍스트가 추가됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 추가된 텍스트]</td> 
   <td>문서에 추가할 텍스트를 입력하거나 매핑합니다</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문서에 이미지 삽입]

이 작업 모듈은 URL의 이미지를 문서에 삽입합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 문서 선택]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>문서 템플릿을 매핑하려면 이 옵션을 선택하십시오.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> 드롭다운 메뉴에서 문서를 선택하려면 이 옵션을 선택하십시오.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>이미지를 추가할 문서가 있는 드라이브 유형을 선택합니다. 이 옵션은 이전 필드에서 [!UICONTROL By Dropdown]을 선택한 경우 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>이미지를 추가할 문서가 있는 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>이미지를 추가할 문서가 있는 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>이미지를 추가할 문서가 있는 공유 드라이브를 선택한 다음 문서를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p>이미지를 삽입할 문서를 매핑하거나 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이미지 삽입]</p> </td> 
   <td> <p>문서에 새 이미지를 삽입할 방법을 선택합니다.</p> 
    <ul> 
     <li> <p>위치 지정별 <strong></strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL By index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL 인덱스]</strong> </p> <p>이미지를 삽입할 인덱스 번호를 입력합니다. [!UICONTROL Get a Document] 모듈을 사용하여 [!UICONTROL Index number]를 검색할 수 있습니다.</p>  </li> 
         <li> <p><strong>[!UICONTROL 이미지 URL]</strong> </p> <p>문서에 삽입할 이미지의 URL을 입력합니다.</p> <p>최대 이미지 크기는 50MB입니다. 2,500만 픽셀을 초과할 수 없습니다. PNG, JPEG 또는 GIF 형식만 지원됩니다.</p> </li> 
        </ul> </li> 
       <li> <p>세그먼트 ID별 <strong></strong> </p> <p>이미지를 삽입할 머리글과 바닥글을 선택하고 해당 필드에 이미지 URL을 입력합니다.</p> <p>최대 이미지 크기는 50MB입니다. 이미지는 2,500만 픽셀을 초과할 수 없습니다. PNG, JPEG 또는 GIF 형식만 지원됩니다.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL 문서 본문에 추가]</strong> </p> <p>문서의 본문 내용 끝에 특정 이미지를 추가합니다.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL By appending to end of segment (Header and Footer)]</strong> </p> <p>이미지를 삽입할 머리글과 바닥글을 선택하고 해당 필드에 삽입할 이미지 URL을 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Height Magnitude in Points/Width Magnitude in Points]</p> </td> 
   <td> <p>삽입된 이미지의 높이 또는 너비를 정의합니다. 종횡비는 그대로 유지됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문서 나열]

이 작업 모듈은 선택한 폴더에서 문서 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>문서를 나열할 드라이브 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>문서 목록을 표시할 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>문서 목록을 표시할 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>문서를 나열할 공유 드라이브를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>한 실행 주기에서 반환되는 [!DNL Workfront Fusion]의 최대 문서 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 문서의 텍스트 바꾸기]

이 작업 모듈은 문서의 텍스트를 대체합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 문서 선택]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>문서 템플릿을 매핑하려면 이 옵션을 선택하십시오.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> 드롭다운 메뉴에서 문서를 선택하려면 이 옵션을 선택하십시오.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>텍스트를 추가할 문서가 있는 드라이브 유형을 선택합니다. 이 옵션은 이전 필드에서 [!UICONTROL By Dropdown]을 선택한 경우 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>텍스트를 추가할 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>텍스트를 추가할 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>텍스트를 추가할 문서가 있는 공유 드라이브를 선택한 다음 문서를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p>텍스트를 바꿀 문서를 매핑하거나 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 텍스트 바꾸기]</p> </td> 
   <td> <p>바꿀 각 텍스트에 대해 <b>항목 추가</b>를 클릭하고 다음을 입력하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 바꿀 이전 텍스트]</strong> </p> <p>바꿀 텍스트를 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 삽입할 새 텍스트]</strong> </p> <p>새 텍스트를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL 이미지를 새 이미지로 바꾸기]

이 작업 모듈은 기존 이미지를 대체합니다. 원본 이미지의 종횡비가 유지됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 문서 선택]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>문서 템플릿을 매핑하려면 이 옵션을 선택하십시오.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> 드롭다운 메뉴에서 문서를 선택하려면 이 옵션을 선택하십시오.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>이미지를 바꿀 문서가 있는 드라이브 유형을 선택합니다. 이 옵션은 이전 필드에서 [!UICONTROL By Dropdown]을 선택한 경우 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>이미지를 바꿀 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>이미지를 바꿀 문서가 있는 폴더를 선택한 다음 문서를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>이미지를 바꿀 문서가 있는 공유 드라이브를 선택한 다음 문서를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p>이미지를 바꿀 문서를 매핑하거나 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 이미지 대체]</p> </td> 
   <td> 바꾸려는 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 기존 이미지 ID를 입력한 다음 기존 이미지를 바꿀 새 이미지의 URL을 입력하거나 매핑합니다. <p>이미지는 문서에 나타나는 순서대로 나열됩니다. 예를 들어 <code>Body: Image No. 1</code>은(는) 문서의 첫 번째 이미지입니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL 문서 보기]

이 트리거 모듈은 선택한 폴더에서 새 문서를 만들거나 수정할 때 문서 세부 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 감시 문서]</td> 
   <td> <p style="color: #000000;">생성된([!UICONTROL By Created Date]) 문서를 감시할지 또는 수정된([!UICONTROL By Modified Date]) 문서를 감시할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>모니터링할 드라이브 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>생성 또는 수정된 문서를 감시할 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>생성 또는 수정된 문서를 감시할 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>보려는 공유 드라이브를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Shared Drive] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한] </td> 
   <td> <p>한 실행 주기에서 Workfront Fusion이 반환하는 최대 문서 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [[!UICONTROL 문서에 있는 모든 링크를 클릭 가능하게 만들기]](#make-all-links-in-a-document-clickable)
* [[!UICONTROL API 호출 만들기]](#make-an-api-call)

#### [!UICONTROL 문서에 있는 모든 링크를 클릭 가능하게 만들기]

이 작업 모듈은 문서의 모든 링크를 찾아 클릭할 수 있도록 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 문서에 모든 링크 만들기]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>문서 템플릿을 매핑하려면 이 옵션을 선택하십시오.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> 드롭다운 메뉴에서 문서를 선택하려면 이 옵션을 선택하십시오.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>링크를 클릭할 수 있게 하려는 문서가 있는 드라이브 유형을 선택합니다. 이 옵션은 이전 필드에서 [!UICONTROL By Dropdown]을 선택한 경우 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 내 드라이브]</strong> </p> <p>링크를 클릭할 수 있게 하려는 문서가 있는 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 이 나와 공유됨]</strong> </p> <p>링크를 클릭할 수 있게 하려는 문서가 있는 폴더를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] 공유 드라이브]</strong>([!DNL Google Workspace] 사용자만 사용 가능)</p> <p>[!UICONTROL Use Domain Admin Access]를 사용할지 여부를 선택합니다. [!UICONTROL 예]를 선택하면 도메인 관리자로서 요청이 발행되고 요청자가 관리자인 모든 공유 드라이브가 반환됩니다.</p> <p>링크를 클릭할 수 있게 하려는 문서가 있는 공유 드라이브를 선택한 다음 문서를 선택합니다.</p> <p>참고: 이 필드에서 [!DNL Google Docs] 옵션을 선택했지만 사용자가 [!DNL Google Workspace]이(가) 아닌 경우 <code>[400] Invalid Value</code> 오류가 반환됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 공유 드라이브]</td> 
   <td> <p>링크를 업데이트할 문서가 들어 있는 드라이브를 선택한 다음 문서를 선택합니다. 이 옵션은 [!UICONTROL 드라이브 선택] 필드에서 [!DNL My Drive]을(를) 선택한 경우 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 문서 ID]</td> 
   <td> <p> 링크를 업데이트할 문서를 선택하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL API 호출 만들기]

이 작업 모듈을 사용하면 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p><code>https://docs.googleapis.com/</code>과(와) 관련된 경로를 입력하십시오. 예: <code>/v1/documents/{presentationID}</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 예: <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion]이(가) 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p> 요청 쿼리 문자열을 입력합니다.</p> </td> 
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

>[!BEGINSHADEBOX]

**예:** 다음 API 호출은 Google Docs에서 지정된 문서에 대한 세부 정보를 검색합니다.

**URL:**

/v1/documents/1ujkf-GDgB0TQSYPrxbCSK4Uso54tHVMqHZEVZZxB6aY

**메서드:**

[!UICONTROL GET]

![API 호출 예](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

검색된 문서에 대한 자세한 내용은 [!UICONTROL 번들] > [!UICONTROL 본문]의 모듈 출력에서 확인할 수 있습니다.

![API 호출 출력](/help/workfront-fusion/references/apps-and-modules/assets/api-output.png)

>[!ENDSHADEBOX]
