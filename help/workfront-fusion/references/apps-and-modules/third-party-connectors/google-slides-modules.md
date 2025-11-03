---
title: Google 슬라이드 모듈
description: Adobe Workfront Fusion Google 슬라이드 모듈을 사용하면 프레젠테이션을 생성, 업데이트, 나열 및/또는 삭제하고 이미지를 Google 슬라이드 계정의 프레젠테이션에 업로드할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2037'
ht-degree: 0%

---

# [!DNL Google Slides]개 모듈

Adobe Workfront Fusion [!DNL Google Slides] 모듈을 사용하면 프레젠테이션을 만들기, 업데이트, 나열 및/또는 삭제하고 이미지를 [!DNL Google Slides] 계정의 프레젠테이션에 업로드할 수 있습니다.

Workfront Fusion에서 [!DNL Google Slides]을(를) 사용하려면 [!DNL Google] 계정이 있어야 합니다. 아직 [!DNL Google] 계정이 없는 경우 [!DNL Google] 계정 도움말 페이지에서 계정을 만들 수 있습니다.

[!DNL Google Slides]에도 [!DNL Google Drive]이(가) 필요합니다.

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

[!DNL Google Slides] 모듈을 사용하려면 [!DNL Google] 계정이 있어야 합니다.

## Google 슬라이드 API 정보

Google 슬라이드 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://slides.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.5.9</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Slides]개 모듈 및 해당 필드

[!DNL Google Slides] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Slides] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [프레젠테이션](#presentation)
* [기타](#other)

### 프레젠테이션

* [[!UICONTROL 슬라이드 추가/삭제]](#adddelete-a-slide)
* [[!UICONTROL 템플릿에서 프레젠테이션 만들기]](#create-a-presentation-from-a-template)
* [[!UICONTROL 페이지/썸네일 가져오기]](#get-a-pagethumbnail)
* [[!UICONTROL 프레젠테이션 가져오기]](#get-a-presentation)
* [[!UICONTROL 프레젠테이션 나열]](#list-presentations)
* [[!UICONTROL 차트 새로 고침]](#refresh-a-chart)
* [[!UICONTROL 프레젠테이션에 이미지 업로드]](#upload-an-image-to-a-presentation)
* [[!UICONTROL 프레젠테이션 보기]](#watch-presentations)

#### [!UICONTROL 슬라이드 추가/삭제]

이 작업 모듈은 지정된 프레젠테이션에서 슬라이드를 만들거나 기존 슬라이드를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드 선택]</td> 
   <td> <p>새 슬라이드를 추가할지 또는 슬라이드를 삭제할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Enter a Slide ID]</td> 
   <td> <p>슬라이드를 삭제하는 경우 슬라이드 ID를 수동으로 입력할지 목록에서 슬라이드를 선택할지를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>프레젠테이션을 선택하거나 슬라이드를 추가하거나 삭제할 프레젠테이션의 프레젠테이션 ID를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Slide Object ID]</td> 
   <td> <p>슬라이드를 삭제하고 슬라이드를 수동으로 입력하도록 선택한 경우 슬라이드 ID를 입력하거나 매핑합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사전 정의된 레이아웃 유형]</td> 
   <td> <p> 추가된 슬라이드에서 사용할 미리 정의된 슬라이드 레이아웃을 선택합니다. 추가 필드(예: [!UICONTROL Title])에 대한 값을 지정하십시오.</p> 
    <ul> 
     <li>[!UICONTROL 자리 표시자 없는 빈 레이아웃]</li> 
     <li>맨 아래에 캡션이 있는 [!UICONTROL 레이아웃]</li> 
     <li>제목 및 부제가 있는 [!UICONTROL 레이아웃]</li> 
     <li>제목 및 본문이 있는 [!UICONTROL 레이아웃]</li> 
     <li>제목과 두 개의 열이 있는 [!UICONTROL 레이아웃]</li> 
     <li>제목만 있는 [!UICONTROL 레이아웃]</li> 
     <li>섹션 제목이 있는 [!UICONTROL 레이아웃]</li> 
     <li>한쪽에는 제목과 부제가 있고 다른 한쪽에는 설명이 있는 [!UICONTROL 레이아웃]</li> 
     <li>한 개의 제목과 한 개의 본문이 있는 [!UICONTROL 레이아웃이 단일 열로 정렬됨]</li> 
     <li>[!UICONTROL 레이아웃(주 지점 포함)]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>이 필드는 슬라이드를 추가하도록 선택한 경우 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>슬라이드의 텍스트 내용을 입력하거나 매핑합니다. 필드는 선택한 템플릿을 기반으로 사용할 수 있습니다.</p> <p>이 필드는 슬라이드를 추가하도록 선택한 경우 사용할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 템플릿에서 프레젠테이션 만들기]

이 작업 모듈은 프레젠테이션을 복사하고 의 `{{Name}}`, `{{Email}}`과(와) 같은 모든 태그를 제공된 데이터로 교체하여 새 프레젠테이션을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>새 프레젠테이션의 이름을 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 복사]</td> 
   <td> <p> 기존 프레젠테이션을 복사하는 경우 다음 옵션을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 기존 프레젠테이션 ID 사본]</td> 
   <td> <p> 복사할 기존 프레젠테이션의 경로 또는 프레젠테이션 ID를 입력합니다. [!UICONTROL By Mapping] 프레젠테이션을 만드는 경우 이 필드가 나타납니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>나열할 프레젠테이션이 있는 [!DNL Google Drive]을(를) 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
     <li>[!UICONTROL [!DNL Google] 공유 드라이브]</li> 
    </ul> <p>[!UICONTROL By Dropdown] 프레젠테이션을 만드는 경우 이 필드가 나타납니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 ID]</td> 
   <td> <p> 프레젠테이션을 선택하거나 템플릿으로 사용할 프레젠테이션의 프레젠테이션 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 값] </td> 
   <td> <p>값을 추가합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL 태그]</strong>: 프레젠테이션에서 바꿀 태그를 입력하십시오. For example, <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: 기존 태그를 대체할 값을 입력하십시오. 예를 들어 프레젠테이션의 문자열 <code>&#123;&#123;Name&#125;&#125;</code>이(가) 있고 대체된 값이 샘플이면 <code>&#123;&#123;Name&#125;&#125;</code>은(는) <code>Sample</code>(으)로 대체됩니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 새 드라이브 위치]</td> 
   <td> <p>새 프레젠테이션을 저장하거나 추가할 [!DNL Google Drive]을(를) 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
     <li>[!UICONTROL [!DNL Google] 공유 드라이브]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 새 문서의 위치]</p> </td> 
   <td> <p>프레젠테이션을 저장하거나 추가할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>프레젠테이션을 공유하려면 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 다른 사용자의 이메일 주소와 공유]</td> 
   <td> <p> 프레젠테이션을 공유할 전자 메일 주소를 입력하십시오. 이 필드에 이메일을 입력하지 않고 공유 옵션을 활성화하면 프레젠테이션을 모든 사람이 공유할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 페이지/썸네일 가져오기]

이 작업 모듈은 프레젠테이션에 있는 페이지의 축소판 또는 지정된 페이지의 최신 버전을 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 및 페이지 ID 입력]</td> 
   <td> <p> 프레젠테이션 및 페이지 ID를 수동으로 입력할지, 목록에서 선택할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 ID]</td> 
   <td> <p> 검색할 프레젠테이션 ID를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지 개체 ID]</td> 
   <td> <p> 페이지 개체 세부 사항을 보려는 슬라이드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지 썸네일 표시]</td> 
   <td> <p> 페이지 썸네일 정보를 보려면 확인란을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 프레젠테이션 가져오기]

이 작업 모듈은 지정된 프레젠테이션의 최신 버전을 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>나열할 프레젠테이션이 있는 [!DNL Google Drive]을(를) 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
     <li>[!UICONTROL [!DNL Google] 공유 드라이브]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 ID]</td> 
   <td> <p> 검색할 프레젠테이션을 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 프레젠테이션 나열]

이 모듈은 지정된 위치에 있는 모든 프레젠테이션의 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 위치 선택]</td> 
   <td> <p>나열할 프레젠테이션이 있는 [!DNL Google Drive]을(를) 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
     <li>[!UICONTROL [!DNL Google] 공유 드라이브]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더 ID]</td> 
   <td> <p>나열할 프레젠테이션의 폴더 위치를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>한 시나리오 실행 주기 동안 모듈이 반환할 최대 프레젠테이션 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 차트 새로 고침]

IS 작업 모듈은 ID로 지정된 프레젠테이션에 저장된 차트 데이터를 새로 고칩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 ID 입력]</td> 
   <td> <p> 프레젠테이션 ID를 수동으로 입력할지 목록에서 선택할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>목록에서 프레젠테이션을 선택하는 경우 나열할 프레젠테이션이 있는 [!DNL Google Drive]을(를) 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
     <li>[!UICONTROL [!DNL Google] 공유 드라이브]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 ID]</td> 
   <td> <p>프레젠테이션을 선택하거나 새로 고침할 차트가 포함된 프레젠테이션의 프레젠테이션 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 차트 개체 ID]</td> 
   <td> <p> 데이터를 수동으로 입력하는 경우 새로 고침할 차트의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 프레젠테이션에 이미지 업로드]

제공된 데이터가 있는 이미지를 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 선택]</td> 
   <td> <p>이미지를 업로드할 프레젠테이션을 선택할 방법을 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>드롭다운에서 선택할 경우 이미지를 추가할 프레젠테이션이 있는 [!DNL Google Drive]을(를) 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
     <li>[!UICONTROL [!DNL Google] 공유 드라이브]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 ID]</td> 
   <td> <p> 이미지를 업로드할 프레젠테이션의 프레젠테이션 ID를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드 선택]</td> 
   <td> <p> 이미지를 바꿀 방법을 선택합니다.</p>
   <ul>
   <li><p><b>텍스트 태그를 교체하여 이미지 업로드</b></p><p>값 필드에서 업로드할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 이미지의 태그와 새 이미지의 URL을 입력합니다.</p></li>
   <li><p><b>이미지를 교체하여 이미지 업로드</b></p><p>값 필드에서 업로드할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 이미지의 개체 ID, 바꾸기 메서드 및 새 이미지의 URL을 입력합니다.</p></li>
   </ul>
  <p>참고: 이미지 크기는 50MB 미만이어야 하고, 2,500만 픽셀을 초과할 수 없으며, PNG, JPEG 또는 GIF 형식이어야 합니다.</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 프레젠테이션 보기]

이 트리거 모듈은 새 프레젠테이션을 만들거나 업데이트할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch] </td> 
   <td> <p>프레젠테이션을 시청하려면 다음 옵션을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 만든 날짜]</p> </li> 
     <li> <p>[!UICONTROL 수정 날짜]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>한 시나리오 실행 주기 동안 Workfront Fusion이 반환해야 하는 최대 프레젠테이션 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [[!UICONTROL 프레젠테이션에 링크 삽입]](#insert-links-in-a-presentation)
* [[!UICONTROL API 호출 만들기]](#make-an-api-call)

#### [!UICONTROL 프레젠테이션에 링크 삽입]

이 모듈은 프레젠테이션의 모든 링크를 클릭 가능으로 만들거나 일치하는 모든 입력 텍스트에 링크를 삽입합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 선택]</td> 
   <td> <p>이미지를 업로드할 프레젠테이션을 선택할 방법을 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 드라이브 선택]</td> 
   <td> <p>나열할 프레젠테이션이 있는 [!DNL Google Drive]을(를) 선택하십시오.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
     <li>[!UICONTROL [!DNL Google] 공유 드라이브]</li> 
    </ul> <p>[!UICONTROL By Dropdown] 프레젠테이션을 만드는 경우 이 필드가 나타납니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프레젠테이션 ID]</td> 
   <td> <p>나열할 프레젠테이션의 폴더 위치를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select]</td> 
   <td> <p>프레젠테이션의 모든 링크를 클릭할 수 있도록 할지, 모든 일치 입력 텍스트에 링크를 삽입할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 텍스트 입력]</td> 
   <td>링크를 삽입하는 경우 링크를 추가할 각 텍스트 항목에 대해 <b>항목 추가</b>를 클릭하고 텍스트와 연결된 링크를 입력합니다. 항목이 프레젠테이션에 나타날 때마다 지정된 사이트에 자동으로 연결됩니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL API 호출 만들기]

임의의 승인된 API 호출을 수행합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Slides] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p><code>https://developers.google.com/slides/</code>과(와) 관련된 경로를 입력하십시오. 예: 프레젠테이션</p> <p>사용 가능한 끝점 목록은 <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides] API 설명서</a>를 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>원하는 요청 헤더를 입력합니다. 인증 헤더를 추가할 필요가 없습니다.</p> </td> 
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

**예:** API 호출을 사용하면 입력한 프레젠테이션 ID에 대한 프레젠테이션 세부 정보를 가져올 수 있습니다. [!DNL Google Slides]에서 프레젠테이션을 열면 URL에서 프레젠테이션 ID를 찾을 수 있습니다.

![API 호출 예](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

다음 API 호출은 프레젠테이션 세부 정보를 반환합니다.

![프레젠테이션 세부 정보](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

검색 일치 항목은 [!UICONTROL 번들] > [!UICONTROL 본문] > [!UICONTROL presentationId]의 모듈 출력에서 찾을 수 있습니다.

이 예제에서 요청된 프레젠테이션 세부 사항이 반환되었습니다.

![프레젠테이션 세부 정보](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
