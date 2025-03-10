---
title: Google 팀 드라이브 모듈
description: ' [!DNL Adobe Workfront Fusion Google Team Drive] 모듈을 사용하면  [!DNL Google Shared] 드라이브에서 파일을 모니터링, 업로드, 업데이트, 복사, 삭제 또는 검색하고 폴더를 만들 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 95dd9d23-1df9-40da-8fd0-646cc697bfc8
source-git-commit: cca7aa6e15df0fd313e9d4ca391994a8ef4c974a
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# [!DNL Google Team Drive]개 모듈

[!DNL Adobe Workfront Fusion] [!DNL Google Team Drive] 모듈을 사용하면 파일을 모니터링, 업로드, 업데이트, 복사, 삭제 또는 검색하고 [!DNL Google Shared Drive]에서 폴더를 만들 수 있습니다.

[!DNL Adobe Workfront Fusion]에 [!DNL Google Team Drive]을(를) 사용하려면 [!DNL Google Workspace] 계정이 있어야 합니다. 계정이 없으면 [[!DNL Google Workspace] 등록 사이트](https://workspace.google.com/business/signup/welcome)에서 [!DNL Google Workspace] 계정을 만들 수 있습니다.

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Google Team Drive]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

[!DNL Google Team Drive] 모듈을 사용하려면 [!DNL Google Team Drive]이(가) 있어야 합니다.

## [!DNL Google Team Drive]개 모듈 및 해당 필드

[!DNL Google Team Drive] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Team Drive] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

**bold**&#x200B;에 표시되는 모듈 대화 상자 필드([!DNL Workfront Fusion] 시나리오에서 이 문서 문서의 **not**)는 필수입니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 트리거

#### [!UICONTROL Watch Files]

지정된 폴더에서 새 파일이 추가 및/또는 수정되면 파일 세부 정보를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 보려는 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>공유 드라이브 내의 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p> 보려는 파일 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] 형식을 지정할 파일] </td> 
   <td> <p>감시된 [!DNL Google Documents] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Sheets] 형식을 지정할 파일] </td> 
   <td> <p>감시된 [!DNL Google Sheets] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] 형식을 지정할 파일] </td> 
   <td> <p>감시된 [!DNL Google Slides] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] 형식을 지정할 파일] </td> 
   <td> <p>감시된 [!DNL Google Drawings] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p> 새 파일과 수정된 파일에 대해 폴더를 모니터링할지 또는 새 파일에만 대해 모니터링할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td> <p> 한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 파일 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL Upload a File]](#upload-a-file)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File]](#delete-a-file)
* [[!UICONTROL Move a File to Trash]](#move-a-file-to-trash)
* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Get a File List]](#get-a-file-list)
* [[!UICONTROL Create a Folder]](#create-a-folder)

#### [!UICONTROL Upload a File]

지정된 공유 드라이브에 파일을 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive] </td> 
   <td> <p>파일을 업로드할 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>공유 드라이브 내의 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>공유 드라이브에 업로드할 파일을 지정합니다.</p> <p>이전 모듈에서 업로드할 파일을 매핑하거나(예: [!UICONTROL HTTP] &gt; [!UICONTROL Get a File] 또는 [!UICONTROL Dropbox] &gt;[!UICONTROL Get a file)]) 파일 이름과 파일 데이터를 수동으로 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td> <p> 공유 폴더에 표시될 파일의 제목을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a File]</td> 
   <td> <p> 파일을 공유 폴더의 해당 Google 형식으로 변환하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

파일 이름 및/또는 파일 내용을 변경할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 업데이트할 파일이 포함된 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>공유 드라이브 내의 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> 업데이트할 파일의 ID를 입력합니다(매핑).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>업데이트된 파일의 새 제목을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a File]</td> 
   <td> <p> 파일을 공유 폴더의 해당 [!DNL Google] 형식으로 변환하려면 이 옵션을 활성화하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

지정한 파일을 선택한 폴더에 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 복사할 파일이 포함된 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>파일을 복사할 대상 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> 복사할 파일의 ID를 입력합니다(매핑).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL The name of the copy file]</p> </td> 
   <td> <p>대상 위치에서 새 파일 이름을 변경하려면 해당 파일 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

지정된 파일을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> 삭제할 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File to Trash]

지정된 파일을 휴지통으로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> 휴지통으로 이동할 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File]

지정된 파일에 대한 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] 형식을 지정할 파일] </td> 
   <td> <p>[!DNL Google Documents] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Sheets] 형식을 지정할 파일] </td> 
   <td> <p>[!DNL Google Sheets] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] 형식을 지정할 파일] </td> 
   <td> <p>[!DNL Google Slides] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] 형식을 지정할 파일] </td> 
   <td> <p>[!DNL Google Drawings] 파일을 변환할 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> 검색할 파일의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File List]

검색어를 기반으로 파일 및/또는 폴더 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 파일을 나열할 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
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
     <li style="font-weight: bold;"> <p>[!UICONTROL Search within file names]</p> <p style="font-weight: normal;">[!UICONTROL Search for exact term Search] 옵션을 선택한 경우 파일 이름(파일 확장명 포함)을 입력하거나 [!UICONTROL Search for names containing the searched term] 옵션을 선택한 경우 이름의 일부를 입력하십시오.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Fulltext search]</p> <p>파일 이름, 설명 및 내용을 검색할 검색어를 입력합니다.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Custom search query]</p> <p>[!DNL Google] 검색 쿼리 용어를 입력하십시오. 자세한 내용은 [!DNL Google]의 <a href="https://developers.google.com/drive/api/v2/ref-search-terms">검색 쿼리 설명서</a>를 참조하세요. 예: <code>fullText contains '"Hello world"'</code></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td>파일을 검색할지, 폴더를 검색할지 또는 둘 다 검색할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p> 한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 파일 또는 폴더 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

새 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Team Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> 폴더를 만들 공유 드라이브를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>폴더를 만들 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the new folder]</td> 
   <td> <p> 새 폴더의 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
