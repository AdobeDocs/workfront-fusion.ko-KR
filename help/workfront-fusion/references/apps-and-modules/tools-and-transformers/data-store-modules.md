---
title: 데이터 저장소 모듈
description: 데이터베이스 또는 간단한 테이블과 유사한 Adobe Workfront Fusion 데이터 저장소는 시나리오의 데이터를 저장할 수 있으므로 개별 시나리오 또는 시나리오 실행 간에 데이터를 전송할 수 있습니다. 동기화 중에 데이터 저장소를 사용하여 다양한 시스템의 새 데이터를 저장할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 0338b822-b345-429e-850d-3978b692231d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 0%

---

# [!UICONTROL 데이터 저장소] 모듈

데이터베이스 또는 간단한 테이블과 유사한 Adobe Workfront Fusion 데이터 저장소는 시나리오의 데이터를 저장할 수 있으므로 개별 시나리오 또는 시나리오 실행 간에 데이터를 전송할 수 있습니다. 동기화 중에 데이터 저장소를 사용하여 다양한 시스템의 새 데이터를 저장할 수 있습니다.

데이터 저장소 모듈을 사용하면 Adobe Workfront Fusion 데이터 저장소에서 레코드를 추가, 교체, 업데이트, 검색, 삭제, 검색 또는 계산할 수 있습니다.

<!--For information on creating, editing, and troubleshooting data stores, see [Data Stores in Adobe Workfront Fusion](/help/workfront-fusion/references/mapping-panel/data-types/)-->

Workfront Fusion의 데이터 저장소에 대한 비디오 소개는 다음을 참조하십시오.

* [데이터 저장소](https://video.tv.adobe.com/v/3427029/){target=_blank}

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>Workfront Fusion 라이센스 요구 사항 없음</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!UICONTROL 데이터 저장소] 모듈을 사용하려면 먼저 데이터 저장소를 만들어야 합니다.

데이터 저장소 만들기에 대한 자세한 내용은 [데이터 저장소 만들기 및 관리](/help/workfront-fusion/create-scenarios/map-data/data-stores.md)를 참조하십시오.

## [!UICONTROL 데이터 저장소] 모듈 및 해당 필드

데이터 저장소 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 데이터 스토어 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

데이터 저장소를 사용하기 위해 연결을 만들 필요는 없습니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [레코드 추가/바꾸기](#addreplace-a-record)
* [레코드 존재 확인](#check-the-existence-of-a-record)
* [레코드 수](#count-records)
* [레코드 삭제](#delete-a-record)
* [모든 레코드 삭제](#delete-all-records)
* [레코드 가져오기](#get-a-record)
* [레코드 검색](#search-records)
* [레코드 업데이트](#update-a-record)

### [!UICONTROL 레코드 추가/바꾸기]

이 작업 모듈은 레코드를 추가하거나 대체합니다.

데이터 저장소 및 레코드 키를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

>[!NOTE]
>
>같은 이름으로 데이터 저장소에 이미 있는 레코드를 추가하려고 하면 모듈에서 오류가 발생하고 [!UICONTROL 기존 레코드 덮어쓰기] 옵션이 비활성화됩니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소]</td> 
   <td> <p> 레코드를 만들 데이터 저장소를 선택하거나 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 키] </td> 
   <td> <p>모듈이 추가하거나 대체할 레코드의 고유 키를 입력합니다. 키는 나중에 레코드를 검색하는 데 사용할 수 있습니다. 이 필드를 비워 두면 키가 자동으로 생성됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 기존 레코드 덮어쓰기] </td> 
   <td> <p>레코드를 덮어쓰려면 이 옵션을 활성화합니다. 덮어쓰려는 레코드는 위의 키 필드에 지정해야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드] </td> 
   <td> <p>레코드의 필드에 원하는 값을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 레코드가 있는지 확인]

이 작업 모듈은 특정 레코드가 존재하는지 여부를 지정합니다.

데이터 저장소 및 레코드 키를 지정합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소] </td> 
   <td> <p>레코드 존재를 확인할 데이터 저장소를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 키] </td> 
   <td> <p>모듈이 존재하는지 확인할 레코드의 고유 키를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 레코드 수]

이 작업 모듈은 데이터 저장소의 레코드에 번호를 지정합니다.

데이터 저장소를 지정합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소] </td> 
   <td> <p>계산할 레코드가 포함된 데이터 저장소를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 레코드 삭제]

이 작업 모듈은 레코드를 삭제합니다.

데이터 저장소 및 레코드 키를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소] </td> 
   <td> <p>레코드 존재를 확인할 데이터 저장소를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 키] </td> 
   <td> <p>모듈에서 삭제할 레코드의 고유 키를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 모든 레코드 삭제]

이 작업 모듈은 특정 데이터 저장소에서 모든 레코드를 삭제합니다.

데이터 저장소를 지정합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소] </td> 
   <td> <p>모든 레코드를 삭제할 데이터 저장소를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 레코드 가져오기]

이 작업 모듈은 레코드를 검색합니다.

데이터 저장소 및 레코드 키를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소]</td> 
   <td> <p> 레코드를 검색할 데이터 저장소를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 키] </td> 
   <td> <p>모듈을 검색할 레코드의 고유 키를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 레코드 검색]

이 검색 모듈은 데이터 저장소의 개체에서 지정한 검색 쿼리와 일치하는 레코드를 찾습니다.

이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소]</td> 
   <td> <p> 검색할 데이터 저장소를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>검색 필터를 설정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Sort]</p> </td> 
   <td> <p style="font-weight: normal;">정렬할 각 필드에 대해 다음 필드를 입력합니다.</p> <p style="font-weight: bold;">[!UICONTROL 키]</p> <p>결과를 정렬할 열 이름을 선택합니다.</p> <p style="font-weight: bold;">[!UICONTROL Order]</p> <p>결과를 오름차순으로 정렬할지 아니면 내림차순으로 정렬할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 제한]</td> 
   <td> <p> 한 실행 주기 동안 Workfront Fusion이 반환하는 최대 검색 결과 수를 설정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 모듈이 결과를 반환하지 않더라도 라우트 실행을 계속합니다.]</td> 
   <td> <p> 활성화된 경우 이 모듈이 속한 경로는 이 모듈이 결과를 반환하지 않는 경우에도 계속 처리됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 레코드 업데이트]

이 작업 모듈은 레코드를 업데이트합니다.

데이터 저장소 및 레코드 키를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 데이터 저장소]</td> 
   <td> <p> 레코드를 만들 데이터 저장소를 선택하거나 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 키] </td> 
   <td> <p>모듈을 업데이트할 레코드의 고유 키를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 누락된 레코드 삽입] </td> 
   <td> <p>지정된 키가 있는 레코드가 없는 경우 새 레코드를 만들려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드]</td> 
   <td> <p> 갱신할 레코드의 필드에 원하는 값을 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
