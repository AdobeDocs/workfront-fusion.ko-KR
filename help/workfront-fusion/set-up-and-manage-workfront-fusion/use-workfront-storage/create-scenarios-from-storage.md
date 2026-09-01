---
title: 스토리지에서 시나리오 만들기
description: 저장소는 Fusion의 시나리오 빌더와 통합되므로 저장소 페이지에서 직접 사전 구성된 시나리오를 만들어 파일을 다운로드하거나 업로드할 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: aef1685cb25c0cdcb0dcdf9b0c73fb482d392e5f
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# 스토리지에서 시나리오 만들기

저장소 개요는 [저장소 개요](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md)를 참조하십시오.

스토리지는 Fusion의 시나리오 빌더와 통합됩니다. 스토리지 페이지에서 사용자는 선택한 파일을 다운로드할 시나리오를 만들 수 있습니다.

## 시나리오에서 다운로드

1. Workfront Fusion의 왼쪽 탐색에서 **저장소**&#x200B;를 클릭합니다.
1. 시나리오에서 다운로드할 파일이 포함된 저장소로 이동합니다.
1. 파일을 선택한 다음 작업 표시줄에서 **&quot;시나리오에서 다운로드&quot;**&#x200B;를 클릭합니다.

그러면 Fusion에서 **&quot;다운로드 {fileName}&quot;**(이)라는 새 시나리오를 만듭니다. 이 시나리오는 별도의 브라우저 탭에서 열립니다.

시나리오가 다음으로 사전 구성됩니다.

* 활성 연결입니다.
* 저장소, 폴더 및 파일이 미리 선택되었습니다.
* 사전 서명된 다운로드 URL을 생성하는 모듈입니다.
* 해당 URL에서 파일을 가져오는 HTTP 모듈입니다.
* 기본 예약 간격은 15분입니다.

## 시나리오에서 파일 업로드

1. Workfront Fusion의 왼쪽 탐색에서 **저장소**&#x200B;를 클릭합니다.
1. 시나리오에서 다운로드할 파일이 포함된 저장소 및 폴더로 이동합니다.
1. 폴더 내부를 탐색하는 동안 **&quot;파일 업로드&quot;** 드롭다운을 클릭합니다.
1. **&quot;시나리오의 파일 업로드&quot;**&#x200B;를 선택합니다.

그러면 Fusion에서 **&quot;{folderName}&quot;**&#x200B;에 업로드라는 새 시나리오를 만듭니다. 이 시나리오는 새 브라우저 탭에서 열립니다. Workfront > 문서 다운로드 모듈과 같이 업로드할 파일을 제공하는 모듈을 추가해야 합니다.

시나리오가 다음으로 사전 구성됩니다.

* 활성 연결입니다.
* 저장소 및 폴더가 미리 선택되었습니다.
* 자리 표시자 파일 이름으로 사전 서명된 업로드 URL을 생성하는 모듈입니다.
* 기본 예약 간격은 15분입니다.

