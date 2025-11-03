---
title: Adobe Firefly 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Adobe Firefly]을(를) 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '2488'
ht-degree: 0%

---

# [!DNL Adobe Firefly]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Adobe Firefly]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

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
   <p>작업 기반: Workfront Fusion 라이센스 요구 사항 없음</p>
   <p>커넥터 기반(레거시): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 조직에서 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Adobe Firefly] 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 [!DNL Adobe Firefly] 계정이 있어야 합니다.

## Adobe Firefly API 정보

Adobe Firefly 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Adobe Firefly]에 연결 만들기

[!DNL Adobe Firefly] 모듈에 대한 연결을 만들려면:

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
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>[!UICONTROL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다.</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭하세요.

## [!DNL Adobe Firefly]개 모듈 및 해당 필드

[!DNL Adobe Firefly] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Adobe Firefly] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 이미지 확장

이 작업 모듈은 선택적으로 사용자가 제공하는 프롬프트의 콘텐츠로 이미지를 확장합니다.

이 모듈은 Firefly API V3 Async에서 작동합니다. 이 모듈의 이전 버전은 더 이상 사용되지 않으며 곧 제거될 예정입니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프롬프트]</td> 
   <td>이미지를 확장할 내용에 대한 프롬프트를 입력하거나 매핑합니다. 프롬프트가 제공되지 않으면 이미지가 원본 이미지와 일치하는 콘텐츠로 확장됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변형 수]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 확장된 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source]</td> 
   <td>소스 파일을 제공하는 방법을 선택하십시오.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 확장된 이미지 형식]</td> 
   <td>확장된 이미지를 저장할 파일 형식을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand by]</td> 
   <td>  <p>이미지 배치를 사용하여 이미지를 확장할지 또는 마스크를 사용하여 이미지를 확장할지 선택합니다.</p> 
   <ul>
   <li><b>배치</b><p>가로 및 세로 정렬, 가장자리에서 가져온 이미지의 삽입 위치를 입력합니다.</p></li>
   <li><b>마스크</b><p>마스크에 대한 소스 파일을 선택하고 마스크를 반전할지 여부를 선택합니다.</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>확장된 이미지를 표시할 높이와 너비를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>모듈에서 생성할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 정수를 입력하거나 매핑합니다. 다른 이미지 모듈 확장에서 이와 동일한 시드를 사용하여 스타일이 다른 유사한 이미지를 생성할 수 있습니다. 추가하는 시드 수는 변형 수 필드와 같아야 합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 이미지 확장(삭제 예정)

이 모듈은 더 이상 사용되지 않으며 곧 제거될 예정입니다. 대신 이미지 모듈 확장 을 사용하십시오.

### 이미지 채우기

이 작업 모듈은 이미지의 마스킹된 영역을 채우며, 원할 경우 제공하는 프롬프트의 콘텐츠로 채웁니다.

이 모듈은 Firefly API V3 Async에서 작동합니다. 이 모듈의 이전 버전은 더 이상 사용되지 않으며 곧 제거될 예정입니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이미지 &gt; Source]</td> 
   <td>이미지 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 마스크 &gt; Source]</td> 
   <td>마스크 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프롬프트]</td> 
   <td>이미지를 채울 콘텐츠에 대한 프롬프트를 입력하거나 매핑합니다. 프롬프트가 제공되지 않으면 이미지는 원본 이미지와 일치하는 콘텐츠로 채워집니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변형 수]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 채워진 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채워진 이미지 형식]</td> 
   <td>채워진 이미지를 저장할 파일 형식을 선택합니다.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>모듈에서 생성할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 정수를 입력하거나 매핑합니다. 다른 이미지 모듈 확장에서 이와 동일한 시드를 사용하여 스타일이 다른 유사한 이미지를 생성할 수 있습니다. 추가하는 시드 수는 변형 수 필드와 같아야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>채워진 이미지를 표시할 크기를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>로케일이 제공되면 모듈은 지정된 로케일과 더 관련이 있는 콘텐츠를 생성합니다. <p>로케일은 ISO 639-1 언어 코드 및 ISO 3166-1 지역에서 제공해야 합니다.</p><p> 예: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### 이미지 채우기(삭제 예정)

이 모듈은 더 이상 사용되지 않으며 곧 제거될 예정입니다. 대신 이미지 채우기 모듈을 사용하십시오.

### 이미지 생성

이 작업 모듈은 사용자가 제공한 프롬프트를 기반으로 및 이미지를 생성합니다. 선택적 참조 이미지를 제공할 수도 있으며, 생성된 이미지는 참조 이미지의 스타일과 일치합니다.

이 모듈은 Firefly API V3 Async에서 작동합니다. 이 모듈의 이전 버전은 더 이상 사용되지 않으며 곧 제거될 예정입니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프롬프트]</td> 
   <td>생성할 이미지에 대한 프롬프트를 입력하거나 매핑합니다. 프롬프트에 자세히 설명되어 있으면 이미지에 나타나는 내용을 보다 세밀하게 제어할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델 버전]</td> 
   <td>이미지를 생성하는 데 사용할 Firefly 모델 버전을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변형 수]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 생성된 이미지 형식]</td> 
   <td>확장된 이미지를 저장할 파일 형식을 선택합니다. 기본값을 선택하면 참조 이미지가 제공되지 않는 경우 파일 형식은 JPEG이 됩니다. 기준 이미지가 제공된 경우, 생성된 이미지의 파일 포맷은 기준 이미지와 동일할 것이다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구조 &gt; 이미지 참조]</td> 
    <td>새 이미지 구조에 대한 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구조 &gt; 강도]</td> 
    <td>Firefly이 소스 이미지의 구조를 얼마나 엄격하게 따르는지 제어하려면 0에서 100 사이의 숫자를 입력합니다. 숫자가 높을수록 Firefly이 이미지를 더 엄격하게 따른다는 것을 의미합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스타일 &gt; 이미지 참조]</td> 
    <td>새 이미지 스타일에 대한 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구조 &gt; 강도]</td> 
    <td>Firefly이 소스 이미지의 스타일을 얼마나 엄격하게 따르는지 제어하려면 0에서 100 사이의 숫자를 입력합니다. 숫자가 높을수록 Firefly이 이미지를 더 엄격하게 따른다는 것을 의미합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스타일 &gt; 사전 설정]</td> 
   <td>사전 설정 스타일을 사용하려면 항목 추가 를 클릭하고 사용할 스타일을 입력하거나 매핑합니다.<p>사전 설정된 스타일 목록을 보려면 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >이미지 모델 스타일</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 음성 프롬프트]</td> 
   <td>생성된 콘텐츠에서 피하려는 단어를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content 클래스]</td> 
   <td>생성된 이미지를 사진과 같은 이미지로 할지 또는 생성된 아트와 같은 이미지로 할지 선택합니다. <ul><li><b>사진</b><p>조리개, 셔터 속도(초) 및 시야(밀리미터)의 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시드]</td> 
   <td>모듈에서 생성할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 정수를 입력하거나 매핑합니다. 다른 이미지 모듈 확장에서 이와 동일한 시드를 사용하여 스타일이 다른 유사한 이미지를 생성할 수 있습니다. 추가하는 시드 수는 변형 수 필드와 같아야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>생성된 이미지를 표시할 크기를 선택합니다.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 시각적 강도]</td> 
   <td>사진의 기존 시각적 특성의 전체 강도를 나타내는 정수를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>로케일이 제공되면 모듈은 지정된 로케일과 더 관련이 있는 콘텐츠를 생성합니다. <p>로케일은 ISO 639-1 언어 코드 및 ISO 3166-1 지역에서 제공해야 합니다.</p><p> 예: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>모든 방향에서 무한히 반복할 수 있는 이미지를 생성하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 이미지 생성(삭제 예정)

이 모듈은 더 이상 사용되지 않으며 곧 제거될 예정입니다. 대신 이미지 생성 모듈을 사용하십시오.

### 오브젝트 합성 생성

이 작업 모듈은 Firefly에서 생성된 이미지를 결합하여 이미지 합성을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프롬프트]</td> 
   <td>생성할 이미지에 대한 프롬프트를 입력하거나 매핑합니다. 프롬프트에 자세히 설명되어 있으면 이미지에 나타나는 내용을 보다 세밀하게 제어할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변형 수]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content 클래스]</td> 
   <td>생성된 이미지를 사진과 비슷하게 할지 아니면 아트와 비슷하게 할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이미지 &gt; Source]</td> 
    <td>새 이미지 구조에 대한 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 생성된 이미지 형식]</td> 
   <td>확장된 이미지를 저장할 파일 형식을 선택합니다. 기본값을 선택하면 참조 이미지가 제공되지 않는 경우 파일 형식은 JPEG이 됩니다. 기준 이미지가 제공된 경우, 생성된 이미지의 파일 포맷은 기준 이미지와 동일할 것이다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스타일 &gt; 이미지 참조]</td> 
    <td>새 이미지 스타일에 대한 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구조 &gt; 강도]</td> 
    <td>Firefly이 소스 이미지의 스타일을 얼마나 엄격하게 따르는지 제어하려면 0에서 100 사이의 숫자를 입력합니다. 숫자가 높을수록 Firefly이 이미지를 더 엄격하게 따른다는 것을 의미합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스타일 &gt; 사전 설정]</td> 
   <td>사전 설정 스타일을 사용하려면 항목 추가 를 클릭하고 사용할 스타일을 입력하거나 매핑합니다.<p>사전 설정된 스타일 목록을 보려면 Adobe 개발자 설명서에서 <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >이미지 모델 스타일</a>을 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>생성된 합성을 적용할 크기를 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>

### 유사 이미지 생성

이 작업 모듈은 지정한 소스 이미지와 유사한 이미지를 생성합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Campaign]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 변형 수]</td> 
   <td>1-4 사이의 숫자를 입력하십시오. 모듈은 이 수의 이미지 변형을 생성합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 모델 버전]</td> 
   <td>이미지를 생성하는 데 사용할 Firefly 모델 버전을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 생성된 이미지 형식]</td> 
   <td>확장된 이미지를 저장할 파일 형식을 선택합니다. 기본값을 선택하면 참조 이미지가 제공되지 않는 경우 파일 형식은 JPEG이 됩니다. 기준 이미지가 제공된 경우, 생성된 이미지의 파일 포맷은 기준 이미지와 동일할 것이다.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 이미지 &gt; Source]</td> 
    <td>새 이미지 구조에 대한 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 스타일 &gt; 이미지 참조]</td> 
    <td>새 이미지 스타일에 대한 소스 파일을 제공하는 방법을 선택합니다.<ul><li><p><b>파일</b></p><p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 참조 이미지 파일 이름과 참조 이미지 파일을 매핑합니다.</p></li><li><p><b>사전 서명된 URL</b></p><p>소스 이미지의 URL을 입력하거나 매핑합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>생성된 합성을 적용할 크기를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>모듈에서 생성할 각 이미지에 대해 <b>항목 추가</b>를 클릭하고 정수를 입력하거나 매핑합니다. 다른 이미지 모듈 확장에서 이와 동일한 시드를 사용하여 스타일이 다른 유사한 이미지를 생성할 수 있습니다. 추가하는 시드 수는 변형 수 필드와 같아야 합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>모든 방향에서 무한히 반복할 수 있는 이미지를 생성하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
 </tbody> 
</table>


### 사용자 지정 API 호출 만들기

이 작업 모듈은 Firefly API에 대한 사용자 지정 호출을 만듭니다.

사용 가능한 특정 API에 대해서는 Adobe Developer 설명서에서 [Adobe Firefly API](https://developer.adobe.com/firefly-services/docs/firefly-api/)를 참조하십시오.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>[!DNL Adobe Firefly]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >[!DNL Adobe Firefly]</a>에 대한 연결 만들기 를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p><code>https://firefly-api.adobe.io/</code>과(와) 관련된 경로를 입력하십시오.</p>
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
        <p>Workfront Fusion은 인증 헤더를 자동으로 추가합니다.</p>
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

