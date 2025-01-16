---
title: Google 드라이브 모듈
description: ' [!DNL Adobe Workfront Fusion Google Drive] 모듈을 사용하면  [!DNL Google Drive]에서 파일, 폴더 또는 공유 드라이브를 모니터링, 검색, 만들기, 업데이트, 삭제 및 관리할 수 있습니다.'
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2489'
ht-degree: 1%

---

# [!DNL Google Drive]개 모듈

[!DNL Adobe Workfront Fusion] [!DNL Google Drive] 모듈을 사용하면 [!DNL Google Drive]에서 파일, 폴더 또는 공유 드라이브를 모니터링, 검색, 만들기, 업데이트, 삭제 및 관리할 수 있습니다.

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Google Drive] 계정을 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

## Google 드라이브 API 정보

Google 드라이브 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://www.googleapis.com/drive/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v4.1.22</td> 
  </tr>
 </tbody> 
 </table>



## [!DNL Workfront Fusion]에 [!DNL Google Drive] 연결 중

[!DNL @gmail.com] 또는 [!DNL @googlemail.com] 사용자인 경우 [!UICONTROL Client ID] 및 [!UICONTROL Client Secret]을(를) 가져오려면 [the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project)에 OAuth 클라이언트를 만들어야 합니다.

OAuth 클라이언트를 만들고 [!UICONTROL Client ID] 및 [!UICONTROL Client Secret]을(를) 얻는 방법에 대한 단계별 지침은 [연결 [!DNL Adobe Workfront Fusion] to [!DNL Google Services] 사용자 지정 OAuth 클라이언트 사용](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)을 참조하십시오.

[!DNL Google Drive] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하세요.

## [!DNL Google Drive]개 모듈 및 해당 필드

[!DNL Google Drive] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Drive] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [트리거](#triggers)
* [액션](#actions)

### 트리거

* [[!UICONTROL Watch Files In Folder]](#watch-files-in-folder)
* [[!UICONTROL Watch All Files]](#watch-all-files)
* [[!UICONTROL Watch shared files]](#watch-shared-files)
* [[!UICONTROL Watch Comments]](#watch-comments)

#### [!UICONTROL Watch Files In Folder]

지정된 폴더에서 파일을 추가하거나 수정할 때 파일 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Select the folder to be watched]</td>
    <td >드라이브에서 파일을 감시할 폴더를 선택합니다.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL What files to watch]</td>
   <td> <p>보려는 파일 유형을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] 형식을 지정할 파일]</td>
    <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 형식을 지정할 파일]</td>
    <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] 형식을 지정할 파일]</td>
    <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] 형식을 지정할 파일]</td>
    <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Watch]</td>
    <td>새 파일과 모든 변경 내용을 보는지 아니면 새 파일만 보는지 선택합니다.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Maximum number of downloaded files]</td>
    <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 다운로드할 최대 결과 수(시나리오 실행당 반복 횟수)를 설정합니다.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch All Files]

[!DNL Google Drive]의 파일을 추가하거나 수정할 때 파일 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>보려는 파일 유형을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] 형식을 지정할 파일]</td>
    <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 형식을 지정할 파일]</td>
    <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] 형식을 지정할 파일]</td>
    <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] 형식을 지정할 파일]</td>
    <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>새 파일과 모든 변경 내용을 보는지 아니면 새 파일만 보는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 다운로드할 최대 결과 수(시나리오 실행당 반복 횟수)를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch shared files]

새 파일이 공유되거나 기존 공유 파일이 업데이트될 때 트리거됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select the folder to be watched]</td> 
   <td>파일을 보려는 공유 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>보려는 파일 유형을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] 형식을 지정할 파일]</td>
    <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 형식을 지정할 파일]</td>
    <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] 형식을 지정할 파일]</td>
    <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] 형식을 지정할 파일]</td>
    <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>새 파일과 모든 변경 내용을 보는지 아니면 새 파일만 보는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 다운로드할 최대 결과 수(시나리오 실행당 반복 횟수)를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comments]

선택한 파일에서 댓글을 추가하거나 수정할 때 트리거됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File]</td> 
   <td>댓글을 확인할 파일을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>모든 변경 사항에 대해 감시할지 또는 새 주석에 대해서만 감시할지 선택</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned comments]</td> 
   <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 반환할 최대 댓글 수(시나리오 실행당 반복 횟수)를 설정하십시오.</td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL Upload a File]](#upload-a-file)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File]](#delete-a-file)
* [[!UICONTROL Move a File/Folder to Trash]](#move-a-filefolder-to-trash)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Search for Files/Folders]](#search-for-filesfolders)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Get a share link]](#get-a-share-link)

#### [!UICONTROL Upload a File]

파일을 [!DNL Google Drive]에 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Destination]</td> 
   <td> <p>파일을 업로드할 대상을 선택합니다.</p> 
    <ul> 
     <li>[!DNL My Drive]</li> 
     <li>[!DNL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>파일을 업로드할 폴더를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>이전 모듈에서 전달된 파일을 사용할지 또는 파일을 수동으로 매핑할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>파일 이름을 선택합니다. 이 옵션은 [!UICONTROL source file] 필드에서 "[!UICONTROL Map]"을(를) 선택하는 경우 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>업로드할 데이터 파일을 선택합니다. 이 옵션은 [!UICONTROL source file] 필드에서 "[!UICONTROL Map]"을(를) 선택하는 경우 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>새 파일의 제목을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a file]</td> 
   <td>이 옵션을 활성화하면 모듈이 파일을 해당 [!DNL Google] 형식으로 변환할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

파일의 메타데이터 또는 컨텐츠를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>파일을 업로드할 대상을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Move to a folder]</td> 
   <td>파일을 다른 폴더로 이동하려면 파일을 이동할 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>업데이트할 파일의 ID를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>업데이트된 파일의 제목을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Change a file content]</td> 
   <td>파일 내용을 바꿀 것인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>이전 모듈에서 전달된 파일을 사용할지 또는 파일을 수동으로 매핑할지 여부를 선택합니다. 이전 필드에서 파일의 내용을 변경하도록 선택한 경우 이 필드를 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>파일 이름을 선택합니다. 이 옵션은 [!UICONTROL source file] 필드에서 "[!UICONTROL Map]"을(를) 선택하는 경우 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>업로드할 데이터 파일을 선택합니다. 이 옵션은 [!UICONTROL source file] 필드에서 "[!UICONTROL Map]"을(를) 선택하는 경우 사용할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

파일을 새 위치에 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>파일을 업로드할 대상을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>복사할 파일이 있는 폴더 선택/</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>업데이트할 파일의 ID를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the copy]</td> 
   <td>새 파일의 제목을 입력합니다. 원래 파일 이름을 변경하지 않으려면 이 필드를 비워 둡니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

파일 또는 폴더를 영구적으로 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>삭제할 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder to Trash]

파일 또는 폴더를 휴지통으로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>휴지통으로 이동할 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

지정된 ID로 파일을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] 형식을 지정할 파일]</td> 
   <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 형식을 지정할 파일]</td> 
   <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] 형식을 지정할 파일]</td> 
   <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] 형식을 지정할 파일]</td> 
   <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>검색할 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Files/Folders]

검색 조건에 따라 파일 또는 폴더를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>검색할 대상을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL List a folder]</td> 
   <td>파일 또는 폴더를 검색할 폴더로 이동합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td> <p> 파일, 폴더 또는 둘 다 검색할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Search]</p> </td> 
   <td> <p>수행할 검색 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search within file/folder names]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>검색할 파일 이름 또는 전체 파일 이름(접미사 포함)의 일부를 입력합니다.</p> </li> 
       <li> <p><strong>[!UICONTROL Search Options]</strong> </p> <p>정확한 용어를 검색할지 또는 검색어가 포함된 이름을 검색할지 여부를 선택합니다.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Fulltext] 검색</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>[!DNL Google Drive]에서 검색할 검색어를 입력하십시오.</p> </li> 
      </ul> </li> 
     <li> <p><strong>사용자 지정 검색 쿼리 입력</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>사용자 지정 검색 쿼리를 입력합니다. 자세한 내용은 이 문서의 [!UICONTROL Search for Files] 섹션을 참조하십시오.</p> </li> 
       <li> <p><strong>위에서 선택한 폴더를 쿼리에 추가</strong> </p> <p>상위 컬렉션에서 폴더를 검색합니다. 이렇게 하면 위에서 선택한 폴더에 직접 있는 모든 파일과 폴더를 찾습니다.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 파일 또는 폴더 수를 설정하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td>모듈이 결과를 반환하지 않는 경우 시나리오가 중지되지 않도록 하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

지정한 위치에 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>파일을 업로드할 대상을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New folder location]</td> 
   <td>새 폴더를 만들 위치로 이동합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the new folder]</td> 
   <td>생성 중인 폴더의 이름을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Share folder]</td> 
   <td>[!UICONTROL Share] 링크를 가진 모든 사람과 폴더를 공유하려면 이 옵션을 선택하십시오. 그렇지 않으면 소유자만 공유 링크를 사용할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a share link]

Google 드라이브의 파일에 대한 공유 링크를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!DNL Google Drive]을(를) [!UICONTROL Workfront Fusion]</a>에 연결하는 방법을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>공유 링크를 가져올 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

## 문제 해결

### 파일을 업로드하거나 업데이트할 수 없음

파일 업로드 또는 업데이트가 실패할 경우 다음과 같은 몇 가지 상황이 발생합니다.

* 업로드한 파일이 너무 커서 [!DNL Google Drive] 계획에 허용된 최대 파일 크기 제한을 초과하거나 [!DNL Google Drive] 저장소 제한을 초과했습니다. 저장소 계획을 업그레이드하거나 [!DNL Google Drive] 서비스에서 기존 파일을 삭제할 수 있습니다.
* 파일을 업로드할 선택한 폴더가 더 이상 존재하지 않습니다. 시나리오가 중지되고 대상 폴더를 다시 선택해야 합니다.

## 파일 검색

폴더의 목록 파일 모듈에서 다음 부분으로 구성된 자체 쿼리를 사용할 수 있습니다.

* **[!UICONTROL Field]** - 검색 중인 파일의 특성(예: 파일의 특성 `name`).

* **[!UICONTROL Operator]** - 일치 항목(예: `contains`)을 제공하기 위해 데이터에 대해 수행되는 테스트입니다.

* **[!UICONTROL Value]** - 테스트된 특성의 콘텐츠(예: `My cool document` 파일의 이름).

절을 연결 `and` 또는 `or`과(와) 결합하고 쿼리를 `not`(으)로 무효화합니다.

* [필드](#fields)
* [값 유형](#value-types)
* [연산자](#operators)
* [예시](#examples)

### 필드

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>필드 </th> 
   <th>값 유형 </th> 
   <th>연산자</th> 
   <th> <p> 설명</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>문자열</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> 파일 이름.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>문자열 </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> 이름, 설명, 콘텐츠 및 색인화 가능한 텍스트가 포함된 파일의 전체 텍스트입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> 문자열</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> 파일의 MIME 유형입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> 날짜<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> 마지막으로 파일을 수정한 날짜입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> 날짜<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> 사용자가 마지막으로 파일을 본 날짜입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>부울 </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> 파일이 휴지통에 있는지 여부.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>부울 </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>파일이 표시되는지 여부입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>컬렉션 </td> 
   <td><code>in </code> </td> 
   <td> <p>[!UICONTROL parents] 컬렉션에 지정된 ID가 포함되어 있는지 여부입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>컬렉션 </td> 
   <td><code>in </code> </td> 
   <td> <p>파일을 소유하는 사용자입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>컬렉션 </td> 
   <td><code>in </code> </td> 
   <td> <p>파일을 수정할 수 있는 권한이 있는 사용자.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>컬렉션 </td> 
   <td><code>in </code> </td> 
   <td> <p>파일을 읽을 수 있는 권한이 있는 사용자.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>부울 </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> 사용자의 "나와 공유" 컬렉션에 있는 파일입니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>컬렉션</td> 
   <td><code>has </code> </td> 
   <td> <p> 공용 사용자 지정 파일 속성입니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

이러한 필드의 연산자에 대해 다음 사항을 고려하십시오.

* `contains` 연산자는 `title`에 대해서만 접두사 일치를 수행합니다.

  예를 들어 &quot;HelloWorld&quot; 제목은 `title contains 'Hello'`에 대해 일치하지만 `title contains 'World'`에는 일치하지 않습니다.

* `contains` 연산자는 `fullText`에 대한 전체 문자열 토큰에 대해서만 일치를 수행합니다.

  예를 들어, 문서의 전체 텍스트에 문자열 &quot;HelloWorld&quot;가 포함되어 있으면 `fullText contains 'HelloWorld'` 쿼리만 결과를 반환합니다. `fullText contains 'Hello'`과(와) 같은 쿼리는 이 시나리오에서 결과를 반환하지 않습니다.

* `contains` 연산자는 큰따옴표로 묶인 경우 정확한 영숫자 구문에서 일치합니다.

  예를 들어, 문서의 `fullText`에 문자열 &quot;Hello there world&quot;가 포함되어 있으면 `fullText contains '"Hello there"'` 쿼리는 결과를 반환하지만 `fullText contains '"Hello world"'` 쿼리는 결과를 반환하지 않습니다.

  또한 검색은 영숫자이므로 문서의 `fullText`에 문자열 &quot;Hello_world&quot;가 포함되어 있으면 `fullText contains '"Hello world"'` 쿼리가 결과를 반환합니다.

* `type` 날짜 필드는 현재 서로 비교할 수 없으며 상수 날짜에만 해당됩니다.

### 값 유형

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>값 유형</th> 
   <th> <p> 메모</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>문자열 </td> 
   <td> <p>작은 따옴표 '(으)로 묶습니다. 쿼리에서 <code>\'</code>(예: <code> 'Valentine\'s Day'</code>)을(를) 사용하여 작은 따옴표를 이스케이프 처리합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>부울 </td> 
   <td> <p><code>true </code>또는 <code>false</code>입니다.</p> </td> 
  </tr> 
  <tr> 
   <td>일자 </td> 
   <td> <p>RFC 3339 형식입니다. 기본 시간대는 UTC입니다(예: <code>2012-06-04T12:00:00-08:00</code>).</p> </td> 
  </tr> 
 </tbody> 
</table>

### 연산자

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>연산자 </th> 
   <th> <p>메모</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>한 문자열의 콘텐츠가 다른 문자열에 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> 문자열 또는 부울의 콘텐츠는 다른 것과 같습니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> 문자열 또는 부울의 콘텐츠가 다른 것과 같지 않습니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> 날짜가 다른 날짜보다 빠릅니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> 날짜가 다른 날짜보다 빠르거나 같습니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> 날짜가 다른 날짜보다 늦습니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> 날짜가 다른 날짜보다 이후이거나 같습니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>요소는 컬렉션 내에 포함됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>두 절과 일치하는 파일을 반환합니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>두 절 중 하나와 일치하는 파일을 반환합니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>검색 절을 부정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>컬렉션에 매개 변수와 일치하는 요소가 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

복합 절의 경우 괄호를 사용하여 절을 함께 그룹화할 수 있습니다. 예:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` 이 검색은 2012년 6월 4일 이후에 마지막으로 수정한 이미지 또는 비디오 MIME 형식의 모든 파일을 반환합니다. `and` 및 `or` 연산자는 괄호를 사용하지 않고 왼쪽에서 오른쪽으로 평가되므로 위의 예에서는 2012년 6월 4일 이후에 수정된 이미지만 반환하지만 2012년 6월 4일 이전의 모든 비디오를 반환합니다.

### 예시

이 페이지의 모든 예제에서는 인코딩되지 않은 `<q>q</q>` 매개 변수를 보여 줍니다. 여기서 `title = 'hello'`은(는) `title+%3d+%27hello%27`(으)로 인코딩됩니다. 클라이언트 라이브러리는 이 인코딩을 자동으로 처리합니다.

* 이름이 &quot;hello&quot;인 파일 검색
  <pre>title = 'hello'</pre>
* 폴더별 MIME 유형을 사용하여 폴더 검색
  <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* 폴더가 아닌 파일 검색
  <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* &quot;hello&quot; 및 &quot;goodbye&quot;가 포함된 이름의 파일 검색
  <pre>제목에 'hello'가 있고 [!UICONTROL name]에 'goodbye'가 있습니다.</pre>
* &quot;hello&quot;라는 단어가 포함되지 않은 이름의 파일 검색
  <pre>제목에 'hello'가 포함되어 있지 않음</pre>
* 콘텐츠에 &quot;hello&quot;라는 단어가 포함된 파일 검색
  <pre>fullText에 'hello'가 포함되어 있습니다.</pre>
* 콘텐츠에 &quot;hello&quot;라는 단어가 포함되지 않은 파일 검색
  <pre>fullText에 'hello'가 포함되어 있지 않습니다.</pre>
* 콘텐츠에서 &quot;hello world&quot;라는 정확한 구문이 포함된 파일을 검색합니다.
  <pre>fullText에 "hello world"가 들어 있습니다."fullText에 "hello_world"가 들어 있습니다."</pre>
* &quot;\&quot; 문자가 포함된 쿼리가 있는 파일 검색(예: &quot;\authors&quot;)
  <pre>전체 텍스트에 '\\authors'가 포함되어 있음</pre>
* `test@example.org` 사용자가 쓸 수 있는 파일 검색
  <pre>의 'test@example.org' [!DNL writers]</pre>
* `parents` 컬렉션에서 ID `1234567`을(를) 검색합니다. ID가 `1234567`인 폴더에서 직접 있는 모든 파일과 폴더를 찾습니다.
  <pre>의 '1234567' [!UICONTROL parents]</pre>
* `parents` 컬렉션에서 별칭 ID `appDataFolder`을(를) 검색합니다. [응용 프로그램 데이터 폴더](https://developers.google.com/drive/api/v2/appdata) 바로 아래에 있는 모든 파일과 폴더를 찾습니다.
  <pre>상위 항목의 'appDataFolder'</pre>
* `test@example.org` 및 `test2@example.org` 사용자가 쓸 수 있는 파일 검색
  <pre>writers의 'test@example.org' 및 writers의 'test2@example.org'</pre>
* 휴지통에 있는 &quot;important&quot; 텍스트가 포함된 파일 검색
  <pre>fullText에 'important'가 포함되어 있고 휴지통으로 이동된 = true</pre>
* 2012년 6월 4일 이후에 수정된 파일 검색
  <pre>modifiedDate &gt; '2012-06-04T12:00:00' // 기본 시간대는 UTC입니다.</pre><pre>modifiedDate &gt; '2012-06-04T12:00:00-08:00'</pre>
* 이름에 &quot;hello&quot;가 있는 인증된 사용자와 공유된 파일을 검색합니다.
  <pre>sharedWithMe 및 제목에 'hello'가 포함됨</pre>
* 값이 `8e8aceg2af2ge72e78`인 이름이 `additionalID`인 [사용자 지정 파일 속성](https://developers.google.com/drive/api/v2/properties)이 있는 파일을 검색합니다.
  <pre>속성에는 { key='additionalID' 및 value='8e8aceg2af2ge72e78' 및 visibility='PRIVATE' }이(가) 있습니다.</pre>

이 안내서의 Source은 [[!DNL Google Drive] 설명서](https://developers.google.com/drive/api/v2/search-shareddrives)입니다.
