---
title: 스토리지 개요
description: 스토리지는 Workfront Fusion의 페이지로, 팀이 Adobe ESM(Enterprise Storage Management) 저장소에 직접 액세스할 수 있으므로 사용자가 폴더를 찾아보고, 파일을 업로드 및 다운로드하고, 버전 기록을 보고, 자동화 시나리오를 만들 수 있습니다.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: d5568479d43bd5518adae5b66b132b4075e7f356
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 2%

---

# 스토리지 개요

<!--Add to navigation articles once this goes to production-->

Workfront Fusion의 스토리지 영역은 팀이 Adobe ESM(엔터프라이즈 스토리지 관리) 저장소에 직접 액세스할 수 있도록 합니다. 사용자는 Fusion을 종료하지 않고도 폴더를 찾아보고, 파일을 업로드 및 다운로드하고, 버전 기록을 보고, 자동화 시나리오를 만들 수 있습니다.

스토리지는 팀이 소유하며, Adobe 스토리지에 대한 액세스 권한이 있는 조직이 Adobe IMS(Identity Management System)에 온보딩되어야 합니다.

Fusion Storage의 파일은 Adobe 파일(adobe.com/files)에 미러링되므로 Adobe 파일에서 액세스할 수 있는 모든 파일은 Fusion Storage에서 액세스할 수 있습니다.

스토리지 사용에 대한 지침은 다음을 참조하십시오.

* [저장소 초기화](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)
* [Workfront Fusion의 스토리지 보기 및 관리](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-and-manage-storage-in-workfront-fusion.md)
* [저장소에 파일 업로드](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/upload-files-to-storage.md)
* [저장소에서 파일 다운로드](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/download-files-from-storage.md)
* [저장소에서 파일 삭제](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/delete-files-from-storage.md)
* [저장소에서 파일 버전 기록 보기](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-storage-file-version-history.md)
* [스토리지에서 시나리오 만들기](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md)

## 스토리지 사전 요구 사항

Workfront Fusion Storage 영역을 사용하려면 다음 사항이 충족되어야 합니다.

* 조직이 **Adobe IMS(Identity Management System)**&#x200B;에 온보딩되었습니다.
* 조직에 사용 가능한 **Adobe 저장소**&#x200B;가 있습니다.
* 사용자가 **올바른 Adobe IMS 조직**(선택한 Fusion 조직과 일치하는 조직)에 로그인되어 있습니다.
* 사용자의 계정에 **Adobe 저장소에 대한 액세스 권한이 있습니다**

## 용어집

사용 시

| 용어 | 정의 |
| ------ | ----------- |
| **저장소** | 일반적으로 프로젝트 또는 작업 영역에 매핑된 Adobe ESM의 최상위 스토리지 컨테이너 |
| **연결** | 초기화 중에 자동으로 생성되는 Fusion과 Adobe 스토리지 간의 보안 링크입니다. 자동 토큰 새로 고침으로 Adobe IMS 인증 사용 |
| **ESM** | Adobe의 클라우드 파일 스토리지 서비스인 엔터프라이즈 스토리지 관리 |
| **IMS** | Adobe Identity Management 시스템, Adobe 인증 및 ID 플랫폼 |

<!--

## UI Reference — Key Screens

### 1. Initialization Screen

* Cloud icon with **"Adobe Storage"** heading
* Description text explaining the feature
* **"Initialize Storage"** button (primary action)
* Error variants for access restriction, org mismatch, access denied, no storage found

### 2. Repository List

* Table with **Name** and **Region** columns
* **"Open"** action button per row

### 3. File Browser

* Breadcrumb navigation bar
* **"Upload File"** dropdown button (with "Upload File" and "Upload File in Scenario" options)
* File/folder table with **Name**, **Type**, **Size**, **Created** columns
* Floating action bar on file selection with: **Download**, **Download in Scenario**, **Versions**, **Delete**
* Upload/download progress banners (top-right corner)

### 4. Version History Panel

* Right-side slide-out panel
* Version list with date, version badge, and download button per entry
* **"current"** label on the latest version

-->
