---
title: 수학 함수
description: Adobe Workfront Fusion 매핑 패널에서 다음 수학 함수를 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# 수학 함수

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

특정 배열에 있는 숫자 값의 평균 값 또는 개별적으로 입력한 숫자 값의 평균 값을 반환합니다.

## [!UICONTROL ceil (number)]

지정된 숫자보다 크거나 같은 가장 작은 정수를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `ceil(` `1.2` `)`

  반환 2

* `ceil(` `4` `)`

  반환 4

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

지정된 숫자보다 작거나 같은 가장 큰 정수를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `floor(` `1.2` `)`

  1 반환

* `floor(` `1.9` `)`

  1 반환

* `floor(` `4` `)`

  반환 4

>[!ENDSHADEBOX]

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

지정된 배열에서 가장 큰 숫자를 반환하거나 개별적으로 입력한 숫자 중 가장 큰 숫자를 반환합니다.

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

지정된 배열에서 가장 작은 숫자를 반환하거나 개별적으로 입력한 숫자 중 가장 작은 숫자를 반환합니다.

## [!UICONTROL round (number)]

숫자 값을 가장 가까운 정수로 반올림합니다.

>[!BEGINSHADEBOX]

**예:**

* `round(` `1.2` `)`

  1 반환

* `round(` `1.5` `)`

  반환 2

* `round(` `1.7` `)`

  반환 2

* `round(` `2` `)`

  반환 2

>[!ENDSHADEBOX]

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

지정된 배열의 값 합계 또는 개별적으로 입력한 숫자 합계를 반환합니다.

## [!UICONTROL parseNumber (number; decimal separator)]

문자열을 숫자로 구문 분석하고 숫자를 반환합니다. 예를 들어 parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

요청한 형식으로 숫자를 반환합니다. 기본적으로 소수점은 쉼표(,)이고 천 단위 구분 기호는 마침표(.)입니다.

>[!BEGINSHADEBOX]

**예:**

`formatNumber( 123456789 ; 3 ; , ; . )`

반환 123.456.789,000

>[!ENDSHADEBOX]
