---
title: 수학 함수
description: Adobe Workfront Fusion 매핑 패널에서 다음 수학 함수를 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
TQID: https://experienceleague.adobe.com/a0WYFvPFBnXOvKS9ndQ-TD5xSvJz2bCbUbDY5VnXW0w
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 404
ht-degree: 6%

---

# 수학 함수

## [!UICONTROL 평균([값 배열]) 평균(value1; [값2], ...)]

특정 배열에 있는 숫자 값의 평균 값 또는 개별적으로 입력한 숫자 값의 평균 값을 반환합니다.

## [!UICONTROL ceil(숫자)]

지정된 숫자보다 크거나 같은 가장 작은 정수를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `ceil(` `1.2` `)`

  반환 2

* `ceil(` `4` `)`

  반환 4

>[!ENDSHADEBOX]

## [!UICONTROL 층(숫자)]

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

## [!UICONTROL max([값 배열]), max(value1;value2; ...)]

지정된 배열에서 가장 큰 숫자를 반환하거나 개별적으로 입력한 숫자 중 가장 큰 숫자를 반환합니다.

## [!UICONTROL 분([값 배열]), min(value1; value2; ...)]

지정된 배열에서 가장 작은 숫자를 반환하거나 개별적으로 입력한 숫자 중 가장 작은 숫자를 반환합니다.

## [!UICONTROL 라운드(숫자)]

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

## [!UICONTROL 합계([값 배열]), sum(value1; value2; ...)]

지정된 배열의 값 합계 또는 개별적으로 입력한 숫자 합계를 반환합니다.

## [!UICONTROL parseNumber(숫자, 소수점 구분 기호)]

문자열을 숫자로 구문 분석하고 숫자를 반환합니다. 예를 들어 parseNumber(1 756,456;,)

## [!UICONTROL formatNumber(number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

요청한 형식으로 숫자를 반환합니다. 기본적으로 소수점은 쉼표(,)이고 천 단위 구분 기호는 마침표(.)입니다.

>[!BEGINSHADEBOX]

**예:**

`formatNumber( 123456789 ; 3 ; , ; . )`

반환 123.456.789,000

>[!ENDSHADEBOX]

### [!UICONTROL abs(number)]

[!BADGE 새로 만들기!]{type=Informative}

숫자의 절대값을 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `abs(-3.14)`

  3.14 반환
* `abs(3.14)`

  3.14 반환


### [!UICONTROL div(number1; number2; ...)]

[!BADGE 새로 만들기!]{type=Informative}

제공된 순서대로 모든 숫자를 나눕니다.

>[!BEGINSHADEBOX]

**예:**

* `div(10; 2)`

  5 반환
* `div(100; 5; 4)`

  5 반환


### [!UICONTROL ln(숫자)]

[!BADGE 새로 만들기!]{type=Informative}

숫자의 자연 로그를 반환합니다.


>[!BEGINSHADEBOX]

**예:**

* `ln(1)`

  0 반환
* `ln(2.718281828)`

  1 반환


### [!UICONTROL log(number1; number2)]

[!BADGE 새로 만들기!]{type=Informative}

밑이 `number1`인 로그값 `number2`을(를) 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `log(10; 100)`

  반환 2
* `log(2; 8)`

  반환 3


### [!UICONTROL number(string)]

[!BADGE 새로 만들기!]{type=Informative}

문자열을 숫자로 변환합니다.

>[!BEGINSHADEBOX]

**예:**

* `number("3.14")`

  3.14 반환
* `number("42")`

  반환 42


### [!UICONTROL 전원(숫자; 전원)]

[!BADGE 새로 만들기!]{type=Informative}

지정된 거듭제곱으로 올림된 숫자를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `power(2; 3)`

  반환 8
* `power(4; 0.5)`

  반환 2


### [!UICONTROL prod(number1; number2; ...)]

[!BADGE 새로 만들기!]{type=Informative}

제공된 모든 숫자를 함께 곱합니다.

>[!BEGINSHADEBOX]

**예:**

* `prod(2; 3; 4)`

  반환 24
* `prod(5; 5)`

  반환 25


### [!UICONTROL sortAscNum(number1; number2; ...)]

[!BADGE 새로 만들기!]{type=Informative}

제공된 숫자를 오름차순으로 정렬하여 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `sortAscNum(3; 1; 2)`

  반환: \[1, 2, 3]
* `sortAscNum(5; 3; 4)`

  반환: \[3, 4, 5]


### [!UICONTROL sortDescNum(number1; number2; ...)]

[!BADGE 새로 만들기!]{type=Informative}

제공된 숫자를 내림차순으로 정렬하여 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `sortDescNum(3; 1; 2)`

  반환: \[3, 2, 1]
* `sortDescNum(5; 3; 4)`

  반환: \[5, 4, 3]


### [!UICONTROL sqrt(숫자)]

[!BADGE 새로 만들기!]{type=Informative}

숫자의 제곱근을 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `sqrt(9)`

  반환 3
* `sqrt(4)`

  반환 2


### [!UICONTROL sub(number1; number2; ...)]

[!BADGE 새로 만들기!]{type=Informative}

제공된 순서대로 모든 숫자를 뺍니다.

>[!BEGINSHADEBOX]

**예:**

* `sub(10; 3; 2)`

  5 반환
* `sub(20; 5)`

  15 반환
