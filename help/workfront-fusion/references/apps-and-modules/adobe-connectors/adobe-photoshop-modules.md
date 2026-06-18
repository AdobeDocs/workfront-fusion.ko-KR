---
title: Adobe Photoshop 모듈
description: Adobe Photoshop 모듈을 사용하면 Adobe Photoshop 계정의 이벤트를 기반으로 Adobe Workfront Fusion 시나리오를 시작하고, 계약 및 기타 레코드를 생성, 읽기 또는 업데이트하고, 설정한 기준을 사용하여 레코드를 검색하고, 문서를 업로드할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
TQID: https://experienceleague.adobe.com/RratZmko93V0LMxJ6qTy6cNvRqgPNvNgHTflRngE6BI
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ce3fb5604ac4ed85af1bcc51143732499dfb0404
workflow-type: tm+mt
source-wordcount: 7285
ht-degree: 12%

---

# [!DNL Adobe Photoshop] 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Adobe Photoshop]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

>[!IMPORTANT]
>
>Adobe Photoshop에는 Fusion에서 Photoshop에서 작업을 수행하는 데 사용하는 API의 일부 요소가 더 이상 사용되지 않습니다.
>
>**따라서 기존 Photoshop 모듈 중 일부는 2026년 7월 30일 이후에 작동하지 않습니다.**
>
>이러한 모듈을 사용하는 모든 시나리오를 업데이트된 모듈로 가능한 한 빨리 업데이트하는 것이 좋습니다.
>
>영향을 받는 모듈 목록은 [Adobe Photoshop API 사용 중단 업데이트](#adobe-photoshop-api-deprecation-updates)를 참조하십시오.
>
>API 변경 내용이 Workfront Fusion에 미치는 영향에 대한 자세한 내용은 [Fusion의 API 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md)를 참조하십시오.

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

[!DNL Adobe Photoshop] 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 [!DNL Adobe Photoshop] 계정이 있어야 합니다.
* Firefly Services 라이선스가 있어야 합니다.
* 클라이언트 ID와 클라이언트 암호가 있어야 합니다. Adobe Developer Console에서 가져올 수 있습니다.

## Adobe Photoshop API 사용 중단 업데이트

Adobe Photoshop에는 Fusion에서 Photoshop에서 작업을 수행하는 데 사용하는 API의 일부 요소가 더 이상 사용되지 않습니다.

**따라서 기존 Photoshop 모듈 중 일부는 2026년 7월 30일 이후에 작동하지 않습니다.**

이 표에서는 이러한 사용 중단의 영향을 받은 모듈 및 업데이트해야 하는 모듈을 설명합니다.

| 더 이상 사용되지 않는 레거시 모듈 | 새 모듈로 업데이트 |
|---|---|
| PSD 편집 적용 | 합성 만들기 또는 편집 |
| 이미지 형식 변환 | 합성 만들기 또는 편집 |
| 합성 만들기 | 합성 만들기 또는 편집 |
| 새 PSD 만들기 | 합성 만들기 또는 편집 |
| 렌디션 만들기 | 합성 만들기 또는 편집 |
| 텍스트 레이어 편집 | Photoshop 작업, 스크립트 및 변형 실행 |
| 텍스트 레이어 편집 2 | Photoshop 작업, 스크립트 및 변형 실행 |
| 작업 JSON 실행 | Photoshop 작업, 스크립트 및 변형 실행 |
| 깊이 흐림 효과 실행 | (사용할 수 없음) |
| Photoshop 작업 실행 | Photoshop 작업, 스크립트 및 변형 실행 |
| 제품 자르기 실행 | Photoshop 작업, 스크립트 및 변형 실행 |
| 레이어 정보 가져오기 | 매니페스트 생성 |
| 이미지 크기 조정 | 합성 만들기 또는 편집 |
| 스마트 오브젝트 바꾸기 | 합성 만들기 또는 편집 |
| 스마트 오브젝트 2 바꾸기 | 합성 만들기 또는 편집 |
| 이미지 회전 | Photoshop 작업, 스크립트 및 변형 실행 |
| 이미지에 워터마크 지정 | 합성 만들기 또는 편집 |

## Adobe Photoshop API 정보

Adobe Photoshop 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Adobe Photoshop]에 연결하기

사용자의 [!DNL Adobe Photoshop] 모듈에 연결하려면:

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL 연결 유형]</td>
        <td>
          <p>JWT 연결을 사용할지 아니면 서버 간 연결을 사용할지 선택합니다.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>이 연결의 이름을 입력합니다.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>[!UICONTROL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력합니다. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 기술 계정 ID]</td>
        <td>JWT 연결을 사용하는 경우 [!DNL Adobe] [!UICONTROL 기술 계정 ID]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 조직 ID]</td>
        <td>JWT 연결을 사용하는 경우 [!DNL Adobe] [!UICONTROL 조직 ID]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 비공개 키]</td>
        <td>
          <p>JWT 연결을 사용하는 경우 [!DNL Adobe Developer Console]에서 자격 증명을 만들 때 생성된 개인 키를 입력하십시오. </p>
          <p>비공개 키 또는 인증서를 추출하려면 다음을 수행합니다.</p>
          <ol>
            <li value="1">
              <p><b>[!UICONTROL 추출]</b>을 클릭합니다.</p>
            </li>
            <li value="2">
              <p>추출할 파일 유형을 선택합니다.</p>
            </li>
            <li value="3">
              <p>비공개 키 또는 인증서가 포함된 파일을 선택합니다.</p>
            </li>
            <li value="4">
              <p>파일의 암호를 입력합니다.</p>
            </li>
            <li value="5">
              <p><b>저장</b>을 클릭하여 파일을 추출하고 연결 설정으로 돌아갑니다.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

## [!DNL Adobe Photoshop] 모듈 및 해당 필드

[!DNL Adobe Photoshop] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL Adobe Photoshop] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 액션

* [HEX를 RGB으로 변환](#convert-hex-to-rgb)
* [아트보드 만들기](#create-an-artboard)
* [합성 만들기 또는 편집](#create-or-edit-a-composite)
* [다양한 조정을 통해 이미지 편집](#edit-an-image-with-various-adjustments)
* [Photoshop 작업, 스크립트 및 변형 실행](#execute-photoshop-actions-scripts-and-transformations)
* [매니페스트 생성](#generate-a-manifest)
* [배경 제거](#remove-background)

#### HEX를 RGB으로 변환

이 모듈은 HEX 색상 코드를 RGB 색상으로 변환합니다.



이 모듈은 이미지에 대해 Lightroom 스타일 조정을 수행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL HEX]</td>
      <td>RGB으로 변환할 16진수 코드를 입력하거나 매핑합니다.</td>
    </tr>
    </tbody>
</table>

#### 아트보드 만들기

이 모듈은 Photoshop에 새 아트보드를 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 이미지]</td>
      <td>
        <p>이 대지에 추가할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 이미지의 소스 유형과 위치를 입력하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 아트보드 간격]</p>
      </td>
   <td>각 대지 사이에 지정할 간격을 픽셀 단위로 입력하거나 매핑합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>생성하려는 변환된 각 파일에 대해 항목 추가 를 클릭하고 나열된 대로 저장소, 위치 및 기타 옵션을 입력합니다.</p>
      </td>
    </tr>
    </tbody>
</table>

#### 합성 만들기 또는 편집

이 모듈은 Photoshop에서 합성을 만들거나 편집합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 이미지]</td>
      <td>
        <p>이 대지에 추가할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 이미지의 소스 유형과 위치를 입력하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 너비]</p>
      </td>
   <td>이미지를 만드는 경우 이미지 너비를 픽셀 단위로 입력하십시오.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 높이]</td>
      <td>
        <p>이미지를 만드는 경우 이미지 높이를 픽셀 단위로 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 모드]</td>
      <td>
        <p>이 이미지의 색상 모드를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 채우기]</td>
      <td>
        <p>배경 레이어의 채우기 유형을 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 이름]</td>
      <td>
        <p>새 이미지의 이름을 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Pixel scale factor]</td>
      <td>
        <p>픽셀 배율 계수를 입력하거나 매핑합니다. 0.1과 1 사이의 숫자여야 합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Resolution]</td>
      <td>
        <p><b>값</b> 필드에 해상도 값을 밀도 단위(인치당 픽셀 수)로 입력합니다. 기본값은 72입니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 프로필 유형]</td>
      <td>
        <p>기본 색상 프로파일을 무시하려면 프로파일 유형을 선택하고 나열된 대로 세부 정보를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 자르기 &gt; 위쪽 / 왼쪽 / 아래쪽 / 오른쪽]</td>
      <td>
        <p>이미지를 자를 범위를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 숨기기]</td>
      <td>
        <p>자르기 경계 외부에 있는 픽셀을 숨기려면 예를 선택합니다. false로 설정하면 자르기 범위를 벗어나는 픽셀이 삭제됩니다. 기본값은 false입니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 크기 조정 &gt; 폭]</td>
      <td>
        <p>너비에 사용할 단위를 선택한 다음 원하는 너비를 나타내는 값을 선택합니다. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 크기 조정 &gt; 높이]</td>
      <td>
        <p>높이에 사용할 단위를 선택한 다음 원하는 높이를 나타내는 값을 선택합니다. </p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Resolution]</td>
      <td>
        <p>해상도에 사용할 단위를 선택한 다음 원하는 해상도를 나타내는 값을 선택합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 리샘플]</td>
      <td>
        <p>크기를 조정할 때 사용할 리샘플링 방법을 선택합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 제한 비율]</td>
      <td>
        <p>폭과 높이 사이의 종횡비를 유지하려면 예를 선택합니다. 폭과 높이를 독립적으로 조정하려면 아니오를 선택합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 래스터화]</td>
      <td>
        <p>이미지를 래스터화할지 여부를 선택합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 배율 스타일]</td>
      <td>
        <p>이미지 크기를 조정할 때 스타일에 배율을 적용할지 여부를 선택합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Trim on]</td>
      <td>
        <p>투명 픽셀에서 트리밍할지 여부를 선택합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 레이어]</td>
      <td>
        <p>나중에 추가할 때마다 <b>항목 추가</b>를 클릭하고 레이어 세부 정보를 입력하십시오. </p><p>자세한 내용은 Adobe 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">합성 만들기 또는 편집</a>을 참조하십시오.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Default font PostScript name]</td>
      <td>
        <p>사용할 기본 글꼴의 PostScript 이름을 입력하거나 매핑합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Missing font strategy]</td>
      <td>
        <p>글꼴을 사용할 수 없는 경우 만들기 또는 편집이 실패하도록 할지 또는 기본 글꼴을 사용할지 선택합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 추가 글꼴]</td>
      <td>
        <p>추가할 각 글꼴에 대해 <b>항목 추가</b>를 클릭하고 해당 글꼴의 소스 URL을 입력하십시오. </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>만들려는 각 편집된 파일에 대해 항목 추가 를 클릭하고 출력 세부 정보를 입력합니다. </p><p>자세한 내용은 Adobe 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/createComposite">합성 만들기 또는 편집</a>을 참조하세요.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 최대 결과 수]</td>
      <td>
        <p>한 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</p>
      </td>
      </tr>
      </tbody>
</table>

#### 다양한 조정을 통해 이미지 편집

이 모듈은 이미지에 대해 Lightroom 스타일 조정을 수행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 이미지]</td>
      <td>
        <p>이미지의 소스 유형 및 위치를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 기타 필드]</p>
      </td>
   <td><p>자세한 내용은 Adobe 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop-v2/#operation/edit">다양한 조정을 통해 이미지 편집</a>을 참조하십시오.</p></td> 
    </tr>
    </tbody>
</table>

#### Photoshop 작업, 스크립트 및 변형 실행

이 모듈은 Firefly Photoshop API에서 사용할 수 있는 작업, 스크립트 및 변환을 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 이미지]</td>
      <td>
        <p>이미지의 소스 유형 및 위치를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Actions]</p>
      </td>
   <td><p>추가할 각 작업에 대해 <b>항목 추가</b>를 클릭하고 작업의 소스, URL 및 이름을 입력합니다.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL UXP source]</p>
      </td>
   <td><p>UXP 스크립트를 사용하는 경우 URL을 제공할지 인라인 콘텐츠를 제공할지 선택한 다음 URL이나 콘텐츠를 입력하거나 매핑합니다.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 추가 컨텐츠]</p>
      </td>
   <td><p>작업 또는 UXP에서 참조한 파일을 최대 25개까지 추가합니다.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>만들려는 각 편집된 파일에 대해 항목 추가 를 클릭하고 형식, 대상 및 출력 패턴을 입력합니다.</p>
      </td>
    </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 최대 결과 수]</td>
      <td>
        <p>한 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</p>
      </td>
      </tr>
    </tbody>
</table>

#### 매니페스트 생성

이 모듈은 지정된 입력 이미지에 대한 PSD 매니페스트를 생성합니다.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source]</td>
      <td>
        <p>이미지의 소스 유형 및 위치를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>만들려는 각 편집된 파일에 대해 항목 추가 를 클릭하고 대상 세부 정보를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레이어 썸네일 포함]</p>
      </td>
   <td><p>매니페스트의 각 레이어에 대해 썸네일 렌디션을 생성하도록 모듈화하려면 예를 선택합니다.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 최대 썸네일 깊이]</p>
      </td>
   <td><p>썸네일 표현물의 최대 깊이를 입력하거나 매핑합니다. 최대 깊이가 없으면 <code>0</code>을(를) 입력하십시오.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레이어 썸네일 형식]</p>
      </td>
   <td><p>썸네일을 JPEG 또는 PNG 형식으로 할지 선택합니다.</p></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 스마트 오브젝트 데이터 추출]</td>
      <td>
        <p>포함된 스마트 개체를 추출하고 매니페스트에 사전 서명된 URL을 포함할지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 트림을 투명도로 트림]</td>
      <td>
        <p>투명 픽셀을 제거하기 위해 각 레이어 썸네일을 트리밍할지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 최대 결과 수]</td>
      <td>
        <p>한 실행 주기 동안 모듈에서 작업할 최대 결과 수를 입력하거나 매핑합니다.</p>
      </td>
      </tr>
    </tbody>
</table>

#### 배경 제거

이 작업 모듈은 이미지의 주요 주제를 식별하고 배경을 제거합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>배경을 제거할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 배경을 제거할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 색상 공간]</p>
      </td>
   <td>출력 이미지에서 RGB 색상을 사용할지 RGBA 색상을 사용할지 선택합니다. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>이미지의 가장자리를 소프트(페더) 또는 바이너리로 할지 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>속도를 위해 최적화하려면 [성능]을 선택하고 대기 시간을 허용하려면 [일괄 처리]를 선택하십시오. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 사후 프로세스]</p>
      </td>
   <td>사후 처리를 사용할지 여부를 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 버전]</p>
      </td>
   <td>기본값은 4.0입니다.</td> 
    </tr> 
    </tbody>
</table>


### 레거시

* [PSD 편집 적용(이전)](#apply-psd-edits-legacy)
* [이미지 자동 색상 교정(이전)](#auto-color-correct-an-image-legacy)
* [이미지 형식 변환(이전)](#convert-image-format-legacy)
* [마스크 만들기(기존)](#create-a-mask-legacy)
* [새 PSD 만들기(이전)](#create-a-new-psd-legacy)
* [렌디션 만들기(기존)](#create-renditions-legacy)
* [텍스트 레이어 편집(이전)](#edit-text-layers-legacy)
* [텍스트 레이어 2 편집(이전)](#edit-text-layers-2-legacy)
* [JSON(이전) 작업 실행](#execute-an-action-json-legacy)
* [깊이 흐림 효과 실행(이전)](#execute-depth-blur-legacy)
* [Photoshop 작업 실행(기존)](#execute-photoshop-actions-legacy)
* [제품 자르기 실행(이전)](#execute-product-crop-legacy)
* [레이어 정보 가져오기(이전)](#get-layer-info-legacy)
* [사용자 지정 API 호출 만들기(이전)](#make-a-custom-api-call-legacy)
* [배경 제거(레거시)](#remove-background-legacy)
* [스마트 오브젝트 바꾸기(기존)](#replace-a-smart-object-legacy)
* [스마트 오브젝트 2(기존) 바꾸기](#replace-a-smart-object-2-legacy)
* [이미지 크기 조정(이전)](#resize-an-image-legacy)
* [이미지에 워터마크 지정 (기존)](#watermark-an-image-legacy)

#### PSD 편집 적용(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [복합 모듈 만들기 또는 편집](#create-or-edit-a-composite) 모듈로 업데이트하세요.

이 작업 모듈은 다양한 문서 및 레이어 수준 편집 사항을 적용합니다.

이 모듈은 대용량 파일을 지원합니다. 대용량 파일에 대한 자세한 내용은 [대용량 파일 작업](/help/workfront-fusion/references/scenarios/fusion-large-files.md)을 참조하십시오.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>편집할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 편집할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Image size) Height]</p>
      </td>
      <td> 이미지의 높이를 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Image size) Width]</p>
      </td>
      <td> 이미지의 폭을 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Canvas size) Top]</p>
      </td>
   <td> 문서 왼쪽 위 모서리의 y 좌표를 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Canvas Size) Bottom]</p>
      </td>
   <td> 문서의 오른쪽 아래 모서리에 대한 y 좌표를 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Canvas Size) Left]</p>
      </td>
   <td> 문서의 왼쪽 위 모서리의 x 좌표를 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Canvas Size) Right]</p>
      </td>
   <td> 문서의 오른쪽 아래 모서리의 x 좌표를 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document) Trim]</p>
      </td>
   <td> 이미지의 투명 픽셀에 트림을 적용하려면 [투명 픽셀]을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Default font]</p>
      </td>
   <td> 문서의 전역 기본값으로 사용할 글꼴의 전체 포스트스크립트 이름을 입력합니다. 이 글꼴은 글꼴이 누락되고 해당 레이어에 대해 특별히 제공된 다른 글꼴이 없는 텍스트 레이어에 사용됩니다. 이 글꼴이 누락된 경우 누락된 글꼴 관리에 지정된 옵션이 적용됩니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> 문서에 필요한 각 글꼴에 대해 항목 추가 를 클릭하고 글꼴의 저장소 위치와 파일 위치를 입력합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) 누락된 글꼴 관리]</p>
      </td>
   <td> 문서에 누락된 글꼴이 하나 이상 있는 경우 수행할 작업을 선택합니다. <ul><li><code>fail</code>: 작업에 성공하지 못하고 상태가 실패 로 설정됩니다. 오류의 세부 정보는 상태의 세부 정보 섹션에 제공됩니다.</li><li><code>useDefault</code>: 작업이 성공하고 누락된 모든 글꼴이 ArialMT로 대체됩니다.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Layers]</p>
      </td>
   <td> 추가할 각 레이어에 대해 항목 추가 를 클릭하고 레이어 세부 정보를 입력합니다. <p>레이어 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/modifyDocumentAsync">PSD 편집 적용</a>을 참조하십시오.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>만들려는 각 편집된 파일에 대해 항목 추가 를 클릭하고 나열된 대로 저장소, 위치 및 유형을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다. 출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>파일을 변환할 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Trim to Canvas]</p>
      </td>
   <td>렌디션이 캔버스 크기여야 하는지 여부를 선택합니다. True이면 렌디션이 캔버스 크기로 트리밍되고 False이면 렌디션 레이어 크기가 됩니다</td> 
    </tr>
    </tbody>
</table>

#### 이미지 자동 색상 교정(이전)

이 작업 모듈은 지정된 이미지를 자동으로 수정합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>색상 수정할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 색상을 수정할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다. 출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>파일을 변환할 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tr>
    </tbody>
</table>

#### 이미지 형식 변환(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [복합 모듈 만들기 또는 편집](#create-or-edit-a-composite) 모듈로 업데이트하세요.

이 작업 모듈은 파일을 JPEG, PNG, PSD 또는 TIFF으로 변환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>배경을 제거할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 배경을 제거할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>생성하려는 변환된 각 파일에 대해 항목 추가 를 클릭하고 나열된 대로 저장소, 위치 및 유형을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다. 출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>파일을 변환할 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tr>
    </tbody>
</table>

#### 마스크 만들기(기존)

이 작업 모듈은 제목 주위에 마스크가 적용된 PNG 파일을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>마스크를 만들 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 마스크를 만들 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>마스크 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 마스크 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. 출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 색상 공간]</p>
      </td>
   <td>출력 이미지에서 RGB 색상을 사용할지 RGBA 색상을 사용할지 선택합니다. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>마스크가 소프트(페더) 또는 바이너리여야 하는지 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>속도를 위해 최적화하려면 [성능]을 선택하고 대기 시간을 허용하려면 [일괄 처리]를 선택하십시오. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 사후 프로세스]</p>
      </td>
   <td>사후 처리를 사용할지 여부를 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 버전]</p>
      </td>
   <td>기본값은 4.0입니다.</td> 
    </tr> 
    </tbody>
</table>

#### 새 PSD 만들기(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [복합 모듈 만들기 또는 편집](#create-or-edit-a-composite) 모듈로 업데이트하세요.

이 작업 모듈은 선택적 레이어로 새 PSD을 만들고 렌디션을 생성하거나 PSD으로 저장합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Image size) Height]</p>
      </td>
      <td> 이미지의 높이를 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Image size) Width]</p>
      </td>
      <td> 이미지의 폭을 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL(옵션 &gt; 문서) 해상도]</p>
      </td>
   <td> 이미지의 해상도를 인치당 픽셀 단위로 입력하거나 매핑합니다. 72에서 300 사이여야 합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL(옵션 &gt; 문서) 모드]</p>
      </td>
   <td> 이미지 모드를 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL(옵션 &gt; 문서) 채우기]</p>
      </td>
   <td> 배경 레이어의 채우기를 투명, 흰색 또는 이미지의 배경색으로 할지 여부를 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL(옵션 &gt; 문서) 깊이]</p>
      </td>
   <td> 이미지의 비트 심도를 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Layers]</p>
      </td>
   <td> 추가할 각 레이어에 대해 항목 추가 를 클릭하고 레이어 세부 정보를 입력합니다. <p>레이어 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">PSD 만들기</a>를 참조하십시오.  </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Global font]</p>
      </td>
   <td> 문서의 전역 기본값으로 사용할 글꼴의 전체 포스트스크립트 이름을 입력합니다. 이 글꼴은 글꼴이 누락되고 해당 레이어에 대해 특별히 제공된 다른 글꼴이 없는 텍스트 레이어에 사용됩니다. 이 글꼴이 누락된 경우 누락된 글꼴 관리에 지정된 옵션이 적용됩니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> 문서에 필요한 각 글꼴에 대해 항목 추가 를 클릭하고 글꼴의 저장소 위치와 파일 위치를 입력합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) 누락된 글꼴 관리]</p>
      </td>
   <td> 문서에 누락된 글꼴이 하나 이상 있는 경우 수행할 작업을 선택합니다. <ul><li><code>fail</code>: 작업에 성공하지 못하고 상태가 실패 로 설정됩니다. 오류의 세부 정보는 상태의 세부 정보 섹션에 제공됩니다.</li><li><code>useDefault</code>: 작업이 성공하고 누락된 모든 글꼴이 ArialMT로 대체됩니다.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>만들려는 각 파일에 대해 항목 추가 를 클릭하고 나열된 대로 저장소, 위치 및 유형을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다. 출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>파일을 변환할 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Other fields]</td>
      <td>
        <p><p>출력 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync">PSD 만들기</a>를 참조하십시오.  </p>
      </td>
    </tr>
    </tbody>
</table>

#### 렌디션 만들기(기존)

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>편집할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 편집할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>만들려는 각 파일에 대해 항목 추가 를 클릭하고 나열된 대로 저장소, 위치, 유형 및 덮어쓰기 옵션을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) 파일 위치]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL(출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
      </tbody>
</table>

#### 텍스트 레이어 편집(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [Photoshop 작업, 스크립트 및 변형 실행](#execute-photoshop-actions-scripts-and-transformations) 모듈로 업데이트합니다.

이 작업 모듈은 Photoshop 파일의 텍스트 레이어를 편집합니다. 동일한 파일에 여러 레이어에 대한 별도의 편집 세부 정보를 입력할 수 있습니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 입력 파일 저장소]</td>
      <td>
        <p>편집할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 입력 파일 URL]</p>
      </td>
   <td> 편집할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 누락된 글꼴 관리]</td>
      <td>
        <p>문서에 누락된 글꼴이 하나 이상 있는 경우 수행할 작업을 선택합니다. 글꼴이 제공되지 않으면 모듈은 기본 글꼴을 사용합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>문서의 전역 기본값으로 사용할 글꼴의 전체 포스트스크립트 이름을 입력합니다. 이 글꼴은 글꼴이 누락되고 해당 레이어에 대해 특별히 제공된 다른 글꼴이 없는 텍스트 레이어에 사용됩니다. 이 글꼴이 누락된 경우 누락된 글꼴 관리에 지정된 옵션이 적용됩니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> 글꼴의 저장소 위치와 파일 위치를 입력합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레이어]</td>
   <td> <p>편집할 각 텍스트 레이어에 대해 <b>항목 추가</b>를 클릭하고 레이어 옵션을 입력합니다.<p>레이어 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">텍스트 편집</a>을 참조하십시오.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### 텍스트 레이어 2 편집(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [Photoshop 작업, 스크립트 및 변형 실행](#execute-photoshop-actions-scripts-and-transformations) 모듈로 업데이트합니다.

이 작업 모듈은 Photoshop 파일의 텍스트 레이어를 편집합니다.

여러 레이어를 편집하려면 [텍스트 레이어 편집](#edit-text-layers) 모듈을 사용하십시오.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 입력 파일 저장소]</td>
      <td>
        <p>편집할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 입력 파일 URL]</p>
      </td>
   <td> 편집할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 누락된 글꼴 관리]</td>
      <td>
        <p>문서에 누락된 글꼴이 하나 이상 있는 경우 수행할 작업을 선택합니다. 글꼴이 제공되지 않으면 모듈은 기본 글꼴을 사용합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>문서의 전역 기본값으로 사용할 글꼴의 전체 포스트스크립트 이름을 입력합니다. 이 글꼴은 글꼴이 누락되고 해당 레이어에 대해 특별히 제공된 다른 글꼴이 없는 텍스트 레이어에 사용됩니다. 이 글꼴이 누락된 경우 누락된 글꼴 관리에 지정된 옵션이 적용됩니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> 글꼴의 저장소 위치와 파일 위치를 입력합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 레이어]</td>
   <td> <p>레이어 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync">텍스트 레이어 편집</a>을 참조하십시오.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력 파일 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
  </tbody>
</table>


#### JSON(이전) 작업 실행

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [Photoshop 작업, 스크립트 및 변형 실행](#execute-photoshop-actions-scripts-and-transformations) 모듈로 업데이트합니다.

이 작업 모듈은 JSON 명령을 사용하여 Photoshop 작업을 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>편집할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 편집할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 작업 JSON]</td>
      <td>
        <p>수행할 작업에 대한 JSON 명령을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 글꼴 / 패턴 / 브러쉬 / 추가 이미지]</td>
      <td>
        <p>이 작업에 사용할 각 글꼴, 패턴, 브러시 또는 추가 이미지에 대해 항목 추가를 클릭하고 항목의 저장소 및 파일 위치를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> 사용할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>만들려는 각 파일에 대해 항목 추가 를 클릭하고 나열된 대로 저장소, 위치, 유형 및 덮어쓰기 옵션을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL(출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
      </tbody>
</table>

#### 깊이 흐림 효과 실행(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.

이 작업 모듈은 선택한 파일에 대해 깊이 흐림 효과를 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 입력 파일 저장소]</td>
      <td>
        <p>편집할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 입력 파일 URL]</p>
      </td>
   <td> 편집할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL(출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL 기타 필드]</td>
      <td>
        <p>다른 깊이 흐림 효과 옵션에 대한 자세한 내용은 Adobe Photoshop API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">깊이 흐림 효과 실행 </a>을(를) 참조하십시오.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Photoshop 작업 실행(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [Photoshop 작업, 스크립트 및 변형 실행](#execute-photoshop-actions-scripts-and-transformations) 모듈로 업데이트합니다.

이 작업 모듈은 선택한 이미지에 대해 Photoshop 작업을 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 입력 파일 저장소]</td>
      <td>
        <p>편집할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 입력 파일 URL]</p>
      </td>
   <td> 편집할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Actions 파일 저장소]</td>
      <td>
        <p>작업 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 작업 파일 URL]</p>
      </td>
   <td> 작업 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Action name]</p>
      </td>
   <td> 특정 작업만 실행하려는 경우 ActionSet에서 재생할 작업을 지정할 수 있습니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 글꼴 / 패턴 / 브러시 저장소]</td>
      <td>
        <p>사용할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> 사용할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL(출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL 기타 필드]</td>
      <td>
        <p>다른 깊이 흐림 효과 옵션에 대한 자세한 내용은 Adobe Photoshop API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">깊이 흐림 효과 실행 </a>을(를) 참조하십시오.</p>
      </td>
    </tr>
  </tbody>
</table>

#### 제품 자르기 실행(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [Photoshop 작업, 스크립트 및 변형 실행](#execute-photoshop-actions-scripts-and-transformations) 모듈로 업데이트합니다.

이 작업 모듈은 선택한 이미지에 대해 제품 자르기를 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 입력 파일 저장소]</td>
      <td>
        <p>자를 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 입력 파일 URL]</p>
      </td>
   <td> 자를 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Unit]</p>
      </td>
   <td> 높이 및 너비 조정을 픽셀 단위로 설명할지 아니면 백분율로 설명할지 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 너비]</p>
      </td>
   <td> 추가할 너비 패딩의 양을 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 높이]</p>
      </td>
   <td> 추가할 높이 패딩 양을 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL(출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL 기타 필드]</td>
      <td>
        <p>다른 깊이 흐림 효과 옵션에 대한 자세한 내용은 Adobe Photoshop API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync">깊이 흐림 효과 실행 </a>을(를) 참조하십시오.</p>
      </td>
    </tr>
  </tbody>
</table>

#### 레이어 정보 가져오기(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [매니페스트 생성](#generate-a-manifest) 모듈로 업데이트하세요.

이 작업 모듈은 지정된 PSD 파일에서 레이어 정보를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 입력 파일 저장소]</td>
      <td>
        <p>레이어 정보를 검색할 파일이 저장되어 있는 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 입력 파일 URL]</p>
      </td>
   <td> 레이어 정보를 검색할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 썸네일]</p>
      </td>
   <td> 썸네일을 표시할 파일 유형을 선택합니다. 축소판은 렌더링 가능한 레이어의 작은 미리 보기입니다.</td> 
    </tr>
  </tbody>
</table>

#### 사용자 정의 API 호출하기

이 작업 모듈은 Photoshop API에 대한 사용자 지정 호출을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p><code>https://image.adobe.io/pie/psdService</code>과 관련된 경로를 입력합니다. 예: <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
      </td>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 헤더]</td>
      <td>
        <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p>
        <p>예: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 본문]</td>
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### 스마트 오브젝트 바꾸기(기존)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [복합 모듈 만들기 또는 편집](#create-or-edit-a-composite) 모듈로 업데이트하세요.

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [복합 모듈 만들기 또는 편집](#create-or-edit-a-composite) 모듈로 업데이트하세요.

이 작업 모듈은 PSD 레이어 내의 스마트 오브젝트를 대체하고 새 렌디션을 생성합니다.

이 모듈은 스마트 오브젝트 API 버전 2를 사용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>스마트 개체가 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 스마트 오브젝트의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레이어]</p>
      </td>
   <td>스마트 오브젝트에 추가할 각 레이어에 대해 항목 추가 를 클릭하고 오브젝트의 이름 또는 ID, 스마트 오브젝트가 저장된 파일 서비스, 레이어의 URL 또는 경로를 입력합니다.<p>이 영역의 고급 설정에 대한 설명은 Photoshop API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">스마트 개체 바꾸기</a>를 참조하십시오 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 가져오는 동안 이미지 크기 조정]</p>
      </td>
   <td> 이미지 크기를 조정할지 여부를 선택합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>모듈에서 생성할 각 새 렌디션에 대해 항목 추가 를 클릭하고 다음 필드를 채웁니다. 최대 25개의 출력 파일을 가질 수 있습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
     </tbody>
</table>

#### 스마트 오브젝트 2(기존) 바꾸기

이 작업 모듈은 PSD 레이어 내의 스마트 오브젝트를 대체하고 새 렌디션을 생성합니다.

이 모듈에서는 기존 버전의 스마트 오브젝트를 사용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>스마트 개체가 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (입력) 파일 위치]</p>
      </td>
   <td> 스마트 오브젝트의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 레이어]</p>
      </td>
   <td>스마트 오브젝트에 추가할 각 레이어에 대해 항목 추가 를 클릭하고 오브젝트의 이름 또는 ID, 스마트 오브젝트가 저장된 파일 서비스, 레이어의 URL 또는 경로를 입력합니다.<p>이 영역의 고급 설정에 대한 설명은 Photoshop API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync">스마트 개체 바꾸기</a>를 참조하십시오 </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>모듈에서 생성할 각 새 렌디션에 대해 항목 추가 를 클릭하고 다음 필드를 채웁니다. 최대 25개의 출력 파일을 가질 수 있습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> 출력 파일의 폭(픽셀 단위)입니다. 모듈은 원래 종횡비를 유지합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tbody>
</table>

#### 이미지 크기 조정(이전)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [복합 모듈 만들기 또는 편집](#create-or-edit-a-composite) 모듈로 업데이트하세요.

이 작업은 동일한 종횡비를 사용하여 이미지 크기를 조정합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>크기를 조정할 파일이 저장된 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 파일 위치]</p>
      </td>
   <td> 크기를 조정할 파일의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>생성하려는 변환된 각 파일에 대해 항목 추가 를 클릭하고 나열된 대로 저장소, 위치 및 기타 옵션을 입력합니다.</p>
      </td>
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 너비]</p>
      </td>
   <td> 출력 파일의 폭(픽셀 단위)입니다. 모듈은 원래 종횡비를 유지합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 최대 너비]</p>
      </td>
   <td>너비가 0인 경우 크기를 얻기 위해 의 최대값을 제공할 수 있습니다. 최대 너비는 문서 너비보다 작을 때 우선합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Trim to canvas]</p>
      </td>
   <td>렌디션을 캔버스 크기로 트리밍하려면 [예]를 선택하고, 렌디션 레이어 크기로 만들려면 [아니요]를 선택합니다.</td> 
    </tr>
    </tbody>
</table>

#### 이미지에 워터마크 지정 (기존)

>[!NOTE]
>
>이 모듈은 사용 중단되었으며 2026년 7월 30일 이후에는 더 이상 작동하지 않습니다.
>이 모듈을 [복합 모듈 만들기 또는 편집](#create-or-edit-a-composite) 모듈로 업데이트하세요.

이 작업 모듈은 선택한 이미지에 워터마크를 추가합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 연결]</td>
      <td>[!DNL Adobe Photoshop]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 연결하기를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (기본 &gt; 입력) 저장소]</td>
      <td>
        <p>워터마크를 추가할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (기본 &gt; 입력) 파일 위치]</p>
      </td>
   <td> 워터마크를 추가할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (워터마크 &gt; 입력) 저장소]</td>
      <td>
        <p>추가하려는 워터마크가 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (워터마크 &gt; 입력) 저장소]</td>
      <td>
        <p>추가하려는 워터마크가 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark &gt; Bounds) Height]</p>
      </td>
   <td>원하는 워터마크 높이를 픽셀 단위로 입력하거나 매핑합니다.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark &gt; Bounds) Width]</p>
      </td>
   <td> 원하는 워터마크 폭을 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (워터마크 &gt; 경계) Left]</p>
      </td>
   <td> 워터마크가 적용되어야 하는 이미지 왼쪽에서 픽셀 단위의 거리를 입력하거나 매핑합니다.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark &gt; Bounds) Top]</p>
      </td>
   <td> 워터마크가 적용되어야 하는 이미지 상단과의 거리를 픽셀 단위로 입력하거나 매핑합니다.</td> 
    </tr>  
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>워터마크 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 워터마크 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. 출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>파일을 변환할 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> 출력 파일의 폭(픽셀 단위)입니다. 모듈은 원래 종횡비를 유지합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (출력) 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다. 이 방법은 Adobe 저장소의 파일에만 적용됩니다.</p>
      </td>
    </tbody>
</table>
