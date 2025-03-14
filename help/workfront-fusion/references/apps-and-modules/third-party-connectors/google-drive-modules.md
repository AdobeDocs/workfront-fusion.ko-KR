---
title: Google 드라이브 모듈
description: ' [!DNL Adobe Workfront Fusion Google Drive] 모듈을 사용하면  [!DNL Google Drive]에서 파일, 폴더 또는 공유 드라이브를 모니터링, 검색, 만들기, 업데이트, 삭제 및 관리할 수 있습니다.'
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Google Drive]개 모듈

[!DNL Adobe Workfront Fusion] [!DNL Google Drive] 모듈을 사용하면 [!DNL Google Drive]에서 파일, 폴더 또는 공유 드라이브를 모니터링, 검색, 만들기, 업데이트, 삭제 및 관리할 수 있습니다.

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Google Drive] 계정을 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

[!DNL @gmail.com] 또는 [!DNL @googlemail.com] 사용자를 사용하는 경우 [!DNL Google Cloud Platform]에 OAuth 클라이언트를 만들어 [!UICONTROL 클라이언트 ID] 및 [!UICONTROL 클라이언트 암호]를 얻어야 합니다.

OAuth 클라이언트를 만들고 [!UICONTROL 클라이언트 ID] 및 [!UICONTROL 클라이언트 암호]를 얻는 방법에 대한 단계별 지침은 [연결 [!DNL Adobe Workfront Fusion] to [!DNL Google Services] 사용자 지정 OAuth 클라이언트 사용](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)을 참조하십시오.

[!DNL Google Drive] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion에 연결 만들기] - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

## [!DNL Google Drive]개 모듈 및 해당 필드

[!DNL Google Drive] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Google Drive] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [트리거](#triggers)
* [액션](#actions)

### 트리거

* [[!UICONTROL 모든 파일 보기]](#watch-all-files)
* [[!UICONTROL 댓글 보기]](#watch-comments)
* [[!UICONTROL 폴더에서 파일 보기]](#watch-files-in-folder)
* [[!UICONTROL 공유 파일 보기]](#watch-shared-files)

#### [!UICONTROL 모든 파일 보기]

이 트리거 모듈은 [!DNL Google Drive]의 파일을 추가하거나 수정할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 조사할 파일]</td> 
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
    <td >[!UICONTROL [!DNL Google Documents]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Spreadsheets]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Slides]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Drawings]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>새 파일과 모든 변경 내용을 보는지 아니면 새 파일만 보는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 다운로드한 최대 파일 수]</td> 
   <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 다운로드할 최대 결과 수(시나리오 실행당 반복 횟수)를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 댓글 보기]

이 트리거 모듈은 선택한 파일에 주석을 추가하거나 수정하면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일]</td> 
   <td>댓글을 확인할 파일을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>모든 변경 사항에 대해 감시할지 또는 새 주석에 대해서만 감시할지 선택</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 주석 수]</td> 
   <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 반환할 최대 댓글 수(시나리오 실행당 반복 횟수)를 설정하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더에서 파일 보기]

이 트리거 모듈은 지정된 폴더에서 파일을 추가하거나 수정할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL 감시할 폴더 선택]</td>
    <td >드라이브에서 파일을 감시할 폴더를 선택합니다.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL 조사할 파일]</td>
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
    <td >[!UICONTROL [!DNL Google Documents]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Spreadsheets]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Slides]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Drawings]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Watch]</td>
    <td>새 파일과 모든 변경 내용을 보는지 아니면 새 파일만 보는지 선택합니다.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL 다운로드한 최대 파일 수]</td>
    <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 다운로드할 최대 결과 수(시나리오 실행당 반복 횟수)를 설정합니다.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 공유 파일 보기]

새 파일이 공유되거나 기존 공유 파일이 업데이트될 때 트리거됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 감시할 폴더 선택]</td> 
   <td>파일을 보려는 공유 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 조사할 파일]</td> 
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
    <td >[!UICONTROL [!DNL Google Documents]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Spreadsheets]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Slides]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL [!DNL Google Drawings]개 파일을 형식으로 변환]</td>
    <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>새 파일과 모든 변경 내용을 보는지 아니면 새 파일만 보는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 다운로드한 최대 파일 수]</td> 
   <td>[!DNL Workfront Fusion]이(가) 한 주기 동안 다운로드할 최대 결과 수(시나리오 실행당 반복 횟수)를 설정합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 파일 복사]](#copy-a-file)
* [[!UICONTROL fFolder 만들기]](#create-a-folder)
* [[!UICONTROL 파일 삭제]](#delete-a-file)
* [[!UICONTROL 파일 가져오기]](#get-a-file)
* [[!UICONTROL 공유 링크 가져오기]](#get-a-share-link)
* [[!UICONTROL 파일을 휴지통으로 이동]](#move-a-filefolder-to-trash)
* [[!UICONTROL 파일/폴더 검색]](#search-for-filesfolders)
* [[!UICONTROL 파일 업데이트]](#update-a-file)
* [[!UICONTROL 파일 업로드]](#upload-a-file)

#### [!UICONTROL 파일 복사]

이 작업 모듈은 파일을 새 위치에 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 대상]</td> 
   <td> <p>파일을 복사할 대상을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 대상 폴더]</td> 
   <td>복사할 파일이 포함된 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td>복사할 파일의 ID를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 사본 이름]</td> 
   <td>새 파일의 제목을 입력합니다. 원래 파일 이름을 변경하지 않으려면 이 필드를 비워 둡니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더 만들기]

이 작업 모듈은 지정된 위치에 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 대상]</td> 
   <td> <p>폴더를 만들 대상을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 새 폴더 위치]</td> 
   <td>새 폴더를 만들 위치로 이동합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 새 폴더의 이름]</td> 
   <td>생성 중인 폴더의 이름을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 공유 폴더]</td> 
   <td>[!UICONTROL 공유] 링크를 가진 모든 사람과 폴더를 공유하려면 이 옵션을 선택합니다. 그렇지 않으면 소유자만 공유 링크를 사용할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 삭제]

이 작업 모듈은 파일 또는 폴더를 영구적으로 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td>삭제할 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 가져오기]

이 작업 모듈은 지정된 ID로 파일을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Documents]개 파일을 형식으로 변환]</td> 
   <td>[!DNL Google Documents]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Spreadsheets]개 파일을 형식으로 변환]</td> 
   <td>[!DNL Google Spreadsheets]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Slides]개 파일을 형식으로 변환]</td> 
   <td>[!DNL Google Slides]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Google Drawings]개 파일을 형식으로 변환]</td> 
   <td>[!DNL Google Drawings]을(를) 변환할 파일 형식을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td>검색할 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 공유 링크 가져오기]

이 작업 모듈은 Google 드라이브의 파일에 대한 공유 링크를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td>공유 링크를 가져올 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일을 휴지통으로 이동]

이 작업 모듈은 파일 또는 폴더를 휴지통으로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td>휴지통으로 이동할 파일의 ID를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일/폴더 검색]

이 검색 모듈은 검색 기준에 따라 파일 또는 폴더를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 대상]</td> 
   <td> <p>검색할 대상 드라이브를 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더 나열]</td> 
   <td>파일 또는 폴더를 검색할 폴더로 이동합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 검색]</td> 
   <td> <p> 파일, 폴더 또는 둘 다 검색할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Search]</p> </td> 
   <td> <p>수행할 검색 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search within file/folder names]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 쿼리]</strong> </p> <p>검색할 파일 이름 또는 전체 파일 이름(접미사 포함)의 일부를 입력합니다.</p> </li> 
       <li> <p><strong>[!UICONTROL 검색 옵션]</strong> </p> <p>정확한 용어를 검색할지 또는 검색어가 포함된 이름을 검색할지 여부를 선택합니다.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL 전체 텍스트] 검색</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 쿼리]</strong> </p> <p>[!DNL Google Drive]에서 검색할 검색어를 입력하십시오.</p> </li> 
      </ul> </li> 
     <li> <p><strong>사용자 지정 검색 쿼리 입력</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 쿼리]</strong> </p> <p>사용자 지정 검색 쿼리를 입력합니다. 자세한 내용은 이 문서의 [!UICONTROL Search for Files] 섹션을 참조하십시오.</p> </li> 
       <li> <p><strong>위에서 선택한 폴더를 쿼리에 추가</strong> </p> <p>상위 컬렉션에서 폴더를 검색합니다. 이렇게 하면 위에서 선택한 폴더에 직접 있는 모든 파일과 폴더를 찾습니다.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 결과 수]</td> 
   <td>한 실행 주기 동안 [!DNL Workfront Fusion]이(가) 반환할 최대 파일 또는 폴더 수를 설정하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 모듈이 결과를 반환하지 않더라도 라우트 실행을 계속합니다.]</td> 
   <td>모듈이 결과를 반환하지 않는 경우 시나리오가 중지되지 않도록 하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업데이트]

이 작업 모듈은 파일의 메타데이터 또는 콘텐츠를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 대상]</td> 
   <td> <p>업데이트할 파일이 포함된 대상을 선택합니다.</p> 
    <ul> 
     <li>[!UICONTROL 내 드라이브]</li> 
     <li>[!UICONTROL 나와 공유됨]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더로 이동]</td> 
   <td>파일을 특정 폴더로 이동하려면 파일을 이동할 폴더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 ID]</td> 
   <td>업데이트할 파일의 ID를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>업데이트된 파일의 제목을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 컨텐츠 변경]</td> 
   <td>파일 내용을 바꿀 것인지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source 파일]</td> 
   <td>콘텐츠를 바꿀 경우 이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 제어]</td> 
   <td>파일을 해당 Google 파일 형식으로 변환하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업로드]

파일을 [!DNL Google Drive]에 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>[!DNL Google Drive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">[!UICONTROL Workfront Fusion]에 [!DNL Google Drive] 연결</a>을 참조하십시오.</p> </td> 
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
   <td>[!UICONTROL 대상 폴더]</td> 
   <td>파일을 업로드할 폴더를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source 파일]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>새 파일의 제목을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 변환]</td> 
   <td>이 옵션을 활성화하면 모듈이 파일을 해당 [!DNL Google] 형식으로 변환할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

## 문제 해결

### 파일을 업로드하거나 업데이트할 수 없음

파일 업로드 또는 업데이트가 실패한 이유는 다음과 같습니다.

* 업로드한 파일이 너무 커서 [!DNL Google Drive] 계획에 허용된 최대 파일 크기 제한을 초과하거나 [!DNL Google Drive] 저장소 제한을 초과했습니다. 저장소 계획을 업그레이드하거나 [!DNL Google Drive] 서비스에서 기존 파일을 삭제할 수 있습니다.
* 파일을 업로드할 선택한 폴더가 더 이상 존재하지 않습니다. 이 경우 시나리오가 중지되며 모듈에서 다른 대상 폴더를 선택해야 합니다.

<!-- Not present February 2025

## Search for files

In the module List files in a folder you can use your own query which consists of these parts:

* **[!UICONTROL Field]** - Attribute of the file that is being searched, for example, the attribute `name` of the file.

* **[!UICONTROL Operator]** - Test that is performed on the data to provide a match, for example, `contains`.

* **[!UICONTROL Value]** - The content of the attribute that is tested, for example, the name of the file `My cool document`.

Combine clauses with the conjunctions `and` or `or`, and negate the query with `not`.

* [Fields](#fields)
* [Value types](#value-types)
* [Operators](#operators)
* [Examples](#examples)

### Fields 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Field </th> 
   <th>Value Type </th> 
   <th>Operators</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Name of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Full text of the file including name, description, content, and indexable text.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME type of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date of the last modification to the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date that the user last viewed a file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Whether the file is in the trash or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Whether the file is starred or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Whether the [!UICONTROL parents] collection contains the specified ID.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who own the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to modify the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to read the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Files that are in the user's "Shared with me" collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Public custom file properties.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following about operators in these fields:

* The `contains` operator only performs prefix matching for a `title`.

   For example, the title "HelloWorld" matches for `title contains 'Hello'` but not for `title contains 'World'`.

* The `contains` operator only performs matching on entire string tokens for `fullText`.

   For example, if the full text of a doc contains the string "HelloWorld" only the query `fullText contains 'HelloWorld'` returns a result. Queries such as `fullText contains 'Hello'` would not return results in this scenario.

* The `contains` operator matches on an exact alphanumeric phrase if it is surrounded by double quotes.

   For example, if the `fullText` of a doc contains the string "Hello there world", then the query `fullText contains '"Hello there"'` returns a result, but the query `fullText contains '"Hello world"'` does not.

   Furthermore, because the search is alphanumeric, if the `fullText` of a doc contains the string "Hello_world", then the query `fullText contains '"Hello world"'` returns a result.

* Fields of `type` date are currently not comparable to each other, only to constant dates.

### Value types

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Value Type</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Surround with single quotes '. Escape single quotes in queries with <code>\'</code>, e.g.,<code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>or <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>RFC 3339 format, default timezone is UTC, e.g., <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operators

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>The content of one string is present in the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> The content of a string or boolean is equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> The content of a string or boolean is not equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> A date is earlier than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> A date is earlier than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> A date is later than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> A date is later than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>An element is contained within a collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Return files that match both clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Return files that match either clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Negates a search clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>A collection contains an element matching the parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

For compound clauses, you can use parentheses to group clauses together. For example:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` This search returns all files with an image or video MIME type that their last modification was after June 4, 2012. Because `and` and `or` operators are evaluated from left to right, without parentheses, the above example would return only images modified after June 4, 2012, but would return all videos, even those before June 4, 2012.

### Examples 

All examples on this page show the unencoded `<q>q</q>` parameter, where `title = 'hello'` is encoded as `title+%3d+%27hello%27`. Client libraries handle this encoding automatically.

* Search for files with the name "hello"
   <pre>title = 'hello'</pre>
* Search for folders using the folder-specific MIME type
   <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Search for files that are not folders
   <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Search for files with a name containing the words "hello" and "goodbye"
   <pre>title contains 'hello' and [!UICONTROL name] contains 'goodbye'</pre>
* Search for files with a name that does not contain the word "hello"
   <pre>not title contains 'hello'</pre>
* Search for files containing the word "hello" in the content
   <pre>fullText contains 'hello'</pre>
* Search for files not containing the word "hello" in the content
   <pre>not fullText contains 'hello'</pre>
* Search for files containing the exact phrase "hello world" in the content
   <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Search for files with a query containing the "\" character (e.g., "\authors")
   <pre>fullText contains '\\authors'</pre>
* Search for files writeable by the user `test@example.org`
   <pre>'test@example.org' in [!DNL writers]</pre>
* Search for the ID `1234567` in the `parents` collection. This finds all files and folders located directly in the folder whose ID is `1234567`.
   <pre>'1234567' in [!UICONTROL parents]</pre>
* Search for the alias ID `appDataFolder` in the `parents` collection. This finds all files and folders located directly under the [Application Data folder](https://developers.google.com/drive/api/v2/appdata).
   <pre>'appDataFolder' in parents</pre>
* Search for files writeable by the users `test@example.org` and `test2@example.org`
   <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Search for files containing the text "important" which are in the trash
   <pre>fullText contains 'important' and trashed = true</pre>
* Search for files modified after June 4th 2012
   <pre>modifiedDate > '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate > '2012-06-04T12:00:00-08:00'</pre>
* Search for files shared with the authorized user with "hello" in the name
   <pre>sharedWithMe and title contains 'hello'</pre>
* Search for files with a [custom file property](https://developers.google.com/drive/api/v2/properties) named `additionalID` with the value `8e8aceg2af2ge72e78`.
   <pre>properties has { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }</pre>

Source of this guide is [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).

-->
