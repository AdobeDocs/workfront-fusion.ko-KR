---
name: fusion-release-notes
description: 새 Workfront Fusion 주간 릴리스 노트 페이지를 만들고 이를 릴리스 활동 개요 페이지 및 목차에 연결합니다. 사용자가 새 Fusion 릴리스 노트 또는 주별 릴리스 페이지를 작성, 추가 또는 작성하거나 릴리스에 대한 새 Fusion 기능을 문서화하도록 요청할 때 사용합니다. 제품 공지/제품 릴리스에서 Workfront(Quicksilver) 릴리스 노트를 사용하지 마십시오. 릴리스 노트 포맷터를 사용하십시오.
source-git-commit: 59a8d8ee83906bc16fc627bd348accc4e588cf9b
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 1%

---


# Fusion 릴리스 노트

`help/workfront-fusion/fusion-product-releases/`에 새 주별 Adobe Workfront **Fusion** 릴리스 정보 페이지를 만들고 이를 검색 가능한 두 위치(릴리스 활동 개요 페이지 및 `help/workfront-fusion/TOC.md`)에서 연결합니다.

`release-notes-formatter` 스킬에서 처리하는 Quicksilver(핵심 Workfront) 릴리스 노트와 다른 시스템입니다.

| | Fusion 릴리스 노트(이 스킬) | Quicksilver 릴리스 정보(`release-notes-formatter`) |
|---|---|---|
| 케이던스 | 매주 | 분기별 |
| 디렉터리 | `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/` | `help/quicksilver/product-announcements/product-releases/` |
| 기능별 날짜 설명선 | 아니요 — 페이지 제목에 주가 포함됩니다. | 예 — 기능당 `>[!NOTE]`개 블록 |
| 색인 페이지 | `fusion-release-activity.md`(연도/월별) | `{YY}-q{N}-release-overview.md`(분기별) |

## 1단계: 기능 수집

해당 주 및 각 문서에 대한 기능/변경 사항 목록을 사용자(아직 제공되지 않은 경우)에게 문의하십시오.

- 짧은 기능 제목
- 변경된 사항과 중요한 이유에 대한 간단한 설명
- 링크가 있는 도움말 문서(경로가 있는지 확인 — 추측하지 않음)
- 사용자/관리자 작업이 필요한지 또는 사용 중단 상태인지 여부(`>[!IMPORTANT]` 설명선 필요)

## 2단계: 파일 이름 및 날짜 확인

- 문서화할 주의 월요일(또는 릴리스 날짜)을 찾아 명확하지 않은 경우 사용자와 확인합니다.
- 파일 경로: `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md`
  - `{M}` 및 `{D}`에 **앞에 0이 없습니다**: `fusion-2026-07-20.md`이(가) 아닌 `fusion-2026-7-20.md`이(가) 있습니다.
  - 연도 폴더가 아직 존재하지 않는 경우 만듭니다.
- 새 페이지를 만들기 전에 해당 주의 페이지가 이미 있는지 확인하십시오.

## 3단계: 페이지 작성

### 프론트메터

```yaml
---
title: Workfront Fusion release activity Week of {Month} {Day}, {Year}
description: Workfront Fusion release activity Week of {Month} {Day}, {Year}
author: {Author}
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
```

규칙:
- `title`과(와) `description`이(가) 동일합니다.
- 일부 이전 페이지에서 쉼표를 생략하더라도 항상 날짜(`July 20, 2026`)에 쉼표를 포함하십시오. 이러한 불일치를 복사하지 마십시오.
- **모든 새 페이지에 `hidefromtoc: true`을(를) 사용합니다. `exl-id` 또는 `TQID`을(를) 추가하지 마십시오.** 이는 페이지가 게시되면 나중에 할당됩니다. 하나가 잘못된 경우 인벤터리를 작성합니다. (2026년 중반 이후의 모든 페이지는 이 패턴을 따릅니다. 예를 확인해야 하는 경우 `_fusion-release-notes-reference.md`을(를) 참조하십시오.)

### 본문

```markdown
# Workfront Fusion release activity: Week of {Month} {Day}, {Year}

This page describes all enhancements made in Adobe Workfront Fusion the week of {Month} {Day}, {Year}.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/ko/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## {Feature title}

Feature description paragraph(s) — what changed, why, and how it affects existing scenarios/configurations if relevant.

For more information, see [{Help article title}](/help/workfront-fusion/{path-to-article}.md).

## {Next feature title}

...
```

참고:
- 기능당 1H2, 사용자가 제공한 순서대로(페이지 내에서 강제 최신 순서 지정 없음 - 1주일).
- 기능별 `>[!NOTE]` 날짜 설명선이 없습니다. 페이지 제목에 이미 날짜가 있습니다.
- 기능에 작업이 필요하거나 변경/사용이 중단되는 경우 설명 앞에 H2 바로 아래에 `>[!IMPORTANT]` 콜아웃을 추가하십시오.

  ```markdown
  ## {Feature title}
  
  >[!IMPORTANT]
  >
  >**Action Required: {short summary of what the user must do and by when}**
  >
  >{Details of the requirement.}
  
  {Regular description paragraph(s).}
  ```

- 모든 기능은 &quot;자세한 내용은 [...]&quot;로 끝나야 합니다. 관련 도움말 문서 링크 링크 대상이 저장소에 있는지 확인합니다.

## 4단계: 개요 색인에 페이지 추가

`help/workfront-fusion/fusion-product-releases/fusion-release-activity.md` 편집:

- `## Fusion releases in {current year}` 섹션을 찾습니다. `+++` 축소 가능한 블록으로 래핑된 섹션이 **not**&#x200B;입니다. 지난 해만 축소됩니다.
- 연도 제목 바로 아래에 있는 릴리스 월의 `### {Month} {Year}` 제목을 찾거나 만듭니다.
  - 월 머리글이 아직 없는 경우 이전 달(최신 월 우선)에 **위**&#x200B;를 추가하십시오.
- 새 페이지를 해당 달 제목 아래의 **첫 번째** 글머리 기호로 추가(최신 주 먼저):

  ```markdown
  * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- 새로운 연도의 첫 번째 릴리스인 경우 이전 연도의 제목 위에 새 `## Fusion releases in {YYYY}` 제목을 추가하고, *이전*&#x200B;년의 섹션을 `+++ **Click to open**`/`+++` 축소 가능한 블록으로 래핑합니다(아직 올해만 확장).

## 5단계: TOC에 페이지 추가

`help/workfront-fusion/TOC.md` 편집:

- `* Fusion release activity {#fusion-release-activity}` 아래에 중첩된 현재 연도의 `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}`을(를) 찾습니다.
- 새 페이지를 해당 제목 아래의 **first** 항목으로 추가하고(가장 최신 항목) 기존 들여쓰기(8개 공백)와 일치시킵니다.

  ```markdown
        * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- 현재 연도의 머리글이 아직 없는 경우 이전 연도의 머리글 위에 `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}`을(를) 추가합니다.
- **새 항목에 `{hide-from-toc}` 접두사를 추가하지 마십시오**. 이 접두사는 이전 항목이 표시되는 탐색 메뉴에서 오래된 경우에만 사용됩니다(아래의 알려진 불일치 참조).

### 감시할 알려진 불일치(복제 안 함)

- 페이지 자체가 2026년 릴리스이지만 실수로 여러 2026년 초반 TOC 항목이 `Fusion releases - 2025` 제목 아래에 중첩되었습니다. 새 항목을 추가할 때 항상 이전 항목이 있는 위치가 아니라 **해당 연도**&#x200B;와 일치하는 머리글 아래에 표시되는지 다시 확인하십시오.
- 일부 이전 페이지 제목/H1에서는 연도 앞에 쉼표를 생략합니다(`July 13, 2026` 대신 `July 13 2026`). 새 페이지에는 항상 쉼표를 사용하십시오.

## 6단계: 최종 검사 목록

- [ 날짜에 앞에 0이 없는 올바른 경로에 ] 파일을 만들었습니다.
- [ ] Frontmatter에서 `hidefromtoc: true`을(를) 사용하고 `exl-id`/`TQID`을(를) 만들지 않았습니다.
- [ ] 제목/설명 일치, 날짜에 쉼표가 포함됨
- [ ] 각 기능에 설명과 &quot;자세한 정보&quot; 확인 링크가 있습니다.
- [ ] 작업 필요/사용 중단 기능에 `>[!IMPORTANT]` 설명선이 있습니다.
- [ ] 새 페이지가 올바른 연도/월 아래 `fusion-release-activity.md`의 최신 항목으로 추가되었습니다.
- [ ] 새 페이지가 올바른 연도 제목 아래에 `TOC.md`의 최신 항목으로 추가되었습니다.
- [ 필요한 경우 ]개의 새 연도/월 머리글이 만들어지고 `fusion-release-activity.md`에서 이전 연도가 축소되었습니다.

## 추가 리소스

전체 작업 예제(간단한 다중 기능 주 및 `>[!IMPORTANT]` 작업이 필요한 콜아웃이 있는 주)에 대해서는 `.claude/commands/_fusion-release-notes-reference.md`을(를) 참조하십시오.
