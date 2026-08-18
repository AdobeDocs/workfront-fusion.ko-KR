---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: '사용자 정의 UI 확장: 문서 인덱스'
description: Workfront Fusion의 사용자 지정 확장
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 3%

---


# 사용자 정의 UI 확장: 문서 인덱스

Fusion은 인터페이스 내에 고유한 웹 UI를 표시할 수 있습니다. 확장이라는 작은 웹 앱을 빌드하여 Adobe에 게시하면 Fusion의 탐색에 단추로 표시됩니다. 사용자가 클릭하면 UI가 Fusion의 기본 영역에 로드되고 로그인한 사용자, 작업 중인 조직 및 팀 등에 대한 정보가 자동으로 전송됩니다.

Fusion 설명서의 이 섹션에서는 Adobe App Builder 또는 프론트엔드 프레임워크에 대한 이전 경험을 가정하지 않고 전체 프로세스를 안내합니다. 해당 코드에 대한 설명과 함께 필요한 코드도 포함되어 있습니다.

## 이 안내서 사용 시기

Fusion에 사용자 지정 화면 또는 도구를 추가하려면 이 안내서를 사용하십시오. 전문 개발자는 아니어도 됩니다. 터미널에 명령을 복사하고 몇 가지 텍스트 파일을 편집하는 것은 편해야 합니다.

사용자 정의 UI 확장을 만들려면 Adobe ID이 필요하고 Adobe 조직에 대한 액세스 권한(Fusion에 로그인하는 데 사용하는 것과 동일한 종류의 액세스 권한)이 필요합니다.

## 빌드할 내용

이 안내서를 마칠 때까지 다음과 같은 작업을 수행할 수 있습니다.

1. 무료 Adobe **App Builder** 프로젝트. 여기서 확장을 사용할 수 있습니다.
1. 사용자 정의 UI를 렌더링하는 작은 웹 앱입니다.
1. 해당 웹 앱은 Fusion의 확장 지점 중 하나에 연결되므로 Fusion 탐색에 표시됩니다.
1. 현재 사용자, 조직 및 팀과 같이 Fusion에서 라이브 컨텍스트를 읽고 사용자가 조직 또는 팀을 전환할 때 반응하는 UI입니다.
1. 조직의 다른 사용자가 볼 수 있도록 확장이 게시되었습니다.

<!--

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  ───────────────────────────────                         ──────────────────────────────
  Left navigation                             A web app hosted by Adobe
   └── Organization                            (App Builder + UI Extensibility)
       └── [Your extension button]  ── click ──▶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

-->

## 목차

페이지를 처음 순서대로 읽습니다. 나중에 필요한 위치로 바로 이동할 수 있습니다.

| # | 페이지 | 대상 |
| --- | ------ | ---------------- |
| 1 | [개요 및 주요 개념](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md) | 어휘, 아키텍처 및 각 Fusion 확장 지점의 용도는 다음과 같습니다. |
| 2 | [도구 및 Adobe 계정 설정](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) | Node.js, Adobe I/O CLI, 로그인 및 Adobe Developer Console에서의 프로젝트 만들기. |
| 3 | [프로젝트를 만들고 Fusion에 맞게 구성](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md) | `aio` 명령줄을 사용하여 일반 App Builder 프로젝트를 생성합니다(제품별 템플릿이 아님). 그런 다음 프로젝트를 Fusion 확장 지점을 가리키고 위젯을 등록합니다. |
| 5 | [UI 빌드](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md) | 사용자 정의 화면을 렌더링하고 Fusion과의 연결(&quot;핸드셰이크&quot;)을 완료합니다. |
| 6 | [Fusion 컨텍스트 참조](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md) | 모든 Field Fusion은 사용자에게 무엇을 의미하는지 그리고 변화에 어떻게 반응하는지를 보냅니다. |
| 7 | [확장 게시](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md) | Fusion에서 확장을 빌드하고 배포하고 표시합니다. |
| 8 | [문제 해결](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md) | 가장 일반적인 오류에 대한 수정 사항. |
| 9 | [데모 연습](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-09-demo-walkthrough.md) | 하나의 선형 복사 붙여넣기 스크립트: 일반 Experience Cloud 셸 템플릿의 스캐폴드→ Fusion으로 재타겟팅하고 Fusion에서 → 스테이지로 →. 라이브 데모에 적합합니다. |
| 10 | [Workfront 및 Fusion API를 호출하는 중](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md) | 런타임 작업 프록시를 사용하여 브라우저 CORS에 도달하지 않고 확장에서 백엔드 API를 호출합니다. `require-adobe-auth`, Fusion v3 헤더 및 작업 예제를 다룹니다. |

## 가용성 참고 사항

Fusion은 현재 다음 확장 지점을 노출합니다.

* `fusion/nav-organization/1` — **조직** 섹션에 표시됩니다.
* `fusion/nav-team/1` — **팀** 섹션에 표시됩니다.

이 중 하나에 대해 게시하려면 먼저 확장 지점을 Adobe 조직에 온보딩해야 합니다. 게시 단계에서 확장 지점이 &quot;존재하지 않습니다&quot;라고 말하지 않으면 [문제 해결](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)을 참조하십시오.

## 공식 Adobe 설명서

이 안내서는 Fusion에만 적용됩니다. 기본 플랫폼의 경우 표준 참조는 다음과 같습니다.

* [UI 확장성 개요](https://developer.adobe.com/uix/docs/)
* [UI 확장 개발 흐름](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [UI 확장 관리(게시/승인/취소)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Adobe App Builder 시작](https://developer.adobe.com/app-builder/docs/getting_started/)
