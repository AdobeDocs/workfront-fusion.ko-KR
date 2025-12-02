---
title: Veeva Vault 모듈
description: Adobe Workfront Fusion 시나리오에서는 Veeva Vault를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
source-git-commit: 881e5ba39d1730b641085cf0d02137d18e443135
workflow-type: tm+mt
source-wordcount: '2485'
ht-degree: 19%

---

# Veeva Vault 모듈

Adobe Workfront Fusion 시나리오에서는 Veeva Vault를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

시나리오 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 색인](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>모든 Adobe Workfront 워크플로 패키지 및 모든 Adobe Workfront 자동화 및 통합 패키지</p><p>Workfront Ultimate</p><p>Workfront Prime 및 Select 패키지 및 Workfront Fusion 추가 구매.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>표준</p><p>작업 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>작업 기반: Workfront Fusion 라이선스 요구 사항 없음</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

Veeva Vault 모듈을 사용하려면 Veeva Vault 계정이 있어야 합니다.

## Veeva Vault를 Workfront Fusion에 연결

Veeva Vault 모듈 내에서 직접 Veeva Vault 계정에 연결할 수 있습니다.

연결을 만들 때 암호를 사용할지 또는 OAuth2 인증을 사용할지 여부를 선택할 수 있습니다.

### 사용자 이름과 암호를 사용하여 Veeva Vault에 연결

1. Veeva Vault 모듈에서 Connection 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. **연결 유형** 필드에서 `Veeva Username Password`을(를) 선택합니다.
1. 다음 필드를 입력합니다.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">연결 이름</td> 
       <td> <p>연결의 이름을 입력합니다.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">사용자 이름</td>
        <td>
          <p>Veeva Vault 계정의 사용자 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">암호</td>
        <td>
          <p>Veeva Vault 계정의 암호를 입력합니다.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">자격 증명 모음 DNS</td> 
       <td>Veeva Vault DNS(도메인 이름)를 입력합니다.</p><p>Veeva Vault DNS를 찾으려면 Veeva Vault에 액세스하는 데 사용하는 URL을 검사합니다.</p>예를 들어 URL <code>https://my-dns.veevavault.com</code>에서 DNS는 <code>my-dns</code>입니다. 전체 URL을 입력할 필요는 없습니다.</td> 
      </tr> 
     </tbody> 
    </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

### OAuth2 인증을 사용하여 Veeva Vault에 연결

1. Veeva Vault 모듈에서 Connection 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
1. **연결 유형** 필드에서 `Veeva Oauth 2`을(를) 선택합니다.
1. 다음 필드를 입력합니다.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">연결 이름</td> 
       <td> <p>연결의 이름을 입력합니다.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">클라이언트 ID</td>
        <td>
          <p>이 연결에 사용할 Veeva Vault 응용 프로그램의 클라이언트 ID를 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">클라이언트 암호</td>
        <td>
          <p>이 연결에 사용할 Veeva Vault 응용 프로그램의 클라이언트 암호를 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">범위</td>
        <td>
          <p>이 연결의 범위를 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">임차인 ID</td>
        <td>
          <p>이 연결에 대한 테넌트 ID를 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">프로필 ID</td>
        <td>
          <p>OAuth2 / Copen ID Connect 프로필의 ID를 입력합니다.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">자격 증명 모음 DNS</td> 
       <td>Veeva Vault DNS(도메인 이름)를 입력합니다.</p><p>Veeva Vault DNS를 찾으려면 Veeva Vault에 액세스하는 데 사용하는 URL을 검사합니다.</p>예를 들어 URL <code>https://my-dns.veevavault.com</code>에서 DNS는 <code>my-dns</code>입니다. 전체 URL을 입력할 필요는 없습니다.</td> 
      </tr> 
     </tbody> 
    </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.


## Veeva Vault 모듈 및 해당 필드

Veeva Vault 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 추가 Veeva Vault 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [문서](#document)
* [오브젝트](#object)
* [기타](#other)

### 문서

* [단일 문서 만들기](#create-a-single-document)
* [여러 문서 만들기](#create-multiple-documents)
* [단일 문서 삭제](#delete-a-single-document)
* [파일 다운로드](#download-file)
* [문서 내보내기](#export-documents)
* [단일 문서 가져오기](#get-a-single-document)
* [사용자 작업 시작](#initiate-user-action)
* [문서 나열](#list-documents)
* [문서 내보내기 결과 가져오기](#retrieve-document-export-results)
* [단일 문서 업데이트](#update-a-single-document)
* [여러 문서 업데이트](#update-multiple-documents)

#### 단일 문서 만들기

이 모듈은 단일 문서, 바인더 또는 템플릿을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서, 바인더 또는 템플릿을 만들지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>필드 선택</p> </td> 
   <td> <p>데이터를 입력할 필드를 선택한 다음 해당 필드에 데이터를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 여러 문서 만들기

이 모듈은 CSV 파일을 사용하여 여러 문서 또는 템플릿을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>템플릿을 만들지 문서를 만들지 선택합니다</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>파일 데이터</p> </td> 
   <td> <p>문서를 만드는 데 사용할 CSV 파일을 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 단일 문서 삭제

이 모듈은 단일 문서, 바인더 또는 템플릿을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서, 바인더 또는 템플릿 중 어떤 것을 삭제할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>문서 ID / 바인더 ID / 템플릿 이름</p> </td> 
   <td> <p>삭제할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 파일 다운로드

이 모듈은 Veeva Vault에서 문서, 문서 버전 또는 템플릿을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서 또는 템플릿을 다운로드할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>다운로드 유형</p> </td> 
   <td> <p>문서 또는 문서 버전을 다운로드할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>문서 ID / 템플릿 이름</p> </td> 
   <td> <p>다운로드할 템플릿의 이름 또는 문서 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>문서 체크 아웃</p> </td> 
   <td> <p>문서를 다운로드하는 경우 다운로드하기 전에 문서를 체크 아웃하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>버전</p> </td> 
   <td> <p>문서 버전을 다운로드하는 경우 다운로드할 버전을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 문서 내보내기

이 모듈은 소스, 렌디션 및 텍스트를 포함하여 사용자가 지정하는 문서를 내보냅니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서, 바인더 또는 템플릿 중 어떤 것을 삭제할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>소스</p> </td> 
   <td> <p>내보내기에 소스 파일을 포함하려면 이 옵션을 활성화합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>표현물</p> </td> 
   <td> <p>내보내기에 변환 파일을 포함하려면 이 옵션을 활성화합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>모든 버전</p> </td> 
   <td> <p>내보내기에 문서 파일의 모든 버전을 포함하려면 이 옵션을 활성화합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>텍스트</p> </td> 
   <td> <p>내보내기에 소스 문서 텍스트를 포함하려면 이 옵션을 활성화합니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 단일 문서 가져오기

이 모듈은 단일 문서, 바인더 또는 템플릿에 대한 메타데이터를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서, 바인더 또는 템플릿에 대한 데이터를 검색할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>문서 ID / 바인더 ID / 템플릿 이름</p> </td> 
   <td> <p>데이터를 검색할 필드를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 사용자 작업 시작

이 모듈은 검토를 위해 문서를 보내거나 문서 상태를 변경하는 등의 문서 및 바인더에 대한 작업을 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서 또는 바인더에 대해 작업을 수행할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>문서/바인더</p> </td> 
   <td> <p>작업을 수행할 문서 또는 바인더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>문서 버전/바인더 버전</p> </td> 
   <td> <p>작업을 수행할 문서 또는 바인더를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>액션</p> </td> 
   <td> <p>문서 또는 바인더에서 수행할 작업을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 문서 나열

이 모듈에는 선택한 유형의 모든 문서가 나열됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서, 바인더 또는 템플릿 나열 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 문서 내보내기 결과 가져오기

이 모듈은 이전에 요청한 문서 내보내기의 결과를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>작업 ID</p> </td> 
   <td> <p>결과를 반환할 작업의 ID를 입력하거나 매핑합니다. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### 여러 문서 업데이트

이 모듈은 CSV 파일을 사용하여 여러 문서 또는 템플릿을 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>템플릿을 만들지 문서를 만들지 선택합니다</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>파일 데이터</p> </td> 
   <td> <p>문서를 만드는 데 사용할 CSV 파일을 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 단일 문서 업데이트

이 모듈은 단일 문서, 바인더 또는 템플릿을 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>문서, 문서 버전, 바인더 또는 템플릿을 만들지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID / 이름</p> </td> 
   <td> <p>템플릿을 업데이트하는 경우 템플릿의 새 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>새 템플릿 이름</p> </td> 
   <td> <p>업데이트할 개체의 ID 또는 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>필드 선택</p> </td> 
   <td> <p>데이터를 입력할 필드를 선택한 다음 해당 필드에 데이터를 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 오브젝트

* [단일 개체 레코드 만들기](#create-a-single-object-record)
* [단일 개체 레코드 삭제](#delete-a-single-object-record)
* [단일 개체 가져오기](#get-a-single-object)
* [목록 개체 레코드](#list-objects-records)
* [단일 개체 레코드 업데이트](#update-a-single-object-record)

#### 단일 개체 레코드 만들기

이 모듈은 단일 객체 레코드를 생성, 복사 또는 딥 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>레코드를 만들거나 복사할지 또는 레코드를 딥 복사할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">마이그레이션 모드</td> 
   <td>레코드를 만들거나 복사하는 경우, 이 옵션을 사용하여 초기 상태가 아닌 최소한의 유효성 검사로 개체 레코드를 만들거나 업데이트하고, 비활성 레코드를 만들고, <code>createdby_v</code>과 같은 표준 및 시스템 관리 필드를 설정합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">트리거 없음</td> 
   <td>true로 설정하고 마이그레이션 모드가 활성화되면 모듈은 모든 시스템, 표준, 사용자 지정 SDK 트리거 및 작업 트리거를 건너뜁니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">개체 이름</td> 
   <td><code>product__v</code>, <code>country__v</code> 또는 <code>custom_object__c</code>과(와) 같은 개체 이름__v 필드 값을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 ID</td> 
   <td>레코드를 완전히 복사하는 경우 복사할 레코드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 필드</td> 
   <td>레코드를 완전히 복사하는 경우 값을 제공할 필드를 선택한 다음 해당 값을 제공합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 단일 개체 레코드 삭제

이 모듈은 단일 객체 레코드를 삭제하거나 계단식으로 삭제합니다. 레코드를 계단식으로 삭제하면 레코드와 모든 하위 개체가 삭제됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>레코드를 삭제할지 아니면 레코드를 계단식으로 삭제할지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">개체 이름</td> 
   <td>삭제할 객체를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 ID</td> 
   <td>삭제할 레코드의 ID를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">외부 ID</td> 
   <td>레코드 ID 대신 이 사용자 정의 문서 외부 ID를 사용할 수 있습니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 단일 개체 가져오기

이 모듈은 저장소의 특정 개체 레코드에 구성된 메타데이터를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">개체 이름</td> 
   <td>메타데이터를 검색할 개체를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 ID</td> 
   <td>메타데이터를 검색할 레코드의 ID를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 목록 개체 레코드

이 모듈은 인증된 저장소의 모든 저장소 개체를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>현지화된 레이블 검색</p> </td> 
   <td> <p>레이블 및 label_plural 객체 필드에 대한 현지화된(번역된) 문자열을 검색하려면 예를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Update a single object record-->

이 모듈은 기존 개체 레코드의 필드를 업데이트합니다.

이 모듈은 단일 객체 레코드를 생성, 복사 또는 딥 복사합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>레코드를 만들거나 복사할지 또는 레코드를 딥 복사할지 여부를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">마이그레이션 모드</td> 
   <td>이 옵션을 활성화하면 초기 상태가 아닌 최소한의 유효성 검사로 개체 레코드를 만들거나 업데이트하고, 비활성 레코드를 만들고, <code>createdby_v</code>과 같은 표준 및 시스템 관리 필드를 설정할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">트리거 없음</td> 
   <td>마이그레이션 모드가 활성화되면 모든 시스템, 표준, 사용자 지정 SDK 트리거 및 작업 트리거를 무시하도록 이 옵션을 활성화할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">개체 이름</td> 
   <td><code>product__v</code>, <code>country__v</code> 또는 <code>custom_object__c</code>과(와) 같은 개체 이름__v 필드 값을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 ID</td> 
   <td>업데이트할 레코드의 ID를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">주/도</td> 
   <td><code>X-VaultAPI-MigrationMode</code>이(가) true로 설정된 경우 레코드의 라이프사이클 상태를 지정하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">상태 레이블</td> 
   <td><code>X-VaultAPI-MigrationMode</code>이(가) true로 설정된 경우 레코드의 라이프사이클 상태 유형을 지정하십시오. <code>base:object_lifecycle:</code> 형식 다음에 개체 상태 형식을 사용하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 필드</td> 
   <td>레코드를 완전히 복사하는 경우 값을 제공할 필드를 선택한 다음 해당 값을 제공합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [사용자 정의 API 호출하기](#make-a-custom-api-call)
* [VQL 쿼리 만들기](#make-a-vql-query)
* [로그 읽기](#read-logs)

#### 사용자 정의 API 호출하기

이 작업 모듈은 Veeva Vault API에 대한 사용자 정의 호출을 수행합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td><code>baseurl/api/v</code>과(와) 관련된 경로를 입력하십시오.  예: <code>/objects/documents</code>. <code>baseurl/api/v/</code>은(는) 이미 포함되어 있으므로 포함하지 마십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">메서드</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">헤더</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">쿼리 문자열</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>예: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">본문</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### VQL 쿼리 만들기

이 모듈은 VQL(저장소 쿼리 언어)을 사용하여 쿼리를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>유형</p> </td> 
   <td> <p>템플릿을 만들지 문서를 만들지 선택합니다</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>파일 데이터</p> </td> 
   <td> <p>문서를 만드는 데 사용할 CSV 파일을 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 로그 읽기

이 모듈은 감사 추적에서 데이터를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결 </td> 
   <td> <p>Veeva Vault 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>감사 유형</p> </td> 
   <td> <p>데이터를 검색할 감사 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>시작 일자</p> </td> 
   <td> <p>검색할 감사의 시작 날짜를 입력하거나 매핑합니다.</p><p>지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">유형 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>종료 일자</p> </td> 
   <td> <p>검색할 감사의 종료 날짜를 입력하거나 매핑합니다.</p><p>지원되는 날짜 및 시간 형식 목록은 <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">유형 강제 변환</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>결과 URL </p> </td> 
   <td> <p>결과의 CSV를 다운로드할 URL을 가져오려면 CSV를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">반환된 최대 결과 수</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>


