---
title: CloudConverter 모듈
description: CloudConverter 모듈
author: Becky
feature: Workfront Fusion
exl-id: 52c4d18a-8bee-44d6-9a2c-cc9e157e1dde
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '2498'
ht-degree: 0%

---

# [!DNL CloudConvert]개 모듈

Adobe Workfront Fusion 시나리오에서는 CloudConvert를 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다. [!DNL CloudConvert] 모듈을 사용하면 [!DNL CloudConvert] 계정에서 작업, 작업을 모니터링하고 관리하며 파일을 가져오고 내보낼 수 있습니다.

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

## CloudConvert API 정보

CloudConvert 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://api.cloudconvert.com/v2/</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v2.14.22</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL CloudConvert]을(를) [!DNL Workfront Fusion]에 연결 {#connect-cloudconvert-to-workfront-fusion}

[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하려면 [!DNL CloudConvert] 계정에서 API 키를 가져와야 합니다.

1. [!DNL CloudConvert] 계정에 로그인하고 [!UICONTROL Dashboard]을(를) 엽니다.
1. **[!UICONTROL Authorization]>[!UICONTROL API Keys]** 섹션을 엽니다.
1. **[!UICONTROL Create New API key]**&#x200B;을(를) 클릭합니다.
1. API 키의 이름을 입력하고 사용할 범위를 사용하도록 설정한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.
1. 제공된 토큰을 복사하여 안전한 장소에 보관합니다.
1. [!DNL Workfront Fusion]에서 시나리오 만들기를 시작하고 [!DNL CloudConvert] 모듈의 **[!UICONTROL Create a connection]** 대화 상자를 엽니다.

   지침은 [시나리오 만들기 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)를 참조하십시오.

1. 5단계에서 저장한 토큰을 입력한 다음 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하여 연결을 설정합니다.

## [!DNL CloudConvert]개 모듈 및 해당 필드 {#cloudconvert-modules-and-their-fields}

[!DNL CloudConvert] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL CloudConvert] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [일반 작업](#common-tasks)
* [작업](#jobs)
* [작업](#tasks)
* [기타](#other)

### 일반 작업

* [웹 사이트 캡처](#capture-a-website)
* [[!UICONTROL Convert a file]](#convert-a-file)
* [보관 만들기](#create-an-archive)
* [파일 병합](#merge-files)
* [파일 최적화](#optimize-a-file)

#### [!UICONTROL Capture a Website]

이 작업 모듈은 지정된 웹 사이트를 캡처하여 PDF, JPG 또는 PNG 형식으로 저장합니다.

웹 사이트의 URL과 정보를 저장할 위치와 같은 기타 정보를 지정합니다.

모듈은 파일의 ID와 연결된 필드, 그리고 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>캡처할 웹 사이트의 URL을 입력합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>캡처된 웹 사이트를 PNG, JPG 또는 PDF 형식으로 저장할지 여부를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td>대상 출력 파일의 파일 이름(확장명 포함)을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>(선택 사항) 요청 헤더를 정의합니다. </p> <p>이 기능은 예를 들어 지정된 URL에 인증이 필요한 경우 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>변환 및 엔진별 옵션을 지정합니다. 사용 가능한 옵션을 보려면 <code>input_format</code> 및 <code>output_format</code>에 대한 <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API</a> 설명서를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>모듈의 출력에 파일 데이터를 포함하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Convert a file]

파일을 선택한 출력 형식으로 변환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input file]</td> 
   <td>[!DNL Workfront Fusion]을(를) 사용하여 파일을 업로드할지 또는 파일을 업로드할 URL을 제공할지 선택하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a File from URL]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>변환할 파일의 URL을 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Headers]</strong></p> <p>요청 헤더를 정의합니다(선택 사항). 이 기능은 예를 들어 지정된 URL에 인증이 필요한 경우 유용합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format]</td> 
   <td>변환할 파일의 입력 형식을 지정할지 여부를 선택합니다. 지정하지 않으면 입력 파일의 확장자가 입력 형식으로 사용됩니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Input Format]</td> 
   <td>파일의 현재 형식을 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td>파일을 변환할 대상 파일 형식을 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL File Name]</td> 
   <td>대상 출력 파일의 파일 이름(확장명 포함)을 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Conversion and engine specific options] </p> </td> 
   <td>변환 및 엔진별 옵션을 지정합니다. 사용 가능한 옵션을 보려면 <code>input_format</code> 및 <code>output_format</code>에 대한 <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API</a> 설명서를 참조하십시오.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Download a file] </td> 
   <td> <p>모듈의 출력에 파일 데이터를 포함하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an Archive]

ZIP, RAR, 7Z, TAR, TAR.GZ 또는 TAR.BZ2 아카이브에 하나 이상의 파일을 추가할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>아카이브에 추가할 파일을 지정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>보관하려는 파일의 URL을 입력합니다.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>요청 헤더를 정의합니다(선택 사항). 이 기능은 예를 들어 지정된 URL에 인증이 필요한 경우 유용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> 보관된 파일의 대상 형식을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> 대상 출력 파일의 파일 이름(확장명 포함)을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>변환 및 엔진별 옵션을 지정합니다. 사용 가능한 옵션을 보려면 <code>input_format</code> 및 <code>output_format</code>에 대한 <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API</a> 설명서를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>모듈의 출력에 파일 데이터를 포함하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Merge Files]

두 개 이상의 파일을 하나의 PDF에 병합합니다. 입력 파일이 PDF이 아닌 경우 자동으로 PDF으로 변환됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Input Files]</p> </td> 
   <td> <p>병합할 파일을 지정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a file from URL]</p> </td> 
   <td> <p><strong>[!UICONTROL URL]</strong> </p> <p>보관하려는 파일의 URL을 입력합니다.</p> <p><strong>[!UICONTROL Headers]</strong> </p> <p>요청 헤더를 정의합니다(선택 사항). 이 기능은 예를 들어 지정된 URL에 인증이 필요한 경우 유용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p> 병합된 파일의 대상 형식을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p> 대상 출력 파일의 파일 이름(확장명 포함)을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options] </td> 
   <td> <p>변환 및 엔진별 옵션을 지정합니다. 사용 가능한 옵션을 보려면 <code>input_format</code> 및 <code>output_format</code>에 대한 <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API</a> 설명서를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a File]</td> 
   <td> <p>모듈의 출력에 파일 데이터를 포함하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Optimize a File]

이 작업 모듈은 파일을 PDF, PNG 또는 JPG 형식으로 최적화 및 압축합니다.

최적화하고 저장하기 위한 파일 및 매개변수를 지정합니다.

모듈은 파일의 ID와 연결된 필드, 그리고 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input File]</td> 
   <td>Workfront Fusion을 사용하여 파일을 업로드할지 또는 파일을 업로드할 URL을 제공할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Upload a File]</p> </td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Import a file from URL] </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: 변환할 파일의 URL을 입력합니다.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (선택 사항) 요청 헤더를 정의합니다. 이 기능은 예를 들어 지정된 URL에 인증이 필요한 경우 유용합니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optimization for] </td> 
   <td> <p>특정 대상 요구 사항에 대한 최적화 프로필을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Web]</strong>: 웹에 대한 최적화(기본값)</p> 
      <ul> 
       <li>웹에 대한 중복되고 불필요한 데이터 제거</li> 
       <li>이미지를 다운 샘플링, 클립 및 지능적으로 압축</li> 
       <li>글꼴 병합 및 하위 집합</li> 
       <li>색상을 RGB으로 변환</li> 
      </ul> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Print]</strong>: 인쇄 최적화</p> 
      <ul> 
       <li> <p>인쇄를 위해 중복되고 불필요한 데이터 제거</p> </li> 
       <li> <p>이미지를 다운 샘플링, 클립 및 지능적으로 압축</p> </li> 
       <li> <p>글꼴 병합 및 하위 집합</p> </li> 
       <li> <p>색상을 CMYK로 변환</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Archive]</strong>: 보관 목적으로 최적화</p> 
      <ul> 
       <li> <p>아카이빙을 위해 중복되고 불필요한 데이터 제거</p> </li> 
       <li> <p>이미지를 지능적으로 압축</p> </li> 
       <li> <p>글꼴 병합 및 하위 집합</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Scanned images]</strong>: 스캔한 이미지에 대한 최적화</p> 
      <ul> 
       <li> <p>주로 래스터 이미지로 구성된 PDF에 최적화된 프로필</p> </li> 
       <li> <p>시각적 품질을 크게 저하시키지 않고 이미지 압축</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL maximal size reduction]</strong>: 최대 크기 감소를 위한 최적화</p> 
      <ul> 
       <li> <p>가능한 최대 압축 사용</p> </li> 
       <li> <p>시각적 품질을 저하시킬 수 있음</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input format] </td> 
   <td>최적화할 입력 파일의 형식을 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td> <p>대상 출력 파일의 파일 이름(확장명 포함)을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Conversion and engine specific options]</td> 
   <td> <p>변환 및 엔진별 옵션을 지정합니다. 사용 가능한 옵션을 보려면 <code>input_format</code> 및 <code>output_format</code>에 대한 <a href="https://cloudconvert.com/api/v2/convert#convert-tasks">[!DNL CloudConvert] API</a> 설명서를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a file]</td> 
   <td> <p>모듈의 출력에 파일 데이터를 포함하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 작업

* [[!UICONTROL Create a Job (advanced)]](#create-a-job-advanced)
* [[!UICONTROL New Job Event]](#new-job-event)
* [[!UICONTROL List Jobs]](#list-jobs)
* [[!UICONTROL Get a Job]](#get-a-job)
* [[!UICONTROL Delete a Job]](#delete-a-job)

#### [!UICONTROL Create a Job (advanced)]

이 모듈은 작업을 생성합니다. 작업은 [!UICONTROL Name] 필드에서 식별되고 [!UICONTROL Input] 필드를 사용하여 서로 연결된 하나 또는 여러 작업일 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input Files]</td> 
   <td> <p>[!DNL Workfront Fusion]을(를) 사용하여 파일을 업로드할지 또는 파일을 업로드할 URL을 제공할지 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a File]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Import a File from URL]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL URL]</strong>: 처리할 파일의 URL을 입력합니다.</li> 
     <li><strong>[!UICONTROL Headers]</strong>: (선택 사항) 요청 헤더를 정의합니다. 이 기능은 예를 들어 지정된 URL에 인증이 필요한 경우 유용합니다.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Tasks]</p> </td> 
   <td> <p>작업 내에서 수행될 작업을 추가합니다.</p> <p>해당 섹션에서 작업 필드에 대한 설명을 확인하십시오.</p> 
    <ul> 
     <li><a href="#convert-a-file" class="MCXref xref">[!UICONTROL Convert a file]</a> </li> 
     <li><a href="#capture-a-website" class="MCXref xref">[!UICONTROL Capture a Websit]e</a> </li> 
     <li><a href="#optimize-a-file" class="MCXref xref">[!UICONTROL Optimize a File]</a> </li> 
     <li><a href="#create-an-archive" class="MCXref xref">[!UICONTROL Create an Archive]</a> </li> 
     <li><a href="#merge-files" class="MCXref xref">[!UICONTROL Merge Files]</a> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL Execute a Command]</strong> </p> <p>명령 실행에 대한 자세한 내용은 <a href="https://cloudconvert.com/api/v2/command#command-tasks">[!DNL CloudConvert] API 설명서</a>를 참조하십시오.</p> </li> 
     <li> <p><strong>[!UICONTROL Export a File to Temporary URL]</strong> </p> <p> 작업 이름 및 입력 작업 이름(예: 전환)을 지정합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag] </td> 
   <td> <p>태그를 입력합니다. 태그는 작업을 식별하는 임의의 문자열입니다. 효과가 없으며 작업을 ID와 연결하는 데 사용할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Job]

이 모듈은 모든 작업 및 데이터를 포함한 작업을 삭제합니다.

>[!NOTE]
>
>작업이 종료된 후 24시간 후에 자동으로 삭제됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>삭제할 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Job]

이 모듈은 작업 세부 정보를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td> <p>세부 정보를 검색할 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Jobs]

이 모듈은 계정에서 실행된 모든 작업을 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>반환된 작업을 필터링할 작업 상태를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>한 실행 주기 동안 Workfront Fusion 2.0이 반환할 작업 수를 설정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL New Job Event]

계정 또는 작업의 작업이 생성되거나 완료되거나 실패하면 트리거됩니다.

>[!NOTE]
>
>* [!UICONTROL Create a Job (advanced)] 모듈에서 만든 작업은 *여러* 작업으로 구성됩니다.
>* *개인* 작업이 만들어지거나 완료되거나 실패한 경우에도 [!UICONTROL New Job Event] 트리거가 트리거됩니다.
>

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhhook name]</td> 
   <td>웹후크 이름을 입력합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format] </td> 
   <td>캡처된 웹 사이트를 PNG, JPG 또는 PDF 형식으로 저장할지 여부를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event]</td> 
   <td>작업 또는 작업이 생성, 완료 또는 실패할 때 모듈을 트리거할지 여부를 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Array Aggregator를 사용하여 작업하는 경우(예: 변환할 다양한 형식의 파일이 있는 경우) [!UICONTROL Add a task] 대화 상자의 **[!UICONTROL I don't know the input format]** 옵션을 사용합니다. 그렇지 않으면 오류가 반환됩니다.
>* 작업 내 작업 연결(이름 > 입력, 이름 > 입력 등):
>
>  ![작업 간 이름 연결](/help/workfront-fusion/references/apps-and-modules/assets/linking-name-across-jobs-350x808.png)>

### 작업

* [[!UICONTROL Get a Task]](#get-a-task)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL List Tasks]](#list-tasks)
* [[!UICONTROL Retry a Task]](#retry-a-task)
* [[!UICONTROL Cancel a Task]](#cancel-a-task)
* [[!UICONTROL Delete a Task]](#delete-a-task)

#### [!UICONTROL Cancel a Task]

이 모듈은 대기 또는 처리 상태의 작업을 취소합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> 취소할 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Task]

모든 데이터를 포함한 작업을 삭제합니다.

>[!NOTE]
>
>작업이 종료된 후 24시간 후에 자동으로 삭제됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> 삭제할 작업의 ID를 입력(매핑)합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

이 모듈은 지정된 작업에서 파일 이름 및 파일 데이터를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> 파일을 다운로드할 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Task]

이 모듈은 작업 세부 정보를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p>세부 정보를 검색할 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Tasks]

이 모듈은 필터 설정을 기반으로 계정의 모든 작업을 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status] </td> 
   <td> <p>반환된 작업을 필터링할 작업 상태를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID] </td> 
   <td> <p>작업 ID를 입력하거나 매핑하여 지정된 작업 내의 작업만 반환합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>작업 유형을 입력하여 지정된 작업이 있는 작업만 반환합니다. </p> <p>참고: 작업을 검색하려면 [!UICONTROL List Possible Operations] 모듈을 사용하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Retry a Task]

이 모듈은 다른 작업의 설정(페이로드)을 기반으로 새 작업을 만듭니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p> 새 작업을 만들 작업의 ID를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 기타

* [[!UICONTROL Get My Info]](#get-my-info)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Get My Info]

현재 사용자에 대한 인증된 계정 세부 정보를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL CloudConvert] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-cloudconvert-to-workfront-fusion" class="MCXref xref">[!DNL CloudConvert]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

사용자 지정 API 호출을 수행할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[Fusion App] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion에 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p><code>https://api.cloudconvert.com/</code>과(와) 관련된 경로를 입력하십시오. For example: <code>/v2/tasks</code></p> <p>사용 가능한 끝점 목록은 <a href="https://cloudconvert.com/api/v2">[!DNL CloudConvert] API v2 설명서</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion 2.0은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다. JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 넣으십시오.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

**예:** 목록 작업

다음 API 호출은 CloudFront 계정의 모든 작업을 반환합니다.

URL: `/v2/tasks`

메서드: `GET`

![API 예제 입력](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-input.png)

검색 일치 항목은 모듈의 출력에서 [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL data] 아래에 있습니다.

이 예에서는 6개의 작업이 반환되었습니다.

![API 예제 출력](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-api-example-output.png)

## 문제 해결 {#troubleshooting}

가능한 오류 및 해결 방법에 대해서는 다음 표를 참조하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> <p>오류</p> </th> 
   <th>다음 단계</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL The output file size exceeds the limit allowed for your scenario.]</span> </p> </td> 
   <td> <p>파일 크기 제한을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL You have exceeded the maximum conversion time.]</span> </p> </td> 
   <td> <p>무료 [!DNL CloudConvert] 플랜은 매일 25분 전환을 제공합니다. 무료 요금제의 한도를 초과하면 (선불) 패키지 또는 구독으로 전환할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p><span style="font-weight: normal;">[!UICONTROL Failed to read frame size: Could not seek to 1508. �/output/JLIADSA00137P0.mp3: Invalid argument.]</span> </p> </td> 
   <td> <p>이 오류는 MP3에서 WAV로 파일을 변환할 때 발생합니다. 파일에 대한 참조뿐만 아니라 올바른 파일에 대한 참조도 찾을 수 있으므로 올바른 영역을 선택했는지 확인하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL RuntimeError:] </p> <p><span style="font-weight: normal;">[!UICONTROL Maximum number of repeats exceeded.]</span> </p> </td> 
   <td> <p>[!DNL CloudConvert] 대시보드의 작업 목록에서 해당 [!DNL CloudConvert] 작업을 찾아 작업 기간을 확인합니다.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-duration-350x177.png" style="width: 350;height: 177;"> </p> <p>[!DNL CloudConvert] &gt; [!UICONTROL Convert a File] 모듈의 시간 제한이 3분으로 설정되어 있습니다. 작업 기간이 3분을 초과하는 경우([!DNL CloudConvert] 서비스의 일시적인 오버로드로 인해 발생 가능) 모듈에서 위에 언급된 오류가 발생합니다.</p> <p>이 경우 다음 옵션 중 하나를 고려하십시오.</p> 
    <ul> 
     <li>시나리오 설정에서 <strong>[!UICONTROL Allow storing of Incomplete Executions]</strong> 옵션을 활성화하여 이후 수동 해결을 위해 불완전한 실행을 저장합니다. 선택적으로 [!UICONTROL Break] 지시문을 사용하여 [!DNL CloudConvert] 모듈에 오류 처리 경로를 연결하여 불완전한 실행을 자동으로 해결할 수 있습니다.</li> 
     <li>[!DNL CloudConvert] &gt; [!UICONTROL Convert a file] 모듈에서 <strong>[!UICONTROL Download a file] 옵션</strong>을(를) 비활성화합니다. 이 경우 모듈은 변환 결과를 기다리지 않습니다. 변환 결과를 얻으려면 새 시나리오를 만들고 [!DNL CloudConvert] &gt; [!UICONTROL New Job Event] 트리거를 사용하십시오.</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## [!DNL CloudConvert] 커넥터에 대한 예제 워크플로

>[!INFO]
>
>**예:** 비디오를 MOV에서 MP4 형식으로 변환
>
>1. [https://cloudconvert.com/video-converter](https://>cloudconvert.com/video-converter) 방문
>1. **[!UICONTROL Select File]**&#x200B;을(를) 클릭하고 샘플 MOV 파일을 선택합니다.
>1. **[!UICONTROL Convert to]** 옆의 드롭다운을 클릭하고 **[!UICONTROL MP4]**&#x200B;을(를) 선택합니다.
>
>1. **[!UICONTROL wrench]** 아이콘을 클릭합니다.
>1. 알맞은 MP4 압축 설정을 구성합니다.
>1. **[!UICONTROL Convert]**&#x200B;을(를) 클릭합니다.
>1. 변환이 완료되면 **[!UICONTROL Download]**&#x200B;을(를) 클릭합니다.
>1. 변환된 비디오를 검토합니다.
>1. 5단계에 대한 최적의 전환 설정을 찾을 때까지 1~8단계를 반복합니다.
>1. [https://cloudconvert.com/api/v2/convert#convert-tasks](https://cloudconvert.com/api/v2/convert#convert-tasks) 방문
>1. **[!UICONTROL input_format]** 필드에 대해 **[!UICONTROL mov]**&#x200B;을(를) 선택합니다.
>
>1. **[!UICONTROL output_format]** 필드에 대해 **[!UICONTROL mp4]**&#x200B;을(를) 선택합니다.
>
>1. video_codec, crf 등과 같은 가능한 모든 매개 변수의 목록입니다. 가 표시됩니다.
>1. Workfront Fusion 2.0에서 시나리오에 **[!UICONTROL CloudConvert]** > **[!UICONTROL Convert a File]** 모듈을 삽입합니다.
>
>1. 모듈의 설정을 엽니다.
>1. 아래와 같이 모듈을 구성합니다.
>
>   ![CloudConvert 예제](/help/workfront-fusion/references/apps-and-modules/assets/cloudconvert-mp4-example.png)
>
>1. 변환 및 엔진 특정 옵션 필드에 모든 설정을 포함해야 합니다. 5단계의 각 설정에 대해 13단계의 해당 매개 변수와 해당 값을 찾습니다.
