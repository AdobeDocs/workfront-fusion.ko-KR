---
title: Adobe Authenticator 모듈
description: Adobe Authenticator 모듈을 사용하면 단일 연결을 사용하여 API를 통해 모든 Adobe 제품에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 983ce043afbcc44ee8af2dfcd46738f170a2b257
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 1%

---

# Adobe Authenticator 모듈

Adobe Authenticator 모듈을 사용하면 단일 연결을 사용하여 모든 Adobe API에 연결할 수 있습니다. 이렇게 하면 아직 전용 Fusion 커넥터가 없는 Adobe 제품에 보다 쉽게 연결할 수 있습니다.

HTTP 모듈에 대한 이점은 전용 앱에서와 같이 연결을 만들 수 있다는 것입니다.

사용 가능한 Adobe API 목록을 보려면 [Adobe API](https://developer.adobe.com/apis)를 참조하십시오. 할당된 API만 사용할 수 있습니다.

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

* 모듈을 연결할 Adobe 제품에 대한 액세스 권한이 있어야 합니다.
* Adobe Developer Console에 대한 액세스 권한이 있어야 합니다.
* 모듈을 연결할 API가 포함된 프로젝트가 Adobe Developer Console에 있어야 합니다. 다음을 수행할 수 있습니다.

   * API를 사용하여 새 프로젝트를 만듭니다.

     또는
   * 기존 프로젝트에 API를 추가합니다.

  Adobe Developer Console에서 API를 만들거나 프로젝트에 추가하는 방법에 대한 자세한 내용은 Adobe 설명서에서 [프로젝트 만들기](https://developer.adobe.com/dep/guides/dev-console/create-project/)를 참조하십시오.

## Adobe Authenticator API 정보

Adobe Authenticator 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## 연결 만들기

Adobe Authenticator 연결은 Adobe Developer Console의 단일 프로젝트에 연결됩니다. 두 개 이상의 Adobe API에 대해 동일한 연결을 사용하려면 동일한 프로젝트에 API를 추가하고 해당 프로젝트에 대한 연결을 만듭니다.

별도의 프로젝트에 대해 별도의 연결을 만들 수 있지만 연결을 사용하여 해당 연결에 지정된 프로젝트에 없는 API에 액세스할 수는 없습니다.

>[!IMPORTANT]
>
>Adobe Authenticator 커넥터를 사용하면 OAuth 서버 간 연결과 서비스 계정(JWT) 연결 중 하나를 선택할 수 있습니다. Adobe에는 더 이상 사용되지 않는 JWT 자격 증명이 있으며, 2025년 1월 1일 이후부터 작동하지 않습니다. **따라서 OAuth 연결을 만드는 것이 좋습니다.**
>
>이러한 연결 유형에 대한 자세한 내용은 Adobe 설명서에서 [서버 간 인증](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/)을 참조하십시오

연결을 만들려면 다음 작업을 수행하십시오.

1. 모든 Adobe Authenticator 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 유형]</td>
        <td>
          <p>OAuth 서버 간 연결을 만들지 서비스 계정(JWT) 연결을 만들지 선택합니다. OAuth 연결을 만드는 것이 좋습니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>[!DNL Adobe] 클라이언트 ID를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>[!DNL Adobe] 클라이언트 암호를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 범위]</td>
        <td>OAuth 연결을 선택한 경우 이 연결에 필요한 범위를 입력하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 기술 계정 ID]</td>
        <td>JWT 연결을 선택한 경우 [!DNL Adobe] 기술 계정 ID를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 조직 ID]</td>
        <td>JWT 연결을 선택한 경우 [!DNL Adobe] 조직 ID를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 메타 범위]</td>
        <td>JWT 연결을 선택한 경우 이 연결에 필요한 메타 범위를 입력합니다. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 개인 키]</td>
        <td>
          <p>JWT 연결을 선택한 경우 [!DNL Adobe Developer Console]에서 자격 증명을 만들 때 생성된 개인 키를 입력하십시오. </p>
          <p>개인 키 또는 인증서를 추출하려면 다음을 수행하십시오.</p>
          <ol>
            <li value="1">
              <p><b>[!UICONTROL Extract]</b>을(를) 클릭합니다.</p>
            </li>
            <li value="2">
              <p>추출 중인 파일 유형을 선택합니다.</p>
            </li>
            <li value="3">
              <p>개인 키 또는 인증서가 포함된 파일을 선택합니다.</p>
            </li>
            <li value="4">
              <p>파일의 암호를 입력합니다.</p>
            </li>
            <li value="5">
              <p><b>[!UICONTROL 저장]</b>을(를) 클릭하여 파일을 추출하고 연결 설정으로 돌아갑니다.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 기본 URL]</td>
        <td>이 인증자가 허용할 기본 URL을 추가해야 합니다. 시나리오의 뒷부분에서 사용자 지정 API 호출 만들기 모듈을 사용할 때 선택한 URL에 대한 상대 경로를 추가합니다. 여기에 URL을 입력하면 사용자 정의 API 호출 만들기 모듈이 연결할 수 있는 내용을 제어할 수 있으므로 보안이 강화됩니다.<p>인증자에 추가하려는 각 기본 URL에 대해 <b>항목 추가</b>를 클릭하고 기본 URL을 입력하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인증 URL]</td>
        <td><code>https://ims-na1.adobelogin.com</code>의 표준 Adobe IMS 인증 URL을 사용하려면 비워 두십시오. 인증에 Adobe IMS를 사용하지 않는 경우 인증에 사용할 URL을 입력합니다.</td>
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## 모듈

* [사용자 지정 API 호출 만들기](#make-a-custom-api-call)
* [사용자 지정 API 호출 만들기(이전)](#make-a-custom-api-call-legacy)

### 사용자 지정 API 호출 만들기

이 작업 모듈에서는 모든 Adobe API를 호출할 수 있습니다. 텍스트 전용 본문 대신 큰 파일을 지원합니다.

이 모듈은 2024년 11월 14일에 출시되었습니다. 이 날짜 이전에 구성된 모든 Adobe Authenticator > 사용자 지정 API 호출 만들기 는 큰 파일을 처리하지 않으며 이제 사용자 지정 API 호출 만들기(기존) 모듈로 간주됩니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Adobe Authenticator 모듈에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection" class="MCXref xref" >연결 만들기</a>를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 기본 URL]</p>
      </td>
      <td>
        <p>연결할 API 지점의 기본 URL을 입력합니다.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>기본 URL에 상대적인 경로를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 인증 헤더를 자동으로 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body Type]</td>
   <td> 이 API 요청에 대한 본문 유형을 선택합니다.
   <ul>
   <li>Raw</li>
   <li>application/x-www-form-urlencoded</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
      </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력 유형]  </td>
      <td>
        <p>모듈에서 출력할 데이터 유형을 선택합니다. 유형을 선택하지 않으면 모듈에서 자동으로 유형을 선택합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

### 사용자 지정 API 호출 만들기(이전)

이 작업 모듈에서는 모든 Adobe API를 호출할 수 있습니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Adobe Authenticator 모듈에 대한 연결 만들기에 대한 지침은 이 문서의 <a href="#create-a-connection" class="MCXref xref" >연결 만들기</a>를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 기본 URL]</p>
      </td>
      <td>
        <p>연결할 API 지점의 기본 URL을 입력합니다.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>기본 URL에 상대적인 경로를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 인증 헤더를 자동으로 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
