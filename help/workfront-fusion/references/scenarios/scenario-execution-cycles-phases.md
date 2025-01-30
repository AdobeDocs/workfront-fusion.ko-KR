---
title: 시나리오 실행, 주기 및 단계
description: 이 문서에서는 초기화, 작업, 커밋 및 롤백과 같이  [!DNL Adobe Workfront Fusion] 시나리오가 실행되는 동안 발생하는 이벤트에 대해 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: abf41be5-df32-4eaf-b3f4-93ddf005bfe3
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 1%

---

# 시나리오 실행, 주기 및 단계

각 시나리오 실행은 초기화 단계로 시작하고, 작업 및 커밋/롤백 단계로 구성된 하나 이상의 주기를 계속하며, 종료 단계로 끝납니다

* 초기화
* 주기 #1
   * 작업(읽기 또는 쓰기)
   * 커밋 또는 롤백
* 주기 #2
   * 작업(읽기 또는 쓰기)
   * 커밋 또는 롤백
* ...
* 주기 #n
   * 작업(읽기 또는 쓰기)
   * 커밋 또는 롤백
* 완료

더 작은 규모에서, 각각의 모듈은 또한 이들 단계를 따른다. 모듈 단계에 대한 정보는 시나리오가 실행된 후 각 모듈의 오른쪽 상단에 있는 번호가 매겨진 버블에 있는 처리된 번들 정보에서 찾을 수 있습니다. 처리된 번들 정보를 찾는 방법에 대한 자세한 내용은 시나리오 실행 흐름의 [처리된 번들에 대한 정보](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md#information-about-processed-bundles)를 참조하십시오.

더 큰 시나리오 단계에 대한 정보는 실행 세부 정보에서 찾을 수 있습니다.

## 시나리오 실행 단계

### 초기화

초기화 단계에서는 필요한 모든 연결(데이터베이스, 이메일 서비스 등에 대한 연결)이 생성되고 확인되어 모듈이 의도한 작업을 수행할 수 있는지 확인합니다.

### 주기

각 주기는 커밋 또는 롤백이 있는 일련의 작업으로 구성된 나눌 수 없는 작업 단위를 나타냅니다.

[!UICONTROL scenario settings] 패널에서 최대 주기 수를 설정할 수 있습니다. 기본 숫자는 1입니다.

* [작업](#operation)
* [커밋](#commit)
* [Rollback](#rollback)

#### 작업

작업 단계 동안 읽기 또는 쓰기 작업이 수행됩니다.

* 읽기 작업은 미리 정의된 시나리오에 따라 다른 모듈에서 처리되는 서비스로부터 데이터를 얻는 것으로 구성됩니다. 예를 들어 [!UICONTROL Workfront] >[!UICONTROL Watch records] 모듈은 마지막 시나리오 실행 이후 만들어진 새 번들(레코드)을 반환합니다.
* 쓰기 작업은 추가 처리를 위해 주어진 서비스에 데이터를 전송하는 것으로 이루어진다. 예를 들어 [!DNL Workfront] >[!UICONTROL Upload Document] 모듈이 Workfront에 파일을 업로드합니다.

#### 커밋

작업 단계가 성공하면 모듈에서 수행한 모든 작업이 커밋되는 커밋 단계가 시작됩니다. 즉, [!DNL Workfront Fusion]이(가) 성공 여부에 대한 정보를 작업 단계에 포함된 모든 서비스에 보냅니다.

### Rollback

모듈에서 작업 또는 커밋 단계 중에 오류가 발생하면 단계가 중단되고 롤백 단계가 시작되므로 주어진 주기 동안 모든 작업이 무효화됩니다.

>[!IMPORTANT]
>
>롤백을 지원하는 모든 [!DNL Workfront Fusion] 모듈(트랜잭션이라고도 함)은 ACID 태그로 표시됩니다.
>
>![Acid 모듈](assets/acid-modules.png)
>
>이 태그로 표시되지 않은 모듈은 다른 모듈에서 오류가 발생할 때 초기 상태로 되돌릴 수 없습니다. ACID가 아닌 모듈의 일반적인 예로는 [!UICONTROL Email] >[!UICONTROL Send an Email] 작업이 있습니다. 이메일을 보낸 후에는 전송을 실행 취소할 수 없습니다.

### 완료

완료 단계에서 열린 연결(예: FTP 연결, 데이터베이스 연결 등)이 닫히고 시나리오가 완료됩니다.

## 리소스

자세한 내용은 [시나리오 설정 구성](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)을 참조하십시오.
