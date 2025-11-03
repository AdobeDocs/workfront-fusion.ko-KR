---
title: Adobe Experience Manager Forms 모듈
description: Adobe Workfront Fusion용  [!DNL Adobe Experience Manager Forms] 커넥터를 사용하면  [!DNL Adobe Experience Manager Forms] 계정의 이벤트를 기반으로 시나리오를 시작하고, 에셋을 만들고, 업로드하고, 업데이트하고, 폴더 및 에셋을 복사하거나 이동할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 1%

---

# [!DNL Adobe Experience Manager Forms]개 모듈

Adobe Workfront Fusion용 [!DNL Adobe Experience Manager Forms] 커넥터를 사용하면 웹후크를 만들어 [!DNL Adobe Experience Manager Forms] 계정의 이벤트를 기반으로 시나리오를 시작할 수 있습니다.

[!DNL Adobe Experience Manager Forms] 내에서 양식을 구성하여 양식 제출을 이 웹후크로 보낼 수 있습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <p>작업 기반: Workfront Fusion 라이센스 요구 사항 없음</p>
   <p>커넥터 기반(레거시): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

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

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>
          <p>이 연결이 프로덕션 환경에 연결되는지 아니면 비프로덕션 환경에 연결되는지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>
          <p>이 계정이 서비스 계정인지 개인 계정인지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">뒤쪽 슬래시가 없는 [!UICONTROL 인스턴스 URL]</td>
        <td>
          <p>계정에 액세스하는 데 사용하는 URL을 최종 슬래시 없이 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS 끝점]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
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
        <td role="rowheader">[!UICONTROL 조직 ID]</td>
        <td>[!DNL Adobe] 조직 ID를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 기술 계정 ID]</td>
        <td>[!DNL Adobe] 기술 계정 ID를 입력하십시오. 이는 [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명 세부 정보] 섹션에서 찾을 수 있습니다.
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta 범위]</td>
        <td>적절한 메타 범위를 입력하십시오.       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 개인 키]</td>
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
              <p><b>[!UICONTROL 저장]</b>을(를) 클릭하여 파일을 추출하고 연결 설정으로 돌아갑니다.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

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
   <td> <p>[!DNL Adobe Experience Manager] 계정을 Workfront Fusion에 연결하는 방법은 <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">연결 만들기 [!DNL Adobe Experience Manager Forms]</a>를 참조하십시오.</p> </td> 
  </tr>

모듈이 웹후크를 만들고 웹후크 주소를 제공합니다. 이 주소는 [!DNL Adobe Experience Manager Forms]의 양식 제출 대화 상자에 입력할 수 있습니다.
