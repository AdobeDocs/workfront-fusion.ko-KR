---
title: 집계 모듈
description: 집계 모듈은 여러 데이터 번들을 단일 번들로 병합하도록 설계된 모듈 유형입니다.
author: Becky
feature: Workfront Fusion
exl-id: 93cde0d0-4013-463a-b19c-d58180632739
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# [!UICONTROL 집계] 모듈

집계 모듈은 여러 개의 데이터 번들을 하나의 번들로 병합하는 모듈입니다.

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
   <td> 새로운 기능: 표준<p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] 라이선스</td> 
   <td>
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 모두 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>[!UICONTROL Select] 또는 [!UICONTROL Prime] Workfront 플랜: 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li><li>[!UICONTROL Ultimate] Workfront 계획: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>


보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 Workfront 관리자에게 문의하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## [!UICONTROL 집계] 모듈 개요

[!UICONTROL 집계] 모듈이 실행되면 다음을 수행합니다.

* 단일 소스 모듈의 작업에서 모든 번들을 누적합니다.
* 누적된 번들에 대해 하나의 항목을 포함하는 배열이 있는 단일 번들을 출력합니다. 배열 항목의 내용은 특정 [!UICONTROL 집계] 모듈과 그 설정에 따라 다릅니다.

다음 이미지는 [!UICONTROL 집계] 모듈의 일반적인 설정을 보여 줍니다.

![배열 집계](assets/array-aggregator.png)

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source Module]</p> </td> 
   <td> <p>번들 집계가 시작되는 모듈입니다. 소스 모듈은 일반적으로 반복자 또는 일련의 번들을 출력하는 검색 모듈이다.</p><p>애그리게이터의 소스 모듈을 설정하고 애그리게이터 설정을 닫으면 소스 모듈과 애그리게이터 모듈 사이의 경로가 회색 영역으로 줄바꿈되어 애그리게이션의 시작과 끝을 명확하게 볼 수 있습니다. 
   </p> <p>반복기에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL 반복기] 모듈</a>을(를) 참조하십시오.</p> 
   <p>검색 모듈에 대한 자세한 내용은 모듈 개요에서 <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#search-modules" class="MCXref xref">검색 모듈</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Target 구조 유형]</p><p>([!UICONTROL Array Aggregator] 모듈에만 적용됩니다.)</p> </td> 
   <td> <p> 데이터가 집계되는 대상 구조입니다. 기본 옵션인 [!UICONTROL Custom]을(를) 사용하면 [!UICONTROL Array Aggregator]의 출력 번들의 <code>Array </code>개 항목으로 집계할 항목을 선택할 수 있습니다.</p> <p> <img src="assets/output-bundle-array-item.png"> </p> <p>[!UICONTROL Array aggregator] 모듈 다음에 더 많은 모듈을 연결하고 집계 모듈의 설정으로 돌아오면 [!UICONTROL Target] 구조 유형 드롭다운 메뉴에 '컬렉션 배열' 유형인 다음 모듈과 해당 필드가 모두 포함됩니다. <p>이 예에서는 [!DNL Slack] &gt;[!UICONTROL 메시지 작성] 모듈의 [!UICONTROL 첨부 파일] 필드가 배열 집계 &gt; 대상 구조 유형 필드에 나타납니다. </p> <p> <img src="assets/array-aggregator-slack.png"> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 집계된 필드]</td> 
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
   <td> <p>기본적으로 [!UICONTROL Aggregator] 모듈은 [!UICONTROL Aggregator] 모듈에 도달한 번들이 없는 경우에도 집계 결과를 출력합니다(예: 모두 집계기가 포함된 경로에서 필터링되었기 때문). 빈 집계 후 [!UICONTROL 처리 중지] 옵션을 활성화하면 입력 번들이 없을 때 [!UICONTROL 집계] 모듈에서 출력 번들을 생성하지 않습니다. 대신 흐름이 중지됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>원본 모듈과 [!UICONTROL 집계] 모듈 사이의 모듈에서 생성된 번들이 [!UICONTROL 집계] 모듈에서 출력되지 않습니다. [!UICONTROL 집계] 이후 흐름의 모듈에서 이러한 번들에 액세스할 수 없습니다. 소스 모듈과 [!UICONTROL 집계] 모듈 사이의 모듈에서 출력된 번들의 데이터가 필요한 경우 [!UICONTROL 집계] 모듈의 설정에 해당 항목을 포함해야 합니다([!UICONTROL 배열 집계] 모듈의 설정에서 [!UICONTROL 집계된 필드] 필드).


## 집계자의 작동 방식에 대한 예제 시나리오

이 예제 시나리오는 모든 이메일 첨부 파일을 압축하고 ZIP을 [!DNL Dropbox]에 업로드하는 방법을 보여 줍니다.

![Dropbox 보관 예제](assets/dropbox-archive.png)

아래 시나리오는 다음 방법을 보여 줍니다.

* 첫 번째 모듈은 수신 이메일에 대한 사서함을 감시합니다. [!UICONTROL 전자 메일] >[!UICONTROL 전자 메일 보기] 트리거는 모든 전자 메일의 첨부 파일이 포함된 배열인 `Attachments[]` 항목이 있는 번들을 출력합니다.

* 두 번째 모델은 전자 메일의 첨부 파일을 반복합니다. [!UICONTROL 전자 메일] >[!UICONTROL 첨부 파일 반복] 반복기는 `Attachments[]` 배열의 항목을 하나씩 가져와서 별도의 번들로 더 보냅니다.

* 세 번째 모듈은 집계자입니다. [!UICONTROL 전자 메일] >[!UICONTROL 첨부 파일 반복] 모듈에서 출력된 번들을 집계합니다. [!UICONTROL 보관] >[!UICONTROL 보관 집계 만들기]에서 받은 모든 번들을 모아 ZIP 파일이 포함된 단일 번들을 출력합니다.

* 마지막 모듈이 결과 ZIP 파일을 [!DNL Dropbox]에 업로드합니다.  [!DNL Dropbox] > [!UICONTROL 파일 업로드] [!UICONTROL 보관] > [!UICONTROL 보관 만들기] 모듈에서 ZIP 파일을 가져와 [!DNL Dropbox]에 업로드합니다.



다음은 [!UICONTROL 보관] > [!UICONTROL 보관 만들기] 집계의 샘플 설정입니다.

![보관 만들기](assets/archive-create-an-archive.png)
