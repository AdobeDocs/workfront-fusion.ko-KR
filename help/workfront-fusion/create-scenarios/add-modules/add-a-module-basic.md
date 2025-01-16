---
title: 시나리오에 모듈 추가
description: 이 문서에서는 시나리오에 모듈을 추가하는 기본 프로세스에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# 시나리오에 모듈 추가

시나리오는 앱 내에서 데이터를 변환하거나 앱과 웹 서비스 간에 데이터를 전송하는 방법을 나타내는 일련의 모듈로 구성됩니다. 모듈을 추가하고 구성하여 모듈을 빌드합니다.

이 문서에서는 시나리오에 모듈을 추가하는 기본 프로세스에 대해 설명합니다. 시나리오를 추가하는 방법에 대한 자세한 지침은 [모듈 추가: 문서 인덱스](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)의 다른 문서를 참조하십시오.

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

## 시나리오에 첫 번째 모듈 추가

시나리오의 첫 번째 모듈은 일반적으로 트리거 모듈입니다.

트리거 모듈에 대한 자세한 내용은 문서 모듈 개요에서 [트리거 모듈](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)을(를) 참조하십시오.

1. 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 화면 오른쪽 상단의 **새 시나리오 만들기**&#x200B;를 클릭하여 시나리오 만들기를 시작합니다.

   자리 표시자(물음표) 모듈과 사용 가능한 커넥터 목록이 있는 시나리오 편집기가 열립니다.

   ![자리 표시자 모듈](assets/placeholder-module.png)

1. 이 시나리오를 시작할 커넥터 또는 웹후크를 선택합니다. 목록의 검색 창에 커넥터 이름을 입력하여 목록을 필터링할 수 있습니다.
1. 모듈을 구성합니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>시나리오에서 첫 번째 모듈을 제거했으며 교체하려면 자리 표시자(물음표) 모듈을 클릭하여 커넥터 목록을 엽니다.

## 시나리오에 다른 모듈 추가

1. 모듈을 추가할 시나리오의 시나리오 편집기에 있지 않은 경우 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 블루프린트를 내보낼 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 다른 모듈에 모듈을 추가하려면 모듈을 추가할 모듈의 오른쪽 핸들을 마우스로 가리킨 다음 모듈이 나타나면 **다른 모듈 추가**&#x200B;를 클릭합니다.

   커넥터 목록이 열리고 시나리오에 이미 사용된 커넥터가 표시됩니다.

1. (선택 사항) 다른 커넥터를 선택하려면 목록에서 **다른 모듈 추가**&#x200B;를 클릭한 다음 커넥터를 선택합니다. 목록의 검색 창에 커넥터 이름을 입력하여 목록을 필터링할 수 있습니다.
1. 모듈을 구성합니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## 시나리오의 기존 모듈 사이에 모듈 삽입

1. 모듈을 추가할 시나리오의 시나리오 편집기에 있지 않은 경우 왼쪽 패널의 **[!UICONTROL Scenarios]** 탭을 클릭합니다.
1. 블루프린트를 내보낼 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. 모듈을 삽입할 모듈 사이의 점선 경로를 클릭합니다.
1. 표시되는 메뉴에서 **모듈 추가**&#x200B;를 선택합니다.

커넥터 목록이 열리고 시나리오에 이미 사용된 커넥터가 표시됩니다.

1. (선택 사항) 다른 커넥터를 선택하려면 목록에서 **다른 모듈 추가**&#x200B;를 클릭한 다음 커넥터를 선택합니다. 목록의 검색 창에 커넥터 이름을 입력하여 목록을 필터링할 수 있습니다.
1. 모듈을 구성합니다.

   특정 모듈 구성에 대한 지침은 [Fusion 응용 프로그램 및 해당 모듈 참조에 나열된 선택한 응용 프로그램에 대한 문서를 참조하십시오. 문서 인덱스](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
