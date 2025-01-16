---
title: MariaDB 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는  [!DNL MariaDB]을(를) 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# [!DNL MariaDB]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL MariaDB]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 플랜*</td>
  <td> <p>[!UICONTROL Pro] 이상</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td> 
   <td>
   <p>현재 라이선스 요구 사항: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합을 위한 [!UICONTROL [!DNL Workfront Fusion]] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>현재 제품 요구 사항: [!UICONTROL Select] 또는 [!UICONTROL Prime] [!DNL Adobe Workfront] 플랜이 있는 경우 조직에서 이 문서에 설명된 기능을 사용하려면 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다. [!DNL Workfront Fusion]이(가) [!UICONTROL Ultimate] [!DNL Workfront] 계획에 포함되어 있습니다.</p>
   <p>또는</p>
   <p>레거시 제품 요구 사항: 이 문서에 설명된 기능을 사용하려면 조직에서 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구매해야 합니다.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

## 전제 조건

[!DNL MariaDB] 모듈을 사용하려면 [!DNL MariaDB] 계정이 있어야 합니다.

## [!DNL MariaDB]을(를) [!DNL Workfront Fusion]에 연결

[!DNL MariaDB] 모듈 내에서 직접 [!DNL MariaDB] 계정에 연결할 수 있습니다.

1. [!DNL MariaDB] 모듈에서 [!UICONTROL Connection] 필드 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 다음 필드를 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>새 연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>데이터베이스 인스턴스의 IP 주소 또는 호스트 이름을 입력합니다. 네트워크 외부에서 이 호스트에 액세스할 수 있어야 합니다.</p> <p>예: <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Port]</td> 
      <td>기본 포트는 3306입니다. 비표준 포트를 사용하는 경우 이 번호를 포트로 설정합니다. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Database Name]</td> 
      <td>상호 작용할 데이터베이스의 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Username]</td> 
      <td>사용자 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>암호를 입력합니다.</td> 
     </tr> 
    </tbody> 
   </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## [!DNL MariaDB] 모듈 및 해당 필드

[!DNL MariaDB] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL MariaDB] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 쿼리 실행(고급)

이 작업 모듈은 제공한 쿼리를 기반으로 데이터베이스에서 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL MariaDB] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">[!DNL MariaDB]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>모듈에서 데이터를 검색하는 데 사용할 SQL 쿼리를 입력합니다.</p> <p>중요: 쿼리에 사용된 변수는 정리되지 않습니다. SQL 삽입을 방지하기 위해 변수를 제대로 정리해야 합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Select rows from a table (advanced)]

이 모듈은 데이터베이스에서 레코드를 읽습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL MariaDB] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">[!DNL MariaDB]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table]</td> 
   <td> <p>읽으려는 레코드가 포함된 테이블을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>행을 선택할 필터 설정</p> 
    <ul> 
     <li> <p>검색할 필드 선택</p> </li> 
     <li> <p>검색에 사용할 연산자를 선택합니다</p> </li> 
     <li> <p>검색할 값을 입력하거나 매핑합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort] </td> 
   <td> <p>결과를 정렬하려는 각 수준에 대해 <strong>[!UICONTROL Add item]</strong>을(를) 클릭한 다음 결과를 정렬하려는 필드와 오름차순 또는 내림차순 정렬 여부를 선택합니다</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
