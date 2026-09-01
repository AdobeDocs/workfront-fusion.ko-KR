---
title: 저장소 초기화
description: 사용자가 처음으로 스토리지로 이동하면 팀을 대신하여 Adobe 스토리지에 대한 보안 연결을 생성하는 초기화 화면이 표시됩니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 0%

---

# Workfront Fusion에서 스토리지 초기화

Adobe 클라우드 스토리지에서 저장소, 폴더 및 파일을 보려면 먼저 Fusion Storage 영역을 초기화해야 합니다.

저장소 개요는 [저장소 개요](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md)를 참조하십시오.

## 저장소 초기화

1. Workfront Fusion의 왼쪽 탐색에서 **저장소**&#x200B;를 클릭합니다.
1. **저장소 초기화**&#x200B;를 클릭합니다.

Fusion은 팀을 대신하여 Adobe 스토리지에 대한 보안 연결을 자동으로 생성합니다.

연결이 설정되면 Fusion은 팀의 저장소 저장소를 로드합니다.

## 초기화 문제 해결

| 메시지 | 이유 | 사용자가 수행해야 하는 작업 |
| -------- | -------- | ------------------------ |
| **액세스가 제한됨** | 조직이 Adobe IMS에 온보딩되어 있지 않습니다. | 조직 관리자에게 문의하여 IMS 온보딩을 완료하십시오. |
| **조직 불일치** | 사용자는 Fusion에서 선택한 조직이 아닌 다른 Adobe 조직에 로그인됩니다. | 로그아웃한 다음 올바른 Adobe IMS 조직을 사용하여 다시 로그인합니다. |
| **액세스 거부됨** | 사용자 계정에 필요한 권한이 없거나 조직에서 Adobe 저장소를 사용할 수 없습니다. | 조직 관리자와 계정 권한을 확인합니다. 해결 후 **다시 시도**&#x200B;를 클릭하세요. |
| **저장소를 찾을 수 없음** | 연결이 설정되었지만 저장소를 찾을 수 없습니다. | 조직에 Adobe 스토리지가 프로비저닝되었는지 확인합니다. 확인한 후 **저장소 로드**&#x200B;를 클릭하여 다시 시도하십시오. |
