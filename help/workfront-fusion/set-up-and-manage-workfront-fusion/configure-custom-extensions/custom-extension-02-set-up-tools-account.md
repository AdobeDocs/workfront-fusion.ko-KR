---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: UI 확장 도구 및 계정 설정
description: UI 확장 도구 및 계정 설정
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 0%

---


# UI 확장 도구 및 계정 설정

Workfront Fusion용 UI 확장을 만들려면 먼저 도구 및 계정을 설정해야 합니다. 이 작업은 한 번만 수행하면 됩니다.

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

<!--Access requirements-->

## 전제 조건

UI 확장성 도구 및 계정을 설정하려면 다음 항목이 필요합니다.

* Adobe 조직에 액세스할 수 있는 **Adobe ID**. Fusion에 로그인하는 데 사용하는 계정입니다.
* **App Builder에 대한 개발자 액세스.** 조직 관리자가 **개발자** 역할을 부여하고 사용자를 App Builder이 포함된 **제품 프로필**&#x200B;에 추가해야 할 수 있습니다. 나중에 &quot;개발자가 아님&quot;으로 명령이 실패하거나 조직이 표시되지 않는 경우 Adobe 조직 관리자에게 사용자를 추가하도록 요청하십시오.
* **시스템 관리자** <!--Adobe? Fusion?-->(팀의 다른 사람일 수 있음)에서 최종 릴리스 단계를 수행합니다. 만들고 배포하려면 개발자 역할만 필요하지만 **승인/게시를 위해 확장을 제출하려면 시스템 관리자 역할**&#x200B;이 필요합니다.

  Adobe 액세스 수준에 대한 자세한 내용은
  Adobe 설명서에서 [액세스 권한을 받는 방법](https://developer.adobe.com/uix/docs/guides/get-access/).

* **소프트웨어를 설치하고** 터미널 명령(macOS, Windows 또는 Linux)을 실행할 수 있는 컴퓨터입니다.

## Node.js 설치

Adobe 도구는 **Node.js**&#x200B;에서 실행됩니다. **LTS** 버전(18 또는 20)을 설치해야 합니다.

1. <https://nodejs.org>(으)로 이동하여 **LTS** 설치 관리자를 다운로드합니다.
1. 설치 관리자를 실행하고 기본값을 사용합니다.
1. 터미널을 열고 다음 작업을 실행하여 작동하는지 확인합니다.

   ```sh
   node --version
   npm --version
   ```

   버전 번호가 표시됩니다(예: `v20.17.0` 및 `10.x`).

1. (조건부) `node`을(를) 찾을 수 없으면 터미널을 닫았다가 다시 열거나 컴퓨터를 다시 시작하십시오.

1. [Adobe I/O CLI 설치(`aio`)](#install-the-adobe-io-cli-aio)를 계속합니다.

>[!TIP]
>
>* 여러 노드 버전을 사용하는 경우 `nvm`과(와) 같은 버전 관리자가 편리하지만 선택 사항입니다.
>* Adobe CLI에는 노드 18 이상이 필요합니다. LTS가 아닌 매우 새로운 버전은 때때로 문제를 일으킬 수 있으므로 LTS를 사용하는 것이 좋습니다.

## Adobe I/O CLI(`aio`) 설치

확장을 만들고 빌드하고 게시하는 데 사용하는 명령줄 도구는 `aio`입니다.

전체적으로 설치하려면:

1. 명령줄에서 다음 `npm` 명령을 사용합니다.

   ```sh
   npm install -g @adobe/aio-cli
   ```

1. 다음 명령을 사용하여 설치되었는지 확인합니다.

   ```sh
   aio --version
   ```

   `@adobe/aio-cli/11.x.x`과(와) 같은 항목이 표시됩니다.

1. [Adobe에 로그인](#sign-in-to-adobe)을 계속합니다.

>[!NOTE]
>
> macOS/Linux에서 권한 오류가 표시되면 **하지 않음**&#x200B;하고 `sudo`을(를) 사용하십시오. 대신 npm의 전역 폴더 권한을 수정하거나 홈 디렉터리에 설치하는 노드 버전 관리자를 사용하십시오.

## Adobe에 로그인

1. 다음 명령을 사용하여 CLI를 Adobe 계정에 연결합니다.

   ```sh
   aio login
   ```

1. 브라우저 창이 열리면 Adobe ID으로 로그인하여 액세스를 승인합니다.

1. 로그인에 성공하면 브라우저 탭을 닫고 터미널로 돌아갑니다.

1. (선택 사항) 나중에 로그아웃하려면(예를 들어 계정을 전환하려면) 다음 명령을 사용합니다. `aio logout`.
1. [활성 조직을 확인](#confirm-your-active-organization)합니다.

## 활성 조직 확인

CLI가 가리키는 조직 확인:

```sh
aio console org list      # see organizations you can use
aio console where         # see your currently selected org/project/workspace
```

여러 조직에 속해 있는 경우 올바른 조직을 선택합니다.

```sh
aio console org select
```

이제 프로젝트를 만들 준비가 되었습니다.
