---
title: Adobe Firefly 모듈
description: Adobe Workfront Fusion 시나리오에서는 Adobe Firefly Lightroom을 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 965cb643039be36eb3608cd801439a6a055974e4
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 16%

---

# Adobe Firefly Lightroom 모듈

<!--add to tocs-->

Adobe Workfront Fusion 시나리오에서는 Adobe Firefly Lightroom을 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

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

Adobe Firefly Lightroom 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 Adobe Firefly Lightroom 계정이 있어야 합니다.

## Adobe Firefly Lightroom에 대한 연결 만들기

Adobe Firefly Lightroom 모듈에 대한 연결을 만들려면 다음 작업을 수행하십시오.

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">연결 이름</td>
        <td>
          <p>이 연결의 이름을 입력합니다.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">환경</td>
        <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">유형</td>
        <td>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">클라이언트 ID</td>
        <td>Adobe 클라이언트 ID를 입력합니다. 이 정보는 Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
        <tr>
        <td role="rowheader">클라이언트 암호</td>
        <td>Adobe 클라이언트 암호를 입력합니다. 이 정보는 Adobe Developer Console의 자격 증명 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.


## Adobe Firefly Lightroom 모듈 및 해당 필드

Adobe Firefly Lightroom 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Adobe Firefly Lightroom 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [이미지에 XMP 추가](#add-xmp-to-image)
* [Lightroom 편집 적용](#apply-lightroom-edits)
* [Lightroom 사전 설정 적용](#apply-lightroom-presets)
* [자동 펴기](#auto-straighten)
* [자동 톤](#auto-tone)


### 이미지에 XMP 추가

이 모듈은 XMP 기반 Lightroom 사전 설정을 이미지에 적용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly Lightroom에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Adobe Firefly Lightroom에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 URL</td> 
   <td>XMP을 적용할 이미지를 나타내는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토리지 유형</td> 
   <td>이미지가 저장되는 저장 영역의 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">XMP 콘텐츠</td> 
   <td>이미지에 추가할 XMP 콘텐츠의 텍스트를 입력하거나 매핑합니다. XML 문자열이어야 합니다.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">방향</td> 
    <td>이미지에 적용할 EXIF 방향을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 스토리지</td> 
    <td>출력 파일을 저장할 위치를 선택합니다. <p>Fusion 내부 스토리지는 시나리오 외부에 이미지를 저장하지 않지만 시나리오의 다른 모듈이 이미지에 액세스할 수 있도록 합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 유형</td> 
   <td>출력 파일의 파일 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">덮어쓰기</td> 
   <td>모듈이 이미 있는 경우 출력을 덮어쓰도록 허용하려면 예를 선택합니다. 이는 Adobe 클라우드 스토리지에만 적용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">품질</td> 
   <td>출력 이미지의 품질을 입력하거나 매핑합니다. 1이 가장 품질이 낮고 12가 가장 높습니다. JPEG 파일에만 적용됩니다.</td> 
  </tr> 
 </tbody> 
</table>

### Lightroom 편집 적용

이 모듈은 이미지에 하나 이상의 Lightroom 편집 내용을 적용합니다. 편집에는 노출, 대비, 선명도 및 채도가 포함됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly Lightroom에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Adobe Firefly Lightroom에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 URL</td> 
   <td>XMP을 적용할 이미지를 나타내는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토리지 유형</td> 
   <td>이미지가 저장되는 저장 영역의 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">옵션 편집</td> 
   <td>이미지에 적용할 편집 옵션을 설정합니다.<p>옵션에 대한 자세한 내용은 Adobe Firefly Lightroom API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/lightroom/api/#operation/applyEdits">Lightroom 편집 적용</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 스토리지</td> 
    <td>출력 파일을 저장할 위치를 선택합니다. <p>Fusion 내부 스토리지는 시나리오 외부에 이미지를 저장하지 않지만 시나리오의 다른 모듈이 이미지에 액세스할 수 있도록 합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 유형</td> 
   <td>출력 파일의 파일 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">덮어쓰기</td> 
   <td>모듈이 이미 있는 경우 출력을 덮어쓰도록 허용하려면 예를 선택합니다. 이는 Adobe 클라우드 스토리지에만 적용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">품질</td> 
   <td>출력 이미지의 품질을 입력하거나 매핑합니다. 1이 가장 품질이 낮고 12가 가장 높습니다. JPEG 파일에만 적용됩니다.</td> 
  </tr> 
 </tbody> 
</table>

### Lightroom 사전 설정 적용

이 모듈은 지정된 XMP 사전 설정 파일을 사용하여 지정된 이미지에 하나 이상의 XMP Lightroom 사전 설정을 적용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly Lightroom에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Adobe Firefly Lightroom에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 URL</td> 
   <td>XMP을 적용할 이미지를 나타내는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토리지 유형</td> 
   <td>이미지가 저장되는 저장 영역의 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">사전 설정</td> 
   <td>적용할 각 사전 설정에 대해 <b>항목 추가</b>를 클릭하고 사전 설정의 사전 지정된 URL을 입력한 다음 저장소 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 스토리지</td> 
    <td>출력 파일을 저장할 위치를 선택합니다. <p>Fusion 내부 스토리지는 시나리오 외부에 이미지를 저장하지 않지만 시나리오의 다른 모듈이 이미지에 액세스할 수 있도록 합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 유형</td> 
   <td>출력 파일의 파일 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">덮어쓰기</td> 
   <td>모듈이 이미 있는 경우 출력을 덮어쓰도록 허용하려면 예를 선택합니다. 이는 Adobe 클라우드 스토리지에만 적용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">품질</td> 
   <td>출력 이미지의 품질을 입력하거나 매핑합니다. 1이 가장 품질이 낮고 12가 가장 높습니다. JPEG 파일에만 적용됩니다.</td> 
  </tr> 
 </tbody> 
</table>

### 자동 펴기

이 모듈은 [자동 올림] 변형을 적용하여 이미지를 자동으로 펴줍니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly Lightroom에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Adobe Firefly Lightroom에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 URL</td> 
   <td>XMP을 적용할 이미지를 나타내는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토리지 유형</td> 
   <td>이미지가 저장되는 저장 영역의 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">업라이트 모드</td> 
   <td>사용할 [수직] 모드 유형을 선택합니다. 값을 설정하지 않으면 적절한 모드가 자동으로 제공됩니다.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">자르기 제한</td> 
   <td>모든 빈 가장자리를 제거하기 위해 곧게 펴진 이미지를 자를지 여부를 선택합니다.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">출력 저장소</td> 
    <td>출력 파일을 저장할 위치를 선택합니다. <p>Fusion 내부 스토리지는 시나리오 외부에 이미지를 저장하지 않지만 시나리오의 다른 모듈이 이미지에 액세스할 수 있도록 합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 유형</td> 
   <td>출력 파일의 파일 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">덮어쓰기</td> 
   <td>모듈이 이미 있는 경우 출력을 덮어쓰도록 허용하려면 예를 선택합니다. 이는 Adobe 클라우드 스토리지에만 적용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">품질</td> 
   <td>출력 이미지의 품질을 입력하거나 매핑합니다. 1이 가장 품질이 낮고 12가 가장 높습니다. JPEG 파일에만 적용됩니다.</td> 
  </tr> 
 </tbody> 
</table>


### 자동 톤

이 모듈은 이미지의 노출, 대비, 선명도 및 채도를 자동으로 수정합니다.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td>Adobe Firefly Lightroom에 대한 연결을 만드는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Adobe Firefly Lightroom에 대한 연결 만들기</a>를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">이미지 URL</td> 
   <td>XMP을 적용할 이미지를 나타내는 사전 서명된 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">스토리지 유형</td> 
   <td>이미지가 저장되는 저장 영역의 유형을 선택합니다.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">출력 스토리지</td> 
    <td>출력 파일을 저장할 위치를 선택합니다. <p>Fusion 내부 스토리지는 시나리오 외부에 이미지를 저장하지 않지만 시나리오의 다른 모듈이 이미지에 액세스할 수 있도록 합니다.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">출력 유형</td> 
   <td>출력 파일의 파일 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">덮어쓰기</td> 
   <td>모듈이 이미 있는 경우 출력을 덮어쓰도록 허용하려면 예를 선택합니다. 이는 Adobe 클라우드 스토리지에만 적용됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">품질</td> 
   <td>출력 이미지의 품질을 입력하거나 매핑합니다. 1이 가장 품질이 낮고 12가 가장 높습니다. JPEG 파일에만 적용됩니다.</td> 
  </tr> 
 </tbody> 
</table>


