---
title: Adobe Substance 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Adobe Substance]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
source-git-commit: 2e44c89d487100b3245b40f6927185a0ff12ef2f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 32%

---

# [!DNL Adobe Substance]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Adobe Substance]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

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

[!DNL Adobe Substance] 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 [!DNL Adobe Substance] 계정이 있어야 합니다.



## [!DNL Adobe Substance] 모듈 및 해당 필드

[!DNL Adobe Substance] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 수준과 같은 요인에 따라 추가적인 [!DNL Adobe Substance] 필드가 표시될 수 있습니다. 모듈에서 필드 이름 옆에 있는 별표는 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [합성](#composites)
* [장면](#scenes)
* [Spaces](#spaces)

### 합성

#### 3D 오브젝트 합성 생성

이 작업 모듈은 선택한 대표 에셋을 포함하는 3D 합성용 콘텐츠를 생성합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Adobe Substance] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td>원하는 대로 다른 필드를 구성합니다. 필드에 대한 자세한 내용은 <a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose">Adobe Substance API 설명서</a>를 참조하십시오.</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### 장면

* [3D 파일 변환](#convert-3d-files)
* [3D 장면 만들기](#create-3d-scene)
* [3D 장면 설명](#describe-3d-scene)
* [3D 개체 렌더링](#render-3d-object)
* [3D 개체 렌더링(기본 버전)](#render-3d-object-basic-version)

#### 3D 파일 변환

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Adobe Substance] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">형식</td> 
   <td>파일을 변환할 형식을 선택합니다.</td> 
  </tr> 
<tr> 
   <td role="rowheader">모델 진입점</td> 
   <td>변환은 일반적으로 유효한 3D 모델로 간주되는 첫 번째 파일을 사용합니다. 여러 옵션이 있는 경우 명확히 하려면 이 진입점을 정의하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">소스</td> 
   <td>변환할 각 파일에 대해 <b> 항목 추가</b>를 클릭하고 파일 정보를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D 장면 만들기

이 작업 모듈은 지정한 자산을 사용하여 장면을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Adobe Substance] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <td role="rowheader">인코딩</td> 
   <td>장면의 파일 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">파일 기본 이름</td> 
   <td>출력 파일의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">기타 필드</td> 
   <td>원하는 대로 다른 필드를 구성합니다. 필드에 대한 자세한 내용은 <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble">Adobe Substance API 설명서</a>를 참조하십시오.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">소스</td> 
   <td>사용하려는 각 파일에 대해 <b> 항목 추가</b>를 클릭하고 파일 정보를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D 장면 설명

이 작업 모듈은 3D 장면 콘텐츠에 대한 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Adobe Substance] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <td role="rowheader">장면 파일</td> 
   <td>설명하려는 장면 파일에 경로를 입력하거나 매핑합니다.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">소스</td> 
   <td>설명하려는 각 파일에 대해 <b> 항목 추가</b>를 클릭하고 파일 정보를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D 개체 렌더링

이 작업 모듈은 장면의 이미지를 렌더링합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Adobe Substance] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
   <td role="rowheader">기타 필드</td> 
   <td>원하는 대로 다른 필드를 구성합니다. 필드에 대한 자세한 내용은 <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render">Adobe Substance API 설명서</a>를 참조하십시오.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">소스</td> 
   <td>사용하려는 각 파일에 대해 <b> 항목 추가</b>를 클릭하고 파일 정보를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D 개체 렌더링(기본 버전)

이 작업 모듈에서는 장면의 이미지를 렌더링하지만 Render 3D 개체 모듈보다 옵션이 적습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Adobe Substance] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
   <td role="rowheader">기타 필드</td> 
   <td>원하는 대로 다른 필드를 구성합니다. 필드에 대한 자세한 내용은 <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render-basic">Adobe Substance API 설명서</a>를 참조하십시오.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">소스</td> 
   <td>사용하려는 각 파일에 대해 <b> 항목 추가</b>를 클릭하고 파일 정보를 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

### Spaces

#### 공간 만들기

이 작업 모듈에서는 파일을 업로드하고 임시로 저장할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Adobe Substance] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
   <td role="rowheader">파일 이름</td> 
   <td>업로드 중인 파일의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">파일 데이터</td> 
   <td>파일의 이진 데이터를 입력하거나 매핑합니다.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">이름</td> 
   <td>다중 부분 양식 값의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>
