---
title: Workfront Fusion 릴리스 활동:&nbsp;2021년 8월 30일 주
description: Workfront Fusion 릴리스 활동:&nbsp;2021년 8월 30일 주
author: Luke
draft: Probably
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: cac11147-5b3d-477b-869b-e255528c4bec
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Workfront Fusion 릴리스 활동: 2021년 8월 30일 주

이 페이지에서는 2021년 8월 30일이 있는 주에 Adobe Workfront Fusion에서 향상된 모든 기능에 대해 설명합니다.

최근 모든 변경 사항의 목록은 [Adobe Workfront Fusion 릴리스 활동](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)을 참조하십시오.

Workfront Fusion의 최근 버그 수정 목록을 보려면 [Workfront 유지 관리 업데이트](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) 페이지를 참조하고 Workfront Fusion 유지 관리 업데이트 레이블이 지정된 업데이트를 확인하십시오.

## Workfront > 이벤트 보기 모듈을 트리거하는 이벤트 필터링

1. Workfront > 이벤트 보기 모듈을 트리거하는 이벤트에 대한 사용자 지정 필터를 설정합니다

   불필요한 시나리오 실행 수를 줄이기 위해 Workfront > 레코드 보기 모듈을 업데이트하여 이벤트 필터링을 활성화합니다. 이제 웹후크를 만들 때 필터를 설정할 수 있습니다. 이렇게 하면 이벤트가 특정 기준을 충족하는 경우에만 시나리오가 트리거될 수 있습니다.

   이벤트 필터는 현재 다음 작업을 제공합니다.

   * 같음: 이벤트가 필터의 조건과 일치하는 경우에만 시나리오를 트리거합니다. 예를 들어 이벤트가 특정 프로젝트에서 발생하는 경우에만 시나리오를 트리거하는 필터를 설정할 수 있습니다.
   * 같지 않음: 이벤트가 필터 조건과 일치하지 않는 경우에만 시나리오를 트리거합니다. 예를 들어에서 이벤트가 발생하는 문제가 닫힘 상태가 아닌 경우에만 시나리오를 트리거하는 필터를 만들 수 있습니다.

   이전에는 레코드 보기 모듈에서 모든 레코드를 검색했습니다. 사용자는 시나리오의 뒷부분에서 필터를 설정해야만 필터링할 수 있습니다.

   이벤트 필터링을 사용하려면 Watch 이벤트 모듈에서 새 웹후크를 만듭니다. 현재 이 기능을 포함하도록 기존 웹후크를 편집할 수 없습니다. 기존 시나리오에 대한 이벤트 필터를 사용하여 새 웹후크를 만드는 것이 좋습니다.

1. 현재 연결에 의해 트리거된 이벤트를 필터링합니다.

   웹 후크를 Workfront > 이벤트 보기 모듈에 대해 더 쉽게 설정할 수 있도록 가장 일반적인 이벤트 필터를 포함했습니다. 이제 Webhook에는 Watch 이벤트 모듈에 대해 지정된 연결을 사용하여 모듈에서 변경한 사항을 필터링하는 옵션이 있습니다. 즉, 이 필터가 활성화된 경우 해당 연결과 연결된 Workfront 사용자가 변경한 내용은 시나리오를 트리거할 수 없습니다.

   이전에는 이 필터를 사용할 수 없었습니다. 따라서 Workfront 모듈에서 변경한 사항이 이러한 모듈을 포함하는 시나리오를 트리거하는 것이 더 쉬웠으며, 이로 인해 시나리오가 무한 루프에서 자체적으로 트리거될 수 있습니다.
