---
title: 날짜 및 시간 구문 분석용 토큰
description: ' [!DNL Adobe Workfront Fusion mapping]  패널에서 날짜 및 시간 구문 분석에 대한 다음 토큰을 사용할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: d3242af3-89e8-45ae-81a1-3b4dadf824fd
TQID: https://experienceleague.adobe.com/ZU2fO6cE2nEceklQoIj6TrpETBbssJe3FuCpcXHZepI
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 17%

---

# 날짜 및 시간 구문 분석용 토큰

## 년, 월, 일 토큰

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>입력 </th> 
   <th>예 </th> 
   <th> <p>설명</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>YYYY </code> </td> 
   <td><code>2014 </code> </td> 
   <td> <p>연도 4자리 또는 2자리</p> </td> 
  </tr> 
  <tr> 
   <td><code>YY</code></td> 
   <td><code>14</code></td> 
   <td> <p>2자리 연도</p> </td> 
  </tr> 
  <tr> 
   <td><code>Y</code> </td> 
   <td><code>-25</code> </td> 
   <td> <p>[!UICONTROL 연도(숫자 및 기호 포함)]</p> </td> 
  </tr> 
  <tr> 
   <td><code>Q</code> </td> 
   <td><code>1..4</code> </td> 
   <td> <p> 사분기. 분기의 월에서 첫째 달까지 설정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td><code>M MM</code> </td> 
   <td><code>1..12</code> </td> 
   <td> <p> 월 번호</p> </td> 
  </tr> 
  <tr> 
   <td><code>MMM MMMM</code> </td> 
   <td><code>Jan..December</code> </td> 
   <td> <p> 월 이름</p> </td> 
  </tr> 
  <tr> 
   <td><code>D DD</code> </td> 
   <td><code>1..31</code> </td> 
   <td> <p> 일(한 달 기준)</p> </td> 
  </tr> 
  <tr> 
   <td><code>Do </code> </td> 
   <td><code>1st..31st</code> </td> 
   <td> <p> 서수가 있는 날짜</p> </td> 
  </tr> 
  <tr> 
   <td><code>DDD DDDD</code> </td> 
   <td><code>1..365</code></td> 
   <td> <p> 일(한 해 기준)</p> </td> 
  </tr> 
  <tr> 
   <td><code>X</code> </td> 
   <td><code>1410715640.579</code> </td> 
   <td> <p> Unix 타임스탬프</p> </td> 
  </tr> 
  <tr> 
   <td><code>x</code> </td> 
   <td><code>1410715640579</code> </td> 
   <td> <p> Unix ms 타임스탬프</p> </td> 
  </tr> 
 </tbody> 
</table>

## 주 연도, 주 및 요일 토큰

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>입력 </th> 
   <th>예 </th> 
   <th> <p>설명</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>ddd dddd</code> </td> 
   <td><code>Mon...Sunday</code> </td> 
   <td> <p> 요일 이름</p> </td> 
  </tr> 
  <tr> 
   <td><code>GGGG</code> </td> 
   <td><code>2014</code> </td> 
   <td> <p> ISO 주 4자리 연도</p> </td> 
  </tr> 
  <tr> 
   <td><code>GG </code> </td> 
   <td><code>14</code> </td> 
   <td> <p> ISO 2자리 주 연도</p> </td> 
  </tr> 
  <tr> 
   <td><code>W WW</code> </td> 
   <td><code>1..53</code></td> 
   <td> <p> 연간 ISO 주</p> </td> 
  </tr> 
  <tr> 
   <td><code>E</code> </td> 
   <td><code>1..7</code> </td> 
   <td> <p> 요일</p> </td> 
  </tr> 
 </tbody> 
</table>

## 시간, 분, 초, 밀리초 및 오프셋 토큰

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>입력 </th> 
   <th>예 </th> 
   <th> <p>설명</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>H HH</code> </td> 
   <td><code>0..23</code></td> 
   <td> <p> 시간(24시간)</p> </td> 
  </tr> 
  <tr> 
   <td><code>h hh</code> </td> 
   <td><code>1..12</code> </td> 
   <td> <p> 시간(A에 12시간 사용)</p> </td> 
  </tr> 
  <tr> 
   <td><code>k kk</code> </td> 
   <td><code>1..24</code> </td> 
   <td> <p> 시간(1~24까지 24시간)</p> </td> 
  </tr> 
  <tr> 
   <td><code>a A</code> </td> 
   <td><code>am pm</code> </td> 
   <td> <p> Post 또는 상쇄(a p도 유효한 것으로 간주됨)</p> </td> 
  </tr> 
  <tr> 
   <td><code>m mm</code> </td> 
   <td><code>0..59</code> </td> 
   <td> <p> 분</p> </td> 
  </tr> 
  <tr> 
   <td><code>s ss</code> </td> 
   <td><code>0..59</code> </td> 
   <td> <p> 초</p> </td> 
  </tr> 
  <tr> 
   <td><code>S SS SSS</code> </td> 
   <td><code>0..999</code> </td> 
   <td> <p> 분수 초</p> </td> 
  </tr> 
  <tr> 
   <td><code>Z ZZ</code> </td> 
   <td><code>+12:00</code> </td> 
   <td> <p> UTC에서 +-HH:mm, +-HHmm 또는 Z로 오프셋</p> </td> 
  </tr> 
 </tbody> 
</table>
