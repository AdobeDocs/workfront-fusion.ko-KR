---
title: Adobe Experience Manager Forms 모듈
description: ' [!DNL Adobe Workfront Fusion], you can start a scenario based on events in your [!DNL Adobe Experience Manager Forms] 계정의  [!DNL Adobe Experience Manager Forms] 커넥터를 사용하여 자산을 만들고, 업로드하고, 업데이트하고, 폴더 및 자산을 복사하거나 이동합니다.'
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# [!DNL Adobe Experience Manager Forms]개 모듈

[!DNL Adobe Workfront Fusion]에 대한 [!DNL Adobe Experience Manager Forms] 커넥터를 사용하면 웹후크를 만들어 [!DNL Adobe Experience Manager Forms] 계정의 이벤트를 기반으로 시나리오를 시작할 수 있습니다.

[!DNL Adobe Experience Manager Forms] 내에서 양식을 구성하여 양식 제출을 이 웹후크로 보낼 수 있습니다.

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

* 이 모듈을 사용하려면 [!DNL Adobe Experience Manager Forms] 계정이 있어야 합니다.

## Adobe Experience Manager Assets API 정보

Adobe Experience Manager Assets 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## Adobe Experience Manager Forms에 대한 연결 만들기

[!DNL Adobe Experience Manager Forms] 모듈에 대한 연결을 만들려면:

1. 연결 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>이 연결이 프로덕션 환경에 연결되는지 아니면 비프로덕션 환경에 연결되는지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>이 계정이 서비스 계정인지 개인 계정인지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance URL without a trailing slash]</td>
        <td>
          <p>계정에 액세스하는 데 사용하는 URL을 최종 슬래시 없이 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS endpoint]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>[!DNL Adobe] 클라이언트 ID를 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>[!DNL Adobe] 클라이언트 암호를 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Org ID]</td>
        <td>[!DNL Adobe] 조직 ID를 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>[!DNL Adobe] 기술 계정 ID를 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>적절한 메타 범위를 입력하십시오.       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>[!DNL Adobe Developer Console]에서 자격 증명을 만들 때 생성된 개인 키를 입력하십시오. </p>
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
              <p><b>[!UICONTROL Save]</b>을(를) 클릭하여 파일을 추출하고 연결 설정으로 돌아갑니다.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## Adobe Experience Manager Forms 모듈 및 해당 필드

현재 Adobe Experience Manager Forms 커넥터에는 모듈이 한 개만 있습니다.

### 양식 이벤트 감시

이 즉시 트리거(웹후크)를 사용하면 Adobe Experience Manager 양식에서 제출 작업이 발생할 때 시나리오를 시작할 수 있습니다.

>[!IMPORTANT]
>
>이 모듈에서는 Adobe Experience Manager의 구성도 필요합니다. 이 웹후크를 설정한 후에는 Adobe Experience Manager을 열고 웹후크로 제출을 보내도록 양식을 구성해야 합니다.
>
><!--For instructions on the required form configuration, see insert url here-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p>Webhook의 이름 입력</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Adobe Experience Manager] 계정을 [!DNL Workfront Fusion]에 연결하는 방법은 <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">연결 만들기 [!DNL Adobe Experience Manager Forms]</a>를 참조하십시오.</p> </td> 
  </tr>

모듈이 웹후크를 만들고 웹후크 주소를 제공합니다. 이 주소는 [!DNL Adobe Experience Manager Forms]의 양식 제출 대화 상자에 입력할 수 있습니다.
