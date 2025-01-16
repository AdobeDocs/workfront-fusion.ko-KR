---
title: 모듈 개요
description: Adobe Workfront Fusion은 작업 모듈, 검색 모듈, 트리거 모듈, 집계기 및 반복기의 5가지 모듈 유형을 구별합니다. 집계기 및 반복기는 고급 시나리오용입니다.
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# 모듈 개요

Adobe Workfront Fusion은 5가지 유형의 모듈을 구별합니다.

* 작업 모듈
* 모듈 검색
* 트리거 모듈
* 집계자
* 반복기

집계기 및 반복기는 고급 시나리오용입니다.

## 작업 모듈

작업 모듈은 가장 일반적인 모듈 유형입니다. 일반적인 작업 모듈은 작업을 수행하고 단일 번들을 반환한 다음 처리를 위해 다음 모듈로 전달합니다.

트리거 모듈과 달리 작업 모듈은 시나리오의 시작, 중간 또는 끝에 배치할 수 있습니다.

시나리오에는 작업 모듈의 개수가 무제한으로 포함될 수 있지만 모듈(150+)의 개수가 많으면 성능에 영향을 줄 수 있습니다.

>[!BEGINSHADEBOX]

**예:**

* **[!DNL Workfront]>[!UICONTROL Upload a file]**&#x200B;에서 [!DNL Workfront]에 파일을 보내고 해당 식별자를 반환합니다.
* **[!UICONTROL Image]>[!UICONTROL Resize]**&#x200B;이(가) 이미지를 받고 지정된 크기로 크기를 조정한 후 다음 작업에 크기 조정된 이미지를 전달합니다.

>[!ENDSHADEBOX]

작업 유형에는 다음과 같은 네 가지 하위 유형이 있습니다.

* 만들기
* 읽기
* 업데이트
* 삭제

업데이트 하위 유형에는 다음 세 가지 작업이 포함됩니다.

* **필드의 내용을 지웁니다**. 이 작업은 필드의 내용이 `erase` 키워드로 평가될 때 수행됩니다(`empty`과 혼동하지 않도록 함).

  ![키워드 지우기](assets/erase-content-of-field.png)

* **필드의 내용을 변경하지 않고 둡니다**. 이 작업은 필드가 비어 있거나 필드의 내용이 비어 있는 것으로 평가될 때(JSON에서 null을 통해 표시됨) 발생합니다.

  ![빈 번들](assets/leave-content-field-unchanged.png)

* **필드의 내용을 바꿉니다**. 이 작업은 상술한 두 가지 경우 이외의 모든 경우에 발생합니다.

>[!NOTE]
>
>* 매핑 패널에 `erase` 키워드가 표시되지 않으면 모듈이 업데이트 모듈이 아니거나 앱에 대한 최신 사양으로 업데이트되지 않은 것입니다.
>* `Empty`은(는) 필드 콘텐츠를 변경하지 않습니다. 필드를 지워야 하는 경우 다음 공식을 사용할 수 있습니다.
>
>   ![비어 있는 경우](assets/formula-ifempty-name-erase.png)
>
>* 콘텐츠가 비어 있는 것으로 평가될 때 필드를 변경하지 않고 남겨 두는 것은 현재 지원되지 않습니다.

## 모듈 검색

검색 모듈은 0개, 1개 또는 그 이상의 번들을 반환하고, 그런 다음 처리를 위해 다음 모듈로 전달합니다.

검색 모듈은 시나리오의 시작, 중간 또는 끝에 배치할 수 있습니다.

시나리오에는 검색 모듈이 무제한으로 포함될 수 있지만 모듈(150+)의 개수가 많으면 성능에 영향을 줄 수 있습니다.

>[!BEGINSHADEBOX]

**예:**

**[!DNL Workfront]>[!UICONTROL Read Related Records]**&#x200B;은(는) 지정한 검색 쿼리와 일치하는 레코드를 특정 상위 개체에서 읽습니다.

>[!ENDSHADEBOX]

## 트리거 모듈

트리거는 레코드 생성이나 업데이트와 같은 해당 서비스가 변경된 경우 번들을 생성합니다.

트리거는 0개, 1개 또는 그 이상의 번들을 반환하고, 그런 다음 처리를 위해 다음 모듈로 전달됩니다.

트리거를 사용하면 시나리오가 실행을 시작하기 때문에 시나리오의 시작 위치에만 배치할 수 있습니다.

각 시나리오에는 하나의 트리거만 포함될 수 있습니다.

[!DNL Workfront Fusion]은(는) 폴링 트리거와 인스턴트 트리거라는 두 가지 유형의 트리거를 사용합니다.

### 폴링 트리거

폴링 트리거는 이전 시나리오 실행 이후 변경 사항이 없더라도 지정된 서비스를 정기적으로 폴링합니다. 폴링 트리거가 포함된 시나리오를 정기적으로 실행하도록 예약하는 것이 좋습니다. 트리거의 구성과 일치하는 변경 사항이 있으면 트리거는 변경 사항에 대한 정보가 포함된 번들을 반환합니다. 구성과 일치하는 변경 사항이 없으면 트리거에서 번들을 출력하지 않습니다.

시나리오 예약에 대한 지침은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하십시오.

폴링 트리거를 사용하면 트리거를 저장하거나 트리거 설정을 변경한 후 자동으로 표시되는 패널을 통해 출력해야 하는 첫 번째 번들을 선택할 수 있습니다. 이 선택은 모듈의 첫 번째 실행에만 영향을 줍니다. 모듈이 한 번 실행된 후 후속 실행은 가장 최근 실행 후 발생하는 변경 사항만 감시합니다.

자세한 내용은 [트리거 모듈의 시작 위치 선택](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md)을 참조하세요.

>[!BEGINSHADEBOX]

**예:**

* **[!DNL Workfront]>[!UICONTROL Watch records]**&#x200B;은(는) 시나리오가 마지막으로 실행된 이후에 새로 추가된 레코드를 반환합니다.

* **[!DNL Google Sheets]>[!UICONTROL Watch Rows]**&#x200B;은(는) 시나리오가 마지막으로 실행된 후에 추가된 새 행을 반환합니다.

>[!ENDSHADEBOX]

### 인스턴트 트리거

인스턴트 트리거를 사용하면 서비스가 변경 내용이 발생한 직후에 변경 내용을 [!DNL Workfront Fusion]에 알릴 수 있습니다. 즉시 트리거가 포함된 시나리오를 즉시 실행하도록 예약하는 것이 좋습니다.

지침은 [시나리오 예약](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)을 참조하세요.

들어오는 데이터를 인스턴트 트리거로 처리하는 방법에 대한 자세한 내용은 [인스턴트 트리거(웹후크)](/help/workfront-fusion/references/modules/webhooks-reference.md)를 참조하십시오.

>[!BEGINSHADEBOX]

**예:**

* **[!DNL Workfront]>[!UICONTROL Watch Events]**&#x200B;은(는) 작업 만들기와 같은 특정 유형의 이벤트가 Workfront에서 발생할 때 정보를 반환합니다.
* **[!DNL Google Sheets]>[!UICONTROL Watch Changes]**&#x200B;은(는) 셀이 업데이트될 때마다 정보를 반환합니다.

>[!ENDSHADEBOX]

## 집계자

취합기 모듈은 여러 번들을 단일 번들로 취합합니다.

집계자는 하나의 번들만 반환하며, 그런 다음 추가 처리를 위해 다음 모듈로 전달됩니다.

집계자는 시나리오 중간에만 배치할 수 있습니다.

시나리오에는 집계가 무제한으로 포함될 수 있지만 모듈(150+)의 개수가 많으면 성능에 영향을 줄 수 있습니다.

>[!BEGINSHADEBOX]

**예:**

* **[!UICONTROL Archive]>[!UICONTROL Create an archive]**&#x200B;에서 여러 파일을 zip 아카이브로 압축합니다.
* **[!UICONTROL CSV]>[!UICONTROL Aggregate to CSV]**&#x200B;이(가) CSV 파일의 여러 문자열을 단일 행으로 병합합니다.
* **[!UICONTROL Tools]>[!UICONTROL Text aggregator]**&#x200B;은(는) 여러 문자열을 하나의 문자열로 결합합니다.

>[!ENDSHADEBOX]

자세한 내용은 [집계 모듈](/help/workfront-fusion/references/modules/aggregator-module.md)을 참조하세요.

## 반복기

반복자는 배열을 별도의 번들로 분할하는 모듈 유형입니다.

반복기는 하나 이상의 번들을 반환한 다음, 처리를 위해 다음 모듈로 전달합니다.

반복기는 시나리오 중간에만 배치할 수 있습니다.

시나리오에는 반복기를 무제한으로 포함할 수 있지만 모듈(150+)이 많으면 성능에 영향을 줄 수 있습니다.

>[!BEGINSHADEBOX]

**예:**

**[!UICONTROL Email]>[!UICONTROL Retrieve attachments]**&#x200B;에서 첨부 파일 배열을 개별 번들로 나눕니다.

>[!ENDSHADEBOX]

자세한 내용은 [반복자 모듈](/help/workfront-fusion/references/modules/iterator-module.md) 및 [배열 매핑](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)을 참조하십시오.
