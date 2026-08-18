---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 사용자 정의 확장 UI 빌드
description: 사용자 정의 확장 UI 빌드
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 0%

---


# 사용자 정의 확장 UI 빌드

>[!NOTE]
>
>이 문서에서는 소프트웨어 개발 도구에 대해 어느 정도 친숙하다고 가정합니다.

이 절차에서는 사용자가 실제로 보는 화면을 빌드하고 Fusion으로 **연결(&quot;핸드셰이크&quot;)**&#x200B;을 완료하는 방법을 설명합니다.

이 프로세스 중에 확장이 숨겨진 **등록** 프레임과 표시되는 **UI** 프레임의 두 프레임으로 실행된다는 점을 상기해야 합니다.

사용자 지정 확장과 관련된 프레임에 대한 자세한 내용은 [UI 확장에 포함된 프레임](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension)을 참조하십시오.

등록 프레임 빌드에 대한 지침은 [UI 확장성에 대한 프로젝트 만들기](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md)를 참조하십시오.

## 두 프레임 간 경로

두 프레임 모두 동일한 `index.html`을(를) 로드합니다. 작은 프런트 엔드 라우터가 URL을 기반으로 표시할 구성 요소를 결정합니다.

1. `web-src/src/components/App.js`에서 경로를 설정합니다. 중요한 부분은 다음과 같습니다.

   ```jsx
   import { HashRouter as Router, Routes, Route } from "react-router-dom";
   import ExtensionRegistration from "./ExtensionRegistration";
   import DashboardWidget from "./DashboardWidget";
   
   export default function App() {
     return (
       <Router>
         <Routes>
           {/* Background frame: registers the extension with Fusion */}
           <Route index element={<ExtensionRegistration />} />
           <Route path="index.html" element={<ExtensionRegistration />} />
   
           {/* Visible frame: the URL you returned from getWidget() */}
           <Route path="my-widget" element={<DashboardWidget />} />
         </Routes>
       </Router>
     );
   }
   ```

   이러한 경로는 다음과 같이 이전 구성에 매핑됩니다.

   * 기본 경로(`index`)는 `register(...)`을(를) 호출하는 숨겨진 프레임인 **`ExtensionRegistration`**&#x200B;을(를) 렌더링합니다.
   * `my-widget` 경로는 **`DashboardWidget`**&#x200B;을(를) 렌더링하며, 표시되는 UI입니다. [이전 페이지](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md)의 `getWidget()`에서 반환된 `url: "/index.html#/my-widget"`과(와) 일치합니다.

   >[!NOTE]
   >
   > **경로와 `getWidget` URL이 일치해야 합니다.** 경로 이름을 변경하는 경우 `url`도 변경하십시오. 그렇지 않으면 빈 페이지가 로드됩니다.

1. [을(를) 계속하고 `attach`](#complete-the-handshake-with-attach)과(와) 핸드셰이크를 완료합니다.

## `attach`(으)로 핸드셰이크 완료

이는 표시되는 UI에서 가장 중요한 단일 행입니다. Fusion은 UI 프레임을 열면 해당 프레임이 &quot;체크 인&quot;될 때까지 기다립니다. 코드가 `attach({ id })`을(를) 호출하여 체크 인합니다.

**생략된 경우 *&quot;대상 iframe에서 초기 메시지를 기다리는 중&quot;*과 같은 오류가 발생하여 Fusion 시간이 초과됩니다**.

1. `web-src/src/components/DashboardWidget.js`에 다음 추가:

   ```jsx
   import { useEffect, useState } from "react";
   import { attach } from "@adobe/uix-guest";
   import { extensionId } from "./Constants";
   
   export default function DashboardWidget() {
     const [connection, setConnection] = useState(null);
   
     useEffect(() => {
       // Tell Fusion this UI frame is ready. Required.
       attach({ id: extensionId })
         .then(setConnection)
         .catch((e) => console.error("attach failed", e));
     }, []);
   
     if (!connection) {
       return <p>Connecting to Fusion...</p>;
     }
   
     return <h2>Hello from my Fusion extension!</h2>;
   }
   ```

   이 코드는 다음을 수행합니다.

   * Fusion이 응답하면 `attach({ id })`이(가) **연결 개체**&#x200B;를 반환합니다. 다음 단계에서 이를 사용하여 Fusion 전송 컨텍스트를 읽게 되므로 이를 저장하는 것이 좋습니다.
   * 연결이 확인될 때까지 짧은 &quot;연결 중...&quot; 메시지가 표시됩니다.
   * `Constants.js`에서 설정한 **동일한`extensionId`**&#x200B;을(를) 사용합니다.

   이 시점에서 작업 중인 확장이 있습니다. 즉, 메시지를 등록 및 첨부하고 표시합니다. 이 이후의 모든 작업은 Fusion이 제공하는 데이터를 사용하는 것입니다.

1. [컨텍스트 Fusion 공유 읽기](#read-the-context-fusion-shares)를 계속합니다.

## Fusion 공유 컨텍스트 읽기

연결하면 현재 사용자, 조직 및 팀에 대한 정보가 있는 **공유 컨텍스트**&#x200B;가 노출됩니다. `connection.sharedContext.get("<key>")`을(를) 사용하여 개별 값을 읽을 수 있습니다.

```jsx
const orgId = connection.sharedContext.get("imsOrgId");
const organization = connection.sharedContext.get("organization"); // full Fusion org
const user = connection.sharedContext.get("user");                 // full Fusion user
```

이 예는 사용자가 조직 또는 팀을 전환할 때도 업데이트되는 완전한 사후 예제를 보여 줍니다.

```jsx
import { useEffect, useState } from "react";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

function readContext(source) {
  // sharedContext behaves like a Map (.get); the change event gives a plain object.
  const get =
    typeof source.get === "function" ? (k) => source.get(k) : (k) => source[k];
  return Object.fromEntries(KEYS.map((k) => [k, get(k)]));
}

export default function DashboardWidget() {
  const [context, setContext] = useState(null);

  useEffect(() => {
    let cleanup = () => {};
    attach({ id: extensionId })
      .then((connection) => {
        // 1) initial values
        setContext(readContext(connection.sharedContext));

        // 2) react to org/team/user changes pushed by Fusion
        const onChange = (event) =>
          setContext(readContext(event?.detail?.context ?? connection.sharedContext));
        connection.addEventListener("contextchange", onChange);
        cleanup = () => connection.removeEventListener?.("contextchange", onChange);
      })
      .catch((e) => console.error("attach failed", e));
    return () => cleanup();
  }, []);

  if (!context) return <p>Connecting to Fusion...</p>;

  return (
    <div>
      <h2>{context.organization?.name ?? "No organization"}</h2>
      <p>Signed in as {context.user?.name} ({context.user?.email})</p>
      <p>IMS org: {context.imsOrgId}</p>
    </div>
  );
}
```

다음 사항을 기억하십시오.

* `attach` 바로 뒤에 있는 `connection.sharedContext.get(key)`에서 **초기 값을 읽기**&#x200B;합니다.
* **동기화 상태를 유지하려면`contextchange`**&#x200B;에 가입하세요. Fusion은 활성 조직, 팀 또는 사용자가 변경될 때마다 이 이벤트를 실행합니다. 새 값이 `event.detail.context`에 도착합니다.

키 전체 목록과 각 키에 포함된 내용은 [Fusion 컨텍스트 참조](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)에 포함되어 있습니다.

사용자 지정 확장을 구성하는 프로세스를 계속하려면 [Fusion 컨텍스트 참조](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)로 이동하십시오.
