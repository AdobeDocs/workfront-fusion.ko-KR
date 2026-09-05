---
name: fusion-doc-request
description: null
source-git-commit: 6726c582294758de0bbab19d6014ad80bb66e553
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---


# Fusion 설명서 요청

`#fusion-documentation` Slack 채널에 게시되는 반복되는 &quot;{person}의 새 설명서 요청&quot; 패턴을 처리합니다. 요청을 읽고 문서를 업데이트한 다음 이 종류의 모든 이전 요청에 사용된 동일한 Workfront 사용자 정의 양식에 대해 추적 작업을 만듭니다.

`fusion-release-notes` 스킬과는 다른 워크플로우입니다. 이 스킬은 참조 문서를 업데이트하고 Workfront 작업을 만듭니다. 요청에 &quot;공지 필요: 예&quot;라고 표시되더라도 이 리포지토리에서 주간 Fusion 릴리스 노트 페이지를 만들거나 업데이트하지 않습니다. 사용자가 주별 릴리스 정보를 별도로 요청하는 경우에만 `fusion-release-notes`을(를) 사용합니다.

## 1단계: 요청 세부 정보 가져오기

Slack 링크가 지정된 경우 URL에서 `channel_id` 및 `message_ts`을(를) 구문 분석하고 스레드(`slack_get_thread_replies` 또는 `slack_read_thread`, 연결된 Slack MCP 도구에 따라 다름)를 가져옵니다. 하나가 실패하면 둘 다 시도하십시오. 스레드의 영구 링크/URL을 유지합니다. 이 URL은 3단계에서 필요합니다.

이 환경의 Slack 연결은 불안합니다(만료된 토큰, 중간 세션 연결 끊기). 가져오기에 실패한 경우:
- 한 번 다시 시도하십시오.
- 그래도 실패하는 경우 사용자에게 가져오기 실패했음을 명확히 알리고 요청 콘텐츠를 직접 붙여넣도록 요청합니다. 내용을 추측하지 말고, 그렇다고 말하지 않고 묵묵히 포기하지 않는다.

요청 템플릿에는 다음 필드가 있습니다. 각 필드를 추출하십시오.

&#x200B;* **기능 제목**
&#x200B;* **설명**
&#x200B;* **설명서에 추가될 점** *(경우에 따라 제공 - 요청자가 원하는 특정 섹션/세부 정보. 제공된 경우 선택 사항이 아닌 필수 사항으로 취급)*
&#x200B;* **릴리스 예상 날짜**
&#x200B;* **발표가 필요함** *(예/아니요 - 정보 제공용입니다. 위의 메모를 참조하세요. 이 필드에 대해 작업하지 마십시오.)*

요청이 전체 사양이 있는 Confluence Wiki 페이지로 링크되는 경우 설명서를 작성하기 전에 해당 페이지(`get_wiki_content`)를 가져오십시오. 기술 세부 사항(정확한 필드 이름, 단계, UI 레이블)에 Slack 요약만 의존하지 말고, 하나가 연결되어 있을 때 위키 사양에서 가져옵니다.

대신 요청이 신뢰할 수 있는 사양이 아닌 비 Confluence 보조 소스(예: Experience League 커뮤니티 게시물, 지원 문서, AI 생성 요약)로 연결되는 경우 이를 사용하여 Slack 텍스트에 없는 기술적인 세부 사항을 채울 수 있지만 Slack 요청 자체보다 낮은 신뢰도로 처리할 수 있습니다. 이 텍스트가 Slack 텍스트(동일한 단추/필드의 다른 이름, Slack에서 전혀 언급되지 않은 세부 정보)와 충돌하거나 추가할 경우 자동으로 선택하지 마십시오. Slack 요청의 구문을 기본 소스로 사용하여 문서를 작성하고, 2단계의 지침에 따라 HTML 주석(예: `<!-- BECKY CHECK ME: Slack calls this "Activate," but the linked community post calls it "Reactivate" - confirm against the live UI. -->`)으로 인라인으로 불일치를 플래그를 지정합니다.

## 2단계: 설명서 업데이트

이 보고서에서 관련 기존 문서를 찾습니다(관련 모듈 이름, UI 레이블 또는 설정 이름의 경우 grep - 파일을 추측하지 마십시오). 해당 문서의 기존 구조, 제목 수준 및 집 스타일에 따라 변경 사항을 반영하도록 업데이트합니다.

&#x200B;* Slack 요청 또는 연결된 wiki 사양에 없는 기술 세부 사항(정확한 필드 이름, 권한 범위, 구성 단계)을 발명하지 마십시오. 확인되지 않은 내용이 있으면 추측이 아닌 HTML 주석(예: `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`)으로 인라인으로 플래그를 지정합니다. 표시되는 설명선은 아닙니다. 게시된 페이지에서 렌더링하면 안 됩니다.
&#x200B;* 새 문서 파일(기존 문서 파일로의 편집뿐만 아니라)이 필요한 경우 이 리포지토리의 일반 규칙을 따릅니다. 즉, 프론트마트에서 조작된 `exl-id`/`TQID`이(가) 없습니다. 파일을 만든 후 CRLF/no-BOM으로 변환합니다(`Write` 도구 기본값은 LF임).
&#x200B;* 새 페이지를 &quot;목차&quot;에 배선한다는 것은 이 두 가지 모두를 의미하며, 한 페이지만이 아닙니다. 페이지가 여전히 독자에게 보이지 않으면서 하위 인덱스에서 연결될 수 있습니다.
  - 제품 영역의 마스터 탐색 파일(예: `help/workfront-fusion/TOC.md`) - 이는 실제로 게시된 탐색 트리를 구동하는 것입니다.
  - 이러한 종류의 문서에 연결되는 모든 콘텐츠 내 하위 인덱스/랜딩 페이지(예: 새 커넥터 모듈 페이지의 경우 `apps-and-modules-toc.md`).
    두 항목을 모두 명시적으로 확인하고 새 항목이 각 파일에서 가장 가까운 형제 문서와 동일한 중첩 수준에서 동일한 목록에 있는지 확인합니다. 다른 항목 위에 항목을 추가한다고 가정하지 마십시오.

## 3단계: Workfront 작업 만들기

프로젝트: **제품 설명서 작업 - 메시지가 필요한 개발 문제에 대한**. 변경되는 경우 하드 코딩하지 않고 `insights_find_id_by_name`(엔터티 `project`)로 ID를 확인합니다. 마지막으로 해결된 ID에 대해서는 아래의 알려진 값 을 참조하십시오.

작업 필드:

| 필드 | 값 |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | 위의 프로젝트 조회에서 |
| `parentID` | 상위 작업 ID(`parentID`, 시스템 필드 - `DE:` 접두사 없음) - 아래 알려진 값을 참조하십시오. 이렇게 하면 새 작업이 프로젝트의 최상위 작업이 아닌 하위 작업이 됩니다. |
| `assignedToID` | `insights_get_current_user`의 현재 사용자 |
| `categoryID` | 제품 설명서 사용자 정의 양식 ID - 아래의 알려진 값 을 참조하십시오. 명확하지 않은 경우 이 프로젝트의 최근 형제 작업에 대해 `task.task_categoryID`을(를) 쿼리하여 확인하십시오. |
| `description` | **전체 Slack 메시지 텍스트**(요청 템플릿의 모든 필드, 패러프어 아님) 뒤에 Slack 대화에 대한 링크가 있습니다. |
| `DE:Release notes` | 형식이 지정된 릴리스 노트는 아래 형식을 참조하십시오. |
| `DE:Preview Date Known` | 기본적으로 `Yes` |
| `DE:Preview Date` | 기본적으로 요청의 **예상 릴리스 일자** |
| 제품/영역 | `Fusion`(제품 설명서 양식의 열거형 필드)을(를) 선택합니다. 불분명한 경우 `insights_search_fields`을(를) 사용하여 정확한 필드 이름을 확인하십시오. |

미리 보기 날짜 필드를 이 동일한 만들기 호출의 일부로 설정합니다. 나중에 보관하거나 요청을 기다리지 마십시오. 사용자가 나중에 다른 날짜를 제공하거나 날짜가 실제로 아직 알려져 있지 않다고 말하는 경우 그에 따라 업데이트하지만 매번 채우도록 기본값이 설정됩니다.

`DE:Release notes` 필드에 대한 릴리스 노트 형식입니다. `***FUSION***`을(를) 첫 줄로 시작하여 빈 줄로 만든 다음 제목을 입력하면 Fusion에 속하는 것으로 메모가 표시됩니다(핵심 Workfront과 반대).

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

만들기 호출 전에 `workfront://tools/create-any-object`(으)로 `read_workflow_docs`을(를) 호출하십시오. 이 호출은 사용자 지정 필드와 열거형 값(`DE:Preview Date Known`)을 설정하며, MCP 서버 규칙에 따라 필요합니다.

## 4단계: 사용자에게 다시 확인

명확하게 보고:

&#x200B;* 변경한 문서 파일과 추가한 내용
&#x200B;* 작업 이름 및 URL.
&#x200B;* 미리 보기 날짜 필드를 포함하여 사용자가 설정한 정확한 필드 값.
&#x200B;* 충분히 신뢰하지 않는 모든 항목. 예를 들어, Slack에 연결할 수 없었고 붙여넣은 텍스트로만 작업했거나, 대상 문서 문서가 애매했거나, 기술 세부 정보가 소스 자료에 없고, 예상하지 못한 대신 플래그가 지정되었습니다.

## 알려진 값(이전 실행에서)

이러한 문제가 영구적이라고 가정하지 않고 여전히 해결되는지 확인합니다.

&#x200B;* 프로젝트 &quot;제품 설명서 작업 - 메시지가 필요한 개발 문제에 대한 작업&quot;이 ID `5e69583f00236b9f767c3e3944100ee4`에 매핑됩니다.
&#x200B;* 상위 작업 &quot;Becky - Fusion-Documentation 채널의 작업&quot;이(가) 동일한 프로젝트의 ID `6a9b065100003a7554832780c2015e93`에 매핑됩니다. 변경되는 경우 하드코딩하지 않고 `insights_find_id_by_name`(엔티티 `task`)로 해결됩니다.
&#x200B;* 제품 설명서 사용자 정의 양식(`categoryID`)은 `5d7275b9000514604bd969d418725843`입니다.
&#x200B;* 사용된 사용자 정의 필드: `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
