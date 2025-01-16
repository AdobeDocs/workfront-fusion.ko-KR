---
title: 모듈 구성
description: 만드는 모든 모듈에 대한 설정을 구성해야 합니다.
author: Becky
feature: Workfront Fusion
exl-id: ae82d1fe-31e1-424a-9c1a-42dc1a20b749
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 2%

---

# 모듈 구성

만드는 모든 모듈에 대한 설정을 구성해야 합니다.

예를 들어 Workfront > 문서 업로드 모듈을 사용하려면 문서를 업로드할 레코드를 지정해야 합니다.

>[!NOTE]
>
>모듈 설정 외에도 시나리오의 설정을 조정할 수도 있습니다. 시나리오 이름을 바꾸고, 일정을 변경하고, 다른 작업 중에서도 추가 설정을 지정할 수 있습니다.

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
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 모듈의 설정 구성

1. 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 필터를 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 시나리오에 새 모듈을 추가합니다.

   또는

   구성할 모듈을 클릭합니다.

1. 모듈에 필요한 경우 [연결 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md)에 설명된 대로 해당 서비스의 등록된 사용자 계정에 **[!UICONTROL Connection]**&#x200B;을(를) 만듭니다.
1. 각 필드에 적절한 텍스트를 입력합니다.

   또는

   이전 모듈의 출력을 필드에 매핑합니다.

   매핑에 대한 자세한 내용은 [매핑 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md)를 참조하십시오.

   [!DNL Workfront Fusion]이(가) 인식할 수 있는 다른 항목 데이터 형식(예: 날짜, 숫자 및 텍스트)에 대한 자세한 내용은 [항목 데이터 형식](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)을 참조하십시오.

   >[!NOTE]
   >
   >굵게 표시된 매개 변수가 필요합니다.

1. (조건부) 모듈에 표시하고 사용할 고급 옵션이 있는 경우 **[!UICONTROL Show advanced settings]**&#x200B;을(를) 선택합니다.
