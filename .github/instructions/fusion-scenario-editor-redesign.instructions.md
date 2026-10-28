---
applyTo: "help/workfront-fusion/**"
source-git-commit: 7c7e80b06b730fd56e581ebf74081f99e04318c0
workflow-type: tm+mt
source-wordcount: '3973'
ht-degree: 1%
---

# Fusion 시나리오 편집기 UI 재디자인 - 프로젝트 노트

> 이 파일은 GitHub Copilot이 동일한 컨텍스트를 갖도록 보관된 클라우드 코드 메모리 파일(`fusion-scenario-editor-redesign.md`)의 동기화된 복사본입니다. 클로드의 사본은 진실의 소스입니다. 파일이 업데이트될 때마다 동일한 편집/커밋에서 일치하도록 이 파일을 업데이트해야 합니다. 두 파일이 동의하지 않으면 클라우드 메모리 파일을 신뢰하고 이 파일을 다시 동기화하십시오.
>
> 이는 저장소 전체 `.github/copilot-instructions.md`이(가) 아닌 범위 Copilot 지침 파일(`.github/instructions/*.instructions.md`)이므로 Copilot이 저장소의 모든 요청이 아닌 `help/workfront-fusion/` 아래의 파일에서 작업할 때만 적용됩니다.

Becky는 많은 문서에서 Fusion의 시나리오 편집기 UI 재디자인(새로운 경험과 클래식 경험 비교)을 문서화하고 있습니다. **라이브 색인** — 새 스크린샷을 찍거나 새 UI 세부 정보가 확인될 때마다 업데이트하십시오(추가하지 마십시오). 따라서 이 작업을 선택하는 모든 사람(또는 모든 도우미)은 &quot;X에 대한 스크린샷/팩트가 이미 있습니까?&quot;라고 답할 수 있습니다. 다시 파생시키지 않고

`becky-updates-to-Fusion-scenario-editor` 분기에서 작업이 수행됩니다. 기본 추적 스프레드시트: `C:\Users\rebeccas\Desktop\Fusion scenario editor UI redesign - affected articles.xlsx`(시트 &quot;영향을 받는 문서&quot; = 기사별 상태/우선 순위, 시트 &quot;기능 비교&quot; = classic-vs-new 기능 차이).

이 문서에서 확인되지 않은 인라인에 플래그를 지정하는 규칙입니다. `<!-- BECKY CHECK ME: ... -->` 바로 그 자리에서, 절대 보이는 설명선으로는 사용할 수 없습니다.

## 스크린샷 인벤토리(새 경험)

파일을 복제하지 않고 절대 경로를 통해 문서 간에 다시 사용합니다(예: `/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png`).

**`help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/`**(`scenario-editor.md` 다시 작성 — 공유 UI 크롬 아이콘, 모든 곳에서 재사용):
`run-once-new.png`(한 번 실행, 아이콘 전용), `save-icon-new.png`, `notes-icon-new.png`, `scheduling-new.png`(하단 표시줄 예약 전환 + 빈도 레이블(예: &quot;데이터가 도착하면 즉시&quot;), `auto-align-icon-new.png`, `scenario-editor-new.png`(전체 캔버스), `top-bar-new.png`, `controls-new.png`, `tools-new.png`, `favorites-new.png`, `ask-ai-new.png`, `canvas-navigation-new.png`, `search-modules-icon-new.png`, `find-and-replace-icon-new.png`, `snippets-icon-new.png`, `explain-flow-icon-new.png`, `export-blueprint-icon-new.png`, `export-as-headless-template-icon-new.png`, `import-blueprint-icon-new.png`, `previous-version-icon-new.png`, `devtool-icon-new.png`, `scenario-settings-icon-new.png`, `additional-controls-new.png`.

**`help/workfront-fusion/build-practice-scenarios/assets/`**(기본 시나리오 자습서):
`new-placeholder-module.png`(빈 캔버스 자리 표시자 카드), `new-connector-picker.png`(앱/서비스 선택기 패널 — 범주 목록 왼쪽: 즐겨찾기, 모든 앱, Adobe Workfront, Adobe Firefly Services, Adobe Creative 및 컨텐츠, Adobe Cloud Services, 생성 AI, 내장, 검색 오른쪽), `new-renamed-module.png`, `new-map-toggle.png`, `new-map-id.png`, `new-execution-bubble.png`, `clock-icon-on-watch-record.png`(카드의 모듈 수준 일정/시계 배지), `new-map-in-filter.png`(매핑된 프로젝트 ID 조건으로 필터 창 설정), `new-mapped-update-record.png`(매핑된 ID를 &quot;레코드 업데이트&quot; 모듈로 설정), `new-text-binary-function.png`(&quot;T&quot; 매핑 패널 탭), `new-module-output-icon.png`(별 매핑 패널 탭), `new-mapped-name-block.png`(`upper(...)` 내의 매핑된 이름 블록).

**`help/workfront-fusion/create-scenarios/add-modules/assets/`**:
`add-a-module-between-modules.png`(두 모듈 사이의 경로를 마우스 오른쪽 단추로 클릭→메뉴: 필터 설정/링크 해제/라우터 추가/모듈 추가/메모 추가 - 아직 필터/라우터가 없는 경로에서 캡처되었으므로 경로별 또는 필터 관련 경로에 전체 옵션 설정이 아닐 수 있음), `new-filter-setup-xml-example.png`(필터 창을 설정하고 `add-a-filter-to-a-scenario.md`에서 사용되는 File-Name-ends-xml 예제와 일치함), `fallback-route-new.png`(필터 창, 대체 경로 확인란을 선택하고 강조 표시, 라우터-module.md에서 사용), `new-filter-specific-user.png`(경로 경로에 &quot;특정 사용자&quot; 레이블이 지정된 필터 창 설정, 대체 확인란 선택 해제, 매핑된 ID 조건, 주황색 강조 상자 포함) - router-module.md의 &quot;새 경험에서 경로에 필터 추가&quot; 단계별로 사용) `new-filter-specific-user-unmarked.png`(동일한 &quot;특정 사용자&quot; 필터, 강조 상자 없음 - router-module.md에서 if/else 예제의 `if` 반으로 사용됨), `new-not-specific-user-unmarked.png`(특정 사용자 아님, 대체 확인란으로 레이블이 지정된 필터 창 설정 선택됨, 조건 없음, 강조 상자 없음 - router-module.md에서 if/else 예제의 `else` 반으로 사용됨).

**아직 가져오지 않음**: router-module.md에 대해 현재 해결되지 않은 항목이 없습니다.

**`help/workfront-fusion/create-scenarios/config-error-handling/assets/`**:
`new-add-error-handler-in-menu.png`(이 모듈을 마우스 오른쪽 단추로 클릭→설정 컨텍스트 메뉴: 이 모듈만 실행/오류 처리기 추가/이름 바꾸기/복제/복사 모듈/메모 추가/복사 매핑/복사 모듈 이름/앱 메타데이터/삭제 모듈 추가 — &quot;오류 처리기 추가&quot;가 강조 표시됨 — 오류 처리.md에서 사용됨), `new-error-handling-directives.png`(앱/서비스 선택기가 오류 처리기에서 열리며 왼쪽 패널의 일반 앱 범주와 함께 전용 &quot;오류 처리&quot; 범주가 선택됨 — 중단, 커밋, 무시, 다시 시작, 롤백 — 모듈 및 라우터가 추가된 오류 처리기 흐름에 모두 사용됨 — 오류 처리.md에서 재사용), `new-error-handler-examples-with-numbers.png`(오류 처리 처리기 계층 구조에 대한 번호가 매겨진 예제, **5&rbrace;의 캔버스-토글 보기에서 캡처됨, 오류 처리.md 이미지에 사용됨; 캡션 (가독성을 위한 작은 보기).**`scenario-editor.md`

**`help/workfront-fusion/get-started-with-fusion/understand-fusion/assets/`**:
`new-scenario-example-unmarked.png`(소스 스크린샷 Becky 제공됨, 표시되지 않음 — 8-module Excel/Workfront 사용자 동기화 시나리오: 추가된 사용자 → 라우터 → Workfront에서 사용자 찾기 → Workfront에서 사용자 찾기 → 3 분기 [기존 사용자 ID 설정/에서 새 사용자 만들기 → 새 사용자 ID 설정/사용자 ID 변수 가져오기 → 스프레드시트에 사용자 ID 업로드] — classic의 `fusion-integration-example.png` 및 `fusion-glossary.md`의 &quot;시나리오&quot; 항목(`entire-scenario-blank.png`)과 동일한 시나리오; 이 예제의 추가 마크업에 대한 소스로 유지), `new-entire-scenario-scenario.png`, `new-scenario-trigger.png`, `new-scenario-module.png`, `new-scenario-route.png`(모두 빨간색 강조 상자를 통해 위의 표시되지 않은 소스에서 파생됨), `new-scenario-connectors.png`(정확한 상자 배치에 대해서는 문서별 메모 참조), (Becky-제공, 앱 주변의 빨간색 상자 새 경험 커넥터 선택기에서, `new-scenario-segment.png`(Becky 제공, 2-module Workfront 감시 이벤트 → 개체 세그먼트 변환, 박스형, unboxed Microsoft 365 이메일 모듈 뒤), `new-fusion-automation-example.png`(Becky 제공, 표시가 해제된 4-module Workfront 전용 예 — 보기 레코드 → 프로젝트 정보 가져오기 → &quot;할당 대상&quot; → 업데이트 만들기 — Classic의 `fusion-template-example.png`과 동일한 시나리오, Becky가 원할 경우 `license-automation-vs-integration.md`의 &quot;작업 자동화를 위한 Workfront Fusion 예제&quot; 섹션에서 재사용 가능), `new-module.png`(PowerShell/System.Drawing을 통해 자르기, `new-scenario-example-unmarked.png`에서 &quot;Workfront에서 사용자 찾기&quot; 모듈의 단일 카드 자르기, 일반적으로 `fusion-glossary.md`의 &quot;모듈 항목&quot;에 사용, 빨간색 상자 없음) `new-map-single.png`, `new-map-multiple-with-text.png`, `new-map-formula-with-text.png`(단일 항목, 텍스트가 있는 여러 항목, 여러 항목 및 텍스트가 있는 함수 등 `mapping-overview.md`의 shadebox 예제에 대한 새로운 경험 대체 요소), `new-mapping-panel-blank.png`(`mapping-overview.md`에서 사용된 새로운 경험 매핑 패널 스크린샷), `new-collection.png`(`mapping-overview.md`에서 사용된 새로운 경험 컬렉션 스크린샷), `new-collection-dropdown.png`(`mapping-overview.md`에서 사용되고 `map-data-from-one-to-another.md`에서 재사용된 새로운 경험 컬렉션 요소 드롭다운 스크린샷), `new-array.png`(`mapping-overview.md`에서 사용된 새로운 경험 배열 스크린샷).

**`help/workfront-fusion/create-scenarios/config-scenarios-settings/assets/`**:
`new-scenario-settings-ex-1.png`(2모듈 예 시나리오 - &quot;수신 요청 감시...&quot; 레이블이 지정된 레코드를 감시합니다. →요청에서 프로젝트로 전환&quot;이라는 레이블이 지정된 기타 작업 — configure-scenario-settings.md의 최대 주기 예제에 사용됨), `new-max-number-cycles.png` (캔버스 위에서 열리는 시나리오 설정 패널, 컨트롤 영역의 톱니바퀴 아이콘을 통해 열리는 &quot;최대 주기 수&quot; 필드, 값 `1`(configure-scenario-settings.md에서 사용됨).

## 새로운 경험 UI 사실 확인(스크린샷 재사용을 위해 불필요)

- **다른 모듈 추가** 단추를 클릭하면 앱/서비스 선택기→ 열립니다(첫 번째 모듈을 추가할 때와 동일한 선택기). → 단추→ 모듈의 오른쪽 가장자리를 가리키면 앱/서비스 선택기가 열립니다.
- 모듈을 마우스 오른쪽 단추로 클릭 → 설정 컨텍스트 메뉴(순서): 이 모듈만 실행 / **오류 처리기 추가** / 이름 바꾸기 / 복제 / 복사 모듈 / 메모 추가 / 복사 매핑 / 복사 모듈 이름 / 앱 메타데이터 / **삭제 모듈**. 두 명 모두 Classic에서 변경되지 않은 것으로 확인되었습니다.
- **필터 설정** 창→ 열리면 두 모듈 사이의 경로를 마우스 왼쪽 단추로 클릭합니다. 동일한 경로를 마우스 오른쪽 버튼으로 클릭하면 &quot;필터 설정&quot;이 옵션으로 제공되는 메뉴가 아닌 다른 전체 컨텍스트 메뉴가 열립니다.
- 경로를 마우스 오른쪽 단추로 → **라우터 추가** 및 **모듈 추가**&#x200B;가 모두 옵션입니다(`add-a-module-between-modules.png` 참조).
- **필터 복사** / **이미 필터가 있는 경로를 마우스 오른쪽 단추로 클릭하여 필터 붙여넣기**&#x200B;가 여전히 존재하고 동일한 방식으로 작동합니다. 즉, 새 카드 캔버스와 일치하도록 시각적으로 재지정되었지만 동일한 옵션/레이블입니다.
- 라우터 모듈 자체를 클릭해도(가장자리를 가리키지 않음) 새 경로가 추가되고, 변경되지 않은 상태로 확인됩니다.
- **경로 순서 지정**(라우터 모듈→ 마우스 오른쪽 단추를 클릭하여 &quot;경로 순서 지정&quot;→ 끌어서 놓기) — 유효하며 classic과 변경되지 않았습니다.
- **경로 비활성화**(&quot;경로 비활성화&quot; → 경로의 경로를 마우스 오른쪽 단추로 클릭) 및 비활성화된 경로 표시(레이블의 회색 경로 + 비활성화된 경로 아이콘) — classic에서 변경되지 않았음을 확인했습니다.
- 라우터 모듈(&quot;흐름 제어&quot; > &quot;라우터&quot;)은 새 선택기의 **기본 제공** 범주 아래에 있습니다(또한 &quot;모든 앱&quot;에도 표시되지만 기본 제공은 지침에 인용할 범주).
- 대체 경로: 라우터 모듈 자체에 별도의 화살표로 표시되는 클래식과 달리 새 경험은 경로의 레이블에 녹색 텍스트로 **&quot;대체&quot;**&#x200B;을(를) 표시하여 대체 경로를 표시합니다. 이 경우 화살표 마커 스크린샷이 필요하지 않습니다.
- 오류 처리기 경로: 클래식(투명 원과 실선 원)과 달리 새 경험은 점선과 빨간색 **&quot;오류 처리기&quot;** 레이블로 오류 처리기 경로를 표시합니다. 이 사실에는 스크린샷이 필요하지 않습니다.
- 모듈 이름 수정(실제 Workfront 이름, 이전 초안에서 전송된 오타가 아님): **&quot;레코드 보기&quot;**(단수, &quot;레코드 보기&quot;가 아님), **&quot;레코드 업데이트&quot;**(레코드 업데이트&quot;가 아님).
- **DevTool 질문이 해결되었습니다(@vtigranyan 릴리스 정보의 10/23/26).** 독립 실행형 개발자 도구가 **제거되지 않음**. 이제 7개의 도구가 디자이너에 빌드되었습니다(아래 &quot;릴리스 정보 업데이트&quot; 참조). **모듈에 초점을 맞추고**, **매핑으로 모듈을 찾고**, **Base64 텍스트 변환기를 찾습니다**. Base64는 `base64()` 및 이진 변환 함수를 통해 매핑에서도 사용할 수 있습니다. `create-a-scenario-workflow.md`에서 &quot;DevTool 열기&quot; 바로 가기 행을 유지합니다.
- 여전히 확인되지 않음: 선택기의 행당 정보 아이콘, 버전 V자형 화살표 및 오른쪽 아래 빠른 액세스 버블의 목적, 선택기의 즐겨찾기 범주가 편집기의 즐겨찾기 패널과 동일한 목록인지 여부, 라우터를 접거나 펼치는 방법(릴리스 정보에 설명되지 않은 컨트롤). 피쳐 비교 시트를 참조하십시오.

## 이 재설계를 위해 설정된 주택 규칙(나머지 모든 문서에 적용)

- 전체 병렬 복제: 앵커 충돌을 피하는 데 필요한 모든 위치에 `(Classic)`개의 접미사가 있는 &quot;...새 경험(권장)&quot;에 대한 H2/H3 트리 하나와 &quot;....클래식 경험&quot;에 대한 별도의 접미사 하나. 이제 2개 이상의 하위 항목이 있는 제목 아래에 미니 목차를 추가합니다.
- &quot;새 제품 및 클래식 제품&quot; 설명을 **문서 소개** 끝(자체 H2가 아님)에 있는 단일 `>[!NOTE]`(으)로 축소하고 이 정확한 단어를 다시 사용합니다. &quot;문서 시나리오 편집기에서&quot;가 링크에 추가됩니다.
  > Workfront Fusion에서 시나리오 편집기를 새 경험으로 전환합니다. 이 전환 중에 클래식 경험과 새 경험을 모두 사용할 수 있으며 언제든지 전환할 수 있습니다. 새 경험을 사용하는 것이 좋습니다. 자세한 내용은 문서 시나리오 편집기에서 [새 경험 및 클래식 경험](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)을 참조하십시오.
- 새 경험 머리글에는 `(Recommended)`(예: `## Add a filter in the new experience (Recommended)`)이(가) 포함됩니다.
- UI와 관계없는 콘텐츠(예: `add-a-module-basic.md`의 `?moduleId=` URL 매개 변수 메모)는 복제하지 않아도 됩니다. 판단을 사용하되, 확실하지 않은 경우 먼저 Becky에게 문의하십시오(메시지가 묻지 않고 이동되기 전에 푸시되었습니다).
- Becky가 전체 프로시저가 경험 간에 동일하다고 확인한 경우(UI에 관계없는 메모뿐만 아니라) 새/클래식 H2/H3으로 아예 분할하지 마십시오. 새 경험 문구를 사용하여 단일 프로시저로 축소하십시오(예: `view-scenario-data-flow.md`의 &quot;실행 중인 시나리오에서 데이터 흐름 보기&quot;). 기본 가정은 여전히 절차가 다르고 분할이 필요하다는 것입니다. 명시적인 확인 후에만 축소됩니다.
- 새로운 시각과 고전적인 시각이 완전히 다른 하나의 실례가 되는 스크린샷(완전한 단계별 절차가 아님)의 경우, 하나를 선택하거나 플래그를 놓고 기다리지 말고 — 둘 다 먼저 표시, 새로운 사항: 각 이미지 바로 위에 일반 텍스트 레이블 라인(&quot;새 경험&quot; / &quot;클래식 경험&quot;), 새로운 경험 먼저. 이미지 레이블뿐만 아니라 주변 산문에서도 새 경험 비헤이비어를 먼저 언급하십시오(예: &quot;...새 경험에서 X로 표시 또는 클래식 경험에서 Y로 표시&quot;). `view-scenario-data-flow.md`의 실행/출력 표시기를 참조하십시오.
- 확인되지 않은 모든 인라인을 즉시 `<!-- BECKY CHECK ME: ... -->`(으)로 플래그를 지정합니다. 표시되는 콜아웃이 없습니다.
- 기사의 모든 플래그가 해결되면 추적 스프레드시트의 &quot;영향을 받는 문서&quot; 시트(G열)에 해당 행 `Yes`을(를) 표시합니다. 일부 플래그만 해결되면 `In progress`을(를) 사용합니다. `Yes`이지만 범위가 커진 행(예: 10/23/26 릴리스 노트 비교 후)에 `Reopen`을(를) 사용합니다.
- 2026년 10월 23일에 추가된 스프레드시트 태그: `NEW (10/23/26)`부터 시작되는 행/메모(밝은 노란색 행)는 릴리스 노트의 새 항목이고, `UPDATED (10/23/26)`부터 시작되는 메모(밝은 주황색 셀)는 기존 행에 추가된 새 정보입니다. 편집하기 전에 스프레드시트를 백업합니다. `Fusion scenario editor UI redesign - affected articles - BACKUP 2026-10-23.xlsx`(데스크톱).

## 릴리스 노트 업데이트 (2026-10-23) - @vtigranyan의 문서 요청에서 새로운 범위

Source: Fusion Scenario Designer: 새로운 UI/UX 문서 요청; **릴리스 예상: 2026-10-28**; 발표 필요. 2026년 10월 23일에 스프레드시트와 비교하여 새 행/노트가 여기에 태그 지정됩니다(규칙 참조). 주요 특징:

- **스위치:** 캔버스의 오른쪽 상단에 있는 &quot;새 디자인을 사용해 보기&quot; 스위치, 시나리오가 다시 로드됨, 사용자당 **저장됨**(팀원은 영향을 받지 않음), 조직이 아직 적합하지 않은 경우 숨겨짐. 피드백은 오른쪽 상단 컨트롤에 있습니다.
- **캔버스:** 가로 카드(아이콘, 이름, 설명, 모듈 ID), 라우터 = 컴팩트 분기 타일, 지시어 = 작은 악센트 카드, **화살표가 있는 곡선 링크, 오류 처리기 링크 파선**, 녹색/노란색/빨간색 상태 표시기, 확대 시 세부 사항이 점진적으로 표시되며 모듈은 축소된 아이콘으로 간소화됩니다. **자세히 보기** = 작은 타일, 더 촘촘한 격자, 래핑된 이름, 다시 로드 안 함(&quot;아이콘&quot; 제외), 시나리오와 점 격자 크기 조절, **어두운 모드**, 포커스 = 맞춤-시나리오, minimap은 뷰포트를 표시하고 클릭-앤-드래그를 지원합니다.
- **실행/예약:** 한 번 실행, 예약 및 예약 온/오프 스위치는 하나의 간단한 컨트롤입니다.
- **라우터 분기 접기**(편집 모드): 경로를 숨기고, 숨겨진 경로/모듈 수 및 경고/오류 심각도를 표시하고, 시나리오와 함께 저장하고 실행 취소/다시 실행으로 작업합니다. 검색, 유효성 검사, 라이브 추적 및 기록이 자동으로 확장되며, 실행 검토에 항상 모든 내용이 표시됩니다.
- **모듈 브라우저:** 검색 우선 순위, 커넥터가 모듈 이름/설명 위의 순위와 일치함, 비공개, 프리미엄, 베타, 커넥터 정의 모듈 그룹에 대한 배지, 오류 처리기 추가 시 우선 순위가 지정된 지시문.
- **편집 중:** 실행 취소/다시 실행/모두 실행 취소; **찾기 및 바꾸기**(변수, Source, 연결 탭, 전체 시나리오 또는 하나의 모듈, 영향을 받는 모듈을 미리 보고, 행을 선택하여 모듈을 표시하고, 연결을 같은 앱의 호환 가능한 모듈 중 하나 또는 모두에 복사); **조각**(검색, 태그, 미리 보기, 고정, 정렬, 드래그 앤 드롭, 가져오기/내보내기, 팀/조직과 공유, 사용자에게 복사본 보내기, 공유 탭).
- **모듈 설정/검사/탐색, 찾기 및 바꾸기, 코드 조각, 라이브 트레일, 요청/응답을 위한** 오른쪽 도크 1개, 중첩된 보기가 현재 패널을 **뒤로** 작업으로 바꿉니다.
- **라이브 추적:** 요청 시간 목록 + 실행 활동; 검색, 상태 필터, 최신 항목 팔로우, 지우기; 닫힌 중간 실행 시 제어 다시 열기. 요청을 선택하면 모듈이 표시되고 요청/응답 세부 정보(작업 탐색, 헤더/본문, 원시 보고서 복사 또는 cURL)가 열립니다.
- **실행 기록**(편집기에 있음): 동일한 마스터/세부 패턴, 상태, 기간, 작업, 데이터 크기, 상태 필터, 이벤트 검색, 이전/다음 실행, 이벤트를 선택하면 모듈이 가운데로 정렬됩니다.
- **캔버스 도구 실행 검토:** 다음 오류 또는 경고(오류 먼저, 경고, 왼쪽에서 오른쪽, 없는 경우 숨김), 검색 모듈(Ctrl+K / ⌘K), 읽기 전용 메모 토글(시나리오에 메모가 있는 경우에만), 흐름 설명(중지 Esc), 확대/축소/포커스/미니맵, Compact View 스위치(편집 모드 설정을 변경하지 않음, 저장된 내용이 없음)로 이동합니다.
- **한 번 실행/트리거:** 동일한 흐름(원시 JSON 포함), 이전 실행 입력 재사용, 웹후크 대기, 웹후크 및 하위 시나리오 입력 포함).
- **임시 디버그 로그**(시나리오 설정): 다음 1시간/1일/다음 실행/다음 10회 실행, 저장하지 않고 즉시 적용, &quot;켜기 전까지&quot;를 표시하거나 왼쪽 실행, 끄기, 자동 끄기, 모든 실행 카운트(새 데이터가 없는 예약된 실행 포함). 한 번 실행은 항상 요청/응답 세부 정보를 유지합니다. 새 디자이너 전용, 조직 기능 플래그, 편집 권한이 필요합니다.
- **7가지 개발자 도구가 내장되어 있습니다.** 앱 메타데이터(마우스 오른쪽 버튼 클릭 모듈), 매핑 복사(소스 모듈을 마우스 오른쪽 버튼으로 클릭하고 호환 모듈에 붙여넣기), 필터 복사(필터링된 링크를 마우스 오른쪽 버튼으로 클릭하고 다른 링크에 붙여넣기), 모듈 이름 복사/모듈 이름 붙여넣기(마우스 오른쪽 버튼 클릭 모듈), 연결 교체/변수 교체/소스 다시 매핑(연결/변수/Source 탭 찾기 및 바꾸기→.
- **변경되지 않음:** 블루프린트, 매핑, 필터, 일정, 연결, 라우터, 오류 처리기, 반복기, 집계, 지시문, 한 번 실행, 검색기, 실행 기록, 불완전한 실행, 유효성 검사, 가져오기/내보내기, 복사/붙여넣기, 자동 정렬, 키보드 기반 편집.

**스프레드시트에서 다시 열림(열 G = `Reopen`, `Yes`):** `scenario-editor.md`, `add-a-module-basic.md`, `router-module.md`(라우터를 접습니다 추가), `add-a-filter-to-a-scenario.md`(DevTool 종속성을 복사/붙여넣기 필터로 바꾸기), `configure-scenario-settings.md`(임시 디버그 로그 추가), `view-a-specific-scenario-execution.md`, `view-scenario-execution-history.md`.

**왼쪽 `Yes`에 확인 메모가 추가됨:** `retrigger-specific-execution.md`(원시 JSON/이전 입력/웹후크 옵션), `copy-modules-or-scenarios.md`(기본 제공 복사 매핑/모듈 이름에 대한 선택적 링크).

**26/10/26에 새로 만든 문서(스프레드시트 행 48-50, 전체 `Yes`, `scenario-editor.md`에서 연결됨, `TOC.md` 및 폴더 TOC에 추가됨):** `create-scenarios/add-modules/use-snippets.md`(시나리오 섹션을 코드 조각으로 저장 및 재사용), `manage-scenarios/live-trail.md`(라이브 추적을 사용하여 시나리오 실행을 검토) 및 `manage-scenarios/find-and-replace.md`(시나리오에서 변수, 소스 및 연결을 찾아서 바꾸기). 새 문서에는 `exl-id`/`TQID`개의 초기 문제가 생략됩니다(파이프라인에 필요한 경우 추가). `debug-a-scenario.md`개의 링크를 통해 Live Trail과 Find and Replace를 찾을 수 있습니다.

**상태 업데이트 10/26/26:** `router-module.md`, `configure-scenario-settings.md`, `view-a-specific-scenario-execution.md` 및 `run-once.md`은(는) `Yes`입니다. `CHECK ME`(미해결 BECKY CHECK ME 주석): `scenario-editor.md`(2행과 53행), `debug-a-scenario.md`(22행, 전체 새/클래식 재구조화도 필요) 및 `view-scenario-execution-history.md`(33행). `add-a-module-basic.md` 및 `add-a-filter-to-a-scenario.md`이(가) 여전히 `Reopen`입니다. 필터 문서를 편집할 필요가 없습니다. 새로운 경험 복사 필터 단계가 이미 있으므로 다시 `Yes`(으)로 설정할 수 있습니다.

**이전 메모, 대체:** 이전에 제안된 새 문서 후보는 라이브 트레일, 코드 조각, 찾기 및 바꾸기였습니다. 이제 존재합니다(위). **기타 추가:** `run-once.md`(요청/응답을 한 번 실행), `manage-connections.md`(추측), 시나리오 편집기 FAQ 콘텐츠, 비디오 감사 범위, 릴리스 정보(릴리스 2026-10-28). `debug-a-scenario.md`은(는) 더 이상 DevTool 질문에 차단되지 않지만, 기본 제공 도구 및 Live Trail에 대한 포인터를 재구성해야 합니다.

## 문서별 상태(스프레드시트는 진실의 소스이며, 명시되지 않은 경우 2026-09-22년 기준 아래 상태 — 재개된 행은 위의 2026-10-23 섹션 참조)

완전히 완료되었습니다(0개 플래그, 스프레드시트 열 G가 `Yes`(으)로 표시됨; `scenario-editor.md`, `add-a-module-basic.md`, `router-module.md`, `add-a-filter-to-a-scenario.md`, `configure-scenario-settings.md`, `view-a-specific-scenario-execution.md` 및 `view-scenario-execution-history.md`이(가) 나중에 `Reopen`(으)로 변경됨). `scenario-editor.md`, `create-basic-scenario.md`, `add-trigger-to-basic-scenario.md`, `add-filter-basic-scenario.md`, `add-a-webhook-to-basic-scenario.md`, `use-function-to-build-practice-scenario.md`, `add-a-module-basic.md`, `add-a-filter-to-a-scenario.md`, `router-module.md`(행 10), `error-handling.md`(행 15, &quot;모듈에 오류 처리기 추가&quot; 및 &quot;..라우터&quot; 모두에 대해 new/classic 병렬 H3/H4 트리로 재구성됨), `configure-scenario-settings.md`(행 20 — 추적 스프레드시트에 `Yes` 표시, 아직 업데이트되지 않음), `mapping-overview.md`(행 35 — 표시 `Yes`, 표준 전환 참고 추가, 새 경험 이미지 `new-map-single.png`, `new-map-multiple-with-text.png`, `new-map-formula-with-text.png`, `new-mapping-panel-blank.png`, `new-collection.png`, `new-collection-dropdown.png` 및 `new-array.png`), `move-modules-to-a-chain.md`(행 28 — 이제 스프레드시트 `Yes`로 표시됨), 표준 전환 참고 추가, Beta 기능 다중 선택 상호 작용과 체인으로 이동 컨텍스트 메뉴 경로가 새 경험에서 동일한지 확인되었으므로 분할이 필요하지 않았습니다. &quot;시나리오 설정 열기&quot;를 새/클래식 H2/H3 분할로 재구성했습니다. 새 경험에서는 클래식 톱니바퀴 아이콘이 아닌 기존 `scenario-settings-icon-new.png`(컨트롤 영역, 3점 아이콘 뒤에 있을 수 있음)을 사용합니다. &quot;최대 주기 수&quot; 예제 섀디박스는 이제 새로운 경험 스크린샷 `new-scenario-settings-ex-1.png`(2모듈 예제 시나리오, Watch Record → 기타 작업/변환 개체) 및 `new-max-number-cycles.png`(제어의 톱니바퀴 아이콘을 통해 열린 시나리오 설정 패널, &quot;최대 주기 수&quot; 필드가 강조 표시됨)을 사용합니다. 세 번째 스크린샷(`scenario-detail-350x207.png`)이 완전히 삭제되었습니다. 텍스트가 대체되었습니다. &quot;시나리오 세부 정보 페이지의 내역 영역에서 이미 실행된 주기를 확인할 수 있습니다.&quot;

`scenario-overview.md`(행 34 — 추적 스프레드시트에서 `Yes`을(를) 표시했지만 아직 업데이트되지 않음): 완료됨, 플래그 0. 완전히 개념적인 문서(단계별 &quot;X&quot; 지침 없음), 따라서 새로운/클래식 H2/H3 분할이 필요하지 않으며, 표준 전환 참고 사항이 추가되었습니다. 8개의 원본 플래그 모두 해결됨:
- 4(전체 시나리오, 트리거, 모듈, 경로) Becky의 표시 없는 소스 `new-scenario-example-unmarked.png`에서 PowerShell/System.Drawing으로 그린 빨간색 강조 상자를 통해 표시 안 된 소스(픽셀 스캔이 아닌 소스를 자르기+확대/축소하여 찾은 좌표). PowerShell 5.1의 플러드 채우기/픽셀 루프 접근 방식이 배열 대 스칼라 쿼리에 계속 실패하여 속도가 너무 느림): `new-entire-scenario-scenario.png`, `new-scenario-trigger.png`, `new-scenario-module.png`, `new-scenario-route.png`.
- Becky가 이미 표시한 스크린샷을 통한 2(커넥터, 시나리오 세그먼트): `new-scenario-connectors.png`, `new-scenario-segment.png`.
- `fusion-integration-example.png`(클래식)을(를) 확인하여 해결한 1(통합 예)이 `new-scenario-example-unmarked.png`과(와) 정확히 동일한 시나리오입니다. 직접 재사용되고 새 마크업이 없습니다.
- 1(템플릿 예)은 Becky의 표시 해제된 `new-fusion-automation-example.png`(classic의 `fusion-template-example.png`과(와) 일치하는 것으로 확인되었으며, Becky가 원할 경우 `license-automation-vs-integration.md`의 &quot;작업 자동화를 위한 Workfront Fusion의 예&quot; 섹션에서도 재사용할 수 있습니다.

`view-scenario-data-flow.md`(행 23 — 추적 스프레드시트에 `Yes`을(를) 표시하지만 아직 업데이트되지 않음): 완전히 완료, 플래그 0. 표준 전환 참고가 추가되었습니다. &quot;실행 중인 시나리오에서 데이터 흐름 보기&quot;가 두 경험에서 동일하게 확인되었습니다(Becky의 호출 — 다른 대부분의 절차와 달리 여기서는 새/클래식 분할이 필요하지 않음). 새 경험 문구를 사용하여 단일 절차로 축소했습니다(시나리오 편집기로 들어가려면 시나리오의 아무 곳이나 클릭&quot; 단계 포함). 실행 기록 패널이 변경되지 않은 상태로 기존 클래식 스크린샷 `assets/currently-running.png`을(를) 유지합니다. 두 가지 예시적인 실행/출력 표시기는 경험마다 시각적으로 다르므로 일반적인 단일 스크린샷 교체 패턴과는 달리 이전 스크린샷과 새 스크린샷이 나란히 표시되며, 각 스크린샷에는 일반 텍스트 레이블이 위에 있습니다(새 경험/클래식 경험, 첫 번째). 실행 표시기는 `assets/new-spinning-icon.png`(모듈 아이콘에서 회전하는 링)과 classic `assets/ring-around-module.png`(모듈 주위에서 회전하는 링)이고, 출력 표시기는 `assets/new-output-indicator.png`과 classic `assets/data-flow-output.png`(동일한 녹색 원형 카운트 버블 개념으로 다시 스타일링)입니다. 이 &quot;둘 다 표시, 레이블이 지정된, 새 우선, 이미지 위에 레이블&quot; 패턴은 주택 규칙입니다. 위를 참조하십시오. 설명 단락 텍스트 자체에도 새로운 경험 동작이 먼저 언급된 다음 고전적인 경우가 있습니다(예: &quot;...는 새 경험에서 모듈 아이콘에 회전하는 고리나 고전적인 경험에서 모듈 주위에 늘어나는 고리로 표시됨). — 새로운 순서 지정은 이미지/레이블 지정뿐만 아니라 prose에 적용됩니다.

`fusion-glossary.md`(행 43 — 추적 스프레드시트에 `Yes`을(를) 표시하지만 아직 업데이트되지 않음): 완전히 완료, 플래그 0. 순수 용어집 테이블, 절차 없음. 표 앞에 표준 전환 참고 사항이 추가되었습니다. 포함된 이미지(원시 HTML `<img>` 태그, Markdown 아님) 모두 새 사용자 제공 스크린샷이 필요 없이 해결되었습니다. &quot;Scenario&quot; 항목의 `entire-scenario-blank.png`은(는) `new-scenario-example-unmarked.png`과(와) 정확히 동일한 시나리오였으며(직접 재사용됨), &quot;Module&quot; 항목의 `module.png`은(는) 동일한 원본에서 만든 단일 카드 자르기인 `new-module.png`(으)로 대체되었습니다.

차단됨(`debug-a-scenario.md`과(와) 동일한 처리 — 플래그 지정됨, 플래그 너머 편집되지 않음, 열 G가 비어 있음): `advanced-error-handling.md`(행 16). 인트로에 표준 전환 참고 사항이 추가되었지만 두 가지 예제(&quot;예제: 필터를 사용한 오류 처리&quot; 및 중첩 예제)는 new/classic으로 분할할 단계별 &quot;X 클릭&quot; 콘텐츠가 없는 단일 연속 예제 Dropbox 시나리오입니다. 스크린샷은 Becky의 지침에 따라 단편적으로 터치하지 않도록 의도적으로 classic으로 남겼습니다. 문서에 기존 시나리오의 스크린샷뿐만 아니라 **새 경험에 구축된 새로운 예제 시나리오**(Dropbox 대신 Becky가 제안하는 Workfront 모듈)가 필요하다는 인라인(&quot;#### 예제: 오류 처리&quot; 바로 앞 및 중첩 `>[!BEGINSHADEBOX]` 바로 전)이 플래그가 지정되었습니다. 스프레드시트 열 D와 F가 동일한 범위 노트로 업데이트되었습니다(열 G는 비어 있음).

`scenario-execution-flow.md`(행 40 — 스프레드시트가 이제 `Yes`(으)로 표시됨): 완전히 완료, 플래그 0개. 표준 전환 참고가 추가되었습니다. 개념 문서이므로 새로운/클래식 분할이 필요하지 않습니다. 클래식 스크린샷 3개를 새 경험 자산으로 대체했습니다. `new-example-execution-flow-wf-only.png`, `new-example-execution-flow-wf-dropbox.png`, `new-Info-processed-bundles.png`.

`flow-control.md`(행 42 — 스프레드시트가 `In progress`(으)로 표시됨): 표준 전환 메모를 추가했습니다. 반복 예제에서 인라인으로 3개의 스크린샷 후속 작업에 플래그를 지정했습니다. 흐름 제어 열기를 위한 하단 화면 `flow-control-icon.gif` 경로와 2개의 반복 스크린샷 `repeater-2-350x207.png` 및 `repeater-3-350x207.png`을(를) 모두 표시합니다.

위에서 다루지 않은 행의 스프레드시트 상태: 9, 12-15, 17-19, 21, 27, 29-31, 36-38, 42행의 `Yes`(`flow-control.md`은(는) 위의 이전 메모에서 진행 중으로 표시되어 있지만 스프레드시트에서 `Yes`입니다). `Blocked`: `run-scenario-scoring.md`. `On Hold`: `view-and-resolve-incomplete-executions.md`. 비어 있거나 시작되지 않음: `advanced-error-handling.md`(새 예제 시나리오 필요), `debug-a-scenario.md`(재구성 필요), `scenario-details.md`, `scenario-execution-cycles-phases.md`, `view-chained-scenario-relationships.md`, `fusion-basics-videos.md`, 릴리스 노트 행 및 `create-a-scenario-workflow.md`(DevTool 바로 가기 행 유지).

(위의 &quot;아직 스프레드시트에서 업데이트되지 않음&quot; 발언은 부실 — 해당 문서에 대해 스프레드시트가 업데이트되었습니다.)


## 최종 상태 동기화(2026-10-27) - 위의 상태 문을 대체합니다.

스프레드시트(&quot;영향 받는 문서&quot;, G열)는 진실의 소스입니다. 릴리스: 새로운 시나리오 편집기 경험, 2026-10-28.

**`Yes`(완료):** 이전에 `Reopen`개의 문서(`scenario-editor.md`, `add-a-module-basic.md`, `router-module.md`, `add-a-filter-to-a-scenario.md`, `configure-scenario-settings.md`, `view-a-specific-scenario-execution.md`, `view-scenario-execution-history.md`), 10/27(`scenario-details.md`, `manage-connections.md`, `scenario-execution-cycles-phases.md`, `view-chained-scenario-relationships.md`, `run-once.md`)에 편집된 10개 이상의 문서, 3개의 새 문서 및 릴리스 노트를 포함하여 아래에 나열되지 않은 모든 행.

**`OK for now - revisit`:** `advanced-error-handling.md`(예: 시나리오가 여전히 클래식, 인라인 메모가 있음, 나중에 새 경험에서 다시 빌드) 및 `fusion-basics-videos.md`(45행 및 54행, 비디오 감사 댓글이 문서에 있음, Live Trail/DevTool 연습 비디오를 추가할 수 있음).

**`Check after release`:** `debug-a-scenario.md`(새 경험에 &quot;사용할 수 있는 이벤트가 없음&quot;으로 표시되기 때문에 보류 중인 라이브 스트림 섹션, 버그일 수 있음, 7개의 기본 제공 도구가 DevTool에서 제거되었는지 확인, Scenario Debugger의 새/클래식 분할이 필요할 수 있음), `run-scenario-scoring.md` 및 `view-and-resolve-incomplete-executions.md`.

**새로 만들기/변경된 10/27(모두 Becky에 의해 해결됨):**
- `debug-a-scenario.md`: DevTool 왼쪽 탐색에 이제 네 번째 항목인 **DevTool 도움말**(물음표 아이콘)이 있고 도구 패널에는 **이름별 검색 도구** 필드와 도구 선택 프롬프트가 있습니다. 10개의 모든 도구가 DevTool에 남아 있습니다. DevTool은 3점 메뉴에서 열리거나 캔버스의 빈 영역을 마우스 오른쪽 단추로 클릭하여 열립니다. Scenario Debugger 단계가 확장되었습니다(ID 배지가 있는 모듈 목록, 이름 또는 ID별 검색, 주기/작업, 요청 헤더/요청 본문/응답 헤더/응답 본문 탭, **RAW 복사** 및 **cURL 복사**).
- `add-a-module-basic.md`: 검색 우선 선택기, **뒤로**&#x200B;가 있는 오른쪽 패널, 배지(비공개, 프리미엄, 베타), 커넥터 정의 모듈 그룹, 오류 처리기 추가 시 먼저 지시문. 여전히 확인되지 않음: 선택기 정보 아이콘, 버전 V자형 화살표, 빠른 액세스 버블.
- `scenario-editor.md`: **피드백** 단추(오른쪽 상단, 간단히 보기 옆)가 편집 작업에 추가됨. 시나리오 설정 행은 임시 디버그 로그에 링크됨. 스위치는 사용자별로 다르며 일부 조직에서는 사용할 수 없습니다.
- 이제 `scenario-details.md` 및 `view-chained-scenario-relationships.md`에서 `/help/workfront-fusion/manage-scenarios/assets/new-exit-editing-arrow.png`을(를) 사용합니다.
- `manage-connections.md`개의 링크를 찾아 바꾸기.
- 릴리스 정보: `fusion-release-activity.md` 및 `TOC.md`에 추가된 `fusion-product-releases/fusion-releases-2026/fusion-2026-10-26.md`(10월 26일 주).

**릴리스 후 후속 작업 열기:** 새 섹션 및 문서에 대한 스크린샷, 라우터를 접거나 펼치는 방법, 편집기에서 실행 기록 패널을 여는 방법, 선택기 정보 아이콘/V자형/버블, 선택기 대 편집기 즐겨찾기, `scenario-execution-cycles-phases.md`에서 클래식 스크린샷 재촬영(ACID 배지), `scenario-details.md`, `advanced-error-handling.md`에서 DataError 필터.

**저장소 노트:**&#x200B;은(는) 요청이 없는 한 커밋되지 않습니다. ~466개의 파일이 CRLF(줄 끝)로 인해 수정된 것으로 표시됩니다. 샌드박스에서 `git status`을(를) 실행하지 마십시오(`.git/index.lock`에서 나갈 수 있음).
