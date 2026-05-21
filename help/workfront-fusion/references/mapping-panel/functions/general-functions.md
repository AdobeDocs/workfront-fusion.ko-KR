---
title: 일반 함수
description: Adobe Workfront Fusion 매핑 패널에서 다음과 같은 일반 기능을 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 478
ht-degree: 6%

---

# 일반 함수

## 변수

다음 일반 변수를 사용하여 실행에 대한 세부 사항을 식별할 수 있습니다.

* `executionID`: 이 시나리오 실행의 ID
* `triggerTimestamp`: 이 실행이 트리거된 시간
* `scenarioID`: 현재 열려 있는 시나리오의 ID
* `scenarioName`: 현재 실행 중인 시나리오의 이름
* `operationsConsumed`: 시나리오의 해당 지점에서 사용된 작업 수.

## [!UICONTROL get(개체 또는 배열, 경로)]

개체 또는 배열의 값 경로를 반환합니다. 중첩된 오브젝트에 액세스하려면 점 표기법을 사용하십시오. 배열의 첫 번째 항목은 인덱스 1입니다.

>[!BEGINSHADEBOX]

**예:**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expression; value1; value2)]

식이 true로 평가되면 `value1`을(를) 반환합니다. 그렇지 않으면 `value2`을(를) 반환합니다.

둘 이상의 식이 true로 평가되는 경우에만 값을 반환하는 if 문을 만들려면 `and` 키워드를 사용합니다.

`if` 문을 결합하려면 `and` 및 `or` 연산자를 사용합니다.

![and 연산자](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**예:**

* `if( 1 = 1 ; A ; B )`

  A 반환

* `if( 1 = 2 ; A ; B )`

  B 반환

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  B 반환

>[!ENDSHADEBOX]

## [!UICONTROL ifempty (value1; value2)]

이 값이 비어 있지 않으면 `value1`을(를) 반환합니다. 그렇지 않으면 `value2`을(를) 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `ifempty(` `A` `;` `B` )

  A 반환

* `ifempty(` `unknown` `;` `B` )

  B 반환

* `ifempty(` `""` `;` `B` )

  B 반환

>[!ENDSHADEBOX]

## [!UICONTROL switch(expression; value1; result1; [value2; result2; ...]; [else])]

값 목록에 대해 하나의 값(식이라고 함)을 평가하고 첫 번째 일치하는 값에 해당하는 결과를 반환합니다. `else` 값을 포함하려면 최종 식 또는 값 뒤에 추가하십시오.

>[!BEGINSHADEBOX]

**예:**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  반환 2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  반환 3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  반환 4

  이 함수에서 4는 식이 적용되지 않는 경우 반환되는 값입니다(`else` 값).

>[!ENDSHADEBOX]

## [!UICONTROL 생략(object; key1; [key2; ...])]

개체의 지정된 키를 생략하고 나머지 키를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

`omit(` 사용자 `;` 암호 `)`

암호를 제외한 사용자 정보의 컬렉션을 반환합니다.

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

개체에서 지정된 키만 선택합니다.

>[!BEGINSHADEBOX]

**예:**

`pick(` 사용자 `;` 암호 `;` 전자 메일 `)`

사용자의 암호와 전자 메일 주소만 모아 놓은 컬렉션을 반환합니다.

>[!ENDSHADEBOX]

## mergeCollections(collection1; collection2)

키-값 쌍을 결합하여 두 컬렉션을 병합합니다. 두 컬렉션에 동일한 키가 들어 있으면 두 번째 컬렉션의 값이 첫 번째 컬렉션의 값을 덮어씁니다.

### [!UICONTROL isBlank(value)]

값이 `null`이거나 빈 문자열이면 `true`을 반환하고, 그렇지 않으면 `false`을 반환합니다. `ifEmpty`과(와) 달리 이 함수는 숫자 `0` 또는 공백 전용 문자열을 공백으로 처리하지 않습니다.

>[!BEGINSHADEBOX]

**예:**

* `isBlank("")     `

  true 반환
* `isBlank(null)   `

  true 반환
* `isBlank("Hello")`

  false 반환
* `isBlank(0)      `

  false 반환
* `isBlank(" ")    `

  false 반환

>[!ENDSHADEBOX]


### [!UICONTROL in(value; value1; value2; ...)]

값이 제공된 값 중 하나와 같으면 `true`을(를) 반환합니다(엄격한 같음, 형식 강제 적용 없음).

>[!BEGINSHADEBOX]

**예:**

* `in("B"; "A"; "B"; "C")`

  true 반환
* `in("D"; "A"; "B"; "C")`

  false 반환
* `in(2; 1; 2; 3)        `

  true 반환
* `in("2"; 1; 2; 3)      `

  false 반환

>[!ENDSHADEBOX]

### [!UICONTROL ifin(value; value1; value2; ...; trueExpression; falseExpression)]

값이 제공된 일치 값과 일치하는 경우 `trueExpression`을(를) 반환하고, 그렇지 않으면 `falseExpression`을(를) 반환합니다. 최소 3개의 인수(값, 하나의 일치 값 및 trueExpression + falseExpression)가 필요합니다.

>[!BEGINSHADEBOX]

**예:**

* `ifin("B"; "A"; "B"; "yes"; "no")`

  예 반환
* `ifin("D"; "A"; "B"; "yes"; "no")`

  아니오 반환
* `ifin("X"; "X"; "found"; "not found")`

  반환 발견

>[!ENDSHADEBOX]

### [!UICONTROL case(indexNumber; value1; value2; ...)]

인덱스 번호(1 기반)로 지정된 위치의 값을 반환합니다. 인덱스가 범위를 벗어나거나 0인 경우 `null`을(를) 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `case(1; "Sun"; "Mon"; "Tue")`

  Sun 반환
* `case(2; "Sun"; "Mon"; "Tue")`

  월 반환
* `case(3; "Sun"; "Mon"; "Tue")`

  화요일 반환
* `case(5; "a"; "b")           `

  null 반환

>[!NOTE]
>
>날짜의 요일 이름을 가져오려면 이 항목을 사용하는 것이 좋습니다.
>`case(dayOfWeek(date); "Sun"; "Mon"; "Tue"; "Wed"; "Thu"; "Fri"; "Sat")`

>[!ENDSHADEBOX]

