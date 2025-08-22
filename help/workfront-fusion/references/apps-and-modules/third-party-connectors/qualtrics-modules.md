---
title: Qualtrics 모듈
description: Adobe Workfront Fusion 시나리오에서는 Qualtrics를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 80b441b7-c808-4c4f-b9ff-d614650dbb73
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---

# Qualtrics 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Qualtrics]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 플랜*</td>
  <td> <p>[!UICONTROL Pro] 이상</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이센스*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재 라이선스 요구 사항: Workfront Fusion 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>현재 제품 요구 사항: [!UICONTROL Select] 또는 [!UICONTROL Prime] Adobe Workfront 플랜이 있는 경우 조직에서 이 문서에 설명된 기능을 사용하려면 Adobe Workfront Fusion과 Adobe Workfront을 구입해야 합니다. Workfront Fusion은 [!UICONTROL Ultimate] Workfront 플랜에 포함되어 있습니다.</p>
   <p>또는</p>
   <p>레거시 제품 요구 사항: 조직에서 이 문서에 설명된 기능을 사용하려면 Adobe Workfront Fusion과 Adobe Workfront을 구입해야 합니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 Workfront 관리자에게 문의하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

## 전제 조건

[!DNL Qualtrics] 모듈을 사용하려면 [!UICONTROL Qualtrics] 계정이 있어야 합니다.

## Qualtrics API 정보

Qualtrics 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://{{connection.dataCenterCode}}.qualtrics.com/API/v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.1.1</td> 
  </tr>
 </tbody> 
 </table>

## Workfront Fusion에 [!DNL Qualtrics] 연결 중

[!DNL Qualtrics]Qualtrics[!UICONTROL &#x200B; 모듈 내에서 직접 &#x200B;] 계정에 연결할 수 있습니다.

1. [!UICONTROL Qualtrics] 모듈에서 **[!UICONTROL 연결]** 필드 옆에 있는 [!UICONTROL 추가]를 클릭합니다.
1. 다음 정보를 입력합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 연결 이름]</p> </td> 
      <td> <p>새 연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 데이터 센터 ID] </td> 
      <td><code>&lt;Data Center ID>.qualtrics.com</code> 형식을 사용합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API 키]</td> 
      <td>API 키를 찾으려면 [!DNL Qualtrics] 설명서를 참조하십시오.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## [!DNL Qualtrics]개 모듈 및 해당 필드

[!DNL Qualtrics] 커넥터에서 다음 모듈을 사용할 수 있습니다.

* [!UICONTROL 새 설문 조사 응답 보기]
* [!UICONTROL 디렉터리 연락처 만들기]
* [!UICONTROL 디렉터리 연락처 삭제]
* [!UICONTROL 디렉터리 연락처 가져오기]
* [!UICONTROL 디렉터리 연락처 업데이트]
* [!UICONTROL SMS를 통해 새 설문 조사 배포 만들기]
* [!UICONTROL 이메일을 통해 설문 조사 배포]
* [!UICONTROL API 호출 만들기]
* [!UICONTROL 디렉터리 연락처 나열]
