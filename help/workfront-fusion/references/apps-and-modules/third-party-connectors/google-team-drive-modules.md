---
title: Google 팀 드라이브 모듈
description: ' [!DNL Adobe Workfront Fusion Google Team Drive] 모듈을 사용하면  [!DNL Google Shared] 드라이브에서 파일을 모니터링, 업로드, 업데이트, 복사, 삭제 또는 검색하고 폴더를 만들 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 95dd9d23-1df9-40da-8fd0-646cc697bfc8
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1370'
ht-degree: 0%

---

# [!DNL Google Team Drive]개 모듈

Adobe Workfront Fusion [!DNL Google Team Drive] 모듈을 사용하면 파일을 모니터링, 업로드, 업데이트, 복사, 삭제 또는 검색하고 [!DNL Google Shared Drive]에서 폴더를 만들 수 있습니다.

Adobe Workfront Fusion에서 [!DNL Google Team Drive]을(를) 사용하려면 [!DNL Google Workspace] 계정이 있어야 합니다. 계정이 없으면 [!DNL Google Workspace]등록 사이트[[!DNL Google Workspace] 에서 &#x200B;](https://workspace.google.com/business/signup/welcome) 계정을 만들 수 있습니다.

Adobe Workfront Fusion 시나리오에서는 [!DNL Google Team Drive]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

[!DNL Google Team Drive] 모듈을 사용하려면 [!DNL Google Team Drive]이(가) 있어야 합니다.

## [!DNL Google Team Drive]개 모듈 및 해당 필드

[!DNL Google Team Drive] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Team Drive] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

**bold**(Workfront Fusion 시나리오에서 이 문서 문서의 **not**)에 표시되는 모듈 대화 상자 필드는 필수입니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 트리거

#### [!UICONTROL 파일 보기]

지정된 폴더에서 새 파일이 추가 및/또는 수정되면 파일 세부 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 보려는 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>공유 드라이브 내의 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 조사할 파일]</td> 
   <td> <p> 보려는 파일 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Documents]개 파일을 형식으로 변환] </td> 
   <td> <p>감시된 [!DNL Google Documents] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Sheets]개 파일을 형식으로 변환] </td> 
   <td> <p>감시된 [!DNL Google Sheets] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Slides]개 파일을 형식으로 변환] </td> 
   <td> <p>감시된 [!DNL Google Slides] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Drawings]개 파일을 형식으로 변환] </td> 
   <td> <p>감시된 [!DNL Google Drawings] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p> 새 파일과 수정된 파일에 대해 폴더를 모니터링할지 또는 새 파일에만 대해 모니터링할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 다운로드한 최대 파일 수]</td> 
   <td> <p> 한 실행 주기 동안 Workfront Fusion이 반환할 최대 파일 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 파일 업로드]](#upload-a-file)
* [[!UICONTROL 파일 업데이트]](#update-a-file)
* [[!UICONTROL 파일 복사]](#copy-a-file)
* [[!UICONTROL 파일 삭제]](#delete-a-file)
* [[!UICONTROL 휴지통으로 파일 이동]](#move-a-file-to-trash)
* [[!UICONTROL 파일 가져오기]](#get-a-file)
* [[!UICONTROL 파일 목록 가져오기]](#get-a-file-list)
* [[!UICONTROL 폴더 만들기]](#create-a-folder)

#### [!UICONTROL 파일 업로드]

지정된 공유 드라이브에 파일을 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive] </td> 
   <td> <p>파일을 업로드할 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>공유 드라이브 내의 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source 파일]</p> </td> 
   <td> <p>공유 드라이브에 업로드할 파일을 지정합니다.</p> <p>이전 모듈에서 업로드할 파일을 매핑합니다(예: [!UICONTROL HTTP] &gt; [!UICONTROL 파일 가져오기] 또는 [!UICONTROL Dropbox] &gt;[!UICONTROL 파일 가져오기)]를 선택하거나 파일 이름과 파일 데이터를 수동으로 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td> <p> 공유 폴더에 표시될 파일의 제목을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 변환]</td> 
   <td> <p> 파일을 공유 폴더의 해당 Google 형식으로 변환하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업데이트]

파일 이름 및/또는 파일 내용을 변경할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 업데이트할 파일이 포함된 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>공유 드라이브 내의 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td> <p> 업데이트할 파일의 ID를 입력합니다(매핑).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source 파일]</p> </td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>업데이트된 파일의 새 제목을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 변환]</td> 
   <td> <p> 파일을 공유 폴더의 해당 [!DNL Google] 형식으로 변환하려면 이 옵션을 활성화하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 복사]

지정한 파일을 선택한 폴더에 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 복사할 파일이 포함된 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>파일을 복사할 대상 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td> <p> 복사할 파일의 ID를 입력합니다(매핑).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 복사 파일의 이름]</p> </td> 
   <td> <p>대상 위치에서 새 파일 이름을 변경하려면 해당 파일 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 삭제]

지정된 파일을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td> <p> 삭제할 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 휴지통으로 파일 이동]

지정된 파일을 휴지통으로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td> <p> 휴지통으로 이동할 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 가져오기]

지정된 파일에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Documents]개 파일을 형식으로 변환] </td> 
   <td> <p>[!DNL Google Documents] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Sheets]개 파일을 형식으로 변환] </td> 
   <td> <p>[!DNL Google Sheets] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Slides]개 파일을 형식으로 변환] </td> 
   <td> <p>[!DNL Google Slides] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Drawings]개 파일을 형식으로 변환] </td> 
   <td> <p>[!DNL Google Drawings] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td> <p> 검색할 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 목록 가져오기]

검색어를 기반으로 파일 및/또는 폴더 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 파일을 나열할 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>파일을 나열할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>수행할 검색 유형을 선택합니다. 아래를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Query]</p> </td> 
   <td> 
    <ul> 
     <li style="font-weight: bold;"> <p>[!UICONTROL 파일 이름 내 검색]</p> <p style="font-weight: normal;">[!UICONTROL Search for exact term Search] 옵션을 선택한 경우 파일 이름(파일 확장자 포함)을 입력하거나 [!UICONTROL Search for names contains the search for the search term] 옵션을 선택한 경우 이름의 일부를 입력합니다.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL 전체 텍스트 검색]</p> <p>파일 이름, 설명 및 내용을 검색할 검색어를 입력합니다.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL 사용자 지정 검색 쿼리]</p> <p>[!DNL Google] 검색 쿼리 용어를 입력하십시오. 자세한 내용은 [!DNL Google]의 <a href="https://developers.google.com/drive/api/v2/ref-search-terms">검색 쿼리 설명서</a>를 참조하세요. 예: <code>fullText contains '"Hello world"'</code></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 검색]</td> 
   <td>파일을 검색할지, 폴더를 검색할지 또는 둘 다 검색할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 결과 수]</td> 
   <td> <p> 한 실행 주기 동안 Workfront Fusion이 반환할 최대 파일 또는 폴더 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더 만들기]

새 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 폴더를 만들 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>폴더를 만들 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 새 폴더의 이름]</td> 
   <td> <p> 새 폴더의 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
