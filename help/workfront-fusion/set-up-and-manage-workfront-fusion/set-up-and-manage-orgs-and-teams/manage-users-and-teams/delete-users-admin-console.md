---
content-type: reference
title: '조직 및 팀 설정 및 관리: 문서 색인'
description: 이 섹션에는 Adobe Workfront Fusion의 조직 및 팀 설정 및 관리와 관련된 문서가 포함되어 있습니다.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# [!DNL Adobe Admin Console]을(를) 통해 사용자 삭제

Adobe Workfront Fusion에서만 사용자를 제거하고 다른 [!DNL Adobe] 제품 프로필에 액세스할 수 있습니다. 또는 [!DNL Adobe Admin Console]에서 사용자를 완전히 제거할 수도 있습니다.

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
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">액세스 수준 구성</td> 
   <td> 
     <p>조직의 Adobe Admin Console 관리자여야 합니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## Adobe Workfront Fusion에서만 사용자 제거

다른 Adobe 제품 권한을 그대로 유지하면서 Workfront Fusion에서 사용자를 제거할 수 있습니다.

자세한 내용은 문서 [Admin Console에서 제품 관리](https://helpx.adobe.com/kr/enterprise/using/manage-products.html)에서 &quot;제품에서 사용자 및 사용자 그룹 제거&quot;를 참조하십시오.

## [!DNL Adobe Admin Console]의 모든 제품에서 사용자 비활성화

사용자를 삭제하려면 [!DNL Adobe Admin Console]을(를) 통해 사용자를 비활성화해야 합니다.

다음 중 하나가 적용되면 사용자가 [!DNL Adobe Admin Console]에서 비활성화됩니다.

* 사용자는 제품 또는 제품 프로필에서 이동되고 다른 제품 또는 제품 프로필에 할당되지 않습니다.
* 사용자는 제품 프로필에 연결된 그룹에서 제거되며 제품 프로필에 연결된 다른 그룹에는 포함되지 않습니다.
* 사용자는 제품 프로필에서 제거되고 다른 제품 프로필에 할당되지 않습니다.
* Workfront Fusion이 포함된 조직에서 사용자가 삭제되거나 비활성화됩니다.

  지침은 [개별적으로 사용자 관리](https://helpx.adobe.com/kr/enterprise/using/manage-users-individually.html)의 &quot;사용자 제거&quot; 섹션을 참조하십시오.

Workfront Fusion에서 비활성화는 다음 방법 중 하나로 사용자에게 영향을 줍니다.

* 사용자가 한 조직에만 있는 경우 사용자는 비활성화됩니다.
* 사용자가 둘 이상의 조직에 있는 경우 사용자가 [!DNL Adobe Admin Console]에서 수정된 조직에서 제거됩니다.
* 사용자를 삭제할 때는 다음 사항을 고려하십시오.

### Workfront Fusion에서 사용자 삭제 시 고려 사항

사용자를 삭제할 때는 다음 사항을 고려하십시오.

* 사용자가 삭제되면 사용자의 연결, 키 및 웹후크가 제거됩니다.
* 사용자에게 속한 모든 시나리오는 조직 소유자에게 전송됩니다. 사용자에게 속한 연결이 더 이상 유효하지 않으므로 이러한 시나리오의 연결을 업데이트해야 합니다.
* 삭제된 사용자가 응용 프로그램 또는 공용 템플릿을 소유하고 있으면 해당 응용 프로그램 또는 공용 템플릿이 조직 소유자에게 이전됩니다. 조직 소유자가 없는 경우 애플리케이션이나 공용 템플릿이 다른 사용자에게 전송됩니다.
