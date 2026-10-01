---
title: Adobe Workfront Fusion MCP 서버 구성
description: Adobe Workfront Fusion을 MCP 호환 AI 에이전트 플랫폼 또는 Coworker(독립 실행형 또는 Fusion 오른쪽 레일)에 연결합니다.
source-git-commit: 6d447c16d199c69ae670f59bb56cf79464cbe057
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 0%
---

# Adobe Workfront Fusion MCP 서버 구성

Adobe Workfront Fusion MCP 서버를 사용하면 지원되는 AI 에이전트 플랫폼에서 자연어 대화를 통해 Fusion 조직의 시나리오, 실행, 연결, 웹후크, 데이터 저장소 등으로 작업할 수 있습니다.

Adobe Workfront Fusion MCP 서버에서 사용할 수 있는 도구 목록은 [Adobe Workfront Fusion MCP 서버 도구](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md)를 참조하십시오.

## 지원되는 AI 에이전트 플랫폼

Fusion MCP 서버는 OAuth를 통해 MCP(Model Context Protocol) 및 원격(스트리밍 가능 HTTP) MCP 서버를 지원하는 모든 AI 에이전트 플랫폼과 작동합니다.

>[!NOTE]
>
> Adobe은 현재 Cloud Connectors 디렉토리 또는 ChatGPT 앱/플러그인 디렉토리에 Workfront Fusion 커넥터를 게시하지 않습니다. Fusion을 Claude, ChatGPT 또는 Microsoft Copilot과 함께 사용하려면 이 문서에 설명된 대로 URL로 **사용자 지정 MCP 서버**&#x200B;로 추가하십시오.

이 문서에서는 다음 연결 단계를 안내합니다.

* [Adobe Coworker](#use-fusion-with-coworker): Fusion 오른쪽 레일에서 Coworker를 독립 실행형으로 설정하고 Coworker를 동료로 설정
* [클라우드](#connect-fusion-to-claude): 사용자 지정 커넥터
* [ChatGPT](#connect-fusion-to-chatgpt): 사용자 지정 MCP 서버
* [사용자 지정 MCP 솔루션](#connect-fusion-to-a-custom-mcp-solution)

>[!IMPORTANT]
>
>Gemini, Cursor 또는 VS 코드와 같은 다른 MCP 호환 플랫폼을 사용하는 경우 해당 플랫폼의 설명서에 따라 사용자 정의 MCP 서버를 추가합니다. MCP 서버 URL을 입력하라는 메시지가 표시되면 다음을 입력합니다.
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## 전제 조건

Fusion을 AI 에이전트 플랫폼에 연결하기 전에 다음을 수행해야 합니다.

* 활성 Adobe Workfront Fusion 라이선스가 있고 하나 이상의 Fusion 조직에 액세스할 수 있습니다.
* 작업할 데이터에 대한 액세스 권한을 부여하는 Fusion 사용자 역할 및 팀 역할이 있어야 합니다.
* Adobe ID(Adobe Identity Management System, IMS)로 로그인
* MCP 호환 AI 에이전트 플랫폼 또는 Coworker에 액세스할 수 있습니다.

## Coworker와 Fusion 사용

동료는 Adobe의 AI 에이전트입니다. Fusion은 Coworker에 내장되어 있으므로 MCP URL을 입력하거나 OAuth 앱을 등록할 필요가 없습니다. 다음 두 위치에서 Fusion과 함께 Coworker를 사용할 수 있습니다.

* [동료(독립 실행형)](#use-fusion-in-coworker): 다른 Adobe 앱과 함께 Fusion을 사용하여 작업합니다.
* [Fusion 오른쪽 레일의 Coworker](#use-coworker-in-the-fusion-right-rail): Fusion UI의 패널에서 Coworker를 엽니다.

둘 다 동일한 Fusion MCP 도구, Adobe ID 및 Fusion 권한을 사용합니다. 읽기 또는 쓰기 MCP 도구 설정은 두 가지 모두에 적용됩니다. 삭제, 큐 지우기 또는 덮어쓰기와 같은 삭제 작업은 항상 확인을 요청합니다.

### 동료에서 Fusion 사용

1. 동료를 엽니다.
2. **사용자 지정** > **통합** 열기
3. **fusion-mcp**&#x200B;을(를) 찾은 다음 **Test**&#x200B;을(를) 클릭합니다.
4. 둘 이상의 Fusion 조직에 대한 액세스 권한이 있는 경우 해당 조직이 자동으로 선택됩니다. 필요한 경우 나중에 동료에게 조직 전환을 요청할 수 있습니다.

### Fusion 오른쪽 레일에서 Coworker 사용

Fusion에서 동료는 오른쪽 레일에서 열립니다

1. Workfront Fusion에 로그인
2. 오른쪽 레일에서 **Coworker** 아이콘을 클릭합니다.
3. 패널에서 질문합니다.

### 프롬프트 예

* *지난 24시간 동안 실행되지 않은 모든 시나리오를 표시합니다.*
* *이번 주에 만들거나 삭제된 모든 시나리오를 가장 최근 항목별로 정렬하여 나열합니다.*
* *이 시나리오가 수행하는 작업*
* *이 실행이 실패한 이유는 무엇입니까?*

## Fusion을 Claude에 연결

Fusion을 사용자 지정 커넥터로 추가합니다.

>[!NOTE]
>
> Cloud Team/Enterprise에서 사용자 정의 커넥터를 추가하려면 소유자여야 합니다. 자세한 내용은 클라우드 설명서에서 [원격 MCP를 사용하여 사용자 지정 커넥터 시작](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)을 참조하십시오.

1. [클라우드](https://claude.ai)에 로그인합니다.
2. 왼쪽 메뉴에서 **사용자 지정**&#x200B;을 선택합니다.
3. **커넥터**&#x200B;를 선택하십시오.
4. **+**&#x200B;을(를) 선택한 다음 **사용자 지정 커넥터 추가**&#x200B;를 선택합니다.
5. 이름(예: &quot;Workfront Fusion&quot;) 및 MCP 서버 URL 입력:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

6. **연결**&#x200B;을 클릭합니다.
7. 로그인. 프로필 및 Fusion 조직을 선택합니다.

클라우드 코드의 경우 명령줄에서 서버를 추가할 수 있습니다.

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Fusion을 ChatGPT에 연결

Fusion을 사용자 지정 MCP 서버로 추가합니다.

### ChatGPT 데스크탑 또는 코드

1. ChatGPT에서 **설정**&#x200B;을 엽니다.
2. **플러그인**&#x200B;을 클릭합니다.
3. **서버 추가**&#x200B;를 클릭합니다.
4. 서버 이름을 입력합니다.
5. 형식에는 **스트리밍 가능한 HTTP**&#x200B;를 선택하십시오.
6. MCP 서버 URL 입력:

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

7. **저장**&#x200B;을 클릭합니다.
8. 새 서버에 대해 **인증**&#x200B;을 클릭하고 로그인하십시오.
9. 서버 옆에 있는 토글이 켜져 있는지 확인합니다.

### 웹에서 ChatGPT

1. [ChatGPT](https://chatgpt.com)에 로그인합니다.
2. [https://chatgpt.com/plugins](https://chatgpt.com/plugins)&#x200B;(으)로 이동합니다. (개발자 모드는 **설정**&#x200B;에서 활성화해야 할 수 있습니다. 비즈니스/엔터프라이즈 플랜에서 관리자는 사용자 지정 커넥터를 허용해야 합니다.)
3. **+**&#x200B;을(를) 클릭합니다.
4. **이름**&#x200B;을(를) 입력하십시오.
5. **연결**&#x200B;의 경우 **서버 URL**&#x200B;을(를) 선택하고 MCP 서버 URL을 입력하십시오.
6. **Authentication**&#x200B;을 **OAuth**(으)로 설정된 상태로 둡니다.
7. 위험 메시지를 읽고 확인란을 선택합니다.
8. **만들기**&#x200B;를 클릭한 다음 로그인하세요.

## Fusion을 사용자 지정 MCP 솔루션에 연결

자체 애플리케이션이나 에이전트를 구축하는 경우 Fusion MCP 서버에 직접 연결합니다.

## 다른 Fusion 조직으로 전환

조직을 변경하기 위해 연결을 끊을 필요가 없습니다. Fusion MCP 서버는 세션 내에서 활성 조직을 전환할 수 있습니다.

* _어떤 Fusion 조직이 있습니까?_
* _1234 조직으로 전환합니다._

에이전트는 `fusion_orgs_list` 및 `fusion_orgs_set`을(를) 사용합니다. 전환은 현재 대화/세션에만 적용됩니다. 서로 다른 데이터 센터 영역(예: 미국 및 EU)의 조직은 모두 동일한 MCP URL을 통해 사용할 수 있습니다.

## 설정 및 인증 문제 해결

| 문제 | 가능한 원인 | 고정 |
| --- | --- | --- |
| Claude 또는 ChatGPT 디렉터리에서 Fusion 커넥터를 찾을 수 없습니다. | Adobe은 Fusion용 디렉터리 커넥터를 게시하지 않습니다. | 이 문서의 URL을 사용하여 Fusion을 사용자 지정 MCP 서버로 추가합니다. |
| Claude 또는 ChatGPT에서는 사용자 지정 커넥터를 추가할 수 없습니다. | 플랜은 사용자 지정 커넥터를 소유자 또는 관리자로 제한합니다. | Cloud 또는 ChatGPT 관리자에게 커넥터를 추가하거나 사용자 지정 MCP 서버를 허용하도록 요청하십시오. |
| 연결했지만 데이터가 없거나 잘못된 데이터가 표시됩니다. | 잘못된 Fusion 조직이 활성 상태입니다. | 에이전트에게 조직 목록을 요청하고 올바른 조직으로 전환하십시오. |
| 인증에 실패했거나 연결이 작동하지 않았습니다. | 세션이 만료되었거나 연결 오류가 발생했습니다. | 서버 연결을 끊고 다시 연결합니다. |
| MCP 액세스가 비활성화되었다는 메시지가 표시됩니다. | Fusion 조직에 대한 MCP 액세스가 해제되었습니다. | Fusion 관리자에게 문의하여 활성화하십시오. |
| 에이전트는 시나리오를 읽을 수 있지만 생성, 실행, 업데이트 또는 삭제할 수 없습니다. | MCP 작성 도구가 비활성화되어 있거나 팀 역할이 허용하지 않습니다. | Fusion 관리자에게 쓰기 도구를 활성화하거나 필요한 팀 역할을 부여하도록 요청하십시오. |
| 사용자 지정 앱 인증이 거부되었습니다. | 콜백 URL이 승인된 목록에 없습니다. | 관리자에게 정확한 콜백 URL을 추가하도록 요청하십시오. |
| Fusion이 Coworker에 나열되지 않거나 Fusion 오른쪽 레일에서 Coworker가 누락되었습니다. | 귀사에 대해 기능이 활성화되지 않았습니다. <!-- BECKY CHECK ME: confirm whether this is the correct admin guidance before publishing. --> | Fusion 관리자에게 문의하십시오. |

## 자주 묻는 질문

### Claude 또는 ChatGPT에 대한 공식 Fusion 커넥터가 있습니까?

현재는 지원되지 않습니다. 사용자 지정 MCP 서버 URL을 사용합니다. Coworker(독립 실행형 및 Fusion 오른쪽 레일 내)에는 Fusion이 내장되어 있습니다.

### 두 개 이상의 Fusion 조직을 사용할 수 있습니까?

예. 다시 연결하지 않고 대화 중에 활성 조직을 전환할 수 있습니다.

### 대리인은 나를 대신해서 무엇을 할 수 있는가?

에이전트는 Fusion 역할 및 팀 권한을 사용하여 사용자의 역할을 합니다. Fusion에서 액세스할 수 없는 모든 항목에 액세스할 수 없습니다. 파괴적 작업에는 명시적 확인이 필요합니다.

### 에이전트가 내 연결 비밀을 보나요?

아니요. 연결 및 키 도구는 자격 증명 또는 비밀 값이 아닌 메타데이터(이름, 유형, 범위, 만료)를 반환합니다.
