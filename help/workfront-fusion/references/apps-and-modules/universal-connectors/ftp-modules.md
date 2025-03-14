---
title: FTP 모듈
description: FTP 모듈을 사용하면 선택한 폴더의 파일 변경 사항을 모니터링하고, 새 파일을 원하는 폴더에 업로드하고, 폴더에 이미 있는 기존 파일을 수정하거나 삭제할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 0%

---

# FTP 모듈

FTP 모듈을 사용하면 선택한 폴더의 파일 변경 사항을 모니터링하고, 새 파일을 원하는 폴더에 업로드하고, 폴더에 이미 있는 기존 파일을 수정하거나 삭제할 수 있습니다.

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

FTP 모듈을 사용하려면 FTP 서비스가 있는 계정이 있어야 합니다.

## FTP 모듈에서 연결 만들기 {#create-a-connection}

1. FTP 모듈에서 연결 상자 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 입력합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL 연결 이름]</td> 
      <td> <p> FTP 연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 환경]</p> </td> 
      <td> <p>프로덕션 환경을 사용하는지 아니면 비프로덕션 환경을 사용하는지 선택합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 유형]</p> </td> 
      <td> <p>서비스 계정을 사용하는지 개인 계정을 사용하는지 선택합니다.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 호스트] </td> 
      <td> <p>FTP 서버 호스트 이름을 입력합니다. 예: <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 포트] </td> 
      <td> <p>FTP 서버 포트 번호를 입력합니다. 예: <code>21</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 사용자 이름] </td> 
      <td> <p>FTP 계정 사용자 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Password] </td> 
      <td> <p>FTP 계정 암호를 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>TLS(보안 연결) 사용</p> </td> 
      <td> <p>보안 연결을 사용할지 여부를 선택합니다.</p> <ul><li><p><b>[!UICONTROL No]</b></p> <p>연결이 보호되지 않습니다.</p></li><li> <p><b>명시적 암호화</b> 또는 <b>암시적 암호화</b></p> <p>연결은 SSL을 사용하여 보호됩니다.</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[!UICONTROL 승인되지 않은 인증서 거부]</p> </td> 
   <td> <p>FTP 서버 인증서를 확인하려면 이 옵션을 활성화하십시오. 확인에 실패하면 연결이 만들어지지 않습니다. 인증을 통과하려면 인증서가 다음 기준 중 하나를 충족해야 합니다.</p> 
    <ul> 
     <li>루트 인증 기관에서 서명해야 합니다.</a></li> 
     <li>중간 인증 기관에서 서명합니다. 이 경우 모든 중간 인증서를 FTP 서버에 설치해야 합니다.</li> 
     <li>[!UICONTROL 자체 서명된 인증서] 필드에 제공된 자체 서명된 인증서여야 합니다(아래 참조)</li> </ul>
     <p>이 옵션이 비활성화되어 있으면 FTP 서버 인증서가 확인되지 않습니다. 연결을 안전하지 않게 만들고 심각한 보안 위험을 초래하므로 옵션을 비활성화하지 않는 것이 좋습니다.</p></td>
    </tr> 
    <tr> 
     <td> <p>[!UICONTROL 자체 서명된 인증서]</p> </td> 
     <td> <p>업로드 대화 상자를 열려면 <b>[!UICONTROL 추출]</b> 단추를 클릭하십시오.</p> <p>자체 서명된 인증서와 함께 TLS를 사용하려면 인증서를 업로드하십시오. [!DNL Workfront Fusion]은(는) 파일 및 암호와 같이 사용자가 제공한 데이터를 유지하거나 저장하지 않습니다. 파일 및 암호는 인증서를 추출하는 데만 사용됩니다.</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## FTP 모듈 및 해당 필드

* [트리거](#triggers)
* [액션](#actions)

### 트리거

#### [!UICONTROL 파일 보기]

[!UICONTROL 파일 보기]가 FTP용 유일한 트리거 모듈입니다. 선택한 폴더의 파일 컨텐츠를 모니터링합니다. 트리거는 새 파일이 지정된 폴더에 추가되면 실행됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>FTP 계정에 연결하는 방법에 대한 지침은 이 문서의 FTP 모듈</a>에서 <a href="#create-a-connection" class="MCXref xref">[!UICONTROL 연결 만들기]를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 폴더]</p> </td> 
   <td> <p>감시할 폴더를 선택합니다.</p> <p><b>참고:</b> 시나리오당 하나의 폴더만 허용됩니다. 하위 폴더는 무시됩니다.</p> <p><b>팁:</b> 여러 폴더를 보려면 각 폴더에 대해 별도의 시나리오를 만드십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 파일 수] </td> 
   <td> <p>한 주기 동안 모듈에서 작업할 최대 결과 수를 설정합니다. 값이 너무 높게 설정되면 FTP 서버 측에서 연결이 중단될 수 있습니다. [!DNL Workfront Fusion]은(는) 이 작업에 영향을 주지 않습니다. 낮은 값을 설정하고 최대 주기 횟수에 대해 높은 값을 정의하거나 시나리오를 더 자주 실행하는 것이 좋습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 권한 변경]](#change-permissions)
* [[!UICONTROL 폴더 만들기]](#create-a-folder)
* [[!UICONTROL 파일 삭제]](#delete-a-file)
* [[!UICONTROL 폴더 삭제]](#delete-a-folder)
* [[!UICONTROL 파일 가져오기]](#get-a-file)
* [[!UICONTROL 폴더에 있는 파일 목록]](#list-of-files-in-a-folder)
* [[!UICONTROL 파일 또는 폴더 이동]](#move-a-file-or-folder)
* [파일 [!UICONTROL 업로드]](#upload-a-file)

#### [!UICONTROL 권한 변경]

이 작업 모듈은 파일 또는 폴더의 권한 설정을 변경합니다.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>FTP 계정에 연결하는 방법에 대한 지침은 이 문서의 FTP 모듈</a>에서 <a href="#Create" class="MCXref xref" >[!UICONTROL 연결 만들기]를 참조하십시오.</td>
         </tr>
         <tr>
            <td>[!UICONTROL 의 권한 설정 변경]</td>
            <td>
               <p>파일 또는 폴더의 설정을 변경할지 여부를 선택합니다.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL 파일 경로]</td>
            <td>폴더 또는 파일에 파일 경로를 입력하거나 매핑합니다.</td>
         </tr>
         <tr>
            <td>[!UICONTROL 권한]</td>
            <td>
               <p>원하는 파일 또는 폴더 권한을 설정합니다. chmod 매개 변수를 사용합니다. 예: <code>777 </code> 또는 <code>-rwxrwxrwx</code>.</p>
               <p>사용 권한은 <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code> 패턴과 일치해야 합니다.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL 폴더 만들기]

이 작업 모듈은 새 폴더를 만듭니다.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>FTP 계정에 연결하는 방법에 대한 지침은 이 문서의 FTP 모듈</a>에서 <a href="#Create" class="MCXref xref" >[!UICONTROL 연결 만들기]를 참조하십시오.</td>
         </tr>
         <tr>
            <td>[!UICONTROL 폴더 경로]</td>
            <td>파일 경로를 입력하거나 새 폴더에 매핑합니다.</td>
         </tr>
         <tr>
            <td>[!UICONTROL 새 폴더 이름]</td>
            <td>
               <p>새 폴더의 이름을 입력하거나 매핑합니다.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL 파일 삭제]

이 작업 모듈은 지정된 폴더에서 파일을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td>FTP 계정에 연결하는 방법에 대한 지침은 이 문서의 FTP 모듈</a>에서 <a href="#Create" class="MCXref xref" >[!UICONTROL 연결 만들기]를 참조하십시오.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>파일을 삭제할 FTP 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 이름]</td> 
   <td> <p> 파일 이름 확장자를 포함하여 파일 이름을 입력합니다. 예: <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더 삭제]

이 작업 모듈은 지정된 폴더를 영구적으로 삭제합니다.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>FTP 계정에 연결하는 방법에 대한 지침은 이 문서의 FTP 모듈</a>에서 <a href="#Create" class="MCXref xref" >[!UICONTROL 연결 만들기]를 참조하십시오.</td>
         </tr>
         <tr>
            <td>[!UICONTROL 폴더]</td>
            <td>
               <p>파일을 삭제할 FTP 폴더를 선택합니다.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL 파일 가져오기]

이 작업 모듈은 FTP 서버에서 파일을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>FTP 계정에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#creating-the-ftp-connection" class="MCXref xref">FTP 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 파일 경로]</td> 
   <td> <p> 가져올 파일의 경로를 입력하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더에 있는 파일 목록]

이 작업 모듈은 파일 및/또는 폴더 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>FTP 계정에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#creating-the-ftp-connection" class="MCXref xref">FTP 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>검색할 FTP 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 표시] </td> 
   <td> <p>파일 또는 폴더에 대한 정보를 검색할지 또는 둘 다에 대한 정보를 검색할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>검색어를 입력합니다. 검색어를 입력하지 않으면 지정된 폴더의 모든 파일 또는 폴더가 검색됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 반환되는 최대 파일 수]</td> 
   <td> <p>한 주기 동안 모듈이 작동하도록 할 최대 결과 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 또는 폴더 이동]

이 작업 모듈은 파일 또는 폴더를 다른 위치로 이동합니다.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>FTP 계정에 연결하는 방법에 대한 지침은 이 문서의 FTP 모듈</a>에서 <a href="#Create" class="MCXref xref" >[!UICONTROL 연결 만들기]를 참조하십시오.</td>
         </tr>
         <tr>
            <td>[!UICONTROL 이전 파일 경로]</td>
            <td>
               <p>파일을 이동할 경로를 입력합니다. 예: <code>/folder1/document.txt</code></p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL 새 파일 경로]</td>
            <td>
               <p>파일을 이동할 경로를 입력합니다. 예: <code>/folder2/document.txt</code></p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL 파일 업로드]

FTP 서버에 파일을 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>FTP 계정에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#creating-the-ftp-connection" class="MCXref xref">FTP 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더] </td> 
   <td> <p>파일을 업로드할 FTP 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source 파일] </td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 기존 파일에 추가]</td> 
   <td> <p>이 옵션을 활성화하고 파일이 FTP 서버에 이미 있으면 파일의 내용이 기존 파일에 추가됩니다. 이 옵션을 활성화하지 않으면 파일의 내용을 덮어씁니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 존재하지 않는 경우 폴더 만들기] </td> 
   <td> <p>이 옵션을 활성화하고 폴더 필드에 입력한 폴더가 FTP 서버에 없는 경우 모듈이 폴더를 만듭니다</p> </td> 
  </tr> 
 </tbody> 
</table>

## 문제 해결 {#troubleshooting}

연결 생성 중이나 모듈 작업 중에 FTP 앱에 문제가 발생하는 경우 자주 사용하는 FTP 클라이언트 중 하나를 사용하고 동일한 작업(예: 연결을 만들거나 폴더에 파일을 나열)을 수행해 보십시오. FTP 클라이언트 사용. FTP 클라이언트에서도 동일한 문제가 발생하는 경우 FTP 서버의 구성이 잘못되었을 수 있습니다.
