---
title: ' [!DNL Adobe Workfront Fusion]의 데이터 저장소'
description: 데이터베이스 또는 간단한 테이블과 유사한 데이터 저장소는 시나리오의 데이터를 저장할 수 있으므로 개별 시나리오 또는 시나리오 실행 간에 데이터를 전송할 수 있습니다. 동기화 중에 데이터 저장소를 사용하여 다양한 시스템의 새 데이터를 저장할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 8bfa3201-45db-49d7-985d-9c324acd56b6
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1215'
ht-degree: 1%

---

# 데이터 저장소 만들기 및 관리

데이터베이스 또는 간단한 테이블과 유사한 데이터 저장소는 시나리오의 데이터를 저장할 수 있으므로 개별 시나리오 또는 시나리오 실행 간에 데이터를 전송할 수 있습니다. 동기화 중에 데이터 저장소를 사용하여 다양한 시스템의 새 데이터를 저장할 수 있습니다.

데이터 저장소 모듈을 사용하면 [!DNL Adobe Workfront Fusion] 데이터 저장소의 레코드에 대해 다음 작업을 수행할 수 있습니다.

* 추가
* 바꾸기
* 업데이트
* 검색
* 삭제
* 검색
* 계수

데이터 저장소 모듈 사용에 대한 자세한 내용은 [[!UICONTROL Data store]개 모듈](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md)을 참조하세요.

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

## 사용 가능한 데이터 공간

조직이 새로운 Workfront 플랜 모델(Select, Prime 및 Ultimate 패키지)에 있는 경우, 조직의 플랜은 Fusion 인스턴스에 사용할 수 있는 데이터 저장소의 크기와 수에 영향을 줍니다.

### Ultimate 플랜

Ultimate 패키지의 Fusion 인스턴스는 다음 항목을 수신합니다.

* 100MB 공간
* 50개 데이터 저장소

### 및 Prime 플랜 선택

Select 또는 Prime 패키지의 Fusion 인스턴스는 다음 항목을 수신합니다.—>

* 처음 500K 작업에는 100MB.

* 10K 작업을 추가로 수행할 때마다 10MB

  예를 들어, 600만 건의 작업을 수행하는 조직은 110MB를 수신합니다.

조직은 최대 50개의 데이터 저장소를 가질 수 있습니다. 이러한 데이터 저장소의 결합된 크기는 조직의 총 데이터 저장소 크기를 초과할 수 없습니다.

## [!DNL Workfront Fusion]에 데이터 저장소 만들기

* [데이터 저장소 설정](#set-up-the-data-store)
* [데이터 구조 설정](#set-up-the-data-structure)

### 데이터 저장소 설정

모듈에서 데이터 저장소를 사용하려면 먼저 [!DNL Workfront Fusion]에 데이터 저장소를 만들어야 합니다.

>[!NOTE]
>
>조직에 사용할 수 있는 데이터 저장소 수가 제한되어 있습니다. 사용 가능한 것보다 더 많은 데이터 저장소를 만들려고 하면 [!DNL Workfront]에서 [!UICONTROL Maximum stores reached] 오류를 반환합니다.
>
>자세한 내용은 이 문서에서 [최대 저장소 도달 오류](#maximum-stores-reached-error)를 참조하십시오.

1. [!DNL Workfront Fusion] 계정에 로그인합니다.
1. 왼쪽 탐색 패널에서 **[!UICONTROL Data stores]**&#x200B;을(를) 클릭합니다.
1. 화면 오른쪽 상단의 **[!UICONTROL Add data store]**&#x200B;을(를) 클릭합니다.
1. 새 데이터 저장소에 대한 설정을 입력하십시오.

   [!DNL Workfront Fusion] 모듈의 필드에 굵게 표시된 제목은 필수 설정을 나타냅니다.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data store name] </td> 
      <td> <p>데이터 저장소의 이름을 입력합니다. </p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Data Structure]</p> </td> 
      <td> <p>데이터 구조는 테이블의 열 목록입니다. 이 목록은 열 이름과 데이터 유형을 나타냅니다.</p> <p>다음 중 하나를 수행하십시오.</p> 
       <ul> 
        <li><b>이미 만들어진 데이터 구조 선택</b></li> 
        <li><b>새 데이터 구조 추가</b> <p>새 데이터 구조를 만들려면 <strong>[!UICONTROL Add]</strong>을(를) 클릭합니다.</p> <p>자세한 내용은 이 문서의 <a href="#set-up-the-data-structure" class="MCXref xref">데이터 구조 설정</a> 섹션을 참조하십시오.</p> </li> 
        <li style="font-weight: bold;"> <p>필드를 비워 둡니다.</p> <p style="font-weight: normal;">데이터 구조를 선택하거나 추가하지 않으면 데이터베이스에는 기본 키만 포함됩니다. 이러한 데이터베이스 유형은 키만 저장하고 특정 키가 데이터베이스에 있는지 여부만 알고 싶은 경우 유용합니다.</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>데이터 스토리지 크기(MB)</td> 
      <td> <p>전체 내부 데이터 저장소에서 데이터 저장소의 크기를 할당합니다.</p> <p> 기본값은 10MB입니다. 95MB 할당에서 할당되지 않은 데이터 저장소 공간이 10MB 미만인 경우 기본 크기는 할당되지 않은 저장소의 양입니다.  <p>참고: 예약된 금액은 언제든지 변경할 수 있습니다.</p>  </td> 
     </tr> 
    </tbody> 
   </table>

### 데이터 구조 설정

1. 데이터 저장소를 만들거나 편집할 때 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 표시되는 **[!UICONTROL Add data structure]** 상자에서 다음 필드를 구성합니다.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data structure name]</td> 
      <td> <p> 새 데이터 구조의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Specification]</p> </td> 
      <td> <p>다음 중 하나를 수행하여 데이터 저장소의 열을 설정합니다.</p> 
       <ul> 
        <li> <p>한 열의 속성을 수동으로 지정하려면 <strong>[!UICONTROL Add item]</strong>을(를) 클릭하십시오.</p> <p>데이터 저장소 열에 대한 <strong>[!UICONTROL Name]</strong> 및 <strong>[!UICONTROL Type]</strong>을(를) 입력하고 해당 속성을 정의합니다.</p> </li> 
        <li> <p>제공한 샘플 데이터에서 열을 확인하려면 <strong>[!UICONTROL Generator]</strong>을(를) 클릭하십시오.</p> 
         <div class="example" data-mc-autonum="<b>Example: </b>">
          <span class="autonumber"><span><b>예: </b></span></span> 
          <p>예를 들어 다음 JSON 샘플 데이터는 이름, 연령 및 전화번호의 세 가지 열을 만듭니다. 전화 번호는 모바일 및 유선 전화 번호의 컬렉션입니다.</p> 
          <p><code>&lbrace;</code> </p> 
          <p><code>"name":"John",</code> </p> 
          <p><code>"age":30,</code> </p> 
          <p><code>"phone number": &lbrace;</code> </p> 
          <p><code>"mobile":"987654321",</code> </p> 
          <p><code>"landline":"123456789"</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p>데이터 저장소 보기의 빈 열:</p> 
          <p> <img src="assets/empty-columns-350x132.png" style="width: 350;height: 132;"> </p> 
          <p>수동으로 또는 [!DNL Workfront Fusion] 데이터 저장소 모듈을 사용하여 데이터 저장소에 값을 추가할 수 있습니다.</p> 
         </div> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Strict] </td> 
      <td> <p>페이로드가 데이터 구조와 일치하는지 확인하려면 이 옵션을 활성화하십시오. 데이터 구조에 지정되지 않은 추가 항목이 포함된 페이로드는 거부됩니다.</p> </td> 
     </tr> 
    </tbody> 
   </table>

## 기존 데이터 저장소 편집

[!DNL Workfront Fusion]의 [!UICONTROL Data stores] 영역에서 기존 데이터 저장소의 속성 및 내용을 편집할 수 있습니다.

* [데이터 저장소의 속성 편집](#edit-the-properties-of-a-data-store)
* [데이터 저장소의 콘텐츠 편집](#edit-the-contents-of-a-data-store)

### 데이터 저장소의 속성 편집

데이터 저장소의 속성에는 데이터 저장소에서 사용하는 데이터 구조와 데이터 저장소의 크기가 포함됩니다.

1. 왼쪽 탐색 패널에서 **[!UICONTROL Data stores]** ![데이터 저장소 아이콘](assets/data-store-icon.png)을 클릭하여 [!UICONTROL Data stores] 영역을 엽니다.
1. 편집할 데이터 저장소 옆에 있는 **[!UICONTROL Edit]** ![데이터 저장소 편집](assets/data-store-edit.png)을 클릭합니다.
1. (선택 사항) 이 데이터 저장소에서 사용하는 데이터 구조를 다른 기존 데이터 구조로 변경하려면 **[!UICONTROL Data structure]** 드롭다운에서 선택합니다.

   또는

   (선택 사항) 이 데이터 저장소에서 사용하는 데이터 구조를 완전히 새로운 데이터 구조로 변경하려면 이 문서에서 [데이터 구조 설정](#set-up-the-data-structure)을 참조하십시오.

1. (선택 사항) **[!UICONTROL Data storage size in MB]** 필드에 새 크기를 입력하여 데이터 저장소의 크기를 변경합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

### 데이터 저장소의 콘텐츠 편집

1. 왼쪽 탐색 패널에서 **[!UICONTROL Data Store]** 아이콘 ![데이터 저장소 아이콘](assets/data-store-icon.png)을 클릭하여 [!UICONTROL Data Store] 영역을 엽니다.
1. 편집할 데이터 저장소 옆의 **[!UICONTROL Browse]**&#x200B;을(를) 클릭합니다.
1. (선택 사항) 열을 원하는 위치로 끌어 열 순서를 변경합니다.
1. (선택 사항) 해당 셀에서 **[!UICONTROL Edit]** 아이콘을 클릭한 다음 원하는 값을 입력하여 단일 셀을 [!UICONTROL Edit]합니다.
1. (선택 사항) **[!UICONTROL Add]**&#x200B;을(를) 클릭한 다음 새 항목에 대한 정보를 입력하여 데이터 저장소에 새 항목을 추가합니다.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 문제 해결

* [데이터 저장소에서 손실된 데이터 복원](#restoring-lost-data-from-a-data-store)
* [공간 부족 오류](#out-of-space-error)
* [최대 저장소 도달 오류](#maximum-stores-reached-error)

### 데이터 저장소에서 손실된 데이터 복원

현재 손실 된 데이터 복원을 자동화할 수 있는 도구는 없습니다.

#### 해결 방법

1. 데이터 저장소에 항목이 삽입된 시나리오의 모든 실행 로그를 검사합니다.

   실행 로그 검사에 대한 자세한 내용은 [시나리오의 실행 기록 보기](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md)를 참조하십시오.

1. 데이터를 복사합니다.
1. 데이터를 데이터 저장소에 다시 삽입합니다.

   데이터 저장소에 데이터를 삽입하는 방법에 대한 자세한 내용은 이 문서에서 [데이터 저장소의 내용 편집](#edit-the-contents-of-a-data-store)을 참조하십시오.

### [!UICONTROL Out of space] 오류

이전에 만든 데이터 저장소에 이미 할당된 데이터 저장소 저장소가 할당되었으므로 [!UICONTROL Out of Space] 오류가 발생합니다.

#### 해결 방법

1. 더 적은 공간을 사용하도록 기존 데이터 저장소를 편집합니다. 이렇게 하면 새 데이터 저장소에 대한 공간이 확보됩니다.

   자세한 내용은 이 문서에서 [데이터 저장소의 속성 편집](#edit-the-properties-of-a-data-store)을 참조하십시오.

>[!NOTE]
>
>추가 데이터 저장소가 필요하지 않다고 확신하지 않는 한 모든 공간을 단일 데이터 저장소에 할당하지 않는 것이 좋습니다.

### [!UICONTROL Maximum stores reached] 오류

조직에서 사용 가능한 모든 데이터 저장소를 사용했기 때문에 [!UICONTROL Maximum stores reached] 오류가 발생합니다.

#### 해결 방법

기존 데이터 저장소 수를 줄이려면 다음 중 하나를 수행하는 것이 좋습니다.

* 기존 데이터 저장소 결합
* 사용하지 않는 데이터 저장소 삭제
