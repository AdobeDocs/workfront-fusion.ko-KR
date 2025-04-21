---
title: 날짜 및 시간 함수
description: Adobe Workfront Fusion 매핑 패널에서 다음 날짜 및 시간 함수를 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 92813dac-4bf0-4681-9b71-7bd2e92a89a4
source-git-commit: 9249223c6fbe0360b11d41988fe8b9c35e45dbb8
workflow-type: tm+mt
source-wordcount: '1876'
ht-degree: 1%

---

# 날짜 및 시간 함수

## 변수

### now

현재 시간을 YYYY-MM-DD-hh:mm:ss 형식으로 가져옵니다.

### timestamp

현재 시간을 Unix 타임스탬프로 가져옵니다.

## 함수

### [!UICONTROL addSeconds(날짜; 숫자)]

날짜에 주어진 시간(초)을 추가한 결과로 새 날짜를 반환합니다. 초를 빼려면 음수를 입력합니다.

>[!BEGINSHADEBOX]

**예:**

* `addSeconds(2016-12-08T15:55:57.536Z;2)`

  2016-12-08T15:55:59.536Z 반환

* `addSeconds(2016-12-08T15:55:57.536Z;-2)`

  2016-12-08T15 반환:55:55.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addMinutes(date; number)] {#addminutes-date-number}

날짜에 주어진 시간(분) 수를 추가한 결과로 새 날짜를 반환합니다. 분을 빼려면 음수를 입력합니다.

>[!BEGINSHADEBOX]

**예:**

* `addMinutes(2016-12-08T15:55:57.536Z;2)`

  2016-12-08T15:57:57.536Z 반환

* `addMinutes(2016-12-08T15:55:57.536Z;-2)`

  2016-12-08T15:53:57.536Z 반환

>[!ENDSHADEBOX]

### [!UICONTROL addHours(date; number)] {#addhours-date-number}

날짜에 지정된 시간(시) 수를 추가한 결과로 새 날짜를 반환합니다. 시간을 빼려면 음수를 입력합니다.

>[!BEGINSHADEBOX]

**예:**

* `addHours(2016-12-08T15:55:57.536Z; 2)`

  2016-12-08T17 반환:55:57.536Z

* `addHours(2016-12-08T15:55:57.536Z;-2)`

  2016-12-08T13 반환:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addDays(date; number)] {#adddays-date-number}

날짜에 지정된 일 수를 추가한 결과로 새 날짜를 반환합니다. 일수를 빼려면 음수를 입력합니다.

>[!BEGINSHADEBOX]

**예:**

* `addDays(2016-12-08T15:55:57.536Z;2)`

  2016-12-10T15:55:57.536Z 반환

* `addDays(2016-12-08T15:55:57.536Z;-2)`

  2016-12-6T15:55:57.536Z 반환

>[!ENDSHADEBOX]

### [!UICONTROL addMonths(date; number)]

날짜에 지정된 개월 수를 추가한 결과로 새 날짜를 반환합니다. 월을 빼려면 음수를 입력합니다.

>[!BEGINSHADEBOX]

**예:**

* `addMonths(2016-08-08T15:55:57.536Z;2)`

  2016-10-08T15:55:57.536Z 반환

* `addMonths(2016-08-08T15:55:57.536Z;-2)`

  2016-06-08T15:55:57.536Z 반환

>[!ENDSHADEBOX]

### [!UICONTROL addYears (date; number)]

날짜에 지정된 연도 수를 추가한 결과로 새 날짜를 반환합니다. 연도를 빼려면 음수를 입력합니다.

>[!BEGINSHADEBOX]

**예:**

* `addYears(2016-08-08T15:55:57.536Z;2)`

  2018-08-08T15:55:57.536Z 반환

* `addYears(2016-12-08T15:55:57.536Z; -2)`

  2014-08-08T15:55:57.536Z 반환

>[!ENDSHADEBOX]

### [!UICONTROL setSecond(date; number)]

이 함수는 매개 변수에 지정된 초 수를 사용하는 새 날짜를 반환합니다.

0에서 59 사이의 숫자를 지정하십시오. 숫자가 해당 범위를 벗어나면 함수는 이전 분 (음수) 또는 이후 분 (양수)에서 1초를 반환합니다.

범위 밖의 숫자를 지정해야 하는 경우 [addSeconds(날짜; 숫자)](#addseconds-date-number) 섹션에 설명된 대로 [!UICONTROL  addSeconds]을 사용하는 것이 좋습니다.

>[!BEGINSHADEBOX]

**예:**

* `setSecond(2015-10-07T11:36:39.138Z;10)`

  2015-10-07T11 반환:36:10.138Z

* `setSecond(2015-10-07T11:36:39.138Z; 61)`

  2015-10-07T11 반환:37:01.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMinute(date; number)]

이 함수는 매개 변수에 지정된 분이 있는 새 날짜를 반환합니다.

0에서 59 사이의 숫자를 지정하십시오. 숫자가 해당 범위를 벗어나면 함수는 이전 시간(음수의 경우) 또는 이후 시간(양수의 경우)에서 1분을 반환합니다.

범위 밖의 숫자를 지정해야 하는 경우 [addMinutes (date; number)](#addminutes-date-number)에서 설명한 대로 addMinutes를 사용하는 것이 좋습니다.

>[!BEGINSHADEBOX]

**예:**

* `setMinute(2015-10-07T11:36:39.138Z;10)`

  2015-10-07T11:10:39.138Z 반환

* `setMinute(2015-10-07T11:36:39.138Z;61)`

  2015-10-07T12:01:39.138Z 반환

>[!ENDSHADEBOX]

### [!UICONTROL setHour(날짜; 숫자)]

이 함수는 매개 변수에 지정된 시간이 있는 새 날짜를 반환합니다.

0에서 23 사이의 숫자를 지정하십시오. 숫자가 이 범위를 벗어나면 함수는 전날(음수의 경우) 또는 다음날(양수의 경우)에서 한 시간을 반환합니다.

범위 밖의 숫자를 지정해야 하는 경우 [addHours(date; number)](#addhours-date-number)에서 설명한 대로 addHours를 사용하는 것이 좋습니다.

>[!BEGINSHADEBOX]

**예:**

* `setHour(2015-08-07T11:36:39.138Z;6)`

  2015-08-07T06 반환:36:39.138Z

* `setHour(2015-08-07T11:36:39.138;-6)`

  2015-08-06T18:36:39.138Z 반환

>[!ENDSHADEBOX]

### [!UICONTROL setDay(날짜; 영어로 된 날짜의 번호/이름)]

이 함수는 매개 변수에 지정된 날짜가 포함된 새 날짜를 반환합니다.

이 함수를 사용하여 일요일을 1로, 토요일을 7로 설정할 수 있습니다. 1에서 7까지의 숫자를 지정하는 경우 결과 날짜는 현재(일요일-토요일) 주 내에 있습니다. 숫자가 해당 범위를 벗어난 경우 함수는 이전 주(음수의 경우) 또는 후속 주(양수의 경우)에서 하루를 반환합니다.

범위 밖의 숫자를 지정해야 하는 경우에는 [addDays(date; number)](#adddays-date-number)에서 설명한 대로 addDays를 사용하는 것이 좋습니다.

>[!BEGINSHADEBOX]

**예:**

* `setDay(2018-06-27T11:36:39.138Z;Monday)`

  2018-06-25T11 반환:36:39.138Z

* `setDay(2018-06-27T11:36:39.138Z;1)`

  2018-06-24T11 반환:36:39.138Z

* `setDay(2018-06-27T11:36:39.138Z;7)`

  반환: 2018-06-30T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setDate(date; number)]

이 함수는 매개 변수에 지정된 월의 일을 사용하는 새 날짜를 반환합니다.

1에서 31 사이의 숫자를 지정하십시오. 숫자가 이 범위를 벗어나면 함수는 이전 달(음수의 경우) 또는 이후 달(양수의 경우)에서 하루를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `setDate(2015-08-07T11:36:39.138Z;5)`

  2015-08-05T11 반환:36:39.138Z

* `setDate(2015-08-07T11:36:39.138Z;32)`

  2015-09-01T11 반환:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMonth(날짜; 영어의 월 번호/이름)]

이 함수는 매개 변수에 지정된 월이 있는 새 날짜를 반환합니다.

1에서 12 사이의 숫자를 지정하십시오. 숫자가 이 범위를 벗어나면 함수는 이전 연도(음수의 경우) 또는 이후 연도(양수의 경우)의 월을 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `setMonth(2015-08-07T11:36:39.138Z;5)`

  2015-05-07T11:36:39.138Z 반환

* `setMonth(2015-08-07T11:36:39.138Z;17)`

  2016-05-07T11:36:39.138Z 반환

* `setMonth(2015-08-07T11:36:39.138Z;january)`

  2015-01-07T12 반환:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setYear(date; number)]

매개 변수에 지정된 연도가 있는 새 날짜를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `setYear(2015-08-07T11:36:39.138Z;2017)`

  2017-08-07T11:36:39.138Z 반환

>[!ENDSHADEBOX]

### [!UICONTROL formatDate(date; format; [timezone])]

`Dec 10, 2021 8:30 PM`과(와) 같이 텍스트 값으로 서식을 지정하려는 Date 값(예: `12-10-2021 20:30`)이 있는 경우 이 함수를 사용합니다.

이 기능은 예를 들어 동일한 시나리오에서 한 앱 또는 웹 서비스의 날짜 형식을 연결된 앱 또는 웹 서비스의 날짜 형식으로 변경해야 하는 경우 유용합니다.

자세한 내용은 문서 [항목 데이터 형식](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)의 날짜 및 텍스트를 참조하십시오.

#### 매개변수

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>매개변수</th> 
   <th>예상 데이터 유형* </th> 
   <th>기능</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 날짜] </td> 
   <td>일자 </td> 
   <td> <p>날짜 값을 텍스트 값으로 변환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL format] </td> 
   <td>텍스트 </td> 
   <td> <p>날짜/시간 형식 토큰을 사용하여 형식을 지정할 수 있습니다. 자세한 내용은 <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">날짜 및 시간 형식에 대한 토큰</a>을 참조하세요.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 시간대] </td> 
   <td>텍스트 </td> 
   <td> <p>(선택 사항) 전환에 사용되는 시간대를 지정할 수 있습니다. </p> <p>인식된 시간대의 목록은 Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">tz 데이터베이스 시간대 목록</a>의 "TZ 데이터베이스 이름" 열을 참조하십시오. 이 열에 나열된 값만 함수에서 유효한 시간대로 인식됩니다. 다른 값은 무시되며 프로필에 지정된 시나리오 시간대가 대신 사용됩니다. </p> <p>이 매개 변수를 생략하면 프로필 설정에 지정된 시나리오 시간대가 적용됩니다. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

다른 유형이 제공되면 유형 보압이 적용됩니다. 자세한 내용은 [형식 강제 변환](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md)을 참조하십시오.

#### 반환 값 및 유형

`formatDate` 함수는 지정된 형식 및 시간대에 따라 지정된 Date 값의 텍스트 표현을 반환합니다. 데이터 유형은 텍스트입니다.

>[!BEGINSHADEBOX]

**예:** 이 예제에서 시나리오와 웹 시간대가 모두 `Europe/Prague`(으)로 설정되었습니다.

![날짜 시간 함수 예제](assets/date&time-functions-examples-350x61.png)

* `formatDate(1. Date created;MM/DD/YYYY)`

  2018/10/01 반환

* `formatDate(1. Date created; YYYY-MM-DD hh:mm A)`

  반환 2018-10-01 09:32 AM

* `formatDate(1. Date created;DD.MM.YYYY HH:mm;UTC)`

  반환 01.10.2018 07:32

* `formatDate(now;DD.MM.YYYY HH:mm)`

  반환 19.03.2019 15:30

>[!ENDSHADEBOX]

### [!UICONTROL parseDate(text; format; [timezone])]

날짜를 나타내는 Text 값(예: `12-10-2019 20:30` 또는 `Aug 18, 2019 10:00 AM`)이 있고 이를 Date 값(이진 컴퓨터 읽기 가능 표시)으로 변환(구문 분석)하려는 경우 이 함수를 사용합니다. 자세한 내용은 문서 [항목 데이터 형식](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)의 날짜 및 텍스트를 참조하십시오.

#### 매개변수

두 번째 열은 예상 유형을 나타냅니다. 다른 유형이 제공되면 유형 보압이 적용됩니다. 자세한 내용은 [형식 강제 변환](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md)을 참조하십시오.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>매개변수</th> 
   <th>예상 데이터 유형* </th> 
   <th>기능</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL text] </td> 
   <td>텍스트 </td> 
   <td> <p>날짜 값을 텍스트 값으로 변환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL format] </td> 
   <td>텍스트 </td> 
   <td> <p>날짜/시간 형식 토큰을 사용하여 형식을 지정할 수 있습니다. 자세한 내용은 <a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">날짜 및 시간 형식에 대한 토큰</a>을 참조하세요.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 시간대] </td> 
   <td>텍스트 </td> 
   <td> <p>(선택 사항) 전환에 사용되는 시간대를 지정할 수 있습니다. </p> <p>인식된 시간대의 목록은 Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones">tz 데이터베이스 시간대 목록</a>의 "TZ 데이터베이스 이름" 열을 참조하십시오. 이 열에 나열된 값만 함수에서 유효한 시간대로 인식됩니다. 다른 값은 무시되며 프로필에 지정된 시나리오 시간대가 대신 사용됩니다. </p> <p>이 매개 변수를 생략하면 프로필 설정에 지정된 시나리오 시간대가 적용됩니다.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>예: </b></span></span><code>Europe/Prague</code>, <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

다른 유형이 제공되면 유형 보압이 적용됩니다. 자세한 내용은 [형식 강제 변환](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md)을 참조하십시오.

#### 반환 값 및 유형

이 함수는 지정한 형식 및 시간대에 따라 텍스트 문자열을 날짜로 변환합니다. 값의 데이터 유형은 날짜입니다.

>[!BEGINSHADEBOX]

**예:** 다음 예제에서 반환된 Date 값은 ISO 8601에 따라 표시되지만 결과의 데이터 형식은 Date입니다.

* `parseDate(2016-12-28;YYYY-MM-DD)`

  2016-12-28T00:00:00.000Z 반환

* `parseDate(2016-12-28 16:03;YYYY-MM-DD HH:mm)`

  2016-12-28T16 반환:03:00.000Z

* `parseDate(2016-12-28 04:03 pm; YYYY-MM-DD hh:mm a)`

  2016-12-28T16 반환:03:06.000Z

* `parseDate(1482940986;X)`

  2016-12-28T16 반환:03:06.000Z

>[!ENDSHADEBOX]

### [!UICONTROL dateDifference(Date1; Date2; Unit)]

두 날짜의 차이를 나타내는 숫자를 지정된 단위로 표시합니다.

Date2는 Date1에서 빼집니다.

`unit` 매개 변수에 다음 시간 값 중 하나를 사용합니다.

* 밀리초
* 초
* 분
* 시간
* 일
* 주
* 개월

단위를 지정하지 않으면 이 함수는 그 차이를 밀리초로 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z)`

  `600,000` 반환

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;hours)`

  `4` 반환

* `dateDifference2021-06-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;months)`

  `1` 반환

>[!ENDSHADEBOX]

### 추가 예시

#### 월의 n번째 요일을 계산하는 방법

이 섹션은 한 달에 n번째 요일을 가져오는 방법을 설명하는 [!DNL Exceljet] 웹 페이지의 [!DNL Workfront Fusion]에 맞게 조정되었습니다.

월의 n번째 요일(예: 첫 번째 화요일, 세 번째 금요일 등)에 해당하는 날짜를 계산해야 하는 경우 다음 공식을 사용할 수 있습니다.

![n일 계산](assets/date&time-functions-calc-nth-day-350x31.png)

```
{{addDays(setDate(1.date; 1); 1.n * 7 - formatDate(addDays(setDate(1.date; 1); "-" + 1.dow); "E"))}}
```

수식에 포함되는 항목은 다음과 같습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>1.n</code> </td> 
   <td> <p> n번째 날:</p> 
    <ul> 
     <li><code>1</code> 첫 번째 화요일로</li> 
     <li><code>2</code> 두 번째 화요일에</li> 
     <li><code>3</code> 셋째 주 화요일 등등</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>2.dow</code> </td> 
   <td> <p> 요일:</p> 
    <ul> 
     <li><code>1</code> - 월요일</li> 
     <li><code>2</code> - 화요일</li> 
     <li><code>3</code> - 수요일</li> 
     <li><code>4</code> - 목요일</li> 
     <li><code>5</code> - 금요일</li> 
     <li><code>6</code> - 토요일</li> 
     <li><code>7</code> - 일요일</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>1.date</code> </td> 
   <td> <p> 날짜는 월을 결정합니다. 현재 월의 n번째 요일을 계산하려면 <code>now</code> 변수를 사용하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

특정 대/소문자만 계산하려는 경우(예: 매주 두 번째 수요일) 수식의 항목 `1.n` 및 `2.dow`을(를) 해당 숫자로 바꿀 수 있습니다. 이번 달의 두 번째 수요일에 다음 값을 사용합니다.

* `1.n` = `2`
* `1.dow` = `3`
* `1.date` = `now`

![N번째 날 변수 값](assets/nth-day-variable-value-350x33.png)

#### 설명:

* `setDate(now;1)`이(가) 현재 월의 첫 번째 반환
* `formatDate(....;E)`이(가) 요일 반환(1, 2, ... 6)

### 날짜 사이의 일 수 계산 방법

한 가지 가능성은 다음 표현식을 사용하는 것입니다.

![날짜 사이의 일 수 계산](assets/calculate-days-between-dates-350x68.png)

```
{{round((2.value - 1.value) / 1000 / 60 / 60 / 24)}}
```

>[!NOTE]
>
>* `D1`과(와) `D2`의 값은 날짜 유형 값입니다. 문자열 형식 값(예: 20.10.2018)인 경우 `parseDate()` 함수를 사용하여 해당 값을 날짜 형식 값으로 변환합니다.
>
>* `round()` 함수는 날짜 중 하나가 일광 절약 시간제에 해당되고 다른 하나는 해당되지 않는 경우에 사용됩니다. 이러한 경우 시간 차이가 1시간 적거나 그 이상입니다. 정수가 아닌 결과에 대해 24로 나눌 수 있습니다. 1시간 일광 절약 시간제를 놓치셨네요. 반올림하면 백분율이 나오지 않습니다

#### 월의 마지막 날/밀리초를 계산하는 방법

날짜 범위를 지정할 때(예: 검색 모듈에서) 범위가 이전 달 전체에 대해 닫힌 간격(해당 제한 지점을 모두 포함하는 간격)으로 걸쳐 있으면 해당 월의 마지막 날을 계산해야 합니다.

2019-09-01 ≤ D ≤ 2019-09-30

아래 수식은 이전 달의 마지막 날을 계산하는 방법 중 하나를 보여 줍니다.

![이전 달의 마지막 날](assets/last-day-prev-month.png)

```
{{addDays(setDate(now; 1); -1)}}
```

경우에 따라 월의 마지막 날뿐만 아니라 문자 그대로 마지막 밀리초를 계산해야 합니다.

2019-09-01T00:00:00.000Z ≤ D ≤ 2019-09-30T23:59:59.999Z

이 수식은 이전 달의 마지막 밀리초를 계산하는 방법을 보여 줍니다.

![이전 달의 마지막 밀리초](assets/last-millisecond-prev-month-350x45.png)

```
{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD"; "UTC") - 1; "x")}}
```

표준 시간대 설정을 사용하기 위해 결과가 필요한 경우 UTC 인수를 생략합니다.

![UTC 생략](assets/omit-utc-argument-350x45.png)

`{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD") - 1; "x")}}`

그러나 다음 달의 1일을 대신 지정하고 &quot;작거나 같음&quot; 연산자를 다음과 같이 &quot;보다 작음&quot;으로 대체하면서 반열기 간격(제한 지점 중 하나를 제외한 간격)을 사용하는 것이 좋습니다.

`2019-09-01 ≤ D < 2019-10-01`

`2019-09-01T00:00:00.000Z ≤ D < 2019-10-01T00:00:00.000Z`
