---
title: 대용량 파일 작업
description: 현재 Workfront 및 HTTP 커넥터에서 대용량 파일을 지원할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 6df81943-e70c-42b3-aa44-d82343598a51
source-git-commit: c4696ad91dd0a2cf753147bffbb6e7b74bb99b02
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---

# 대용량 파일 작업

>[!IMPORTANT]
>
>대용량 파일 기능은 Workfront Ultimate 고객만 사용할 수 있으며 단계별 롤아웃입니다. Workfront Ultimate 플랜을 보유한 모든 Fusion 조직은 2025년 1월까지 대용량 파일 기능을 보유하게 됩니다.

이제 Workfront Fusion에서 향상된 데이터 전송 기능을 사용할 수 있으므로 훨씬 더 큰 파일을 시나리오에서 처리할 수 있습니다.

더 큰 파일을 처리하려면 시나리오를 업데이트해야 합니다.

>[!NOTE]
>
>이 기능은 Ultimate Workfront 패키지의 사용자만 사용할 수 있습니다.

## 대용량 파일을 지원하는 커넥터

초기 릴리스의 경우 다음 커넥터가 대용량 파일을 지원합니다.

* Workfront > 문서 업로드
* Adobe Experience Manager Assets > 문서 업로드
* Workfront Proof > 파일 업로드
* Adobe Authenticator > 사용자 지정 API 호출 만들기
* SharePoint > 파일 만들기 및 SharePoint > 파일 가져오기
* Salesforce > 파일 업로드
* AWS S3 > 파일 업로드 및 AWS S3 > 파일 가져오기
* HTTP

다른 커넥터는 향후 릴리스에서 지원됩니다.

## 대용량 파일을 처리하도록 시나리오 업데이트

Workfront > 문서 업로드 모듈이 더 큰 파일을 처리하도록 수정되었습니다. 이 모듈의 이전 버전에는 모듈 이름에 추가된 `(Legacy)`이(가) 표시됩니다. 대부분의 경우 레거시 모듈은 계속 작동합니다.

더 큰 파일로 작업할 계획이라면 기존 모듈을 새 문서 업로드 모듈로 대체하는 것이 좋습니다. 새로운 업로드 문서 모듈은 시간 초과 및 기타 오류를 방지합니다.

![문서 업로드](assets/new-upload-document.png)

## FAQ

### 새로운 파일 크기 제한은 얼마입니까?

이제 사용자는 이전의 1GB 제한을 초과하는 파일을 처리할 수 있으므로 효율성과 생산성을 향상시킬 수 있습니다.  플랫폼은 단일 작업(예: 파일 업로드)에 대해 최대 15GB의 개별 파일을 지원할 수 있지만 데이터 전송에 영향을 주는 다른 요인이 있습니다. 단일 작업의 파일 크기 제한은 궁극적으로 Fusion이 연결되는 웹 서비스에 따라 다릅니다. 데이터 전송은 단일 실행에 대한 총 처리입니다. 즉, 한 번의 실행으로 여러 가지 작업이 전체 데이터 전송에 기여합니다.

Fusion은 실행 제한 40분에 도달할 때까지 파일을 처리합니다. 큰 파일은 Fusion 시나리오에서 업로드, 다운로드 또는 처리하는 데 시간이 걸릴 수 있습니다. 개별 파일 크기에는 제한이 없지만 시나리오 실행 시간에는 40분 제한이 있습니다. 따라서 큰 파일이 실행되어 40분 이상 걸리는 경우 시나리오가 실패합니다. 시나리오 실행 시간은 시나리오 크기, 모듈 복잡성 및 네트워크 속도의 영향을 받을 수도 있습니다. 따라서 큰 파일을 사용할 때는 시나리오의 이러한 측면을 고려하는 것이 좋습니다.

### Fusion의 새 파일 전송은 어떻게 작동합니까?

Fusion이 파일을 처리하면 더 큰 파일이 영구 저장소(S3 버킷 또는 Azure Blob 저장소)에 추가됩니다. Fusion 모듈이 업로드 또는 다운로드와 같은 파일 작업을 실행할 때 Fusion은 활성 메모리 대신 영구 저장소의 파일을 소스로 사용합니다.

### 불완전한 실행을 사용하여 더 큰 파일로 작업할 수 있습니까?

예. Fusion은 더 큰 파일이 있는 불완전한 실행을 지원합니다. 미완료 실행은 조직의 크기가 제한되어 있으므로 적극적으로 관리해야 합니다.

### 어떤 커넥터에서든 더 큰 파일을 사용할 수 있습니까?

더 큰 파일을 지원하려면 각 Fusion 커넥터를 업데이트해야 합니다. 지원되는 커넥터에는 Workfront, HTTP 및 AEM Assets이 있습니다. Fusion Connectors는 여전히 웹 서비스에서 지원하는 파일 크기로 제한됩니다. 파일 크기 제한은 일반적으로 파일을 다운로드하고 업로드하는 웹 서비스 끝점에 대한 API 설명서에 포함됩니다.

### 이것이 작업에 영향을 줍니까?

아니요. 모듈에서 실행되는 작업 수는 동일합니다.

### 파일 전송 데이터를 표시하도록 Fusion의 UI는 언제 업데이트됩니까?

대시보드 및 시나리오 실행 세부 정보 페이지에서 파일 전송을 위한 Fusion의 UI에 대한 업데이트 작업을 진행 중이며 2025년 1분기를 타깃팅했습니다.

### 시나리오를 디자인하는 데 도움이 되는 새로운 파일 처리 제한에 대해 생각할 수 있는 몇 가지 방법은 무엇입니까?

40분 실행 제한 내에서 작동하도록 시나리오를 디자인하는 것은 복잡해 보일 수 있습니다. 시나리오를 디자인할 때는 다음 사항을 염두에 두는 것이 좋습니다.

* **실행 시간에 대한 비즈니스 요구 사항 이해**: 실행 시간에 대한 Fusion의 플랫폼 제한은 40분이지만 대부분의 비즈니스 프로세스 자동화는 훨씬 더 빨리 실행될 것으로 예상됩니다. 예를 들어, 사용자가 시작한 자동화는 40분 제한 하에서 완료될 것으로 예상됩니다.
* **디자인 시 실행 시간 고려**: 시나리오를 디자인할 때는 업로드 및 다운로드와 같은 개별 파일 작업에 대한 모듈 실행 시간을 이해하는 것이 중요합니다. 이 지식은 여러 파일 작업을 포함하는 시나리오를 계획하는 데 도움이 됩니다.  설계의 정확성을 보장하려면 모듈의 실행 시간을 반올림하여 버퍼를 포함하는 것이 좋습니다.
예를 들어 Fusion이 144초(2.4분) 만에 문서를 다운로드하는 경우 단일 실행에서 유사한 작업을 여러 번 수행할 수 있다고 예상할 수 있습니다. 이 예에서 모듈 실행은 실행하는 데 144초가 걸리며, 다운로드를 위해 3분의 실행 시간을 계획해야 합니다. 요구 사항에 업로드와 다운로드가 모두 포함된 경우 예상 실행 시간은 약 6분이 됩니다. Fusion 실행 시간은 40분으로 제한됩니다.

* **파일 작업 통합**: Fusion 시나리오에서 가장 일반적인 파일 작업의 예로는 다운로드 하나와 업로드 하나가 있습니다. 이 두 가지 작업만 있는 대부분의 시나리오는 몇 분 안에 실행됩니다. 가능한 경우 Fusion 디자이너는 시나리오를 하나의 다운로드 및 하나의 업로드로 제한해야 합니다.

* **매핑 패널을 사용하여 크기 계산**: Workfront 및 기타 웹 서비스에는 다운로드 모듈의 출력에 파일의 크기가 포함됩니다. 이 데이터를 사용하여 모듈 업로드에 대해 너무 크거나 시나리오 실행 시간에 대해 너무 큰 파일을 필터링할 수 있습니다.

* **여러 파일로 작업할 때 파일 작업을 자체 시나리오로 분리**: Fusion 디자이너는 파일 작업을 별도의 시나리오로 분리하는 것을 고려해야 합니다. 예를 들어 여러 개의 첨부 파일이 있는 새 Workfront 요청으로 트리거되는 Fusion 시나리오는 최대 30개의 파일을 수용해야 할 수 있습니다. 각 파일을 업로드하고 다운로드하는 데 최대 3분이 소요될 수 있으므로 모든 파일을 한 번에 처리하면 Fusion의 40분 실행 제한을 초과할 수 있습니다. 솔루션은 개별 파일의 업로드 및 다운로드를 처리하는 데 사용되는 파일 작업 시나리오를 만드는 것입니다. 요청이 트리거된 시나리오는 첨부된 파일을 반복하고 HTTP 모듈을 사용하여 각 파일에 대한 파일 작업 시나리오를 호출합니다. 이 방법을 사용하면 각 파일이 실행 시간 제한 내에 처리됩니다.

<!--
## Connectors that do not support large files

Some Fusion connectors do not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

The following connectors do **not** support large files. 

* Archive
* Box
* Convert
* CSV
* Datastores
* Flow control
* FTP
* JSON
* JWT
* Markdown
* Math
* Microsoft Word templates
* MIME
* Microsoft SQL
* SFTP
* Adobe Acrobat Sign
* SOAP
* Tools
* XML

If a connector is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.-->






<!--## Connectors that support large files

The following connectors support large files.

Workfront
HTTP
Webhooks
Salesforce
Microsoft Email
Workfront Proof
AEM Assets
Email
Slack
Jira
Microsoft Excel
SharePoint
Frame.io
Adobe PDF Services
Marketo
Azure Devops 
Google Email
Jira Server
Google Sheets
Microsoft OneDrive
ServiceNow 
AWS S3
Bynder
OneDrive Business
Adobe Authenticator
Google Drive
Microsoft Dynamics
Google Docs
NetSuite
Airtable
Azure AD
QuickBase 
Adobe Target
Adobe Campaign Classic
Microsoft Calendar
Workfront Planning
HubSpot CRM  
DropBox
Cloud Convert
Egnyte
Adobe Firefly
OpenAI / Chat GPT
Allocadia
Cvent
GitLab 
Google Team Drive
Google Calendar
Workfront SDL Managed Translation
Widen
Workfront Boards
Google Slides
Qualtrics
Microsoft Power BI
Adobe Photoshop
Anaplan
DocuSign 
MariaDB
Adobe Creative Cloud Libraries
Figma
AEM Forms
Datadog
GitHub 
Google Forms
Adobe I/O Events
Trello
Workday
Adobe Journey Optimizer
Adobe Lightroom


If a file is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

-->
