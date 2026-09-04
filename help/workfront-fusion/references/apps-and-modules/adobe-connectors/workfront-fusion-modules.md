---
title: Workfront Fusion 모듈
description: Workfront Fusion 커넥터를 사용하면 레코드, 후크, 시나리오 및 연결을 비롯한 시나리오 내에서 자체 Fusion 조직을 관리할 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 557ec6de4ccf0753005fed3e4772d2eb9317537d
workflow-type: tm+mt
source-wordcount: 1374
ht-degree: 21%

---

# Workfront Fusion 모듈

Workfront Fusion 커넥터를 사용하면 시나리오 내에서 자체 Fusion 조직을 관리할 수 있습니다. Fusion을 서드파티 앱 또는 서비스에 연결하는 다른 커넥터와 달리 이 커넥터를 사용하면 시나리오가 Workfront을 관리하는 방식과 유사한 Adobe Workfront 커넥터를 사용하여 Fusion의 자체 API를 호출할 수 있습니다.

시나리오 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 색인](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

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
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## Workfront Fusion을 Workfront Fusion에 연결

1. Workfront Fusion 모듈에서 [연결] 필드 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL 연결 유형]</td> 
      <td>만들려는 연결 유형을 선택합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 연결 이름]</td> 
      <td>연결의 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 클라이언트 ID]</td> 
      <td>[!DNL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 클라이언트 암호]</td> 
      <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력합니다. [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 조직 ID]</td> 
      <td>[!DNL Adobe] IMS 조직 ID를 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 영역]</td> 
      <td>이 연결에 대한 Fusion 영역을 선택합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

## Workfront Fusion 모듈 및 해당 필드

Workfront Fusion 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [내보내기](#export)
* [기타](#misc)

### 액션

* [레코드 복제](#clone-a-record)
* [레코드 만들기](#create-a-record)
* [레코드 삭제](#delete-a-record)
* [목록 레코드](#list-records)
* [레코드 읽기](#read-a-record)
* [레코드 업데이트](#update-a-record)

#### 레코드 복제

이 모듈은 지정된 레코드의 복사본을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> 복제할 레코드 유형을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">시나리오 ID</td> 
   <td> 복제할 시나리오의 ID를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">이름</td> 
   <td> 새 시나리오의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 만들기

이 모듈은 지정된 데이터로 레코드를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> 만들려는 레코드 유형을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">팀 ID</td> 
   <td> 이 레코드를 소유할 팀의 ID를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">이름</td> 
   <td> 새 레코드의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 삭제

이 모듈은 지정된 레코드를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> 삭제할 레코드 유형을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td>다른 필드의 값을 입력합니다. 사용 가능한 필드는 선택한 레코드 유형에 따라 다릅니다. </td> 
  </tr> 
 </tbody> 
</table>

#### 목록 레코드

이 모듈은 커서 기반 페이징 및 속성 필터를 사용하여 페이징된 레코드 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td>목록을 반환할 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">속성</td> 
   <td>결과를 반환할 각 속성 필터에 대해 <b>항목 추가</b>를 클릭하고 필터링할 필드, 연산자 및 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">시작</td> 
   <td>반환된 결과를 시작할 위치를 입력합니다. 페이지 매김에 사용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 실행 주기에 대해 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">정렬 기준</td> 
   <td>결과 순서를 지정할 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">방향</td> 
   <td>결과의 순서를 오름차순으로 지정할지 아니면 내림차순으로 지정할지 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 읽기

이 모듈은 지정된 레코드를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> 삭제할 레코드 유형을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td>다른 필드의 값을 입력합니다. 사용 가능한 필드는 선택한 레코드 유형에 따라 다릅니다. </td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 업데이트

지정된 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> 업데이트할 레코드 유형을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">이름</td> 
   <td> 레코드에 대한 새 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td> 업데이트할 레코드의 ID를 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

### 내보내기

#### 활동 로그 내보내기

이 모듈은 활동 로그를 내보냅니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">파일 유형</td> 
   <td>로그를 내보낼 파일 형식을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">속성</td> 
   <td>결과를 반환할 각 속성 필터에 대해 <b>항목 추가</b>를 클릭하고 필터링할 필드, 연산자 및 값을 입력합니다. 필드의 존재 여부를 기준으로 필터링할 수도 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">시작</td> 
   <td>반환된 결과를 시작할 위치를 입력합니다. 페이지 매김에 사용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 실행 주기에 대해 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">정렬 기준</td> 
   <td>결과 순서를 지정할 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">방향</td> 
   <td>결과의 순서를 오름차순으로 지정할지 아니면 내림차순으로 지정할지 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [후크에 대한 대기열 통계 가져오기](#get-queue-statistics-for-a-hook)
* [레코드 종속성 가져오기](#get-record-dependencies)
* [연결에 대한 시나리오 나열](#list-scenarios-for-a-connection)
* [Fusion 지역 및 조직 나열](#list-the-fusion-regions-and-organizations)

#### 후크에 대한 대기열 통계 가져오기

이 모듈은 지정된 후크에 대한 대기열 통계(현재 대기열에 추가된 이벤트 수, 대기열 제한 및 후크 활성화 여부)를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  <tr> 
   <td role="rowheader">후크 ID</td> 
   <td> 세부 정보를 반환할 후크 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 종속성 가져오기

이 모듈은 레코드의 종속성을 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td> 종속성을 검색할 레코드 유형을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">시나리오 ID</td> 
   <td> 종속성을 검색할 레코드의 ID를 입력하거나 매핑합니다. </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### 연결에 대한 시나리오 나열

이 모듈은 지정된 연결을 참조하는 페이지 매김된 시나리오 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">연결 ID</td> 
   <td>시나리오를 반환할 연결의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">속성</td> 
   <td>결과를 반환할 각 속성 필터에 대해 <b>항목 추가</b>를 클릭하고 필터링할 필드, 연산자 및 값을 입력합니다. 필드의 존재 여부를 기준으로 필터링할 수도 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">시작</td> 
   <td>반환된 결과를 시작할 위치를 입력합니다. 페이지 매김에 사용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 실행 주기에 대해 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">정렬 기준</td> 
   <td>결과 순서를 지정할 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">방향</td> 
   <td>결과의 순서를 오름차순으로 지정할지 아니면 내림차순으로 지정할지 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### Fusion 지역 및 조직 나열

이 모듈은 연결에 사용된 자격 증명의 IMS 사용자 프로필에 있는 자격 증명 및 액세스를 기반으로 연결이 액세스할 수 있는 모든 Fusion 조직에 대한 지역 및 조직 ID를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront Fusion을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Workfront Fusion을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>





