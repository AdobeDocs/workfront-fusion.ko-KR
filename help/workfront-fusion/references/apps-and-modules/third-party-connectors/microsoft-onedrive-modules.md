---
title: Microsoft OneDrive 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 OneDrive를 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: d21eafad-9c67-4f42-b718-0aa4223846e6
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3286'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL OneDrive]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

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

[!DNL OneDrive] 모듈을 사용하려면 [!DNL Microsoft OneDrive] 계정이 있어야 합니다.



## OneDrive API 정보

OneDrive 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://graph.microsoft.com/v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>


## [!DNL Workfront Fusion]에 [!DNL OneDrive] 서비스를 연결하는 중

[!DNL OneDrive] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 [[!UICONTROL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하세요.

>[!NOTE]
>
>일부 Microsoft 앱은 개별 사용자 권한에 연결된 동일한 연결을 사용합니다. 따라서 연결을 만들 때 권한 동의 화면에는 현재 애플리케이션에 필요한 새 권한 외에도 이 사용자의 연결에 대해 이전에 부여된 모든 권한이 표시됩니다.
>
>예를 들어 사용자가 Excel 커넥터를 통해 부여된 &quot;테이블 읽기&quot; 권한을 가지고 있는 다음 Outlook 커넥터에서 연결을 만들어 이메일을 읽은 경우 권한 동의 화면에 이미 부여된 &quot;테이블 읽기&quot; 권한과 새로 필요한 &quot;이메일 쓰기&quot; 권한이 모두 표시됩니다.

## [!DNL Microsoft OneDrive]개 모듈 및 해당 필드

[!DNL OneDrive] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL OneDrive] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [파일/폴더](#filefolder)
* [기타](#other)

### 파일/폴더

* [[!UICONTROL Watch Files/Folders]](#watch-filesfolders)
* [[!UICONTROL Search Files/Folders]](#search-filesfolders)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Download a file]](#download-a-file)
* [[!UICONTROL Upload a file]](#upload-a-file)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Get a Share Link]](#get-a-share-link)
* [[!UICONTROL Move a File/Folder]](#move-a-filefolder)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File/Folder]](#delete-a-filefolder)

#### [!UICONTROL Watch Files/Folders]

이 트리거 모듈은 파일 또는 폴더가 생성 또는 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Files/Folders]</td> 
   <td> <p>파일 또는 폴더를 볼 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL By Created Time]</b> </p> <p>새 파일 또는 폴더를 확인하십시오.</p> </li> 
     <li> <p><b>[!UICONTROL By Updated Time]</b> </p> <p>업데이트된 기존 파일 또는 폴더를 확인하십시오.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>감시할 위치 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>모듈에서 볼 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>모듈에서 감시할 폴더로 이동합니다. 쿼리를 입력하여 반환된 결과를 필터링할 수도 있습니다.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>모듈은 드라이브 소유자와 공유된 파일을 감시합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>모듈에서 볼 SharePoint 사이트를 선택합니다. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>모듈에서 조사할 드라이브의 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>파일, 폴더 또는 두 가지 모두를 감시할지 여부를 선택합니다.</p> <p>참고: [!UICONTROL Shared With Me] 드라이브의 폴더를 감시할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Search Files/Folders]

이 검색 모듈은 사용자가 설정한 기준에 따라 파일과 폴더를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>검색할 위치를 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>모듈이 검색할 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>모듈이 검색할 폴더로 이동합니다. 쿼리를 입력하여 반환된 결과를 필터링할 수도 있습니다.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>모듈은 드라이브 소유자와 공유된 파일을 검색합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>모듈이 검색할 [!DNL SharePoint] 사이트를 선택하십시오. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>모듈에서 검색할 드라이브의 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>파일, 폴더 또는 둘 다 검색할지 선택합니다.</p> <p>참고: [!UICONTROL Shared With Me] 드라이브에서 폴더를 검색할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

이 작업 모듈은 지정된 파일의 메타데이터를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>파일 ID로 파일을 식별할지 파일 경로로 파일을 식별할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>파일 ID 또는 파일 경로 입력 방법 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 파일 또는 경로 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>검색할 위치를 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>가져올 파일이 포함된 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>가져올 파일이 포함된 SharePoint 사이트를 선택합니다. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>드라이브에 가져올 파일이 들어 있는 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>가져올 파일이 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>[!UICONTROL Enter Manually]을(를) 선택한 경우 가져올 파일의 파일 ID 또는 경로를 입력하거나 매핑하십시오.</p> <p>[!UICONTROL Select from the list]을(를) 선택한 경우 가져올 파일을 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a file]

이 작업 모듈은 지정된 파일을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>파일 ID로 파일을 식별할지 파일 경로로 파일을 식별할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">파일 ID/파일 경로 입력</td> 
   <td> <p>파일 ID 또는 파일 경로 입력 방법 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 파일 또는 경로 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>다운로드할 파일을 포함할 위치를 선택하십시오.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>다운로드할 파일이 포함된 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>다운로드할 파일이 포함된 SharePoint 사이트를 선택합니다. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>다운로드하려는 파일이 드라이브에 들어 있는 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>다운로드할 파일이 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>[!UICONTROL Enter Manually]을(를) 선택한 경우 다운로드할 파일의 파일 ID 또는 경로를 입력하거나 매핑합니다.</p> <p>[!UICONTROL Select from the list]을(를) 선택한 경우 다운로드할 파일을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Convert to PDF]</td> 
   <td> <p>파일을 PDF 파일로 변환하려면 이 옵션을 활성화합니다. 다음 파일 형식에서 변환할 수 있습니다.</p> 
    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td> 
        <ul> 
         <li> <p> <p>CSV</p> </p> </li> 
         <li> <p> <p>DOC</p> </p> </li> 
         <li> <p> <p>DOCX</p> </p> </li> 
         <li> <p> <p>ODP</p> </p> </li> 
         <li> <p> <p>ODS</p> </p> </li> 
         <li> <p> <p>ODT</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p> <p>포트</p> </p> </li> 
         <li> <p> <p>POTM</p> </p> </li> 
         <li> <p> <p>POTX</p> </p> </li> 
         <li> <p> <p>PPS</p> </p> </li> 
         <li> <p> <p>PPSX</p> </p> </li> 
         <li> <p> <p>PPSXM</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p>PPT</p> </li> 
         <li> <p>PPTM</p> </li> 
         <li> <p>PPTX</p> </li> 
         <li> <p>RTF</p> </li> 
         <li> <p>XLS</p> </li> 
         <li> <p>XLSX</p> </li> 
        </ul> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

이 작업 모듈은 지정된 폴더에 파일을 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">(폴더 위치 ID 및 경로) 입력</td> 
   <td>ID로 대상 폴더를 식별할지 아니면 경로로 대상 폴더를 식별할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>파일을 업로드할 위치를 선택하십시오.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>가져올 파일이 포함된 드라이브를 선택합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>파일을 업로드할 폴더가 포함된 [!DNL SharePoint] 사이트를 선택하십시오. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>드라이브에 파일을 업로드할 폴더가 포함된 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>파일을 업로드할 폴더가 포함된 드라이브를 선택합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the File with the Same Name Exists]</td> 
   <td>이름이 같은 파일이 이미 있는 경우 진행 방법을 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>업로드된 파일에 설명을 추가합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

이 작업 모듈은 지정된 드라이브에 새 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>폴더를 만들 위치를 선택하십시오.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>폴더를 만들 드라이브를 선택합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>폴더를 만들 [!DNL SharePoint] 사이트를 선택하십시오. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>폴더를 만들 드라이브를 소유한 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>폴더를 만들 드라이브를 선택합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>새 폴더를 하위 폴더로 설정하려면 하위 폴더로 설정할 폴더로 이동합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Folder Name]</td> 
   <td> <p>새 폴더의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the Folder with the Same Name Exists]</td> 
   <td>이름이 같은 파일이 이미 있는 경우 진행 방법을 선택하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Share Link]

이 작업 모듈은 지정된 파일에 대한 공유 링크를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>파일 ID로 파일을 식별할지 파일 경로로 파일을 식별할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>파일 ID 또는 파일 경로 입력 방법 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 파일 또는 경로 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>공유 링크를 검색할 위치 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>공유 링크를 검색할 파일이 포함된 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>공유 링크를 검색할 파일이 포함된 SharePoint 사이트를 선택합니다. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>공유 링크를 검색할 파일이 드라이브에 들어 있는 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>공유 링크를 검색할 파일이 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>[!UICONTROL Enter Manually]을(를) 선택한 경우 공유 링크를 검색할 파일의 파일 ID 또는 경로를 입력하거나 매핑합니다.</p> <p>목록에서 [!UICONTROL Select]을(를) 선택한 경우 공유 링크를 검색할 파일을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permission Type]</td> 
   <td> <p>링크가 있는 사람이 파일을 읽고 쓸 수 있게 할지 아니면 읽기 전용으로 할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td>링크를 가진 모든 사용자가 파일을 사용할 수 있게 할지 또는 링크를 가진 조직 구성원만 파일을 사용할 수 있게 할지 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder]

이 작업 모듈은 파일 또는 폴더를 새 폴더 위치로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>파일 ID로 파일을 식별할지 파일 경로로 파일을 식별할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID / File Path]</td> 
   <td> <p>파일 ID 또는 파일 경로 입력 방법 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 파일 또는 경로 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>이동할 파일 또는 폴더가 포함된 위치를 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>이동할 파일 또는 폴더가 포함된 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>이동할 파일 또는 폴더가 포함된 [!DNL SharePoint] 사이트를 선택하십시오. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>드라이브에 이동할 파일 또는 폴더가 포함된 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>이동할 파일 또는 폴더가 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">선택 [!UICONTROL File/Folder]</td> 
   <td>파일을 이동할지 폴더를 이동할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> <p role="rowheader">[!UICONTROL Folder] / [!UICONTROL Folder ID] / [!UICONTROL Folder Path]</p> </td> 
   <td> <p>[!UICONTROL Enter Manually]을(를) 선택한 경우 이동할 파일 또는 폴더의 ID 또는 경로를 입력하거나 매핑합니다.</p> <p>목록에서 [!UICONTROL Select]을(를) 선택한 경우 이동할 파일 또는 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>파일 또는 폴더를 이동할 위치를 입력할 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 파일 또는 경로 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>파일 또는 폴더를 이동할 위치를 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>파일이나 폴더를 이동할 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>파일 또는 폴더를 이동할 [!DNL SharePoint] 사이트를 선택하십시오. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>파일이나 폴더를 이동할 드라이브를 선택한 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>파일이나 폴더를 이동할 폴더가 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> <p>이 항목을 비워 두면 파일 또는 폴더는 동일한 [!DNL OneDrive] 내에서만 이동할 수 있습니다.</p> <p>파일과 폴더를 [!UICONTROL My Drive]에서 [!UICONTROL Site's Drive] 또는 [!UICONTROL Group's Drive](으)로 이동할 수 있습니다. </p> <p>[!UICONTROL Site's Drive]에서 같은 사이트의 같은 드라이브로만 파일을 이동할 수 있습니다.</p> <p>[!UICONTROL Group's Drive]에서 같은 그룹의 같은 드라이브로만 파일을 이동할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>파일이나 폴더를 이동할 폴더를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

이 작업 모듈은 파일을 새 폴더 위치에 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>파일 ID로 파일을 식별할지 파일 경로로 파일을 식별할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>파일 ID 또는 파일 경로 입력 방법 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 파일 또는 경로 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>복사할 파일이 포함된 위치를 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>복사할 파일 또는 폴더가 포함된 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>이동할 파일이 포함된 SharePoint 사이트를 선택합니다. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>드라이브에 복사할 파일이 들어 있는 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>복사할 파일이 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> </td> 
   <td> <p>[!UICONTROL Enter Manually]을(를) 선택한 경우 복사할 파일의 ID 또는 경로를 입력하거나 매핑하십시오.</p> <p>목록에서 [!UICONTROL Select]을(를) 선택한 경우 복사할 파일을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>파일을 복사하거나 다음과 같은 위치에 입력할 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 폴더 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New OneDrive location]</td> 
   <td> <p>파일러를 복사할 위치를 선택합니다. 목록에서 새 폴더 위치를 선택한 경우 이 옵션을 사용할 수 있습니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>파일을 복사할 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>파일을 복사할 [!DNL SharePoint] 사이트를 선택하십시오. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>파일을 복사할 드라이브의 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>파일을 복사할 폴더가 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> <p>이 항목을 비워 두면 파일 또는 폴더는 동일한 [!UICONTROL OneDrive] 내에서만 복사할 수 있습니다.</p> <p>[!UICONTROL My Drive]에서 [!UICONTROL Site's Drive] 또는 [!UICONTROL Group's Drive](으)로 파일 및 폴더를 복사할 수 있습니다. </p> <p>[!UICONTROL Site's Drive]의 파일을 같은 사이트의 같은 드라이브에만 복사할 수 있습니다.</p> <p>[!UICONTROL Group's Drive]의 파일을 같은 그룹의 같은 드라이브에만 복사할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>복사 또는 폴더를 이동할 폴더를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Copied File Name]</td> 
   <td> <p>파일의 새 복사본 이름을 입력하거나 매핑합니다. 원본 파일 이름을 변경하지 않으려면 이 항목을 비워 둘 수 있습니다.</p> <p>이름에는 파일 확장명이 포함되어야 합니다. 예:<code> file.txt</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File/Folder]

이 작업 모듈은 선택한 파일을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File/Folder ID & Path)]</td> 
   <td>파일 ID로 파일을 식별할지 파일 경로로 파일을 식별할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File/Folder ID /Enter a File/Folder Path]</td> 
   <td> <p>파일 ID 또는 파일 경로 입력 방법 선택:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>ID 또는 경로를 직접 입력하거나 이전 모듈에서 매핑하려면 이 옵션을 선택합니다.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>사용 가능한 파일 또는 경로 목록에서 선택하려면 이 옵션을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>검색할 위치를 선택합니다.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>모듈에서 드라이브 ID를 입력하도록 할지 여부를 선택합니다.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>삭제할 파일 또는 폴더가 포함된 드라이브의 ID를 입력합니다.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>삭제할 파일 또는 폴더가 포함된 [!DNL SharePoint] 사이트를 선택하십시오. 사용 가능한 사이트는 사이트 다음에 로그인한 사용자가 표시됩니다.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>드라이브에 삭제할 파일 또는 폴더가 포함된 그룹을 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>삭제할 파일 또는 폴더가 포함된 드라이브를 선택하거나 매핑합니다. [!UICONTROL Enable to Enter a Drive ID] 필드에서 [!UICONTROL No]을(를) 선택한 경우 이 필드를 사용할 수 없습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">선택 [!UICONTROL File/Folder]</td> 
   <td>파일 또는 폴더 삭제 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>[!UICONTROL Enter Manually]을(를) 선택한 경우 삭제할 파일의 파일 ID 또는 경로를 입력하거나 매핑합니다.</p> <p>목록에서 [!UICONTROL Select]을(를) 선택한 경우 삭제할 파일을 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

#### [!UICONTROL Make an API Call]

이 모듈은 사용자 지정 API 호출을 수행합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL OneDrive] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://graph.microsoft.com</code>과(와) 관련된 경로를 입력하십시오. 예:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
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



## 파일을 업로드하거나 업데이트할 수 없는 경우

파일 업로드 또는 업데이트가 실패할 때 발생할 수 있는 몇 가지 문제가 있습니다.

* 업로드한 파일이 너무 커서 [!DNL OneDrive] 계획에 대한 최대 파일 크기 제한을 초과하거나 [!DNL OneDrive] 계정의 저장소 할당량을 모두 사용했습니다. 저장소 공간을 늘리려면 [!DNL OneDrive]에서 기존 파일을 삭제하거나 [!DNL OneDrive] 계정을 업그레이드하세요.
* OneDrive에서는 이름이 같은 두 파일을 하나의 폴더에 업로드할 수 없습니다. 대상 폴더에 업로드되는 파일과 같은 이름의 파일이 포함되어 있으면 오류가 발생하여 시나리오 실행이 종료됩니다. 해결 방법은 업로드되는 파일의 이름을 바꾸는 것입니다. 파일을 업데이트하는 것이 목표라면 [!UICONTROL Update a file] 액션을 사용하십시오.
* 이전에 선택한 파일 업로드 폴더가 더 이상 존재하지 않습니다. 시나리오가 중지되며 대상 폴더를 다시 선택해야 합니다.
