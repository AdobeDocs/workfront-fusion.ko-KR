---
title: SharePoint 모듈
description: Adobe Workfront Fusion 시나리오에서는 Microsoft SharePoint Online을 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 2493ce7ccca599e30b44b62558573ce2a55b03e0
workflow-type: tm+mt
source-wordcount: '4276'
ht-degree: 13%

---

# Microsoft SharePoint Online 모듈

Adobe Workfront Fusion 시나리오에서는 Microsoft SharePoint Online을 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

시나리오 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 색인](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

Microsoft SharePoint Online 모듈을 사용하려면 Microsoft SharePoint Online 계정이 있어야 합니다.

## SharePoint API 정보

SharePoint 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## Microsoft SharePoint Online을 Workfront Fusion에 연결 {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [&#x200B; [!DNL Microsoft] 계정을 사용하여 Microsoft SharePoint Online을 Workfront Fusion에 연결](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [고급 설정을 사용하여 Microsoft SharePoint Online을 Workfront Fusion에 연결](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)
* [인증서 인증을 사용하여 Microsoft SharePoint Online을 Workfront Fusion에 연결](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-certificate-authorization)

### [!DNL Microsoft] 계정을 사용하여 Microsoft SharePoint Online을 Workfront Fusion에 연결

[!DNL Microsoft] 계정을 사용하여 Microsoft SharePoint Online에 연결할 수 있습니다. [!DNL Sharepoint] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 [Adobe Workfront Fusion 연결 만들기 - 기본 지침](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)을 참조하십시오.

### 고급 설정을 사용하여 Microsoft SharePoint Online을 Workfront Fusion에 연결

연결에 자격 증명을 포함하려면 고급 설정 표시 옵션을 활성화합니다. 이 유형의 연결에는 클라이언트 ID, 클라이언트 암호 및 테넌트 ID가 필요합니다.

1. 모든 SharePoint 모듈에서 연결 필드 옆의 **[!UICONTROL 추가]**&#x200B;를 클릭하여 **[!UICONTROL 연결 만들기]** 상자를 엽니다.
1. **[!UICONTROL 고급 설정 표시]**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 유형]</p> </td> 
      <td>클라이언트 자격 증명을 사용하려면 <b>Microsoft 365 전자 메일</b>을(를) 선택하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 이름]</p> </td> 
      <td>연결의 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 클라이언트 ID]</p> </td> 
      <td>연결 중인 SharePoint 앱의 클라이언트 ID를 입력합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 클라이언트 암호]</p> </td> 
      <td>연결 중인 SharePoint 앱의 클라이언트 암호를 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 테넌트 ID]</p> </td> 
      <td>연결 중인 SharePoint 앱의 테넌트 ID를 입력합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 저장하고 모듈로 돌아가려면 **계속**&#x200B;을 클릭합니다.

### 인증서 인증을 사용하여 Microsoft SharePoint Online을 Workfront Fusion에 연결

인증서 인증을 사용하여 SharePoint에 연결할 수 있습니다.

>[!IMPORTANT]
>
>인증서 인증을 사용하려면 먼저 Microsoft Entra에서 앱을 만들고 인증서를 업로드해야 합니다.
>
>자세한 내용은 Microsoft 설명서의 [Microsoft Entra 인증서 기반 인증을 위한 인증 기관을 구성하는 방법](https://learn.microsoft.com/en-us/entra/identity/authentication/how-to-configure-certificate-authorities)을 참조하십시오.

1. 모든 SharePoint 모듈에서 연결 필드 옆의 **[!UICONTROL 추가]**&#x200B;를 클릭하여 **[!UICONTROL 연결 만들기]** 상자를 엽니다.
1. **[!UICONTROL 고급 설정 표시]**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 유형]</p> </td> 
      <td>인증서 인증을 사용하려면 <b>Microsoft SharePoint Online(인증서 인증)</b>을(를) 선택하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 이름]</p> </td> 
      <td>연결의 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 클라이언트 ID]</p> </td> 
      <td>연결 중인 SharePoint 앱의 클라이언트 ID를 입력합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Thumbprint]</p> </td> 
      <td>연결 중인 SharePoint 앱의 지문을 입력합니다.</td> 
     </tr> 
      <tr>
        <td role="rowheader">[!UICONTROL 비공개 키]</td>
        <td>
          <p>Microsoft에서 자격 증명을 만들 때 생성된 인증서 또는 개인 키를 입력합니다. </p>
          <p>비공개 키 또는 인증서를 추출하려면 다음을 수행합니다.</p>
          <ol>
            <li>
              <p><b>[!UICONTROL 추출]</b>을 클릭합니다.</p>
            </li>
            <li>
            <p>인증서를 추출할지 또는 개인 키를 추출할지 선택합니다.</li>
            <li>
              <p>추출할 파일 유형을 선택합니다.</p>
            </li>
            <li>
              <p>비공개 키 또는 인증서가 포함된 파일을 선택합니다.</p>
            </li>
            <li>
              <p>파일의 암호를 입력합니다.</p>
            </li>
            <li>
              <p><b>[!UICONTROL 저장]</b>을 클릭하여 파일을 추출하고 연결 설정으로 돌아갑니다.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody> 
   </table>

1. 연결을 저장하고 모듈로 돌아가려면 **계속**&#x200B;을 클릭합니다.

## Microsoft SharePoint 모듈 및 해당 필드

Microsoft SharePoint Online 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Microsoft SharePoint Online 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [드라이브 항목](#drive-item)
* [항목](#item)
* [목록](#list)
* [페이지(Beta)](#page-beta)
* [Site](#site)
* [기타](#other)

### 드라이브 항목

* [파일 만들기](#create-a-file)
* [폴더 만들기](#create-a-folder)
* [파일 가져오기](#get-a-file)
* [폴더 가져오기](#get-a-folder)
* [폴더 또는 파일 업데이트](#update-a-folder-or-a-file)
* [감시 폴더 항목](#watch-folder-items)

#### 파일 만들기

이 모듈은 SharePoint에서 파일을 생성합니다. 이 모듈의 성능은 파일 만들기(기존) 모듈보다 뛰어납니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 폴더 ID 입력]</td> 
   <td> <p>변경 사항을 검색할 폴더의 위치를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>파일을 만들 위치의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 드라이브 ID]</strong> 및 <strong>[!UICONTROL 폴더 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>파일을 만들 위치를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일] </td>
      <td><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p></td>
  </tr>  </tbody> 
</table>



#### 파일 만들기(이전)

이 모듈은 SharePoint에서 파일을 만듭니다.

성능을 향상시키려면 [파일 만들기](#create-a-file) 모듈을 사용하는 것이 좋습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 폴더 ID 입력]</td> 
   <td> <p>변경 사항을 검색할 폴더의 위치를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>파일을 만들 위치의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 드라이브 ID]</strong> 및 <strong>[!UICONTROL 폴더 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>파일을 만들 위치를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
      <td><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p></td>
  </tr>  </tbody> 
</table>

#### 폴더 만들기

이 작업 모듈은 SharePoint에 새 폴더를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 폴더 ID 입력]</td> 
   <td> <p>만들려는 폴더의 위치를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>폴더를 만들 위치의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 드라이브 ID]</strong> 및 <strong>[!UICONTROL 폴더 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>폴더를 만들 위치를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더 이름]</td> 
   <td>새 폴더의 이름을 입력하거나 매핑합니다.</td> 
  </tr>
  </tbody> 
</table>

#### 파일 가져오기

이 작업 모듈은 지정된 SharePoint 파일을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 폴더 ID 입력]</td> 
   <td> <p>가져올 파일의 위치를 식별하는 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>검색할 파일의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 파일 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>파일 위치를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### 폴더 가져오기

이 모듈은 지정된 폴더에 대한 세부 정보를 검색했습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 파일 입력                ID]</td> 
   <td> <p>가져올 파일의 위치를 식별하는 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>검색할 폴더의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 폴더 경로]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>폴더의 위치를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### 폴더 또는 파일 업데이트

이 작업 모듈은 폴더 또는 파일의 메타데이터를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 파일 입력                ID]</td> 
   <td> <p>가져올 파일의 위치를 식별하는 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>검색할 폴더 또는 파일의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 폴더 또는 항목 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>폴더의 위치를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  </tr> 
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td>업데이트할 각 메타데이터 필드에 대해 <b>항목 추가</b>를 클릭하고 필드의 경로와 값을 입력하십시오.</td> 
  <tr>
</tbody> 
</table>

#### 감시 폴더 항목

이 트리거 모듈은 선택한 폴더에서 항목이 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 폴더 ID 입력]</td> 
   <td> <p>가져올 파일의 위치를 식별하는 방법을 선택하십시오.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>표시되는 필드에 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 폴더 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>감시할 폴더의 위치를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td>한 시나리오 실행 주기 동안 Workfront Fusion이 반환해야 하는 최대 항목 수를 입력합니다.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### 항목

* [[!UICONTROL 항목 복사]](#copy-an-item)
* [[!UICONTROL 항목 만들기]](#create-an-item)
* [[!UICONTROL 항목 삭제]](#delete-an-item)
* [[!UICONTROL 항목 가져오기]](#get-an-item)
* [세부 정보 가져오기](#get-details)
* [[!UICONTROL 목록 항목]](#list-items)
* [[!UICONTROL 항목 이동]](#move-an-item)
* [[!UICONTROL 항목 업데이트]](#update-an-item)
* [[!UICONTROL 항목 보기]&#x200B;(예약됨)](#watch-items-scheduled)


#### [!UICONTROL 항목 복사]

이 작업 모듈은 SharePoint 목록의 기존 항목을 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">사이트, 드라이브 및 폴더 ID 입력</td> 
   <td> <p>복사할 항목이 들어 있는 사이트 및 드라이브를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>복사할 항목의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 드라이브 ID]</strong> 및 <strong>[!UICONTROL 항목 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>항목 유형 필드에서 필드를 이동할 것인지 폴더를 이동할 것인지 선택합니다.  복사할 항목이 들어 있는 사이트를 선택한 다음 목록을 선택하고 항목을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 대상 ID]</td> 
   <td> 항목을 복사할 폴더의 ID를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 새 이름]</td> 
   <td>항목의 새 복사본에 대한 이름을 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 항목 만들기]

이 작업 모듈은 SharePoint 목록에 새 항목을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 항목 만들기]</td> 
   <td> <p>항목을 만들 사이트 및 드라이브를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>항목을 만들 <strong>[!UICONTROL Site ID]</strong> 및 <strong>[!UICONTROL List ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>항목을 만들 목록이 포함된 사이트를 선택한 다음 목록을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td>새 항목에 대해 설정할 각 필드에 대해 <b>항목 추가</b>를 클릭하고 필드의 키(필드를 식별함)와 해당 필드에 대해 새 항목에 사용할 값을 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 항목 삭제]

이 작업 모듈은 SharePoint 목록의 기존 항목을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 항목 업데이트]</td> 
   <td> <p>삭제하려는 항목이 포함된 사이트 및 목록을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>삭제하려는 항목의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 항목 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>삭제할 항목이 포함된 사이트를 선택한 다음 목록을 선택하고 항목을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 항목 가져오기]

이 작업 모듈은 지정된 항목의 데이터를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 항목 가져오기]</td> 
   <td> <p>가져오려는 항목이 포함된 사이트 및 목록을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>데이터를 반환할 항목의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 항목 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>항목을 검색할 목록이 포함된 사이트를 선택한 다음 목록을 선택하고 항목을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 세부 정보 가져오기

이 모듈은 지정된 URL에서 항목 세부 정보를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">웹 URL</td> 
   <td> 세부 정보를 검색할 항목의 URL을 입력하거나 매핑합니다. </td> 
  </tr> 
</tbody> 
</table>

#### [!UICONTROL 목록 항목]

이 작업 모듈은 지정된 목록의 모든 항목 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 목록 항목]</td> 
   <td> <p>항목을 검색할 목록을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>항목을 나열할 목록의 <strong>[!UICONTROL 사이트 ID]</strong> 및 <strong>[!UICONTROL 목록 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>항목을 검색할 목록이 포함된 사이트를 선택한 다음 목록을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 항목 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 항목 이동]

이 작업 모듈은 SharePoint 목록의 기존 항목을 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">사이트, 드라이브 및 폴더 ID 입력</td> 
   <td> <p>이동할 항목이 포함된 사이트 및 목록을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>이동할 항목의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 항목 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>항목 유형 필드에서 필드를 이동할 것인지 폴더를 이동할 것인지 선택합니다. 복사할 항목이 들어 있는 사이트를 선택한 다음 목록을 선택하고 항목을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 대상 ID]</td> 
   <td> 항목을 이동할 폴더의 ID를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 새 이름]</td> 
   <td>이동된 항목의 이름을 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 항목 업데이트]

이 작업 모듈은 SharePoint 목록의 기존 항목을 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 항목 업데이트]</td> 
   <td> <p>업데이트하려는 항목이 포함된 사이트 및 목록을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>업데이트하려는 항목의 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 목록 ID]</strong> 및 <strong>[!UICONTROL 항목 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>업데이트할 항목이 들어 있는 사이트를 선택한 다음 목록을 선택하고 항목을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td>새 항목에 대해 업데이트할 각 필드에 대해 <b>항목 추가</b>를 클릭하고 필드의 키(필드를 식별함)와 해당 필드에 대해 항목을 사용할 새 값을 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 항목 보기]&#x200B;(예약됨)

이 트리거 모듈은 항목을 만들거나 수정할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 감시 목록]</td> 
   <td>생성 시간(새 항목)별로 또는 수정 시간(업데이트된 항목)별로 목록을 시청할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>보려는 사이트 및 목록을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>보려는 <strong>[!UICONTROL 사이트 ID]</strong> 및 <strong>[!UICONTROL 목록 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>보려는 사이트를 선택한 다음 목록을 선택합니다. 이러한 드롭다운은 팔로우한 사이트만 검색합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 항목 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 목록

* [[!UICONTROL 목록 만들기]](#create-a-list)
* [[!UICONTROL 목록 가져오기]](#get-a-list)
* [[!UICONTROL 목록]](#list-lists)
* [[!UICONTROL 시청 목록]](#watch-lists)

#### [!UICONTROL 목록 만들기]

이 작업 모듈은 SharePoint에 새 목록을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트 ID 입력]</td> 
   <td> <p>목록을 만들 사이트를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>목록을 만들 <strong>[!UICONTROL 사이트 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>목록을 만들 사이트를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display Name]</td> 
   <td>새 목록의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td>새 목록에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 열 추가]</td> 
   <td>새 목록에 설정할 각 열에 대해 <b>항목 </b> 추가를 클릭하고 필드에 <strong>[!UICONTROL 이름]</strong>을(를) 입력한 다음 새 열에 사용할 <strong>[!UICONTROL 유형]</strong> 값을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 목록 가져오기]

이 작업 모듈은 지정된 목록의 데이터를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 목록 가져오기]</td> 
   <td> <p>가져오려는 항목이 포함된 사이트 및 목록을 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>반환할 <strong>[!UICONTROL 사이트 ID]</strong> 및 <strong>목록 ID</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>검색할 목록이 포함된 사이트를 선택한 다음 목록을 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 목록]

이 작업 모듈은 지정된 사이트의 모든 항목 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 목록]</td> 
   <td> <p>목록을 검색할 사이트를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>반환할 목록을 포함하는 <strong>[!UICONTROL 사이트 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>검색할 목록이 포함된 사이트를 선택합니다. 드롭다운은 팔로우하는 사이트만 검색합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 목록 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 시청 목록]

이 트리거 모듈은 목록을 만들거나 수정할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 감시 목록]</td> 
   <td>생성 시간(새 항목)별로 또는 수정 시간(업데이트된 항목)별로 목록을 시청할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트 ID 입력]</td> 
   <td> <p>목록을 보려는 사이트를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>목록을 보려는 <strong>[!UICONTROL 사이트 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>보려는 사이트를 선택합니다. 드롭다운은 팔로우하는 사이트만 검색합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 목록 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 페이지(Beta)

>[!NOTE]
>
>`beta`에서 [!DNL Microsoft Graph] 버전의 API는 변경될 수 있습니다. 프로덕션 응용 프로그램에서는 이러한 API를 사용할 수 없습니다.

* [페이지 가져오기](#get-a-page)
* [목록 페이지](#list-pages)
* [페이지 게시](#publish-a-page)
* [시청 페이지](#watch-pages)

#### [!UICONTROL 페이지 가져오기]

이 작업 모듈은 지정된 페이지의 데이터를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지 가져오기]</td> 
   <td> <p>검색할 페이지를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL 사이트 ID]</strong> 및 <strong>[!UICONTROL 페이지 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>검색할 페이지가 포함된 사이트를 선택한 다음 페이지를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 목록 페이지

이 모듈은 모든 페이지의 목록을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 목록 페이지]</td> 
   <td> <p>나열할 페이지를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>나열할 페이지가 포함된 사이트의 <strong>[!UICONTROL 사이트 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>나열할 페이지가 포함된 사이트를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 페이지 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 페이지 게시

이 작업 모듈은 선택한 페이지의 최신 버전을 게시합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이지 게시]</td> 
   <td> <p>게시할 페이지를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL 사이트 ID]</strong> 및 <strong>[!UICONTROL 페이지 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>게시할 페이지가 포함된 사이트를 선택한 다음 페이지를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 시청 페이지

이 트리거 모듈은 지정된 사이트에서 페이지가 수정되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트 ID 입력]</td> 
   <td> <p>나열할 페이지를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>보려는 페이지가 포함된 사이트의 <strong>[!UICONTROL 사이트 ID]</strong>을(를) 입력하거나 매핑하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL 팔로우하는 목록에서 선택]</strong> </p> <p>보려는 페이지가 포함된 사이트를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 페이지 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Site

* [[!UICONTROL 사이트 가져오기]](#get-a-site)
* [[!UICONTROL 사이트 검색]](#search-sites)

#### [!UICONTROL 사이트 가져오기]

이 작업 모듈은 지정된 사이트의 데이터를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트 가져오기]</td> 
   <td> <p>검색할 페이지를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p><strong>[!UICONTROL 사이트 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>검색할 사이트를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사이트 검색]

이 작업 모듈은 지정한 매개 변수로 사이트를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword of Display Name]</td> 
   <td> <p>사이트를 검색할 검색어를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 사이트 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [변경 사항 가져오기](#get-changes)
* [API 호출 만들기](#make-an-api-call)
* [이벤트 보기](#watch-events)

#### 변경 사항 가져오기

이 모듈은 SharePoint 폴더에서 만든 추가, 업데이트 및 삭제 작업을 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 사이트, 드라이브 및 폴더 ID 입력]</td> 
   <td> <p>업데이트할 항목이 들어 있는 사이트 및 드라이브를 식별하는 방법을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>표시되는 필드에 <strong>[!UICONTROL 사이트 ID]</strong>, <strong>[!UICONTROL 드라이브 ID]</strong> 및 <strong>[!UICONTROL 폴더 ID]</strong>을(를) 입력하거나 매핑합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 목록에서 선택]</strong> </p> <p>업데이트할 항목이 있는 사이트를 선택한 다음 드라이브를 선택하고 폴더를 선택합니다. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> 토큰은 모듈이 변경 사항 검색을 시작해야 하는 시점을 식별합니다.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL API 호출 만들기]

이 모듈에서는 사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Microsoft SharePoint Online 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Microsoft SharePoint Online을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code>https://graph.microsoft.com</code>와 관련된 경로를 입력합니다. 예:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 메서드]</p> </td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다. 예, <code>{"Content-type":"application/json"}</code>. Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p> 표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 유형]</td> 
   <td>API 호출에서 전송할 데이터 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 이벤트 보기

이 즉시 트리거 모듈은 SharePoint에서 항목이 추가, 업데이트 또는 삭제될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to Workfront Fusion, see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL 웹후크]</td> 
   <td> <p>기존 웹후크를 선택하거나 추가 를 클릭하고 연결을 입력하여 새 웹후크를 생성합니다.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
