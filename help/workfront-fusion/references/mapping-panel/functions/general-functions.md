---
title: 일반 함수
description: Adobe Workfront Fusion 매핑 패널에서 다음과 같은 일반 기능을 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 일반 함수

## [!UICONTROL get (object or array; path)]

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

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

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

## [!UICONTROL omit(object; key1; [key2; ...])]

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
