---
title: Adobe Photoshop 모듈
description: Adobe Photoshop 모듈을 사용하면 Adobe Photoshop 계정의 이벤트를 기반으로 Adobe Workfront Fusion 시나리오를 시작하고, 계약 및 기타 레코드를 생성, 읽기 또는 업데이트하고, 설정한 기준을 사용하여 레코드를 검색하고, 문서를 업로드할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
source-git-commit: a9e7053c443c9603ab3dc84c094196b7506cc7d0
workflow-type: tm+mt
source-wordcount: '4976'
ht-degree: 0%

---

# [!DNL Adobe Photoshop]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Adobe Photoshop]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.


시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

+++**이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.**

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 플랜*</td>
      <td>
        <p>[!UICONTROL Pro] 이상</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 라이센스*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스**</td>
      <td >
        <p>작업 자동화 및 통합을 위한 [!UICONTROL Workfront Fusion]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">제품</td>
      <td>조직에서 이 문서에 설명된 기능을 사용하려면 [!DNL Adobe Workfront Fusion]과(와) [!DNL Adobe Workfront]을(를) 구입해야 합니다.</td>
    </tr>
    </tr>
  </tbody>
</table>


&#42;플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

&#42;&#42;[!DNL Adobe Workfront Fusion]개 라이선스에 대한 자세한 내용은 [!DNL [Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)을(를) 참조하세요.

+++

## 전제 조건

[!DNL Adobe Photoshop] 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 [!DNL Adobe Photoshop] 계정이 있어야 합니다.
* Firefly Services 라이선스가 있어야 합니다.
* 클라이언트 ID와 클라이언트 암호가 있어야 합니다. Adobe Developer Console에서 가져올 수 있습니다.

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

## [!DNL Adobe Photoshop]에 연결 만들기

[!DNL Adobe Photoshop] 모듈에 대한 연결을 만들려면:

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>[!UICONTROL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 기술 계정 ID]</td>
        <td>[!DNL Adobe] [!UICONTROL 기술 계정 ID]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 조직 ID]</td>
        <td>[!DNL Adobe] [!UICONTROL 조직 ID]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 개인 키]</td>
        <td>
          <p>[!DNL Adobe Developer Console]에서 자격 증명을 만들 때 생성된 개인 키를 입력하십시오. </p>
          <p>개인 키 또는 인증서를 추출하려면 다음을 수행하십시오.</p>
          <ol>
            <li value="1">
              <p><b>[!UICONTROL Extract]</b>을(를) 클릭합니다.</p>
            </li>
            <li value="2">
              <p>추출 중인 파일 유형을 선택합니다.</p>
            </li>
            <li value="3">
              <p>개인 키 또는 인증서가 포함된 파일을 선택합니다.</p>
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

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## [!DNL Adobe Photoshop]개 모듈 및 해당 필드

[!DNL Adobe Photoshop] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Adobe Photoshop] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [PSD 편집 적용](#apply-psd-edits)
* [이미지 자동 색상 교정](#auto-color-correct-an-image)
* [이미지 형식 변환](#convert-image-format)
* [마스크 만들기](#create-a-mask)
* [새 PSD 만들기](#create-a-new-psd)
* [텍스트 레이어 편집](#edit-text-layers)
* [텍스트 레이어 편집(이전)](#edit-text-layers-legacy)
* [깊이 흐림 효과 실행](#execute-depth-blur)
* [Photoshop 작업 실행](#execute-photoshop-actions)
* [Photoshop 작업 실행(JSON)](#execute-photoshop-actions-json)
* [제품 자르기 실행](#execute-product-crop)
* [레이어 정보 가져오기](#get-layer-info)
* [사용자 지정 API 호출 만들기](#make-a-custom-api-call)
* [배경 제거](#remove-background)
* [스마트 오브젝트 바꾸기](#replace-a-smart-object)
* [스마트 오브젝트 바꾸기(기존)](#replace-a-smart-object-legacy)
* [이미지 크기 조정](#resize-an-image)
* [이미지에 워터마크 지정](#watermark-an-image)

### PSD 편집 적용

이 작업 모듈은 다양한 문서 및 레이어 수준 편집 사항을 적용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
   <td> 문서에 누락된 글꼴이 하나 이상 있는 경우 수행할 작업을 선택합니다. <ul><li><code>fail</code>: 작업에 성공하지 못하고 상태가 실패 로 설정됩니다. 오류의 세부 정보는 상태의 세부 정보 섹션에 제공됩니다.</li><li><code>useDefault</code>: 작업이 성공하지만 기본적으로 누락된 모든 글꼴은 ArialMT로 대체됩니다.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Layers]</p>
      </td>
   <td> 추가할 각 레이어에 대해 항목 추가 를 클릭하고 레이어 세부 정보를 입력합니다. <p>레이어 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_applyPsdEdits/">PSD 편집 적용</a>을 참조하십시오.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>생성할 변환된 각 파일에 대해 항목 추가 를 클릭하고 이 표에 나열된 대로 저장소, 위치 및 유형을 입력합니다.</p>
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
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>



### 이미지 자동 색상 교정

이 작업 모듈은 지정된 이미지를 자동으로 수정합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>


### 이미지 형식 변환

이 작업 모듈은 파일을 JPEG, PNG, PSD 또는 TIFF으로 변환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
        <p>생성할 변환된 각 파일에 대해 항목 추가 를 클릭하고 이 표에 나열된 대로 저장소, 위치 및 유형을 입력합니다.</p>
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
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>



### 마스크 만들기

이 작업 모듈은 제목 주위에 마스트가 적용된 PNG 파일을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 버전]</p>
      </td>
   <td>기본값은 4.0입니다.</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>

### 새 PSD 만들기

이 작업 모듈은 선택적 레이어로 새 PSD을 만들고 렌디션을 생성하거나 PSD으로 저장합니다.

이 모듈과 관련된 필드는 Adobe Photoshop 설명서에서 [새 PSD 만들기](https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/documentCreate)를 참조하십시오.

### 텍스트 레이어 편집

이 작업 모듈은 Photoshop 파일의 텍스트 레이어를 편집합니다. 동일한 파일에 여러 레이어에 대한 별도의 편집 세부 정보를 입력할 수 있습니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
      <td role="rowheader">[!UICONTROL 레이어]</td>
   <td> <p>편집할 각 텍스트 레이어에 대해 <b>항목 추가</b>를 클릭하고 레이어 옵션을 입력합니다.<p>레이어 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_editText/">텍스트 편집</a>을 참조하십시오.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력 파일 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 유형]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compression]</p>
      </td>
   <td> 출력 파일의 압축 레벨을 선택합니다. </td> 
    </tr>
  </tbody>
</table>



### 텍스트 레이어 편집(이전)

이 작업 모듈은 Photoshop 파일의 텍스트 레이어를 편집합니다.

여러 레이어를 편집하려면 [텍스트 레이어 편집](#edit-text-layers) 모듈을 사용하십시오.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
      <td role="rowheader">[!UICONTROL 레이어]</td>
   <td> <p>레이어 옵션에 대한 자세한 내용은 Adobe Photoshop 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_editText/">텍스트 레이어 편집</a>을 참조하십시오.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력 파일 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 유형]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compression]</p>
      </td>
   <td> 출력 파일의 압축 레벨을 선택합니다. </td> 
    </tr>
  </tbody>
</table>


### Photoshop 작업 실행(JSON)

이 작업 모듈은 JSON 명령을 사용하여 Photoshop 작업을 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
      <td role="rowheader">[!UICONTROL 출력 파일 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p><p>Fusion 내부 저장소를 선택하면 파일을 이후 모듈에서 사용할 수 있지만 시나리오 외부에서 파일을 사용할 수는 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다.  출력 스토리지에 대해 Fusion 내부 스토리지를 선택하지 않은 경우에만 필요합니다.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 유형]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compression]</p>
      </td>
   <td> 출력 파일의 압축 레벨을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 출력]</td>
      <td>
        <p>생성할 변환된 각 파일에 대해 항목 추가 를 클릭하고 이 표에 나열된 대로 저장소, 위치 및 유형을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>새 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (출력) 파일 위치]</p>
      </td>
   <td> 새 파일이 저장될 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
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
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
      </tbody>
</table>

### 깊이 흐림 효과 실행

이 작업 모듈은 선택한 파일에 대해 깊이 흐림 효과를 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
      <td role="rowheader">[!UICONTROL 출력 파일 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 유형]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 기타 필드]</td>
      <td>
        <p>다른 깊이 흐림 효과 옵션에 대한 자세한 내용은 Adobe Photoshop API 설명서의 <a href="https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/depthBlur">깊이 흐림 효과 실행 </a>을(를) 참조하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compression]</p>
      </td>
   <td> 출력 파일의 압축 레벨을 선택합니다. </td> 
    </tr>
  </tbody>
</table>

### Photoshop 작업 실행

이 작업 모듈은 선택한 이미지에 대해 Photoshop 작업을 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
      <td role="rowheader">[!UICONTROL 출력 파일 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 유형]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compression]</p>
      </td>
   <td> 출력 파일의 압축 레벨을 선택합니다. </td> 
    </tr>
  </tbody>
</table>

### 제품 자르기 실행

이 작업 모듈은 선택한 이미지에 대해 제품 자르기를 실행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
      <td role="rowheader">[!UICONTROL 출력 파일 저장소]</td>
      <td>
        <p>편집한 파일을 저장할 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 URL]</p>
      </td>
   <td> 편집된 파일이 저장되는 위치의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 출력 파일 유형]</p>
      </td>
   <td> 편집한 파일의 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 덮어쓰기]</td>
      <td>
        <p>새로 편집한 파일이 이미 있는 출력 파일을 덮어쓸지 여부를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Compression]</p>
      </td>
   <td> 출력 파일의 압축 레벨을 선택합니다. </td> 
    </tr>
  </tbody>
</table>

### 레이어 정보 가져오기

이 작업 모듈은 지정된 PSD 파일에서 레이어 정보를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
   <td> </td> 
    </tr>
  </tbody>
</table>

### 사용자 지정 API 호출 만들기

이 작업 모듈은 Photoshop API에 대한 사용자 지정 호출을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p><code>https://image.adobe.io/pie/psdService</code>과(와) 관련된 경로를 입력하십시오. 예: <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
      </td>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 인증 헤더를 자동으로 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### 배경 제거

이 작업 모듈은 이미지의 주요 주제를 식별하고 배경을 제거합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 버전]</p>
      </td>
   <td>기본값은 4.0입니다.</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>



### 스마트 오브젝트 바꾸기

이 작업 모듈은 PSD 레이어 내의 스마트 오브젝트를 대체하고 새 렌디션을 생성합니다.

이 모듈은 스마트 오브젝트 API 버전 2를 사용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
   <td>스마트 오브젝트에 추가할 각 레이어에 대해 항목 추가 를 클릭하고 오브젝트의 이름 또는 ID, 스마트 오브젝트가 저장된 파일 서비스, 레이어의 URL 또는 경로를 입력합니다.<p>이 영역의 고급 설정에 대한 설명은 Photoshop API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">스마트 개체 바꾸기</a>를 참조하십시오 </td> 
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
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>



### 스마트 오브젝트 바꾸기(기존)

이 작업 모듈은 PSD 레이어 내의 스마트 오브젝트를 대체하고 새 렌디션을 생성합니다.

이 모듈에서는 기존 버전의 스마트 오브젝트를 사용합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
   <td>스마트 오브젝트에 추가할 각 레이어에 대해 항목 추가 를 클릭하고 오브젝트의 이름 또는 ID, 스마트 오브젝트가 저장된 파일 서비스, 레이어의 URL 또는 경로를 입력합니다.<p>이 영역의 고급 설정에 대한 설명은 Photoshop API 설명서의 <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">스마트 개체 바꾸기</a>를 참조하십시오 </td> 
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
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>



### 이미지 크기 조정

이 작업은 동일한 종횡비를 사용하여 이미지 크기를 조정합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
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
        <p>생성할 변환된 각 파일에 대해 항목 추가 를 클릭하고 이 표에 나열된 대로 저장소, 위치 및 기타 옵션을 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 유형]</p>
      </td>
   <td>파일을 변환할 파일 유형을 선택합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 너비]</p>
      </td>
   <td>크기 조정된 이미지의 너비를 나타내는 숫자를 픽셀로 입력합니다. 종횡비는 그대로 유지됩니다.</td> 
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

### 이미지에 워터마크 지정

이 작업 모듈은 선택한 이미지에 워터마크를 추가합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Photoshop]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >[!DNL Adobe Photoshop]</a>에 대한 연결 만들기 를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (기본/입력) 저장소]</td>
      <td>
        <p>워터마크를 추가할 파일이 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (기본/입력) 파일 위치]</p>
      </td>
   <td> 워터마크를 추가할 파일의 URL 또는 경로를 입력하거나 매핑합니다. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (워터마크 / 입력) 저장소]</td>
      <td>
        <p>추가하려는 워터마크가 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (워터마크 / 입력) 저장소]</td>
      <td>
        <p>추가하려는 워터마크가 저장된 파일 서비스를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (워터마크 / 경계) 높이]</p>
      </td>
   <td>원하는 워터마크 높이를 픽셀 단위로 입력하거나 매핑합니다.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark / Bounds) Width]</p>
      </td>
   <td> 원하는 워터마크 폭을 픽셀 단위로 입력하거나 매핑합니다. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (워터마크 / 경계) 왼쪽]</p>
      </td>
   <td> 워터마크가 적용되어야 하는 이미지 왼쪽에서 픽셀 단위의 거리를 입력하거나 매핑합니다.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (워터마크 / 경계) 상위]</p>
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
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL 반환되는 최대 결과 수]</p>
      </td>
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
    </tr>
    </tbody>
</table>
