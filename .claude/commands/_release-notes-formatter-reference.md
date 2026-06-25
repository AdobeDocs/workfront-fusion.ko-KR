---
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---
# 릴리스 노트 참조 템플릿

각 릴리스 노트 페이지 유형에 대한 자세한 템플릿입니다. 다음의 템플릿을 기반으로 합니다
`help/quicksilver/product-announcements/product-releases/release-note-templates/` 및
최근 분기별 릴리스에 사용된 실제 서식.

&#x200B;---

## 제품 영역 페이지 템플릿

```markdown
---
title: {Written Quarter} {Year} {Area} enhancements
description: {Written Quarter} {Year} {Area} enhancements
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} {Area} enhancements

This page describes {Area} enhancements made with the {Written Quarter} {Year} release to the Preview environment. These enhancements will be made available in the Production environment as noted.

For a list of all changes available at this point in the {Written Quarter} {Year} release cycle, see [{Written Quarter} {Year} release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title Here

>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}

Feature description paragraph.

For more information, see [Help article title](/help/quicksilver/path/to/article.md).
```

### 제품 영역 페이지에 대한 규칙

- 본문 컨텐츠에 Markdown(HTML 아님) 사용
- 각 기능은 H2 제목을 가져옵니다.
- `>[!NOTE]` 설명선에는 빈 줄이 있어야 합니다.
- `>[!NOTE]` 형식은 정확히 다음과 같습니다.

  ```
  >[!NOTE]
  >
  >Preview: {date}
  >Production fast release: {date}
  >Production for everyone: {date}
  ```

- 기능이 일시적으로 제거된 경우 날짜 뒤에 줄을 추가합니다.

  ```
  >
  >This feature has been temporarily removed from the Production environment on {date}.
  ```

- 도움말 링크는 `/help/quicksilver/`(으)로 시작하는 절대 경로를 사용합니다.

&#x200B;---

## 개요 페이지 템플릿

```markdown
---
title: {Written Quarter} {Year} release overview
description: This page provides information about functionality that is included in the {Written Quarter} {Year} release. These enhancements are planned to become available in the Production environment throughout the quarter.
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} release overview

This page provides information about functionality that is included in the {Written Quarter} {Year} release scheduled for {Release Month} {Year}.

The enhancements on this page are available in the Preview environment. This page will be updated with additional enhancements as the {Written Quarter} {Year} release nears its planned Production release.

>[!IMPORTANT]
>
>
>Monthly and quarterly releases are planned to be available on the Thursday of the second full week of the month, unless otherwise specified.
>
>|Monthly release|Quarterly release|
>|----|----|
>|<ul><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li></ul>|<ul><li>{VV}.{M} ({Month Day, Year})</li></ul>|
>
>Note that for the final release of each quarter ({VV}.{M} this quarter), users on the fast release schedule will receive the release one day early ({Month Day, Year}).
>
>For more information on the fast release process, see [Enable or disable the fast release process](/help/quicksilver/administration-and-setup/set-up-workfront/configure-system-defaults/enable-fast-release-process.md).

## Adobe Workfront enhancements

* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
* [Project enhancements](#project-enhancements)
* [Reporting enhancements](#reporting-enhancements)
* [Requesting enhancements](#requesting-enhancements)
* [Other enhancements](#other-enhancements)
```

### 개요 기능 테이블

각 H3 제품 영역 섹션에는 HTML 테이블이 있습니다. 다음과 같은 정확한 구조를 사용합니다.

```html
### {Area} enhancements

<table>
            <col style="width: 50%;" />
            <col style="width: 25%;" />
            <tbody>
              <tr>
        <td><strong>Feature</strong>
        </td>
        <td><strong>Preview</strong></td>
        <td><strong>Fast release</strong></td>
        <td><strong>Quarterly</strong></td>
        </tr>
    <tr>
        <td>
            <a href="/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-{area}.md" class="MCXref xref" xrefformat="{para}">Feature Title</a><p>Short description of the feature.</p>
        </td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
    </tr>
            </tbody>
        </table>
```

#### 테이블 규칙

- 기능 셀: `class="MCXref xref" xrefformat="{para}"` 뒤에 `<p>` 설명이 있는 `<a>` 태그
- `href` 링크는 제품 영역 페이지로 연결됩니다(특정 앵커 아님)
- 날짜 셀: `<p>`개 태그로 래핑됨
- 일정 외 항목의 경우 링크 뒤에 `<p>[!BADGE Off schedule]{type=Neutral}</p>`을(를) 추가하십시오.
- 배지가 필요하지 않은 경우 링크 뒤에 빈 `<p></p>`을(를) 사용할 수 있습니다.
- HTML 들여쓰기를 기존 파일과 일관되게 유지

### 개요 후행 섹션

모든 제품 영역 테이블 이후:

```markdown
## Release notes for other areas

### Workfront Fusion enhancements

New features in Workfront Fusion are available in Production at a cadence outside of the standard release schedule. For more information about the latest features, see [Adobe Workfront Fusion release activity](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/fusion-release-activity/fusion-release-activity).

### Workfront Planning enhancements

New features in Workfront Planning are available in Production. For more information about the latest features, see [{Written Quarter} {Year} release activity for Adobe Workfront Planning](/help/quicksilver/product-announcements/product-releases/planning-release-activity/planning-release-activity-{YY}-q{N}.md).

There are no updates for the following at this point in the release:

* Scenario Planner
* Proof
* Goals

## Desktop proofing viewer updates

{Version info if available, otherwise omit section}

## Announcements

{Announcement content}

### API version {NN}

{API version info}

### Workfront Maintenance Updates

For information about the maintenance updates made during the {Written Quarter} {Year} release, see [Workfront Maintenance Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html).

### Training updates

Explore the latest updates made to learning programs, learning paths, videos, and guides for each Adobe Workfront product release. For more information, see the "What's New" section of the [Workfront Tutorials page](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/home.html).
```

&#x200B;---

## 디자인 페이지 템플릿

```markdown
---
title: Look-and-feel updates during the {Written Quarter} {Year} release time frame
description: Look-and-feel updates during the {Written Quarter} {Year} release time frame
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---

# Look-and-feel updates during the {Written Quarter} {Year} release time frame

This page describes minor updates to the look and feel of various areas of the Adobe Workfront application that were made within the {Written Quarter} {Year} release timeframe. These enhancements will be made available in the Production environment a minimum of 2 weeks after releasing to Preview.

For a list of all changes available with the {Written Quarter} {Year} release, see [{Written Quarter} {Year} Release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title

>[!NOTE]
>
>Preview release: {Month Day, Year}; Planned Production release: {Month Day, Year}

Description of the look-and-feel change.
```

&#x200B;---

## 날짜 설명선 형식

### 제품 영역 페이지(여러 줄)

```markdown
>[!NOTE]
>
>Preview: March 5, 2026
>Production fast release: April 15, 2026
>Production for everyone: April 16, 2026
```

### 디자인 페이지(한 줄)

```markdown
>[!NOTE]
>
>Preview release: March 5, 2026; Planned Production release: March 19, 2026
```

### 주별 페이지(한 줄)

```markdown
>[!NOTE]
>
>Preview release: February 9, 2023; Planned Production release: February 23, 2023
```

&#x200B;---

## 감시할 알려진 불일치

1. **잘못된 개요 링크 분기** — 제품 영역 페이지가 이전 분기의 개요에 링크되는 경우가 있습니다(예: `26-q2` 대신 `26-q1`).
2. **잘못된 연도를 표시하는 미리 보기 날짜** — 개요 테이블은 때때로 미리 보기 열에 이전 연도를 표시합니다(예: &quot;2026&quot; 대신 &quot;2025&quot;).
3. **닫는 `</tr>`개 태그 누락** — 일부 HTML 테이블 행에 적절한 닫는 태그가 없습니다.
4. **`content-type: release-notes`** — 이전 파일에 있으며, 최신 26-q2 제품 영역 페이지에서는 생략되었습니다. 현재 분기의 패턴을 따릅니다.
5. 템플릿의 **오타** - 유사 템플릿에 `release` 대신 `relesae`이(가) 있습니다. 항상 올바른 철자를 사용하십시오.
6. **기능 링크 뒤에 `<p></p>`이(가) 없음** — 일부 개요 테이블 행에는 `<a>` 태그 뒤에 빈 `<p>` 태그가 없습니다.
