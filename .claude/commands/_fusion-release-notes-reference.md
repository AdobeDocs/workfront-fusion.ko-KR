---
source-git-commit: 59a8d8ee83906bc16fc627bd348accc4e588cf9b
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---
# Fusion 릴리스 노트 참조 예

의 실제 최근 페이지를 기반으로 한 `fusion-release-notes` 스킬에 대한 작업 예제
`help/workfront-fusion/fusion-product-releases/fusion-releases-2026/`.

&#x200B;---

## 예 1: 간단한 다중 기능 주

`fusion-2026-6-22.md`을(를) 기반으로 합니다.

```markdown
---
title: Workfront Fusion release activity Week of June 22, 2026
description: Workfront Fusion release activity Week of June 22, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of June 22, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of June 22, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/ko/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Create custom JavaScript packages to use in scenarios

To provide better flexibility and control of your scenarios, we've added the ability to create a custom JavaScript packages that you can then use in scenarios. You can create custom packages in the Packages area of Fusion. You then add functions or variables from these packages to your scenarios in the form of an Adobe App Builder module.

Packages include functions, along with any variables or dependencies the functions rely on. You can also test functions in your package before using them in your scenarios

Because custom packages work through Adobe App Builder, your organization must have an Adobe App Builder license to use them.

For more information on using custom functions in Fusion, see [Use custom function packages](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

## View changes between scenario versions

To make it easier to understand changes between scenario versions, we've added the ability to view and compare those changes. Now you can bring up a window that displays specific changes between two selected versions of the same scenario.

For more information, see [View and manage scenario versions](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md).
```

&#x200B;---

## 예 2: 작업 필요/사용 중단 설명선이 있는 주

`fusion-2026-3-9.md`을(를) 기반으로 합니다.

```markdown
---
title: Workfront Fusion release activity Week of March 9, 2026
description: Workfront Fusion release activity Week of March 9, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of March 9, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of March 9, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/ko/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Log in to Fusion through Adobe IMS

>[!IMPORTANT]
>
>**Action Required: Migrate to IMS Login for Adobe Workfront Fusion by April 15.**
>
>To ensure that you will be able to log in after April 15, your Fusion administrator must migrate you to Adobe IMS. Please contact your Fusion administrator to be migrated.

As part of our ongoing security enhancements, Adobe is deprecating the legacy username and password login method for Adobe Workfront Fusion. Effective **April 15**, the legacy login flow **will no longer be supported**.

Going forward, access to Adobe Workfront Fusion will require authentication through the Adobe Identity Management System (IMS) login flow.

For instructions on provisioning access through the Adobe Admin Console, see [Add users to Adobe Workfront Fusion through the Adobe Admin Console](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-fusion-users-admin-console.md).

If you have questions or need assistance with the migration process, please contact your Adobe representative.

## New route labels

To make it easier to identify routes, we've added labels. Now, routes are labeled in the order they execute. Fallback and error handling routes are also labeled. Route labels also display any filters used for that route.

For more information on routes, see [Add a Router module and configure routes](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).
```

&#x200B;---

## 개요 페이지(`fusion-release-activity.md`) 업데이트 패턴

기존 2026년 7월 섹션에 2026년 7월 20일 주를 추가합니다.

```markdown
## Fusion releases in 2026

### July 2026

* [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
* [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
```

완전히 새로운 연도 시작(예: {YYYY+1}의 첫 번째 릴리스가 게시될 때만 수행):

```markdown
## Fusion releases in 2027

### January 2027

* [Workfront Fusion release activity: Week of January 4, 2027](/help/workfront-fusion/fusion-product-releases/fusion-releases-2027/fusion-2027-1-4.md)

## Fusion releases in 2026

+++ **Click to open**

### December 2026
...
+++
```

&#x200B;---

## TOC.md 업데이트 패턴

2026년 7월 20일 주간을 최신 항목으로 추가:

```markdown
* Fusion release activity {#fusion-release-activity}
    * [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)
    * Fusion releases - 2026 {#fusion-releases-2026}
        * [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
        * [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
        ...
```

&#x200B;---

## 기존 페이지의 알려진 불일치 사항(참조용 — 새 페이지에 복사하지 않음)

1. **TOC.md에 잘못 배치된 연도 제목** — 현재 2026년 1월 2일 항목은 `Fusion releases - 2026` 대신 `Fusion releases - 2025` 제목 아래에 있습니다. 이는 의도한 구조가 아닌 기존 버그입니다.
2. **연도 전에 쉼표 누락** — `fusion-2026-7-13.md`과(와) 같은 페이지는 제목/설명/H1에서 &quot;2026년 7월 13일&quot; 대신 &quot;2026년 7월 13일&quot;을 사용합니다. 새 페이지에는 항상 쉼표를 포함하십시오.
3. **`hidefromtoc`과(와) `exl-id`/`TQID`** — `fusion-2026-4-27.md`까지의 페이지에는 `exl-id`(및 경우에 따라 `TQID`)이 포함되며, `fusion-2026-5-4.md`부터 이후의 페이지는 대신 `hidefromtoc: true`을(를) 사용합니다. 새 페이지는 나중에 게시 파이프라인에 의해 할당되므로 최신 패턴(`hidefromtoc: true`, `exl-id`/`TQID` 없음)을 따라야 합니다.
4. TOC.md **의**`{hide-from-toc}` 접두사 — 이전 항목이 최근 보기에서 오래된 경우 렌더링된 탐색에서 강조 표시를 제거하는 데 사용됩니다. 새 항목에 추가하지 마십시오.
