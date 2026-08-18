---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Fusion 컨텍스트 참조
description: Fusion 컨텍스트 참조
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 757
ht-degree: 8%

---

# Fusion 컨텍스트 참조

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

UI에서 `attach(...)`을(를) 호출하면 Fusion에서 현재 세션을 설명하는 **컨텍스트** 개체를 공유합니다. 이 페이지에는 모든 필드, 의미 및 Fusion과 Adobe IMS 식별자의 관계 방식이 나열됩니다.

## 컨텍스트를 읽는 방법

* **초기값:** `connection.sharedContext.get("<key>")`
* **업데이트:** `contextchange` 이벤트를 수신합니다. 최신 개체가 `event.detail.context`에 도착합니다.

전체 코드 패턴에 대해서는 [사용자 지정 확장 UI 빌드](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)를 참조하십시오.

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## 최상위 키

| 키 | 유형 | 설명 |
| ----- | ------ | ------------- |
| `imsToken` | 문자열 | 로그인한 사용자의 Adobe **IMS 액세스 토큰**. 이 토큰을 `Bearer` 토큰으로 사용하여 사용자를 대신하여 Adobe 또는 Fusion API를 호출하십시오. **민감한 항목이므로 기록하거나 표시하지 마십시오.** |
| `imsOrgId` | 문자열 | `XXXXXXXXXXXX@AdobeOrg` 형식의 Adobe **IMS 조직 ID**. |
| `imsUserId` | 문자열 | 로그인한 사용자의 Adobe **IMS 사용자 ID**. |
| `organization` | 오브젝트 | **전체 활성 Fusion 조직**. 자세한 내용은 이 문서에서 [`organization` 필드](#organization-fields)을(를) 참조하십시오. |
| `team` | 오브젝트 \| 정의되지 않음 | **전체 활성 Fusion 팀**(활성화된 경우)(항상 `fusion/nav-team/1`과(와) 관련) 자세한 내용은 이 문서에서 [`team` 필드](#team-fields)을(를) 참조하십시오. |
| `user` | 오브젝트 | **전체 로그인 Fusion 사용자**&#x200B;입니다. 자세한 내용은 이 문서에서 [`user` 필드](#user-fields)을(를) 참조하십시오. |

### Fusion ID 및 IMS ID

각 엔터티에는 **Fusion ID**(Fusion의 자체 API에서 사용)와 **Adobe IMS ID**(Adobe 플랫폼 API에서 사용)가 있습니다.

| 엔티티 | Fusion id | Adobe IMS ID |
| -------- | ----------- | -------------- |
| 조직 | `organization.id` | `imsOrgId`(`organization.externalOrgId`(으)로도 표시됨) |
| 팀 | `team.id` | *(Teams는 Fusion 전용이며 IMS ID가 없음)* |
| 사용자 | `user.id` | `imsUserId` |

## `organization`개 필드

이러한 필드는 활성 조직 레코드에서 찾을 수 있습니다. 대부분의 확장에는 `id`, `name` 및 식별자만 필요합니다.

| 필드 | 유형 | 설명 |
| ------- | ------ | ------------- |
| `id` | 문자열 | Fusion 조직 ID. |
| `name` | 문자열 | 조직 표시 이름 |
| `externalOrgId` | 문자열 | Adobe IMS 조직 ID(`imsOrgId`과(와) 같은 값). |
| `externalId` | 문자열 | Fusion 통합에서 사용하는 외부 식별자 |
| `countryId` | 문자열 | 국가 설정 ID. |
| `timezoneId` | 문자열 | 시간대 설정 ID |
| `serviceName` | 문자열 | 서비스/플랜 식별자 |
| `teamIds` | 문자열[] | 이 조직의 팀 ID |
| `license` | 오브젝트 | 작업, 데이터 전송, 사용자 시트 및 기능 플래그와 같은 플랜 제한 및 권한 |
| `scenariosCount` | 번호 | 조직의 총 시나리오 |
| `activeScenarios` | 번호 | 현재 활성화된 시나리오 |
| `activeApps` | 번호 | 활성 앱 또는 연결 수 |
| `operations`, `operationsExt` | 번호 | 작업 사용 카운터 |
| `transfer`, `transferExt` | 번호 | 데이터 전송 사용 카운터 |
| `isPaused` | 부울 | 조직이 일시 중지되었는지 여부 |
| `isDeleted` | 부울 | 조직이 삭제됨으로 표시되는지 여부 |
| `imsEnabled` | 부울 | 조직이 Adobe IMS에 연결되어 있는지 여부 |
| `usersCount` | 번호 | 조직의 사용자 수 |
| `nextReset` | 문자열(날짜) | 사용 카운터가 다음에 재설정되는 경우. [날짜](#dates) 보기 |

## `team`개 필드

이러한 필드는 팀이 활성 상태일 때 표시됩니다. 팀이 `undefined`인 경우(예: 선택한 팀이 없는 조직 수준 화면) 대체 항목을 제공해야 합니다.

| 필드 | 유형 | 설명 |
| ------- | ------ | ------------- |
| `id` | 문자열 | Fusion 팀 ID. |
| `name` | 문자열 | 팀 표시 이름. |
| `organizationId` | 문자열 | 이 팀이 속한 조직의 Fusion ID. |
| `country` | 문자열 | 팀 국가 설정. |
| `timezone` | 문자열 | 팀 시간대. |
| `license` | 오브젝트 | 팀 수준 제한 및 권한. |
| `activeScenarios` | 번호 | 팀의 활성 시나리오 |
| `activeApps` | 번호 | 팀의 활성 앱 또는 연결. |
| `scenarioDrafts` | 부울 | 시나리오 초안의 활성화 여부입니다. |
| `isDeleted` | 부울 | 팀을 삭제 표시할지 여부입니다. |
| `created` | 문자열(날짜) | 팀을 만든 시간. [날짜](#dates)를 참조하세요. |

## `user`개 필드

이 필드는 로그인한 Fusion 사용자에게 적용됩니다.

| 필드 | 유형 | 설명 |
| ------- | ------ | ------------- |
| `id` | 문자열 | Fusion 사용자 ID. |
| `name` | 문자열 | 전체 이름. |
| `email` | 문자열 | 이메일 주소. |
| `avatar` | 문자열 | 아바타 이미지 URL. |
| `locale` | 문자열 | 사용자 로케일(예: `en`). |
| `language` | 문자열 | 기본 설정 언어(설정된 경우) |
| `timezone` | 문자열 | 시간대 이름. |
| `timezoneId` | 문자열 | 시간대 설정 ID입니다. |
| `countryId` | 문자열 | 국가 설정 ID. |
| `localeId` | 문자열 | 로케일 설정 ID. |
| `features` | 오브젝트 | 사용자별 기능 플래그(예: `allow_apps`, `public_templates`). |
| `usersAdminsRoleId` | 문자열 | 해당되는 경우 사용자의 관리자 역할 ID입니다. |

>[!NOTE]
>
> `user` 개체에는 추가 내부 필드가 포함될 수 있습니다. 여기에 설명된 필드만 사용해야 합니다. 다른 필드는 예고 없이 변경될 수 있으며 일부 인증 관련 필드는 기록하거나 표시해서는 안 됩니다.

## 일자

컨텍스트는 확장에 도달하기 전에 serialize되므로 **날짜 필드가 JavaScript `Date` 개체가 아닌 문자열**(예: `"2026-06-24T00:00:00.000Z"`)로 도착합니다. 필요한 경우 다음과 같이 변환할 수 있습니다.

```js
const resetDate = new Date(context.organization.nextReset);
```

## 컨텍스트 업데이트

Fusion은 다음과 같은 경우 전체 컨텍스트를 `contextchange`을 통해 다시 보냅니다.

* **사용자가 조직을 전환**,
* **사용자가 팀 전환** 또는
* **로그인한 사용자의** 정보가 변경됩니다.

하나의 값만 변경되었다고 가정하지 않고 `contextchange` 처리기 내에서 사용하는 모든 키를 항상 다시 읽으십시오.

## 보안 모범 사례

* **`imsToken`을(를) 기록하거나 표시하거나 유지하지 마십시오.** 암호처럼 취급하십시오.
* HTTPS를 통해 신뢰할 수 있는 Adobe/Fusion 종단점에만 토큰을 `Bearer` 토큰으로 보냅니다.
* 기능에 필요한 것 외에 컨텍스트의 개인 데이터를 저장하지 마십시오.

## 토큰을 사용하여 API 호출

`imsToken`(더하기 `organization.id`/`team.id`)을(를) 실제 Workfront으로 전환하거나
Fusion 데이터, CORS가 차단되므로 브라우저에서 직접 해당 API를 호출할 수 없습니다.
그래. 대신 작은 App Builder 런타임 작업을 통해 호출을 라우팅합니다. 다음을 참조하십시오
[Workfront 및 Fusion API를 호출하는 중](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


사용자 지정 확장을 만드는 프로세스를 계속하려면 [확장 게시](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md)를 참조하십시오.
