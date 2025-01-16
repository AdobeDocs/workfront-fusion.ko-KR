---
title: 시나리오 계획 FAQ
description: 이 문서의 정보는 Workfront Fusion에서 시나리오를 만들 때 유용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 1%

---

# 시나리오 계획 FAQ

이 문서의 정보는 Workfront Fusion에서 시나리오를 만들 때 유용할 수 있습니다.

## 시나리오란 무엇입니까?

### 답변

시나리오는 Adobe Workfront Fusion에서 실행할 일련의 단계를 정의합니다. 각 시나리오에 대해 사용할 데이터 소스, 데이터 처리 방법을 지정합니다. Fusion을 사용하면 간단하거나 복잡한 시나리오를 만들어 조직의 사용 사례를 충족할 수 있습니다.

시나리오에 대한 자세한 내용은 [시나리오 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md)를 참조하십시오.

## 시나리오에 몇 개의 모듈을 사용할 수 있습니까?

### 답변

시나리오에 원하는 만큼 모듈을 사용할 수 있습니다. 모듈을 루트로 분리하고 각 루트를 통해 처리해야 하는 데이터를 지정할 수 있습니다. 한 모듈의 출력을 다른 모듈에 대한 입력으로 사용할 수도 있습니다.

시나리오의 모듈 수에는 제한이 없지만 150개 이상의 모듈이 시나리오 성능에 영향을 줄 수 있습니다.

모듈에 대한 자세한 내용은 [모듈 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md)를 참조하세요.

## [!DNL Workfront Fusion]이(가) 파일로 작업할 수 있습니까?

### 답변

예. Workfront Fusion은 파일을 수신, 저장, 변환, 변환 및 암호화할 수 있습니다. 또한 Fusion은 사용자가 파일에 포함된 데이터를 효과적이고 창의적으로 작업할 수 있도록 설계된 다양한 기본 제공 기능을 제공합니다.

Fusion에서 파일 작업에 대한 자세한 내용은 [모듈 간 파일 매핑](/help/workfront-fusion/create-scenarios/map-data/map-files.md)을 참조하십시오.

## 일부 트리거를 사용하면 시나리오를 즉시 실행할 수 있습니다. &#39;즉시&#39;는 무엇을 의미합니까?

### 답변

시나리오는 매 시간 또는 매 5분 등 사용자가 지정하는 일정에 따라 간격을 두고 실행될 수 있습니다. 특정 서비스로부터 데이터를 받은 후 즉시 시나리오를 시작할 수 있는 특수 트리거(웹후크)가 있습니다. Fusion은 다음 예약된 실행을 기다리지 않고 수신된 데이터를 즉시 처리합니다.

폴링된 트리거와 인스턴트 트리거 간의 차이에 대한 자세한 내용은 문서 모듈 개요에서 [트리거 모듈](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)을(를) 참조하십시오.

## 수술이란?

### 답변

작업은 모듈에서 수행되는 모든 작업입니다. 예를 들어 트리거가 실행될 때마다 작업이 작업을 수행할 때마다 작업이 발생합니다.

일부 Fusion 계획은 조직이 사용하는 작업 수를 기반으로 합니다.

작업에 대한 자세한 내용은 [작업](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md)을 참조하세요.

## 데이터 전송이란 무엇입니까?

### 답변

데이터 전송이란 시나리오를 통해 전송된 데이터의 양을 의미합니다. 예를 들어, Workfront에서 100KB 이미지를 검색한 다음 이미지를 문서 스토리지 공급자에게 업로드하는 시나리오입니다. 이 시나리오에서 사용되는 데이터의 양은 200KB입니다.

## 연결이란 무엇입니까?

### 답변

연결은 [!DNL Workfront Fusion] 계정과 사용할 서드파티 서비스 간의 연결입니다. 시나리오를 편집할 때 연결을 만들 수 있습니다.

자세한 내용은 [연결 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md)를 참조하십시오.

## 집계자란 무엇입니까?

### 답변

[!UICONTROL Aggregator]이(가) 데이터를 하나의 컬렉션으로 병합합니다. 예를 들어 파일이 zip 아카이브로 압축되어 이메일 첨부 파일로 전송되는 경우가 있습니다.

자세한 내용은 [[!UICONTROL Aggregator] 모듈](/help/workfront-fusion/references/modules/aggregator-module.md)을 참조하세요.

## [!DNL Workfront Fusion]에서 첨부 파일이 두 개 이상 포함된 전자 메일을 처리하도록 하면 어떻게 됩니까?

### 답변

[!UICONTROL Email] 모듈 [!UICONTROL Retrieve attachments]을(를) 사용하는 경우 시나리오의 나머지 모듈을 통해 각 첨부 파일이 개별적으로 전송됩니다. 여러 파일을 한 번에 수신하는 다른 앱에서도 유사한 모듈을 사용할 수 있습니다.
