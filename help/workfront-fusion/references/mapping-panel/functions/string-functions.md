---
title: 문자열 함수
description: Adobe Workfront Fusion 매핑 패널에서 다음 문자열 함수를 사용할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: d3e49fce-85bc-4ee6-9a94-497a306e0c74
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 4%

---

# 문자열 함수

## [!UICONTROL 길이(텍스트 또는 버퍼)]

텍스트 문자열 길이(문자 수) 또는 이진 버퍼(버퍼 크기(바이트))를 반환합니다.

>[!BEGINSHADEBOX]

**예:**

`length( hello )`

반환: 5

>[!ENDSHADEBOX]

## [!UICONTROL 하단(텍스트)]

텍스트 문자열의 모든 알파벳 문자를 소문자로 변환합니다.

>[!BEGINSHADEBOX]

**예:**

`lower( Hello )`

반환: hello

>[!ENDSHADEBOX]

## [!UICONTROL 자본화(텍스트)]

텍스트 문자열의 첫 번째 문자를 대문자로 변환합니다.

>[!BEGINSHADEBOX]

**예:**

`capitalize( workfront )`

반환: Workfront

>[!ENDSHADEBOX]

## [!UICONTROL 시작 사례(텍스트)]

모든 단어의 첫 번째 문자를 대문자로 사용하고 다른 모든 문자는 소문자로 바꿉니다.

>[!BEGINSHADEBOX]

**예:**
`startcase( hello WORLD )`

반환: [!UICONTROL Hello World]

>[!ENDSHADEBOX]

## [!UICONTROL ascii(텍스트; [분음 부호 제거])]

텍스트 문자열에서 ASCII가 아닌 모든 문자를 제거합니다.

>[!BEGINSHADEBOX]

**예:**

* `ascii(` `Wěošrčkřfžrýoáníté` `)`

반환: Workfront

* `ascii(` `ěščřž` `;` `true` `)`

반환: [!UICONTROL escrz]

>[!ENDSHADEBOX]

## [!UICONTROL 바꾸기(텍스트;검색 문자열; 대체 문자열)]

검색 문자열을 새 문자열로 바꿉니다.

>[!BEGINSHADEBOX]

**예:**

`replace( Hello World ; Hello ; Hi )`

반환: [!UICONTROL Hi World]

>[!ENDSHADEBOX]

정규식(`/.../`(으)로 묶음)은 플래그(예: `g`, `i`, `m`)가 추가된 검색 문자열로 사용할 수 있습니다.

>[!BEGINSHADEBOX]

**예:**

![Replace](assets/replace---1-350x31.png)

X X X X는 모두 X로 대체된다

>[!ENDSHADEBOX]

대체 문자열에는 다음과 같은 특수 대체 패턴이 포함될 수 있습니다.

* `$&` 일치하는 하위 문자열을 삽입합니다.
* `$n` n이 100보다 작은 양의 정수인 경우 n번째 괄호로 묶인 하위 일치 문자열을 삽입합니다. 1개 색인화되었습니다.

>[!BEGINSHADEBOX]

**예:**

![변수 값](assets/variable-value-350x63.png)

반환: 전화 번호 `+420777111222`

![변수 반환](assets/variable-value---2-350x55.png)

반환: 전화 번호: `+420777111222`

>[!CAUTION]
>
>대체 문자열 인수에는 `/ is (?<number>\d+)/`과(와) 같은 명명된 캡처 그룹을 사용하지 마십시오. 이렇게 하면 오류가 발생합니다.


>[!ENDSHADEBOX]

정규식에 대한 자세한 내용은 [텍스트 구문 분석기](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/text-parser.md)를 참조하십시오.

## [!UICONTROL 트리밍(텍스트)]

텍스트의 시작 또는 끝에 있는 공백 문자를 제거합니다.

## [!UICONTROL upper(텍스트)]

텍스트 문자열의 모든 알파벳 문자를 대문자로 변환합니다.

>[!BEGINSHADEBOX]

**예:**

`upper( Hello )`

반환: [!UICONTROL HELLO]

>[!ENDSHADEBOX]

## [!UICONTROL 하위 문자열(텍스트; start;end)]

시작 위치와 끝 위치 사이의 텍스트 문자열 부분을 반환합니다.

>[!BEGINSHADEBOX]

**예:**

* `substring( Hello ; 0 ; 3)`

  반환: 도움말

* `substring( Hello ; 1 ; 3 )`

  반환: el

>[!ENDSHADEBOX]

## [!DNL indexOf (string; value; [start])]

문자열에서 지정된 값의 첫 번째 발생 위치를 반환합니다. 이 메서드는 검색된 값이 없는 경우 &#39;-1&#39;을 반환합니다. 시작 값은 문자열에서 검색이 시작되는 위치를 나타냅니다.

>[!BEGINSHADEBOX]

**예:**

* `indexOf( Workfront ; o )`

  반환: 1

* `indexOf( Workfront ; x )`

  반환: -1

* `indexOf( Workfront ; o ; 3 )`

  반환: 6

>[!ENDSHADEBOX]

## [!UICONTROL toBinary(값)]

모든 값을 이진 데이터로 변환합니다.

16진수 또는 base64의 이진 변환을 이진 데이터에 적용할 두 번째 인수로 인코딩을 지정할 수도 있습니다.

>[!BEGINSHADEBOX]

**예:**

* `toBinary( Workfront )`

  반환: 57 6f 72 6b 66 72 6f 6e 74

* `toBinary( V29ya2Zyb250 ; base64 )`

  반환: 57 6f 72 6b 66 72 6f 6e 74

>[!ENDSHADEBOX]

## [!UICONTROL toString(값)]

모든 값을 문자열로 변환합니다.

## [!UICONTROL encodeURL(텍스트)]

일부 텍스트의 특수 문자를 유효한 URL 주소로 인코딩합니다.

## [!UICONTROL decodeURL(텍스트)]

URL의 특수 문자를 텍스트로 디코딩합니다.

>[!BEGINSHADEBOX]

**예:**
`decodeURL( Automate%20your%20workflow )`

반환: [!UICONTROL 워크플로우 자동화]

>[!ENDSHADEBOX]

## [!UICONTROL 이스케이프 HTML(텍스트)]

텍스트의 모든 HTML 태그를 이스케이프 처리합니다.

>[!BEGINSHADEBOX]

**예:**

`escapeHTML( <b>Hello</b> )`

반환: `&lt;b&gt;Hello&lt;/b&gt;`

>[!ENDSHADEBOX]

## [!UICONTROL escapeMarkdown(text)]

텍스트의 모든 Markdown 태그를 이스케이프 처리합니다.

>[!BEGINSHADEBOX]

**예:**

`escapeMarkdown( # Header )`

반환: `&#35; Header`

>[!ENDSHADEBOX]

## [!UICONTROL stripHTML(텍스트)]

텍스트에서 모든 HTML 태그를 제거합니다.

>[!BEGINSHADEBOX]

**예:**

`stripHTML( <b>Hello</b> )`

반환: 안녕하세요.

>[!ENDSHADEBOX]

## 포함(텍스트, 검색 문자열)

텍스트에 검색 문자열이 포함되어 있는지 확인합니다.

>[!BEGINSHADEBOX]

**예:**

* `contains( Hello World ; Hello )`

  반환: [!UICONTROL true]

* `contains( Hello World ; Bye )`

  반환: [!UICONTROL false]

>[!ENDSHADEBOX]

## [!UICONTROL 분할(텍스트, 구분 기호)]

문자열을 하위 문자열로 분리하여 문자열을 문자열 배열로 분할합니다.

>[!BEGINSHADEBOX]

**예:**

`split( John, George, Paul ; , )`

>[!ENDSHADEBOX]

## [!UICONTROL md5(텍스트)]

문자열의 md5 해시를 계산합니다.

>[!BEGINSHADEBOX]

**예:**

`md5( Workfront )`

반환: `1448bbbeaa7a9b8091d426999f1f666b`

>[!ENDSHADEBOX]

## [!UICONTROL sha1(텍스트; [인코딩]; [키])]

문자열의 sha1 해시를 계산합니다. key 인수를 지정하면 sha1 HMAC 해시가 대신 반환됩니다. 지원되는 인코딩: &quot;hex&quot;(기본값), &quot;base64&quot; 또는 &quot;latin1&quot;.

>[!BEGINSHADEBOX]

**예:**

`sha1( workfront )`

반환: b2b30b8ae1f9e5b40fbb0696eaabdbfd8d0c087f

>[!ENDSHADEBOX]

## [!UICONTROL sha256(텍스트; [인코딩]; [키])]

문자열의 sha256 해시를 계산합니다. key 인수를 지정하면 sha256 HMAC 해시가 대신 반환됩니다. 지원되는 인코딩: &quot;hex&quot;(기본값), &quot;base64&quot; 또는 &quot;latin1&quot;.>

>[!BEGINSHADEBOX]

**예:**

`sha256( workfront )`

반환: ed3d7397eec7b94453035b67ba4468c883ee3bedeb57137f7371f2e0cf5e2bbc

>[!ENDSHADEBOX]

## [!UICONTROL sha512(텍스트; [출력 인코딩]; [키]; [키 인코딩])]

문자열의 sha512 해시를 계산합니다. key 인수를 지정하면 sha512 HMAC 해시가 대신 반환됩니다.

지원되는 인코딩:

* &quot;[!UICONTROL hex]&quot;(기본값)
* &quot;[!UICONTROL base64]&quot;
* &quot;[!UICONTROL latin1]&quot;

지원되는 키 인코딩:

* &quot;[!UICONTROL text]&quot;(기본값)
* &quot;[!UICONTROL hex]&quot;
* &quot;[!UICONTROL base64]&quot; 또는 &quot;[!UICONTROL binary]&quot;

&quot;[!UICONTROL binary]&quot; 키 인코딩을 사용하는 경우 키는 문자열이 아닌 버퍼여야 합니다.

>[!BEGINSHADEBOX]

**예:**

`sha512(workfront)`

반환: 789ae41b9456357e4f27c6a09956a767abbb8d80b206003ffdd1e94dbc687cd119b85e1e19db58bb44b234493af35fd431639c0345aadf2cf7ec26e9f4a7fb19

>[!ENDSHADEBOX]

## [!UICONTROL base64(텍스트)]

텍스트를 base64로 변환합니다.

>[!BEGINSHADEBOX]

**예:**

`base64( workfront )`

반환: d29ya2Zyb250==

>[!ENDSHADEBOX]
