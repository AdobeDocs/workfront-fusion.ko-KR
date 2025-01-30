---
title: 모듈 간 파일 매핑
description: 일부 모듈에는 파일을 처리하는 기능이 있습니다. 이러한 모듈은 추가 처리를 위해 전송할 출력 파일을 반환하거나 처리를 위해 파일을 해당 모듈에 전달해야 합니다. 이러한 모듈을 함께 사용하여 파일을 처리하려면 먼저 모듈을 서로 매핑해야 합니다.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# 모듈 간 파일 매핑

일부 모듈은 파일을 처리할 수 있습니다. 이러한 모듈은 추가 처리를 위해 전송할 출력 파일을 반환하거나 처리를 위해 파일을 해당 모듈에 전달해야 합니다. 파일은 매핑될 수 있으므로 한 모듈에서 출력된 파일을 다른 모듈에서 처리할 수 있습니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스</td> 
   <td> <p>신규: [!UICONTROL Standard]</p><p>또는</p><p>현재: [!UICONTROL Work] 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Workfront] 플랜: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 플랜: [!DNL Workfront Fusion]이(가) 포함되어 있습니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직에서 [!DNL Adobe Workfront Fusion]을(를) 구매해야 합니다.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성*</td> 
   <td> 
     <p>조직의 [!DNL Workfront Fusion] 관리자여야 합니다.</p>
     <p>팀의 [!DNL Workfront Fusion] 관리자여야 합니다.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 소스 모듈에서 타겟 모듈로 파일 매핑

모듈은 파일을 처리할 때 다음 두 가지 정보를 필요로 합니다.

* 파일 이름
* 파일 콘텐츠(데이터)

이전 모듈에서 파일을 출력하는 경우 소스 모듈을 선택할 수 있으며, 해당 모듈에서 출력된 파일의 이름과 데이터는 대상 모듈에 매핑됩니다.

이 이름과 데이터를 수동으로 입력하거나 이전 모듈에서 매핑할 수도 있습니다. 예를 들어 파일 이름을 바꾸는 경우 편리할 수 있습니다.

>[!NOTE]
>
>URL에서 파일을 처리해야 하는 경우 `HTTP > Get a File` 모듈을 사용하여 URL에서 파일을 다운로드한 다음 `HTTP > Get a File` 모듈에서 파일을 시나리오에서 원하는 모듈의 필드에 매핑하는 것이 좋습니다.
>
>![맵 파일](assets/map-source-file.png)

파일을 매핑하려면 다음과 같이 하십시오.

1. 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 파일을 매핑할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 매핑할 대상인 대상 모듈에서 **Source 파일** 영역을 찾습니다.
1. 이전 모듈에서 출력한 파일을 매핑하려면 파일을 출력하는 모듈을 선택합니다.

   ![Workfront 다운로드 문서](assets/wf-download-document.png)

1. 이름과 데이터를 수동으로 매핑하려면 맵을 선택한 다음 파일 이름과 데이터를 입력하거나 매핑합니다.

   ![맵 옵션 사용](assets/use-the-map-option.png)

1. 모듈 구성을 계속하거나 **확인**&#x200B;을 클릭합니다.
