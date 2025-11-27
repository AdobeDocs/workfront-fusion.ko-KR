---
title: Adobe Experience Manager Assets 모듈
description: Adobe Workfront Fusion용 Adobe Experience Manager Assets 커넥터를 사용하면 에셋을 생성, 업로드 및 업데이트하고 폴더와 에셋을 복사하거나 이동할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: ht
source-wordcount: '3734'
ht-degree: 100%

---

# Adobe Experience Manager Assets 모듈

Adobe Workfront Fusion용 Adobe Experience Manager Assets 커넥터를 사용하면 에셋을 생성, 업로드 및 업데이트하고 폴더와 에셋을 복사하거나 이동할 수 있습니다.

Adobe Experience Manager Assets 커넥터에 대한 소개 비디오는 다음을 참조하십시오.

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

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
   <p>작업 기반: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

* 이 모듈을 사용하려면 Adobe Experience Manager Assets 계정이 있어야 합니다.
* Adobe Developer 콘솔에서 서버 간 흐름을 설정해야 합니다.

  Adobe Developer 콘솔에서 서버 간 흐름을 설정하는 방법에 대한 지침은 [서버측 API용 액세스 토큰 생성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=ko#the-server-to-server-flow)을 참조하십시오.
* Adobe Experience Manager 기술 계정에 쓰기 권한이 있어야 합니다.

  Adobe Experience Manager 기술 계정에 쓰기 권한을 추가하는 방법에 대한 지침은 Adobe Experience Manager 설명서의 [서비스 자격 증명](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)을 참조하십시오.

## Adobe Experience Manager Assets API 정보

Adobe Experience Manager Assets 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Adobe Experience Manager Assets을 Workfront Fusion에 연결 {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Adobe Experience Manager Assets 모듈에 대한 연결을 만들려면 다음 작업을 수행하십시오.

1. 연결 상자 옆에 있는 추가를 클릭합니다.

2. 생성할 연결 유형을 선택합니다.

   * **AEM Assets as a Cloud Service**

     이 구성에는 Adobe Admin Console의 정보가 필요합니다.

   * **AEM Assets 기본(Adobe Managed Services)**

     이 구성에는 사용자 이름과 암호가 필요합니다.

3. 생성할 연결 유형의 필드를 입력합니다.

   AEM Assets as a Cloud Service의 경우 [AEM Assets as a Cloud Service에 대한 연결 구성](#configure-the-connection-for-aem-assets-as-a-cloud-service)을 참조하십시오.

   AEM Assets 기본(Adobe Managed Services)의 경우, [AEM Assets 기본에 대한 연결 구성](#configure-the-connection-for-aemassets-basic-adobe-managed-services)을 참조하십시오.

4. 연결을 저장하고 모듈로 돌아가려면 **계속**&#x200B;을 클릭합니다.


### AEM Assets as a Cloud Service에 대한 연결 구성

>[!NOTE]
>
>* 이 필드에 대한 정보는 Adobe Developer Console에서 서버 간 흐름을 설정하는 과정에서 생성됩니다. 이 값들은 해당 설정의 일부로 생성된 서비스 자격 증명 JSON 파일에서 찾을 수 있습니다.
>
>   Adobe Developer Console에서 서버 간 흐름을 설정하는 방법에 대한 지침은 [서버측 API용 액세스 토큰 생성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=ko#the-server-to-server-flow)을 참조하십시오.
>
>* Adobe Experience Manager 기술 계정에 쓰기 권한이 있어야 합니다.
>
>   Adobe Experience Manager 기술 계정에 쓰기 권한을 추가하는 방법에 대한 지침은 Adobe Experience Manager 설명서의 [서비스 자격 증명](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)을 참조하십시오.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">연결 이름</td>
                  <td>
                      <p>이 연결의 이름을 입력합니다.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">뒤쪽 슬래시가 없는 인스턴스 URL</td>
                  <td>Adobe Experience Manager 인스턴스의 URL을 입력합니다. URL 끝에 슬래시 <code>/</code>를 포함하지 마십시오.</td>
              </tr>
              <tr>
                  <td role="rowheader">계정 세부 정보 채우기 옵션</td>
                  <td>계정 세부 정보를 설명하는 JSON을 제공할지, 아니면 수동으로 세부 정보를 입력할지 선택합니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">JSON 형식의 기술 계정 세부 정보</td>
                  <td>JSON을 제공하는 경우 계정 세부 정보를 설명하는 JSON을 입력하거나 붙여넣습니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">클라이언트 ID</td>
                  <td>세부 정보를 수동으로 입력하는 경우, 서버 간 설정에서 생성된 클라이언트 ID를 입력합니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">클라이언트 암호</td>
                  <td>세부 정보를 수동으로 입력하는 경우, 서버 간 설정에서 생성된 클라이언트 암호를 입력합니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">기술 계정 ID</td>
                  <td>세부 정보를 수동으로 입력하는 경우 기술 계정의 ID를 입력합니다. 클라이언트 자격 증명 JSON 파일의 “id” 필드입니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">조직 ID</td>
                  <td class="">세부 정보를 수동으로 입력하는 경우 조직의 ID를 입력합니다. 클라이언트 자격 증명 JSON 파일의 “org” 필드입니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">Meta 범위</td>
                  <td>서버 간 설정에서 생성된 Meta 범위를 입력합니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">비공개 키</td>
                  <td>서버 간 설정에서 생성된 비공개 키를 입력합니다. 비공개 키를 추출하려면 추출을 클릭한 다음 추출할 파일과 파일의 암호를 입력합니다.</td>
              </tr>
              <tr>
                  <td role="rowheader">인증 URL</td>
                  <td>이 계정에 대한 인증 URL을 입력합니다.</td>
              </tr>
          </tbody>
      </table>


### AEM Assets 기본(Adobe Managed Services)에 대한 연결 구성

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">연결 이름</td>
                <td>
                    <p>이 연결의 이름을 입력합니다.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">뒤쪽 슬래시가 없는 인스턴스 URL</td>
                <td>Adobe Experience Manager 인스턴스의 URL을 입력합니다. URL 끝에 슬래시 <code>/</code>를 포함하지 마십시오.</td>
            </tr>
            <tr>
                <td role="rowheader">사용자 이름</td>
                <td>이 연결이 사용하는 AEM Assets 계정의 사용자 이름을 입력합니다.</td>
            </tr>
            <tr>
                <td role="rowheader">암호</td>
                <td>이 연결이 사용하는 AEM Assets 계정의 암호를 입력합니다.</td>
            </tr>
        </tbody>
    </table>


## Adobe Experience Manager Assets 모듈 및 해당 필드

Adobe Experience Manager Assets 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이러한 필드와 함께 앱 또는 서비스의 액세스 수준과 같은 요인에 따라 Adobe Experience Manager Assets 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [파일 작업](#files-operations)
* [기타](#other)
* [에셋(Author API)](#assets-author-api)
* [이벤트(Author API)](#events-author-api)
* [메타데이터(Author API)](#metadata-author-api)
* [가져오기(Author API)](#import-author-api)
* [관계(Author API)](#relations-author-api)
* [폴더(Folders API)](#folders-folders-api)

### 파일 작업

* [업로드 완료](#complete-upload)
* [미리 서명된 스토리지 가져오기](#get-presigned-storage)
* [업로드 시작](#initiate-upload)
* [에셋 업로드](#upload-an-asset)

#### 업로드 완료

이 액션 모듈은 파일의 모든 부분이 업로드된 후에 시작된 업로드를 완료합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">파일 이름</td> 
   <td> <p>업로드한 파일의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">토큰 업로드</td> 
   <td>초기화에 제공된 대로 바이너리의 업로드 토큰을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">MIME 유형</td> 
   <td>완료된 파일에 대한 MIME 유형을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URI 완료</td> 
   <td>파일의 전체 URI를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>


#### 미리 서명된 스토리지 가져오기

이 액션 모듈은 직접 자격 증명 없이 AEM에서 파일을 안전하게 업로드하거나 다운로드할 수 있도록 임시로 미리 서명된 URL을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">조회 유형</td> 
   <td> <p>에셋을 경로별로 조회할지, ID별로 조회할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋</td> 
   <td>에셋에 대한 경로를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>에셋에 대한 UDID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 업로드 시작

이 액션 모듈은 업로드를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">대상</td> 
   <td> <p>파일을 업로드할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">파일 이름</td> 
   <td> <p>업로드한 파일의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">최대 파일 크기</td> 
   <td>업로드한 파일의 크기를 바이트 단위로 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>


#### 에셋 업로드

이 액션 모듈은 Adobe Experience Manager Assets 계정에 에셋을 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">대상</td> 
   <td> <p>에셋을 업로드할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">소스 파일</td> 
   <td>소스 파일의 이름과 데이터를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 기타


* [폴더 또는 에셋 복사](#copy-a-folder-or-asset)
* [레코드 만들기](#create-a-record)
* [폴더, 에셋 또는 렌디션 삭제](#delete-a-folder-asset-or-rendition)
* [폴더 목록 가져오기](#get-a-folder-listing)
* [사용자 정의 API 호출하기](#make-a-custom-api-call)
* [폴더 또는 에셋 이동](#move-a-folder-or-asset)
* [레코드 업데이트](#update-a-record)



#### 폴더 또는 에셋 복사

이 액션 모듈은 폴더 또는 에셋을 Adobe Experience Manager Assets 계정의 다른 위치로 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>폴더를 복사할지 에셋을 복사할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">폴더 / 에셋</td> 
   <td>복사할 폴더 또는 에셋을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">대상 경로</td> 
   <td>새 폴더 또는 에셋의 위치로 경로를 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">복사된 폴더 / 에셋 이름</td> 
   <td>새 폴더 또는 에셋의 이름을 입력합니다. Adobe Experience Manager Assets에 표시되는 폴더 이름은 원래 이름과 동일합니다. 여기에 입력된 이름은 새 폴더 또는 에셋의 URL에 나타납니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">하위 복사</td> 
   <td>폴더를 복사하는 경우, 이 옵션을 활성화하여 폴더 내의 하위 폴더나 에셋을 복사할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">덮어쓰기</td> 
   <td>이 옵션을 활성화하면 복사 중인 폴더나 에셋과 이름이 같은 대상 위치의 폴더나 에셋을 덮어쓰게 됩니다.</td> 
  </tr> 
 </tbody> 
</table>



#### 레코드 만들기

이 액션 모듈은 폴더 또는 에셋 댓글을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">오브젝트 유형</td> 
   <td> <p>폴더를 만들 것인지, 에셋에 대한 댓글을 만들 것인지 선택합니다.</p> 
    <ul> 
     <li> <p>폴더</p> <p>다음 필드를 채웁니다.</p> 
      <ul> 
       <li> <p>이름</p> <p>폴더의 이름을 입력합니다. 이 이름은 파일 경로에 표시되므로 공백이나 다른 문자를 포함해서는 안 됩니다. </p> </li> 
       <li> <p>제목</p> <p>폴더의 제목을 입력하면 이름 대신 표시할 수 있습니다.</p> </li> 
      </ul> </li> 
     <li> <p>에셋 댓글</p> <p>다음 필드를 채웁니다.</p> 
      <ul> 
       <li> <p>에셋 선택</p> <p>댓글을 추가할 에셋의 ID를 선택하거나 매핑합니다.</p> </li> 
       <li> <p>댓글</p> <p>댓글의 텍스트를 입력합니다.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 폴더, 에셋 또는 렌디션 삭제

이 액션 모듈은 폴더, 에셋 또는 렌디션을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>폴더, 에셋 또는 렌디션을 삭제할 것인지 선택합니다.</p> 
    <ul> 
     <li> <p>폴더</p> <p>경로에 있는 폴더를 선택하여 삭제할 폴더를 선택합니다.</p> </li> 
     <li> <p>에셋</p> <p>경로에 있는 폴더를 선택한 다음 삭제할 에셋을 선택합니다.</p> </li> 
     <li> <p>렌디션</p> <p>경로에 있는 폴더를 선택하여 렌디션을 선택합니다.</p> <p>렌디션의 이름을 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 폴더 목록 가져오기

이 액션 모듈은 기존 폴더와 하위 엔티티(폴더 또는 에셋)의 표시를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">폴더</td> 
   <td>가져오려는 폴더를 선택하거나 매핑합니다. 경로에 하위 폴더를 추가하려면 더하기 아이콘을 클릭하고 하위 폴더를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 정의 API 호출하기

이 액션 모듈은 Adobe Experience Manager Assets API에 사용자 정의 API 호출을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>Adobe Experience Manager 기본 URL과 관련된 경로를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>메서드</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">헤더</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">쿼리 문자열</td> 
   <td> <p>요청 쿼리 문자열을 입력합니다. 각 키/값 쌍에 대해 <b>항목 추가</b>를 클릭하고 키와 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">본문</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 폴더 또는 에셋 이동

이 액션 모듈은 지정된 경로에 있는 에셋이나 폴더를 새로운 위치로 이동합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>폴더를 이동할지 에셋을 이동할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">폴더 / 에셋</td> 
   <td>이동할 폴더 또는 에셋을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">대상 경로</td> 
   <td>폴더나 에셋을 이동할 위치로 경로를 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이동한 폴더/에셋 이름</td> 
   <td>이동한 폴더 또는 에셋의 새로운 이름을 입력합니다. Adobe Experience Manager Assets에 표시되는 폴더 이름은 원래 이름과 동일합니다. 여기에 입력된 이름은 이동한 폴더 또는 에셋의 URL에 나타납니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">덮어쓰기</td> 
   <td>이 옵션을 활성화하면 이동 중인 폴더 또는 에셋과 이름이 같은 대상 위치의 폴더나 에셋을 덮어쓰게 됩니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 업데이트

이 액션 모듈은 기존 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> <p>에셋 메타데이터를 삭제할지 에셋 렌디션을 삭제할지 선택합니다.</p> 
    <ul> 
     <li> <p>에셋 메타데이터</p> 
      <ul> 
       <li> <p>메타데이터를 업데이트할 에셋을 선택합니다.</p> </li> 
       <li> <p>에셋의 새 제목을 입력합니다.</p> </li> 
      </ul> </li> 
     <li> <p>에셋 렌디션</p> 
      <ul> 
       <li> <p>렌디션을 업데이트할 에셋을 선택합니다.</p> </li> 
       <li> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### 에셋(Author API)

* [에셋 삭제](#delete-asset)
* [작업 상태 가져오기](#get-job-status)

#### 에셋 삭제

이 액션 모듈은 ID에 따라 단일 에셋을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 ID</td> 
   <td> <p>삭제할 에셋의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">강제</td> 
   <td>이 옵션을 활성화하면 참조된 에셋도 삭제하도록 강제할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 작업 상태 가져오기

이 액션 모듈은 비동기 작업의 현재 상태를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">작업 ID</td> 
   <td> <p>상태를 가져오려는 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 이벤트(Author API)

#### 이벤트 보기

이 트리거 모듈은 AEM Assets에서 이벤트가 발생할 때 시나리오를 시작합니다.

모듈에는 단일 필드: 웹후크가 포함되어 있습니다. 이 이벤트에 사용할 기존 웹후크를 선택하거나 새 웹후크를 만듭니다.

새 웹후크를 생성하는 방법:

1. 웹후크 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">웹후크 이름</td>
        <td>이 웹후크의 이름을 입력합니다.</td>
       </tr>
       <tr>
         <td role="rowheader">연결</td>
        <td>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</td>
       </tr>
     </tbody>
   </table>

1. 저장을 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다.


### 메타데이터(Author API)

* [에셋 메타데이터 가져오기](#get-asset-metadata)
* [에셋 메타데이터 업데이트](#update-asset-metadata)

#### 에셋 메타데이터 가져오기

이 액션 모듈은 지정된 에셋에 대한 메타데이터를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 ID</td> 
   <td> <p>메타데이터를 가져올 에셋의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 에셋 메타데이터 업데이트

이 액션 모듈은 지정된 에셋에 대한 메타데이터를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 ID</td> 
   <td> <p>메타데이터를 업데이트할 에셋의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">업데이트</td> 
   <td> <p>업데이트할 각 메타데이터 항목에 대해 <b>항목 추가</b>를 클릭하고 작업을 선택합니다. 항목 추가 상자의 다른 필드는 선택한 작업에 따라 달라집니다.</p> </td> 
  </tr> 
 </tbody> 
</table>


### 가져오기(Author API)

* [가져오기 작업 결과 가져오기](#get-import-job-results)
* [가져오기 작업 상태 가져오기](#get-import-job-status)
* [URL에서 에셋 업로드](#upload-an-asset-from-a-url)

#### 가져오기 작업 결과 가져오기

이 액션 모듈은 지정된 가져오기 작업에 대한 결과를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">가져오기 작업 ID</td> 
   <td> <p>결과를 가져오려는 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 가져오기 작업 상태 가져오기

이 액션 모듈은 지정된 가져오기 작업의 상태를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">가져오기 작업 ID</td> 
   <td> <p>상태를 가져오려는 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### URL에서 에셋 업로드

이 액션 모듈은 지정된 URL에서 파일을 가져와 새 에셋을 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제목</td> 
   <td> <p>에셋의 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">설명</td> 
   <td> <p>에셋에 대한 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제목</td> 
   <td> <p>에셋의 제목을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">작성자</td> 
   <td> <p>에셋 작성자를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">만료 날짜</td> 
   <td> <p>에셋의 만료 날짜를 입력하거나 매핑합니다.</p><p>지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">유형 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">사용자 정의 메타데이터</td> 
   <td> <p>에셋에 추가할 각 사용자 정의 메타데이터 항목에 대해 <b>항목 추가</b>를 클릭하고 메타데이터의 이름과 값을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">폴더 경로 또는 ID</td> 
   <td> <p>대상 폴더를 경로 또는 ID로 지정할지 선택한 다음 경로를 선택하거나 ID를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">가져올 파일</td> 
   <td> <p>가져올 각 파일에 대해 <b>추가 항목&lt;/&gt;을 클릭하고 파일의 세부 정보를 입력합니다. <code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### 관계(Author API)

* [에셋 관계 만들기](#create-asset-relations)
* [에셋 관계 삭제](#create-asset-relations)
* [에셋 관계 유형 가져오기](#get-asset-relation-types)
* [에셋 관계 가져오기](#get-asset-relations)

#### 에셋 관계 만들기

이 액션 모듈은 선택한 에셋에 대한 새로운 에셋 관계를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 ID</td> 
   <td> <p>다른 에셋과 연관시킬 ID 에셋을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">관련 에셋</td> 
   <td> <p>선택한 에셋과 관련된 각 에셋에 대해 <b>항목 추가</b>를 클릭하고 해당 에셋의 ID와 관계 유형을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 에셋 관계 삭제

이 액션 모듈은 에셋에 대한 에셋 관계를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 ID</td> 
   <td> <p>관계를 삭제할 ID 에셋을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">관련 에셋</td> 
   <td> <p>삭제할 관계 유형을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">삭제할 관련 에셋의 특정 ID를 입력합니다.</td> 
   <td> <p>특정 관계를 삭제하려면 이 상자를 선택합니다. 이 상자를 선택하지 않으면 선택한 유형의 모든 관계가 삭제됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">관련 에셋 ID</td> 
   <td> <p>특정 관계를 삭제하는 경우 삭제할 관계의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### 에셋 관계 유형 가져오기

이 모듈은 지정된 에셋에 대해 존재하는 에셋 관계 유형을 나열합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 ID</td> 
   <td> <p>관계 유형을 나열할 ID 에셋을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 에셋 관계 가져오기

이 모듈은 지정된 에셋에 대한 에셋 관계를 나열합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">에셋 ID</td> 
   <td> <p>관계를 나열할 ID 에셋을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">관계 유형</td> 
   <td> <p>관계를 나열할 관계 유형의 쉼표로 구분된 목록을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>



### 폴더(Folders API)

* [폴더 만들기](#create-folders)
* [ID로 폴더 삭제](#delete-a-folder-by-id)
* [경로별 폴더 삭제](#delete-folders-by-path)
* [폴더 작업 결과 가져오기](#get-folders-job-results)
* [폴더 작업 상태 가져오기](#get-folders-job-status)
* [목록 폴더](#list-folders)

#### 폴더 만들기

이 액션 모듈은 Adobe Experience Manager Assets에 새 폴더를 만듭니다.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">만들려는 폴더</td> 
   <td> <p>만들려는 각 폴더에 대해 <b>항목 추가</b>를 클릭하고 다음 정보를 입력합니다.</p>
   <ul>
   <li><b>새 폴더 위치</b><p>새 폴더를 만들 위치의 경로를 선택합니다.</p></li>
       <li> <b>이름</b> <p>폴더의 이름을 입력합니다. 이 이름은 파일 경로에 표시되므로 공백이나 다른 문자를 포함해서는 안 됩니다. </p> </li> 
       <li> <b>제목</b> <p>폴더의 제목을 입력하면 이름 대신 표시할 수 있습니다.</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### ID로 폴더 삭제

이 액션 모듈은 특정 ID로 Adobe Experience Manager Assets 폴더를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">폴더 ID</td> 
   <td> 삭제할 폴더의 ID를 입력하거나 매핑합니다.</td>
  </tr> 
 <tr> 
   <td role="rowheader">하위 폴더 삭제</td> 
   <td> 폴더 및 모든 하위 폴더를 삭제하려면 이 옵션을 활성화합니다.</td>
  </tr> 
 <tr> 
   <td role="rowheader">강제</td> 
   <td> 이 옵션을 활성화하면 참조된 폴더도 삭제하도록 강제할 수 있습니다.</td>
  </tr> 
 </tbody> 
</table>

#### 경로별 폴더 삭제

이 액션 모듈은 특정 경로의 Adobe Experience Manager Assets 폴더를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">폴더 경로</td> 
   <td>삭제할 각 폴더에 대해 <b>항목 추가</b>를 클릭하고 폴더의 경로를 선택합니다.</td>
  </tr> 
 <tr> 
   <td role="rowheader">하위 폴더 삭제</td> 
   <td> 폴더 및 모든 하위 폴더를 삭제하려면 이 옵션을 활성화합니다.</td>
  </tr> 
 <tr> 
   <td role="rowheader">강제</td> 
   <td> 이 옵션을 활성화하면 참조된 에셋도 삭제하도록 강제할 수 있습니다.</td>
  </tr> 
 </tbody> 
</table>

#### 폴더 작업 결과 가져오기

이 모듈은 Adobe Experience Manager Assets 폴더 API에서 생성된 비동기 작업의 결과를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">작업 ID</td> 
   <td> 결과를 가져오려는 작업의 ID를 입력하거나 매핑합니다.</td>
  </tr> 
 </tbody> 
</table>

#### 폴더 작업 상태 가져오기

이 모듈은 Adobe Experience Manager Assets 폴더 API에서 생성된 비동기 작업의 상태를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">작업 ID</td> 
   <td> 상태를 가져오려는 작업의 ID를 입력하거나 매핑합니다.</td>
  </tr> 
 </tbody> 
</table>


#### 목록 폴더

이 모듈은 특정 폴더의 하위 폴더를 나열합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Adobe Experience Manager Assets 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서에서 <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Adobe Experience Manager Assets을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">폴더 경로 또는 ID</td> 
   <td> <p>대상 폴더를 경로 또는 ID로 지정할지 선택한 다음 경로를 선택하거나 ID를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->

