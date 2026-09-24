---
applyTo: "help/workfront-fusion/**"
source-git-commit: e3e28f86494207dd5e674a2882887d00da6a0c61
workflow-type: tm+mt
source-wordcount: '2352'
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
`new-add-error-handler-in-menu.png`(이 모듈을 마우스 오른쪽 단추로 클릭→설정 컨텍스트 메뉴: 이 모듈만 실행/오류 처리기 추가/이름 바꾸기/복제/복사 모듈/메모 추가/복사 매핑/복사 모듈 이름/앱 메타데이터/삭제 모듈 추가 — &quot;오류 처리기 추가&quot;가 강조 표시됨 — 오류 처리.md에서 사용됨), `new-error-handling-directives.png`(앱/서비스 선택기가 오류 처리기에서 열리며 왼쪽 패널의 일반 앱 범주와 함께 전용 &quot;오류 처리&quot; 범주가 선택됨 — 중단, 커밋, 무시, 다시 시작, 롤백 — 모듈 및 라우터가 추가된 오류 처리기 흐름에 모두 사용됨 — 오류 처리.md에서 재사용), `new-error-handler-examples-with-numbers.png`(오류 처리 처리기 계층 구조에 대한 번호가 매겨진 예제, **5}의 캔버스-토글 보기에서 캡처됨, 오류 처리.md 이미지에 사용됨; 캡션 (가독성을 위한 작은 보기).**`scenario-editor.md`

**`help/workfront-fusion/get-started-with-fusion/understand-fusion/assets/`**:
`new-scenario-example-unmarked.png`(소스 스크린샷 Becky 제공됨, 표시되지 않음 — 8-module Excel/Workfront 사용자 동기화 시나리오: 추가된 사용자 → 라우터 → Workfront에서 사용자 찾기 → Workfront에서 사용자 찾기 → 3 분기 [기존 사용자 ID 설정/에서 새 사용자 만들기 → 새 사용자 ID 설정/사용자 ID 변수 가져오기 → 스프레드시트에 사용자 ID 업로드] — classic의 `fusion-integration-example.png` 및 `fusion-glossary.md`의 &quot;시나리오&quot; 항목(`entire-scenario-blank.png`)과 동일한 시나리오; 이 예제의 추가 마크업에 대한 소스로 유지), `new-entire-scenario-scenario.png`, `new-scenario-trigger.png`, `new-scenario-module.png`, `new-scenario-route.png`(모두 빨간색 강조 상자를 통해 위의 표시되지 않은 소스에서 파생됨), `new-scenario-connectors.png`(정확한 상자 배치에 대해서는 문서별 메모 참조), (Becky-제공, 앱 주변의 빨간색 상자 새 경험 커넥터 선택기에서, `new-scenario-segment.png`(Becky 제공, 2-module Workfront 감시 이벤트 → 개체 세그먼트 변환, 박스형, unboxed Microsoft 365 이메일 모듈 뒤), `new-fusion-automation-example.png`(Becky 제공, 표시가 해제된 4-module Workfront 전용 예 — 보기 레코드 → 프로젝트 정보 가져오기 → &quot;할당 대상&quot; → 업데이트 만들기 — Classic의 `fusion-template-example.png`과 동일한 시나리오. Becky가 원할 경우 `license-automation-vs-integration.md`의 &quot;작업 자동화를 위한 Workfront Fusion 예제&quot; 섹션에서 재사용 가능), `new-module.png`(PowerShell/System.Drawing을 통해 자른 `new-scenario-example-unmarked.png`에서 &quot;Workfront에서 사용자 찾기&quot; 모듈의 단일 카드 자르기, 일반적으로 `fusion-glossary.md`의 &quot;모듈 항목&quot;에 사용, 빨간색 상자 없음).

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
- `debug-a-scenario.md`을(를) 아직 확인하지 않고 차단합니다. + 몇 가지 다른 문서: **DevTool**&#x200B;이(가) 새 경험에서 전혀 제거되는지 여부(소문으로 들림, 아직 다른 세부 사항은 없음) - 기능 비교 시트, &quot;DevTool&quot; 행 참조.

## 이 재설계를 위해 설정된 주택 규칙(나머지 모든 문서에 적용)

- 전체 병렬 복제: 앵커 충돌을 피하는 데 필요한 모든 위치에 `(Classic)`개의 접미사가 있는 &quot;...새 경험(권장)&quot;에 대한 H2/H3 트리 하나와 &quot;....클래식 경험&quot;에 대한 별도의 접미사 하나. 이제 2개 이상의 하위 항목이 있는 제목 아래에 미니 목차를 추가합니다.
- &quot;새 제품 및 클래식 제품&quot; 설명을 **문서 소개** 끝(자체 H2가 아님)에 있는 단일 `>[!NOTE]`(으)로 축소하고 이 정확한 단어를 다시 사용합니다. &quot;문서 시나리오 편집기에서&quot;가 링크에 추가됩니다.
  > Workfront Fusion에서 시나리오 편집기를 새 경험으로 전환합니다. 이 전환 중에 클래식 경험과 새 경험을 모두 사용할 수 있으며 언제든지 전환할 수 있습니다. 새 경험을 사용하는 것이 좋습니다. 자세한 내용은 문서 시나리오 편집기에서 [새 경험 및 클래식 경험](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)을 참조하십시오.
- 새 경험 머리글에는 `(Recommended)`(예: `## Add a filter in the new experience (Recommended)`)이(가) 포함됩니다.
- UI와 관계없는 콘텐츠(예: `add-a-module-basic.md`의 `?moduleId=` URL 매개 변수 메모)는 복제하지 않아도 됩니다. 판단을 사용하되, 확실하지 않은 경우 먼저 Becky에게 문의하십시오(메시지가 묻지 않고 이동되기 전에 푸시되었습니다).
- Becky가 전체 프로시저가 경험 간에 동일하다고 확인한 경우(UI에 관계없는 메모뿐만 아니라) 새/클래식 H2/H3으로 아예 분할하지 마십시오. 새 경험 문구를 사용하여 단일 프로시저로 축소하십시오(예: `view-scenario-data-flow.md`의 &quot;실행 중인 시나리오에서 데이터 흐름 보기&quot;). 기본 가정은 여전히 절차가 다르고 분할이 필요하다는 것입니다. 명시적인 확인 후에만 축소됩니다.
- 새로운 시각과 고전적인 시각이 완전히 다른 하나의 실례가 되는 스크린샷(완전한 단계별 절차가 아님)의 경우, 하나를 선택하거나 플래그를 놓고 기다리지 말고 — 둘 다 먼저 표시, 새로운 사항: 각 이미지 바로 위에 일반 텍스트 레이블 라인(&quot;새 경험&quot; / &quot;클래식 경험&quot;), 새로운 경험 먼저. 이미지 레이블뿐만 아니라 주변 산문에서도 새 경험 비헤이비어를 먼저 언급하십시오(예: &quot;...새 경험에서 X로 표시 또는 클래식 경험에서 Y로 표시&quot;). `view-scenario-data-flow.md`의 실행/출력 표시기를 참조하십시오.
- 확인되지 않은 모든 인라인을 즉시 `<!-- BECKY CHECK ME: ... -->`(으)로 플래그를 지정합니다. 표시되는 콜아웃이 없습니다.
- 기사의 모든 플래그가 해결되면 추적 스프레드시트의 &quot;영향을 받는 문서&quot; 시트(G열)에 해당 행 `Yes`을(를) 표시합니다. 일부 플래그만 해결되면 `In progress`을(를) 사용합니다.

## 기사별 상태 (2026-09-22 기준)

완전히 완료(0개 플래그, 스프레드시트 열 G가 `Yes`(으)로 표시됨): `scenario-editor.md`, `create-basic-scenario.md`, `add-trigger-to-basic-scenario.md`, `add-filter-basic-scenario.md`, `add-a-webhook-to-basic-scenario.md`, `use-function-to-build-practice-scenario.md`, `add-a-module-basic.md`, `add-a-filter-to-a-scenario.md`, `router-module.md`(행 10), `error-handling.md`(행 15, &quot;모듈에 오류 처리기 추가&quot; 및 &quot;...라우터에 추가&quot; 모두에 대해 new/classic 병렬 H3/H4 트리로 재구조화됨), `configure-scenario-settings.md`(행 20 — 추적 스프레드시트에 `Yes` 표시하지만 아직 업데이트되지 않음). &quot;시나리오 설정 열기&quot;를 새/클래식 H2/H3 분할로 재구성했습니다. 새 경험에서는 클래식 톱니바퀴 아이콘이 아닌 기존 `scenario-settings-icon-new.png`(컨트롤 영역, 3점 아이콘 뒤에 있을 수 있음)을 사용합니다. &quot;최대 주기 수&quot; 예제 섀디박스는 이제 새로운 경험 스크린샷 `new-scenario-settings-ex-1.png`(2모듈 예제 시나리오, Watch Record → 기타 작업/변환 개체) 및 `new-max-number-cycles.png`(제어의 톱니바퀴 아이콘을 통해 열린 시나리오 설정 패널, &quot;최대 주기 수&quot; 필드가 강조 표시됨)을 사용합니다. 세 번째 스크린샷(`scenario-detail-350x207.png`)이 완전히 삭제되었습니다. 텍스트가 대체되었습니다. &quot;시나리오 세부 정보 페이지의 내역 영역에서 이미 실행된 주기를 확인할 수 있습니다.&quot;

`scenario-overview.md`(행 34 — 추적 스프레드시트에서 `Yes`을(를) 표시했지만 아직 업데이트되지 않음): 완료됨, 플래그 0. 완전히 개념적인 문서(단계별 &quot;X&quot; 지침 없음), 따라서 새로운/클래식 H2/H3 분할이 필요하지 않으며, 표준 전환 참고 사항이 추가되었습니다. 8개의 원본 플래그 모두 해결됨:
- 4(전체 시나리오, 트리거, 모듈, 경로) Becky의 표시 없는 소스 `new-scenario-example-unmarked.png`에서 PowerShell/System.Drawing으로 그린 빨간색 강조 상자를 통해 표시 안 된 소스(픽셀 스캔이 아닌 소스를 자르기+확대/축소하여 찾은 좌표). PowerShell 5.1의 플러드 채우기/픽셀 루프 접근 방식이 배열 대 스칼라 쿼리에 계속 실패하여 속도가 너무 느림): `new-entire-scenario-scenario.png`, `new-scenario-trigger.png`, `new-scenario-module.png`, `new-scenario-route.png`.
- Becky가 이미 표시한 스크린샷을 통한 2(커넥터, 시나리오 세그먼트): `new-scenario-connectors.png`, `new-scenario-segment.png`.
- `fusion-integration-example.png`(클래식)을(를) 확인하여 해결한 1(통합 예)이 `new-scenario-example-unmarked.png`과(와) 정확히 동일한 시나리오입니다. 직접 재사용되고 새 마크업이 없습니다.
- 1(템플릿 예)은 Becky의 표시 해제된 `new-fusion-automation-example.png`(classic의 `fusion-template-example.png`과(와) 일치하는 것으로 확인되었으며, Becky가 원할 경우 `license-automation-vs-integration.md`의 &quot;작업 자동화를 위한 Workfront Fusion의 예&quot; 섹션에서도 재사용할 수 있습니다.

`view-scenario-data-flow.md`(행 23 — 추적 스프레드시트에 `Yes`을(를) 표시하지만 아직 업데이트되지 않음): 완전히 완료, 플래그 0. 표준 전환 참고가 추가되었습니다. &quot;실행 중인 시나리오에서 데이터 흐름 보기&quot;가 두 경험에서 동일하게 확인되었습니다(Becky의 호출 — 다른 대부분의 절차와 달리 여기서는 새/클래식 분할이 필요하지 않음). 새 경험 문구를 사용하여 단일 절차로 축소했습니다(시나리오 편집기로 들어가려면 시나리오의 아무 곳이나 클릭&quot; 단계 포함). 실행 기록 패널이 변경되지 않은 상태로 기존 클래식 스크린샷 `assets/currently-running.png`을(를) 유지합니다. 두 가지 예시적인 실행/출력 표시기는 경험마다 시각적으로 다르므로 일반적인 단일 스크린샷 교체 패턴과는 달리 이전 스크린샷과 새 스크린샷이 나란히 표시되며, 각 스크린샷에는 일반 텍스트 레이블이 위에 있습니다(새 경험/클래식 경험, 첫 번째). 실행 표시기는 `assets/new-spinning-icon.png`(모듈 아이콘에서 회전하는 링)과 classic `assets/ring-around-module.png`(모듈 주위에서 회전하는 링)이고, 출력 표시기는 `assets/new-output-indicator.png`과 classic `assets/data-flow-output.png`(동일한 녹색 원형 카운트 버블 개념으로 다시 스타일링)입니다. 이 &quot;둘 다 표시, 레이블이 지정된, 새 우선, 이미지 위에 레이블&quot; 패턴은 주택 규칙입니다. 위를 참조하십시오. 설명 단락 텍스트 자체에도 새로운 경험 동작이 먼저 언급된 다음 고전적인 경우가 있습니다(예: &quot;...는 새 경험에서 모듈 아이콘에 회전하는 고리나 고전적인 경험에서 모듈 주위에 늘어나는 고리로 표시됨). — 새로운 순서 지정은 이미지/레이블 지정뿐만 아니라 prose에 적용됩니다.

`fusion-glossary.md`(행 43 — 추적 스프레드시트에 `Yes`을(를) 표시하지만 아직 업데이트되지 않음): 완전히 완료, 플래그 0. 순수 용어집 테이블, 절차 없음. 표 앞에 표준 전환 참고 사항이 추가되었습니다. 포함된 이미지(원시 HTML `<img>` 태그, Markdown 아님) 모두 새 사용자 제공 스크린샷이 필요 없이 해결되었습니다. &quot;Scenario&quot; 항목의 `entire-scenario-blank.png`은(는) `new-scenario-example-unmarked.png`과(와) 정확히 동일한 시나리오였으며(직접 재사용됨), &quot;Module&quot; 항목의 `module.png`은(는) 동일한 원본에서 만든 단일 카드 자르기인 `new-module.png`(으)로 대체되었습니다.

차단됨(`debug-a-scenario.md`과(와) 동일한 처리 — 플래그 지정됨, 플래그 너머 편집되지 않음, 열 G가 비어 있음): `advanced-error-handling.md`(행 16). 인트로에 표준 전환 참고 사항이 추가되었지만 두 가지 예제(&quot;예제: 필터를 사용한 오류 처리&quot; 및 중첩 예제)는 new/classic으로 분할할 단계별 &quot;X 클릭&quot; 콘텐츠가 없는 단일 연속 예제 Dropbox 시나리오입니다. 스크린샷은 Becky의 지침에 따라 단편적으로 터치하지 않도록 의도적으로 classic으로 남겼습니다. 문서에 기존 시나리오의 스크린샷뿐만 아니라 **새 경험에 구축된 새로운 예제 시나리오**(Dropbox 대신 Becky가 제안하는 Workfront 모듈)가 필요하다는 인라인(&quot;#### 예제: 오류 처리&quot; 바로 앞 및 중첩 `>[!BEGINSHADEBOX]` 바로 전)이 플래그가 지정되었습니다. 스프레드시트 열 D와 F가 동일한 범위 노트로 업데이트되었습니다(열 G는 비어 있음).

시작되지 않음: 추적 스프레드시트의 다른 모든 항목(`debug-a-scenario.md`은(는) DevTool 확인에서 차단됨, 나머지는 그대로 있음).
