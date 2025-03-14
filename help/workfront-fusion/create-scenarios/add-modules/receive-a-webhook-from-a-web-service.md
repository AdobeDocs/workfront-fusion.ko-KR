---
title: 커넥터 없이 웹 서비스에 대한 웹후크 구성
description: 웹 서비스에 현재 Workfront Fusion의 전용 커넥터가 없지만 웹 후크 전송을 지원하는 경우, 사용자 지정 웹 후크 모듈을 인스턴트 트리거로 사용하여 시나리오에 서비스를 추가할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# 커넥터 없이 웹 서비스에 대한 웹후크 구성

웹 서비스에 현재 Workfront Fusion의 전용 커넥터가 없지만 웹 후크 전송을 지원하는 경우, 사용자 지정 웹 후크 모듈을 인스턴트 트리거로 사용하여 시나리오에 서비스를 추가할 수 있습니다. 이 프로세스를 웹후크 수신이라고 하며, 연결하려는 응용 프로그램의 측면에 몇 가지 구성이 필요합니다.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지 
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
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 플랜 선택: 귀사는 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 플랜: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## Webhook 받기

1. 왼쪽 패널의 **[!UICONTROL 시나리오]** 탭을 클릭합니다.
1. 웹후크를 추가할 시나리오를 선택합니다.
1. 시나리오의 아무 곳이나 클릭하여 시나리오 편집기를 입력합니다.
1. **Webhooks > 사용자 지정 Webhook** 모듈을 추가하여 시나리오를 시작합니다.
1. Webhook 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. 표시되는 상자에 **Webhook 이름**&#x200B;을 입력하십시오.
1. (선택 사항) Webhook를 구성합니다.

   자세한 내용은 [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)을(를) 참조하십시오.

1. **저장**&#x200B;을 클릭합니다.

1. **클립보드에 주소 복사**&#x200B;를 클릭한 다음 **확인**&#x200B;을 클릭합니다.

1. 웹 서비스에 로그인하고 다음 작업을 수행합니다.

   1. 웹 서비스의 설정 영역에서 웹후크를 만듭니다.

      특정 지침은 애플리케이션에 따라 다릅니다. 애플리케이션 설명서에서 &quot;웹후크 만들기&quot;를 검색하는 것이 좋습니다.
   1. 3단계에서 클립보드로 복사한 주소를 붙여넣습니다.
   1. 웹후크를 트리거할 이벤트를 선택합니다.

1. 시나리오를 실행합니다.

   이벤트가 발생하면 사용자 지정 웹후크 모듈이 트리거되고 시나리오가 실행됩니다.
