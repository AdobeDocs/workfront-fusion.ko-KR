---
title: 암호화기
description: Adobe Workfront Fusion Encryptor 모듈을 사용하면 모든 텍스트 데이터를 암호화할 수 있습니다. 현재 AES256 및 PGP(OpenPGP)를 통해 메시지 암호화를 지원합니다.
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# 암호화기

[!DNL Adobe Workfront Fusion] [!UICONTROL Encryptor] 모듈을 사용하면 모든 텍스트 데이터를 암호화할 수 있습니다. 현재 AES256 및 PGP([!UICONTROL OpenPGP])를 통해 메시지 암호화를 지원합니다.

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
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합의 경우 [!UICONTROL [!DNL Workfront Fusion], 작업 자동화의 경우 [!UICONTROL [!DNL Workfront Fusion]]</p>
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

## PGP를 이용한 메시지 암호화 및 복호화

PGP를 통해 암호화 및 복호화할 때 키체인을 사용하고 개인 또는 공개 키(또는 둘 다)를 생성해야 한다.

공개 키와 개인 키에 대한 자세한 내용은 [Adobe Workfront Fusion 용어집](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md)을 참조하십시오. <!--For more information on keychains, see [Keys in [!DNL Adobe Workfront Fusion]]().-->

## [!UICONTROL Encryptor]개 모듈 및 해당 필드

[!UICONTROL Encryptor] 모듈을 구성할 때 다음 필드가 표시됩니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

### PGP 메시지 암호화

이 모듈에서는 공개 및 개인 키를 사용하여 메시지를 암호화할 수 있습니다.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>보낸 사람의 개인 키를 입력합니다. 발신자의 신원을 인증할 수 있습니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>수신자의 공개 키를 입력합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>암호화할 메시지를 입력합니다.</td>
    </tr>

### PGP 메시지 암호 해독

이 모듈에서는 공개 및 개인 키를 사용하여 메시지의 암호를 해독할 수 있습니다.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>수신자의 개인 키를 입력합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>수신자의 공개 키를 입력합니다. 발신자의 신원을 인증할 수 있습니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>해독할 메시지를 매핑합니다.</td>
    </tr>
</table>
