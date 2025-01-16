---
title: SFTP 모듈
description: ' [!DNL Adobe Workfront Fusion SFTP] 모듈을 사용하면 선택한 폴더/하위 폴더의 파일 변경 내용을 모니터링하거나, 새 파일을 원하는 폴더에 업로드하거나, 이미 폴더에 있는 기존 파일을 수정 또는 삭제하거나, 파일 권한을 변경할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# SFTP 모듈

[!DNL Adobe Workfront Fusion] SFTP 모듈을 사용하면 선택한 폴더/하위 폴더의 파일 변경 사항을 모니터링하고, 새 파일을 원하는 폴더로 업로드하고, 이미 폴더에 있는 기존 파일을 수정 또는 삭제하거나, 파일 권한을 변경할 수 있습니다.

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

SFTP를 [!DNL Workfront Fusion]과(와) 함께 사용하려면 SFTP 계정이 있어야 합니다(예: [!DNL GoDaddy] 웹 호스팅).

## SFTP를 [!DNL Workfront Fusion]에 연결 {#connect-sftp-to-workfront-fusion}

SFTP 계정을 [!DNL Workfront Fusion]에 연결하려면 대상 호스트와 SFTP 자격 증명(사용자 이름 및 암호 또는 사용자 이름 및 키)을 모듈의 [!UICONTROL Create a connection] 대화 상자에 입력해야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> SFTP 연결의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>연결할 SFTP 서버의 호스트 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Port] </td> 
   <td> <p>SFTP 서버 포트를 입력합니다. 예를 들어 22입니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Auth type]</p> </td> 
   <td> <p>SFTP 서버 연결에 사용할 인증 방법을 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL User name and password]</strong>: 자격 증명을 입력합니다.</li> 
     <li> <p><strong>[!UICONTROL User name and key]</strong>: 사용자 이름 및 개인 키/인증서 입력</p> <p>클라이언트측 인증을 사용하도록 개인 키를 업로드하거나 자체 서명된 인증서를 사용하여 TLS를 사용하려는 경우 인증서(P12 또는 PFX 파일)를 업로드합니다. 클라이언트측 인증서 인증을 사용하는 경우 여기에 CA 인증서를 입력할 수 있습니다.</p> <p>[!DNL Workfront Fusion] 여기서 제공하는 데이터(파일, 암호)는 유지하거나 저장하지 않습니다. 파일 및 암호는 개인 키/인증서를 추출하는 데만 사용됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

연결 정보를 입력한 후 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하여 연결을 설정합니다.

## [!UICONTROL SFTP]개 모듈 및 해당 필드

[!UICONTROL SFTP] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!UICONTROL SFTP] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 트리거

#### [!UICONTROL Watch Files in a Folder]

지정된 폴더에서 파일을 만들거나 변경할 때 세부 정보가 있는 파일을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>보려는 폴더를 입력하거나 매핑합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>버퍼 크기 [B]</td> 
   <td> <p> 버퍼 크기를 바이트 단위로 입력하십시오. 값은 서버에서 전송된 청크의 크기를 정의합니다. 값이 너무 높을 때 일부 서버에서 문제가 발생하거나 파일이 손상될 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 사용할 최대 파일 수 설정</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Subfolders in a Folder]

지정된 폴더에서 폴더를 만들거나 변경할 때 세부 정보가 있는 폴더를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>보려는 폴더를 입력하거나 매핑합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환할 최대 폴더 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

#### [!UICONTROL List a folder's content]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>파일, 폴더 또는 둘 다 검색할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>나열할 파일 또는 폴더가 포함된 폴더를 입력하거나 매핑합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>검색어를 입력하거나 매핑합니다. 예를들어 파일 확장명이 .txt인 파일을 검색하려면 <code>.txt</code>을(를) 입력합니다. 검색할 파일의 이름을 입력하거나 매핑할 수도 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> 파일 이름, 크기, 마지막 액세스 날짜 또는 마지막 수정 날짜별로 결과를 정렬할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order] </td> 
   <td> <p>결과를 오름차순으로 반환할지 아니면 내림차순으로 반환할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>이 옵션을 활성화하면 이 모듈에서 결과가 반환되지 않는 경우 시나리오를 중지하지 않습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환할 최대 결과 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Files]

이 모듈은 지정된 폴더의 파일을 나열합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> 버퍼 크기를 바이트 단위로 입력하십시오. 값은 서버에서 전송된 청크의 크기를 정의합니다. 값이 너무 높을 때 일부 서버에서 문제가 발생하거나 파일이 손상될 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>나열할 파일 또는 폴더가 포함된 폴더를 입력하거나 매핑합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>검색어를 입력하거나 매핑합니다. 예를들어 파일 확장명이 .txt인 파일을 검색하려면 <code>.txt</code>을(를) 입력합니다. 검색할 파일의 이름을 입력하거나 매핑할 수도 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> 파일 이름, 크기, 마지막 액세스 날짜 또는 마지막 수정 날짜별로 결과를 정렬할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order]</td> 
   <td> <p> 결과를 오름차순으로 반환할지 아니면 내림차순으로 반환할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>이 옵션을 활성화하면 이 모듈에서 결과가 반환되지 않는 경우 시나리오를 중지하지 않습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p> [!DNL Workfront Fusion]이(가) 한 주기 동안 반환할 최대 파일 수를 설정하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File]

이 모듈은 파일의 데이터를 포함한 파일 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> 버퍼 크기를 바이트 단위로 입력하십시오. 값은 서버에서 전송된 청크의 크기를 정의합니다. 값이 너무 높을 때 일부 서버에서 문제가 발생하거나 파일이 손상될 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path] </td> 
   <td> <p>파일 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

이 모듈에서는 SFTP 서버에 파일을 업로드할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>기존 폴더를 파일의 저장 위치로 지정합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td> <p> [!UICONTROL Dropbox] &gt; [!UICONTROL Get File]과(와) 같은 이전 모듈의 소스 파일을 매핑합니다. 파일 이름과 파일 데이터를 입력하거나 매핑할 수도 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>파일 또는 폴더에 대해 원하는 권한을 설정합니다. chmod 매개 변수를 사용합니다. 예: <code>777 </code> 또는 <code>-rwxrwxrwx</code>.</p> <p>chmod에 대한 자세한 내용은 <a href="https://ss64.com/bash/chmod.html">chmod 설명서</a>를 참조하세요.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File]

파일 이름을 바꿉니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> 이름을 바꿀 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New file name]</td> 
   <td> <p> 파일 확장명을 포함하여 파일의 새 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> 이동할 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New Folder]</td> 
   <td> <p> 파일의 새 위치에 대한 경로를 입력합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> 삭제할 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update file permissions]

파일의 권한을 변경할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> 이동할 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>원하는 파일 권한을 설정합니다. chmod 매개 변수를 사용합니다. 예: <code>777 </code> 또는 <code>-rwxrwxrwx</code>.</p> <p>패턴과 일치해야 함 <code> /(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>chmod에 대한 자세한 내용은 <a href="https://ss64.com/bash/chmod.html">chmod 설명서</a>를 참조하세요.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Folder]

지정된 위치에 새 폴더를 만듭니다.

>[!NOTE]
>
>폴더가 이미 있으면 모듈에서 오류가 발생합니다. 흐름을 중단하지 않고 계속하려면 모듈에 오류 처리기 경로를 연결하여 오류를 포착하고 [!UICONTROL Resume] 지시문을 사용하여 흐름을 계속합니다. 오류 처리기 경로를 연결하는 방법에 대한 자세한 내용은 [오류 처리 위치 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)를 참조하십시오. 오류 처리기 경로에 대한 자세한 내용은  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/errors/directives-for-error-handling.md)의 오류 처리에 대한 [지시문을 참조하십시오.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>기존 폴더를 새 폴더의 저장소 위치로 지정합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name]</td> 
   <td> <p> 폴더 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>원하는 폴더 권한을 설정합니다. chmod 매개 변수를 사용합니다. 예: <code>777 </code> 또는 <code>-rwxrwxrwx</code>.</p> <p>패턴과 일치해야 함 <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>chmod에 대한 자세한 내용은 <a href="https://ss64.com/bash/chmod.html">chmod 매뉴얼 페이지</a>를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">SFTP를 [!DNL Workfront Fusion]</a>에 연결을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> 삭제할 폴더의 경로를 지정합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
