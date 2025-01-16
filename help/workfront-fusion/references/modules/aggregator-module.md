---
title: 집계 모듈
description: 집계 모듈은 여러 데이터 번들을 단일 번들로 병합하도록 설계된 모듈 유형입니다.
author: Becky
feature: Workfront Fusion
exl-id: 93cde0d0-4013-463a-b19c-d58180632739
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# [!UICONTROL Aggregator] 모듈

집계 모듈은 여러 개의 데이터 번들을 하나의 번들로 병합하는 모듈입니다.

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
   <td> 새로운 기능: 표준<p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] 라이센스</td> 
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


보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## [!UICONTROL Aggregator] 모듈 개요

[!UICONTROL Aggregator] 모듈이 실행되면 다음을 수행합니다.

* 단일 소스 모듈의 작업에서 모든 번들을 누적합니다.
* 누적된 번들에 대해 하나의 항목을 포함하는 배열이 있는 단일 번들을 출력합니다. 배열 항목의 내용은 특정 [!UICONTROL Aggregator] 모듈과 해당 설정에 따라 다릅니다.

다음 이미지는 [!UICONTROL Aggregator] 모듈의 일반적인 설정을 보여 줍니다.

![](assets/array-aggregator.png)

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source Module]</p> </td> 
   <td> <p>번들 집계가 시작되는 모듈입니다. 소스 모듈은 일반적으로 반복자 또는 일련의 번들을 출력하는 검색 모듈이다.</p><p>애그리게이터의 소스 모듈을 설정하고 애그리게이터 설정을 닫으면 소스 모듈과 애그리게이터 모듈 사이의 경로가 회색 영역으로 줄바꿈되어 애그리게이션의 시작과 끝을 명확하게 볼 수 있습니다. 
   </p> <p>반복기에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator] 모듈</a>을 참조하세요.</p> 
   <p>검색 모듈에 대한 자세한 내용은 모듈 개요에서 <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#search-modules" class="MCXref xref">검색 모듈</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Target structure type]</p><p>[!UICONTROL Array aggregator] 모듈에만 적용됩니다.</p> </td> 
   <td> <p> 데이터가 집계되는 대상 구조입니다. 기본 옵션 [!UICONTROL Custom]을(를) 사용하면 [!UICONTROL Array aggregator]의 출력 번들의 <code>Array </code> 항목으로 집계할 항목을 선택할 수 있습니다.</p> <p> <img src="assets/output-bundle-array-item.png"> </p> <p>[!UICONTROL Array aggregator] 모듈 뒤에 더 많은 모듈을 연결하고 집계 모듈의 설정으로 돌아오면 [!UICONTROL Target] 구조 유형 드롭다운 메뉴에 '컬렉션 배열' 유형의 모든 모듈 및 해당 필드가 포함됩니다. <p>이 예제에서는 [!DNL Slack] &gt;[!UICONTROL Create a Message] 모듈의 [!UICONTROL Attachments] 필드가 Array aggregator &gt; Target 구조 유형 필드에 나타납니다. </p> <p> <img src="assets/array-aggregator-slack.png"> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aggregated fields]</td> 
   <td>집계 모듈 출력에 포함할 필드입니다.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>그룹화 기준 필드를 사용하여 하나 이상의 매핑된 항목이 포함된 표현식을 정의할 수 있습니다. 그런 다음 집계된 데이터가 표현식 값에 따라 그룹으로 구분됩니다. 각 그룹은 키와 데이터 배열이 포함된 별도의 번들로 출력합니다. 결과를 그룹화하면 키를 후속 모듈에서 필터로 사용할 수 있습니다.</p>
   <p>각 번들에는 두 개의 항목이 포함되어 있습니다.</p> 
    <ul> 
     <li><code>Key</code>: 그룹화 기준 값입니다.</li> 
     <li><code>Array</code>: 수식이 <code>Key</code> 값으로 평가된 번들의 집계된 데이터입니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>빈 집계 후 처리 중지</p> </td> 
   <td> <p>기본적으로 [!UICONTROL Aggregator] 모듈은 [!UICONTROL Aggregator] 모듈에 도달한 번들이 없는 경우에도 집계 결과를 출력합니다(예: 모든 번들이 집계를 포함하는 경로에서 필터링되었기 때문). [!UICONTROL Stop processing after an empty aggregation] 옵션을 사용하도록 설정한 경우 입력 번들이 없으면 [!UICONTROL Aggregator] 모듈에서 출력 번들을 생성하지 않습니다. 대신 흐름이 중지됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>원본 모듈과 [!UICONTROL Aggregator] 모듈 사이의 모듈에서 생성된 번들이 [!UICONTROL Aggregator] 모듈에서 출력되지 않습니다. [!UICONTROL Aggregator] 이후 흐름의 모듈에서 이러한 번들에 액세스할 수 없습니다. 원본 모듈과 [!UICONTROL Aggregator] 모듈 사이의 모듈에서 출력된 번들의 데이터가 필요한 경우 해당 항목을 [!UICONTROL Aggregator] 모듈의 설정(예: [!UICONTROL Array aggregator] 모듈의 설정의 [!UICONTROL Aggregated fields] 필드)에 포함해야 합니다.


## 집계자의 작동 방식에 대한 예제 시나리오

이 예제 시나리오는 모든 이메일 첨부 파일을 압축하고 ZIP을 [!DNL Dropbox]에 업로드하는 방법을 보여 줍니다.

![](assets/dropbox-archive.png)

아래 시나리오는 다음 방법을 보여 줍니다.

* 첫 번째 모듈은 수신 이메일에 대한 사서함을 감시합니다. [!UICONTROL Email] >[!UICONTROL Watch emails] 트리거는 `Attachments[]` 항목이 있는 번들을 출력합니다. 이 항목은 전자 메일의 모든 첨부 파일이 포함된 배열입니다.

* 두 번째 모델은 전자 메일의 첨부 파일을 반복합니다. [!UICONTROL Email] >[!UICONTROL Iterate attachments] 반복기는 `Attachments[]` 배열의 항목을 하나씩 가져와서 별도의 번들로 더 보냅니다.

* 세 번째 모듈은 집계자입니다. [!UICONTROL Email] >[!UICONTROL Iterate attachments] 모듈에서 출력된 번들을 집계합니다. [!UICONTROL Archive] >[!UICONTROL Create an archive aggregator]에서 받은 모든 번들을 누적하고 ZIP 파일이 포함된 단일 번들을 출력합니다.

* 마지막 모듈이 결과 ZIP 파일을 [!DNL Dropbox]에 업로드합니다.  [!DNL Dropbox] > [!UICONTROL Upload a file]이(가) [!UICONTROL Archive] > [!UICONTROL Create an archive] 모듈에서 ZIP 파일을 가져와서 [!DNL Dropbox]에 업로드합니다.



다음은 [!UICONTROL Archive] > [!UICONTROL Create an archive] 집계의 샘플 설정입니다.

![](assets/archive-create-an-archive.png)
