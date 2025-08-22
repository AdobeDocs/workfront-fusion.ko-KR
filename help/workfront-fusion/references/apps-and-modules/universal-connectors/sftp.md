---
title: SFTP 모듈
description: ' [!DNL Adobe Workfront Fusion SFTP] 모듈을 사용하면 선택한 폴더/하위 폴더의 파일 변경 내용을 모니터링하거나, 새 파일을 원하는 폴더에 업로드하거나, 이미 폴더에 있는 기존 파일을 수정 또는 삭제하거나, 파일 권한을 변경할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2216'
ht-degree: 0%

---

# SFTP 모듈

Adobe Workfront Fusion SFTP 모듈을 사용하면 선택한 폴더/하위 폴더의 파일 변경 사항을 모니터링하고, 새 파일을 원하는 폴더로 업로드하고, 이미 폴더에 있는 기존 파일을 수정 또는 삭제하거나, 파일 권한을 변경할 수 있습니다.

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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

SFTP를 Workfront Fusion과 함께 사용하려면 SFTP 계정(예: [!DNL GoDaddy] 웹 호스팅)이 있어야 합니다.

## SFTP를 Workfront Fusion에 연결 {#connect-sftp-to-workfront-fusion}

SFTP 계정을 Workfront Fusion에 연결하려면 대상 호스트 및 SFTP 자격 증명(사용자 이름 및 암호 또는 사용자 이름 및 키)을 지정하는 연결을 만들어야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결 이름]</td> 
   <td> <p> SFTP 연결의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 환경]</td>
    <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 유형]</td>
    <td>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</td>
  </tr>
  <tr>
   <td role="rowheader"> <p>[!UICONTROL 호스트]</p> </td> 
   <td> <p>연결할 SFTP 서버의 호스트 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 포트] </td> 
   <td> <p>SFTP 서버 포트를 입력합니다. 예를 들어 22입니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 인증 유형]</p> </td> 
   <td> <p>SFTP 서버 연결에 사용할 인증 방법을 선택합니다.</p> 
    <ul> 
     <li><strong>[!UICONTROL 사용자 이름 및 암호]</strong>: 자격 증명을 입력하십시오.</li> 
     <li> <p><strong>[!UICONTROL 사용자 이름 및 키]</strong>: 사용자 이름과 개인 키/인증서를 입력하십시오.</p> <p>클라이언트측 인증을 사용하도록 개인 키를 업로드하거나 자체 서명된 인증서를 사용하여 TLS를 사용하려는 경우 인증서(P12 또는 PFX 파일)를 업로드합니다. 클라이언트측 인증서 인증을 사용하는 경우 여기에 CA 인증서를 입력할 수 있습니다.</p> <p>Workfront Fusion은 사용자가 여기에 제공한 데이터(파일, 암호)를 보존하거나 저장하지 않습니다. 파일 및 암호는 개인 키/인증서를 추출하는 데만 사용됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 키 교환 알고리즘] </td> 
   <td> <p>키 교환에 사용할 알고리즘 세트를 입력할 수 있습니다. 모듈은 추가된 순서에 따라 알고리즘에 우선 순위를 지정합니다. 추가할 각 알고리즘에 대해 <b>항목 추가</b>를 클릭하고 알고리즘을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 암호] </td> 
   <td> <p>키 교환에 사용할 암호 집합을 입력할 수 있습니다. 모듈은 추가된 순서에 따라 암호 우선 순위를 지정합니다. 추가할 각 암호에 대해 <b>항목 추가</b>를 클릭하고 암호를 선택하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

연결 정보를 입력한 후 **[!UICONTROL 계속]**&#x200B;을 클릭하여 연결을 설정합니다.

### 지원되는 연결 옵션

SFTP 커넥터는 연결을 만들 때 다음을 지원합니다.

#### 키 교환 알고리즘(KEX)

* `ecdh-sha2-nistp256`
* `ecdh-sha2-nistp384`
* `ecdh-sha2-nistp521`
* `diffie-hellman-group-exchange-sha256`
* `diffie-hellman-group14-sha256`
* `diffie-hellman-group16-sha512`
* `diffie-hellman-group18-sha512`
* `diffie-hellman-group14-sha1`

#### 암호

* `aes256-gcm@openssh.com`
* `aes256-gcm`
* `aes128-gcm@openssh.com`
* `aes128-gcm`
* `aes256-ctr`
* `aes192-ctr`
* `aes128-ctr`
* `aes256-cbc`
* `aes192-cbc`
* `aes128-cbc`
* `blowfish-cbc`

#### 서버 호스트 키 형식

* `ssh-ed25519`
* `ecdsa-sha2-nistp256`
* `ecdsa-sha2-nistp384`
* `ecdsa-sha2-nistp521`
* `ssh-rsa`
* `ssh-dss`
<!--
* `rsa-sha2-256`
* `rsa-sha2-512`
-->

## [!UICONTROL SFTP] 모듈 및 해당 필드

[!UICONTROL SFTP] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 추가 [!UICONTROL SFTP] 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 트리거

* [폴더에서 파일 보기](#watch-files-in-a-folder)
* [폴더에서 하위 폴더 보기](#watch-subfolders-in-a-folder)

#### [!UICONTROL 폴더에서 파일 보기]

지정된 폴더에서 파일을 만들거나 변경할 때 세부 정보가 있는 파일을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>보려는 폴더를 입력합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정하거나 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>버퍼 크기 [B]</td> 
   <td> <p> 버퍼 크기를 바이트 단위로 입력하십시오. 값은 서버에서 전송된 청크의 크기를 정의합니다. 값이 너무 높을 때 일부 서버에서 문제가 발생하거나 파일이 손상될 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 파일 수]</td> 
   <td> <p> 각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더에서 하위 폴더 보기]

지정된 폴더에서 폴더를 만들거나 변경할 때 세부 정보가 있는 폴더를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>보려는 폴더를 입력하거나 매핑합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 파일 수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [폴더 만들기](#create-a-folderr)
* [파일 삭제](#delete-a-file)
* [폴더 삭제](#delete-a-folder)
* [파일 가져오기](#get-a-file)
* [파일 가져오기](#get-files)
* [폴더의 컨텐츠 나열](#list-a-folders-content)
* [파일 이동](#move-a-file)
* [파일 이름 바꾸기](#rename-a-file)
* [파일 권한 업데이트](#update-file-permissions)
* [파일 업로드](#upload-a-file)

#### [!UICONTROL 폴더 만들기]

이 작업 모듈은 지정된 위치에 새 폴더를 만듭니다.

>[!NOTE]
>
>폴더가 이미 있으면 모듈에서 오류가 발생합니다. 흐름을 중단하지 않고 계속하려면 모듈에 오류 처리기 경로를 연결하여 오류를 catch하고 [!UICONTROL Resume] 지시문을 사용하여 흐름을 계속하십시오. 오류 처리기 경로를 연결하는 방법에 대한 자세한 내용은 [Adobe Workfront Fusion의 오류 처리](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)를 참조하십시오. 오류 처리기 경로에 대한 자세한 내용은 [Adobe Workfront Fusion의 오류 처리에 대한 지시문](/help/workfront-fusion/references/errors/directives-for-error-handling.md)을 참조하십시오.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>기존 폴더를 새 폴더의 저장소 위치로 지정합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더 이름]</td> 
   <td> <p> 폴더 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 권한]</p> </td> 
   <td> <p>원하는 폴더 권한을 설정합니다. chmod 매개 변수를 사용합니다. 예: <code>777</code> 또는 <code>-rwxrwxrwx</code>.</p> <p>이러한 권한은 패턴과 일치해야 합니다. <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>chmod에 대한 자세한 내용은 <a href="https://ss64.com/bash/chmod.html">chmod 설명서</a>를 참조하세요.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 삭제]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 경로]</td> 
   <td> <p> 삭제할 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더 삭제]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> 삭제할 폴더의 경로를 지정합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 가져오기]

이 모듈은 파일의 데이터를 포함한 파일 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 버퍼 크기 [B]]</td> 
   <td> <p> 버퍼 크기를 바이트 단위로 입력하십시오. 값은 서버에서 전송된 청크의 크기를 정의합니다. 값이 너무 높을 때 일부 서버에서 문제가 발생하거나 파일이 손상될 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 경로] </td> 
   <td> <p>파일 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 가져오기]

이 모듈은 지정된 폴더에서 파일을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 버퍼 크기 [B]]</td> 
   <td> <p> 버퍼 크기를 바이트 단위로 입력하십시오. 값은 서버에서 전송된 청크의 크기를 정의합니다. 값이 너무 높을 때 일부 서버에서 문제가 발생하거나 파일이 손상될 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>나열할 파일 또는 폴더가 포함된 폴더를 입력하거나 매핑합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>검색어를 입력하거나 매핑합니다. 예를들어 파일 확장명이 .txt인 파일을 검색하려면 <code>.txt</code>을(를) 입력합니다. 검색할 파일의 이름을 입력하거나 매핑할 수도 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 정렬 기준]</td> 
   <td> <p> 파일 이름, 크기, 마지막 액세스 날짜 또는 마지막 수정 날짜별로 결과를 정렬할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 정렬 순서]</td> 
   <td> <p> 결과를 오름차순으로 반환할지 아니면 내림차순으로 반환할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 모듈이 결과를 반환하지 않더라도 라우트 실행을 계속합니다.]</p> </td> 
   <td>이 옵션을 활성화하면 이 모듈에서 결과가 반환되지 않는 경우 시나리오를 중지하지 않습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 결과 수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더의 콘텐츠 나열]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 표시] </td> 
   <td> <p>파일, 폴더 또는 둘 다 검색할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>나열할 파일 또는 폴더가 포함된 폴더를 입력하거나 매핑합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>검색어를 입력하거나 매핑합니다. 예를들어 파일 확장명이 .txt인 파일을 검색하려면 <code>.txt</code>을(를) 입력합니다. 검색할 파일의 이름을 입력하거나 매핑할 수도 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 정렬 기준]</td> 
   <td> <p> 파일 이름, 크기, 마지막 액세스 날짜 또는 마지막 수정 날짜별로 결과를 정렬할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 정렬 순서] </td> 
   <td> <p>결과를 오름차순으로 반환할지 아니면 내림차순으로 반환할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 모듈이 결과를 반환하지 않더라도 라우트 실행을 계속합니다.]</p> </td> 
   <td>이 옵션을 활성화하면 이 모듈에서 결과가 반환되지 않는 경우 시나리오를 중지하지 않습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 결과 수]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 이동]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 경로]</td> 
   <td> <p> 이동할 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 새 폴더]</td> 
   <td> <p> 파일의 새 위치에 대한 경로를 입력합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 이름 바꾸기]

파일 이름을 바꿉니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 경로]</td> 
   <td> <p> 이름을 바꿀 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 새 파일 이름]</td> 
   <td> <p> 파일 확장명을 포함하여 파일의 새 이름을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 권한 업데이트]

파일의 권한을 변경할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 경로]</td> 
   <td> <p> 이동할 파일의 경로를 입력합니다. <code>/home/user/file.txt</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 로그인한 사용자의 특정 폴더(예: <code>./file.txt</code>)를 가리키는 상대 경로를 지정할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 권한]</p> </td> 
   <td> <p>원하는 파일 권한을 설정합니다. chmod 매개 변수를 사용합니다. 예: <code>777</code> 또는 <code>-rwxrwxrwx</code>.</p> <p>이러한 권한은 패턴과 일치해야 합니다. <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>chmod에 대한 자세한 내용은 <a href="https://ss64.com/bash/chmod.html">chmod 설명서</a>를 참조하세요.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업로드]

이 모듈에서는 SFTP 서버에 파일을 업로드할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>SFTP 계정을 Workfront Fusion에 연결하는 방법은 이 문서의 <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 SFTP 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>기존 폴더를 파일의 저장 위치로 지정합니다. <code>/home/user/</code>과(와) 같은 절대 경로를 지정할 수 있습니다. 또는 다음과 같이 로그인한 사용자의 특정 폴더를 가리키는 상대 경로를 지정할 수 있습니다. <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source 파일]</td> 
   <td> <p> 이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 권한]</p> </td> 
   <td> <p>파일 또는 폴더에 대해 원하는 권한을 설정합니다. chmod 매개 변수를 사용합니다. 예: <code>777</code> 또는 <code>-rwxrwxrwx</code>.</p> <p>이러한 권한은 패턴과 일치해야 합니다. <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>chmod에 대한 자세한 내용은 <a href="https://ss64.com/bash/chmod.html">chmod 설명서</a>를 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 버퍼 크기(B)]</p> </td> 
   <td> <p>파일을 업로드할 때 각 청크의 크기(바이트)를 설정합니다. 이 기능은 대용량 파일에 유용하며, 서버 메모리 제한에 더 작은 업로드가 필요한 경우에 유용합니다. 이 값을 설정하지 않으면 파일이 한 번의 작업으로 작성됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
