---
title: 배열 함수
description: Adobe Workfront Fusion 매핑 패널에서 다음 배열 함수를 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: 9b61a3b18df1f755cc7ccc28889564e4bcb6cda0
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# 배열 함수

## [!UICONTROL 조인(배열, 구분 기호)]

각 항목 사이에 지정된 구분 기호를 사용하여 배열의 모든 항목을 문자열로 연결합니다.

## [!UICONTROL 길이(배열)]

배열의 항목 수를 반환합니다.

## [!UICONTROL 키(개체)]

특정 개체 또는 배열의 속성 배열을 반환합니다.

## [!UICONTROL 슬라이스(배열; 시작; [끝])]

선택한 항목만 포함하는 새 배열을 반환합니다.

## [!UICONTROL 병합(array1; array2; ...)]

하나 이상의 배열을 하나의 배열로 병합합니다.

## [!UICONTROL 포함(배열; 값)]

배열에 값이 포함되어 있는지 확인합니다.

## [!UICONTROL 제거(array; value1; value2; ...)]

배열의 매개 변수에 지정된 값을 제거합니다. 이 함수는 텍스트나 숫자의 기본 배열에만 적용됩니다.

## [!UICONTROL add(array; value1; value2; ...)]

매개 변수에 지정된 값을 배열에 추가하고 해당 배열을 반환합니다.

## [!UICONTROL 맵(복합 배열; 키;[필터링용 키];[필터링용 가능한 값])]

복합 배열의 값을 포함하는 기본 배열을 반환합니다. 이 함수를 사용하면 값을 필터링할 수 있습니다. 키에 원시 변수 이름을 사용합니다.

>[!BEGINSHADEBOX]

**예:**

* `map(Emails[];email)`

  이메일이 포함된 기본 배열을 반환합니다.

* `map(Emails[];email;label;work)`

  작업과 동일한 레이블을 갖는 이메일이 포함된 기본 배열을 반환합니다.

>[!ENDSHADEBOX]

자세한 내용은 [배열 또는 배열 요소 매핑](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)을 참조하십시오.

## 무작위 재생

## [!UICONTROL 정렬(배열; [순서]; [키])]

배열의 값을 정렬합니다. `order` 매개 변수의 올바른 값은 다음과 같습니다.

* `asc`

  (기본값) - 숫자 유형의 오름차순: 1, 2, 3, ... A, B, C, a, b, c, ... (텍스트 유형)

* `desc`

  내림차순: ..., 3, 2, 1(숫자 유형). ..., c, b, a, C, B, A(텍스트 유형).

* `asc ci`

  대/소문자를 구분하지 않는 오름차순: Text 유형의 경우 A, a, B, b, C, c, ...

* `desc ci`

  대소문자를 구분하지 않는 내림차순: ..., C, B, b, A, a(텍스트 유형).

복잡한 개체 내의 속성에 액세스하려면 `key` 매개 변수를 사용하십시오.

키에 원시 변수 이름을 사용합니다.

중첩된 속성에 액세스하려면 점 표기법을 사용하십시오.

배열의 첫 번째 항목은 인덱스 1입니다.

>[!BEGINSHADEBOX]

**예:**

* `sort(Contacts[];name)`

  기본 오름차순으로 &quot;name&quot; 속성을 기준으로 연락처 배열 정렬

* `sort(Contacts[];desc;name)`

  &quot;name&quot; 속성을 기준으로 연락처 배열을 내림차순으로 정렬합니다.

* `sort(Contacts[];asc ci;name)`

  대소문자를 구분하지 않는 오름차순으로 &quot;name&quot; 속성으로 연락처 배열 정렬

* `sort(Emails[];sender.name)`

  &quot;sender.name&quot; 속성별로 이메일 배열 정렬

>[!ENDSHADEBOX]

## [!UICONTROL 역방향(배열)]

배열의 첫 번째 요소는 마지막 요소가 되고, 두 번째 요소는 다음-마지막 요소가 됩니다.

## [!UICONTROL 병합(배열)]

지정된 깊이까지 모든 하위 배열 요소가 재귀적으로 연결된 새 배열을 만듭니다.

## [!UICONTROL distinct(배열; [키])]

배열 내의 중복을 제거합니다. 복잡한 개체 내의 속성에 액세스하려면 &quot;[!UICONTROL key]&quot; 인수를 사용하십시오. 중첩된 속성에 액세스하려면 점 표기법을 사용하십시오. 배열의 첫 번째 항목은 인덱스 1입니다.

>[!BEGINSHADEBOX]

**예:** `distinct(Contacts[];name)`

&quot;name&quot; 속성을 비교하여 연락처 배열 내의 중복을 제거합니다.

>[!ENDSHADEBOX]

## toCollection

* 이 함수는 키-값 쌍을 포함하는 배열을 가져와 컬렉션으로 변환합니다. 함수에는 3개의 인수가 있습니다.

* (배열) 키 값 쌍이 포함된 경우
* (문자열) 키로 사용할 필드의 이름
* (문자열) 값으로 사용할 필드의 이름

>[!BEGINSHADEBOX]

예:

지정된 배열:

```
[{"name":"Bob", "age":22}, {"name":"Tim", "age":23}]
```

및 인수

```
{{toCollection(6.array; "name"; "age")}}
```

함수는 를 반환합니다.

```
{
    "Bob": 22,
    "Tim": 23
}
```

>[!ENDSHADEBOX]

## toArray

이 함수는 컬렉션을 키-값 쌍의 배열로 변환합니다.

>[!BEGINSHADEBOX]

**예:**

주어진 컬렉션

`{ key1: "value1", key2: "value2:}`

함수

`toArray({ key1: "value1", key2: "value2:})`

키-값 쌍의 배열 반환

`[{ key1: "value1"}, { key2: "value2"}]`

>[!ENDSHADEBOX]

## [!UICONTROL arrayDifference [array1, array2, mode]]

두 배열 간의 차이점을 반환합니다.

`mode` 매개 변수에 대해 다음 값 중 하나를 입력하십시오.

* `classic`: `array1`에 없는 `array2`의 모든 요소를 포함하는 새 배열을 반환합니다.

* `symmetric`: 두 배열에 공통되지 않는 요소의 배열을 반환합니다.

  즉, 이 함수는 `array1`에 없는 `array2`의 모든 요소와 `array2`에 없는 `array1`의 모든 요소를 포함하는 배열을 반환합니다.

>[!BEGINSHADEBOX]

**예:**

다음 배열이 지정된 경우:

```
myArray = [1,2,3,4,5]
```

```
yourArray = [3,4,5,6,7]
```

* `arrayDifference [myArray, yourArray, classic]`

  `[1,2]` 반환

* `arrayDifference [yourArray, myArray, classic]`

  `[6,7]` 반환

* `arrayDifference [myArray, yourArray, symmetric]`

  `[1,2,6,7]` 반환

>[!ENDSHADEBOX]

## 중복 제거

## 키워드

## emptyarray
