---
title: Figma 모듈
description: ' [!DNL Adobe Workfront Fusion] Figma 모듈을 사용하면 주석, 파일, 파일 버전 또는 프로젝트 목록을 검색할 수 있습니다. Figma API에 댓글을 게시하거나 호출할 수도 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 1220460b-1957-4dfc-b7c1-4c97b36ea061
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---

# [!DNL Figma]개 모듈

[!DNL Adobe Workfront Fusion] [!DNL Figma] 모듈을 사용하면 주석, 파일, 파일 버전 또는 프로젝트 목록을 검색할 수 있습니다. 댓글을 게시하거나 [!DNL Figma] API를 호출할 수도 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## 전제 조건

[!DNL Figma] 모듈을 사용하려면 [!DNL Figma] 계정이 있어야 합니다.

## Figma API 정보

Figma 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://api.figma.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.8.25</td> 
  </tr>
 </tbody> 
 </table>

## Figma에 대한 연결 만들기

Figure 모듈에 대한 연결을 만들려면:

1. Figure 모듈에서 연결 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p> 새 연결의 경우 기존 태그 없이 <code>Figma</code>을(를) 선택하십시오. </p><p>Figma는 2025년 1월에 인증 요구 사항을 변경했습니다. <code>Figma</code> 연결 유형이 새 요구 사항을 충족합니다. <code>Figma (Legacy)</code> 연결 형식은 나중에 제거됩니다.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>[!UICONTROL Figme] [!UICONTROL Client ID]을(를) 입력하십시오.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>그림 [!UICONTROL Client Secret]을(를) 입력하십시오.</td>
        </tr>
        <tr>
        <td role="rowheader">사용자 지정 범위</td>
        <td>이 연결에 필요한 사용자 지정 범위를 입력하십시오.</td>
        </tr>
        <tr>
        <td role="rowheader">사용자 지정 연결 확인 URL</td>
        <td>연결을 성공적으로 만들었는지 확인하기 위한 기본 끝점은 <code>https://api.figma.com/v1/me</code>입니다. 이 URL이 사용자 지정 범위에 대해 지원되지 않는 경우 사용자 지정 확인 URL을 제공하십시오.</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.



## [!DNL Figma]개 모듈 및 해당 필드

[!DNL Figma] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Figma] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [댓글](#comments)

* [프로젝트 및 파일](#projects-and-files)

* [구성 요소 및 스타일](#components-and-styles)

* [기타](#other)


### 댓글

* [댓글 삭제](#delete-a-comment)

* [댓글 나열](#list-comments)

* [댓글 게시](#post-a-comment)


#### [!UICONTROL Delete a comment]

이 작업 모듈은 파일에서 하나의 주석을 삭제합니다.

<table style="table-layout:auto"> 
  <col/>
  <col />
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>삭제 댓글을 추가할 파일의 파일 ID를 입력하거나 매핑합니다. </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comment ID]</td>
      <td>삭제할 댓글의 텍스트를 입력합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List comments]

이 검색 모듈은 [!DNL Figma]의 단일 파일에 첨부된 모든 설명을 나열합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>주석을 검색할 파일의 파일 ID를 입력하거나 매핑합니다. </p>
        <ul>
          <li>
            <p>ID를 모를 경우 <b>[!UICONTROL Find Files]</b>을(를) 클릭하고 파일이 연결된 프로젝트의 ID를 입력하거나 매핑한 다음 파일을 선택합니다.</p>
          </li>
          <li>
            <p>프로젝트의 ID를 모를 경우 <b>[!UICONTROL Find Projects]</b>을(를) 클릭하고 파일이 연결된 프로젝트를 소유한 팀의 ID를 입력하거나 매핑한 다음 프로젝트를 선택하고 파일을 선택합니다.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 주석 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL Post a comment]

이 작업 모듈은 Figma 파일에 주석을 게시합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    </tr>
    <tr>
      <td  role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>댓글을 게시하려는 파일의 파일 ID를 입력하거나 매핑합니다. </p>
        <ul>
          <li>
            <p>파일의 ID를 모를 경우 <b>[!UICONTROL Find Files]</b>을(를) 클릭하고 파일이 연결된 프로젝트의 ID를 입력하거나 매핑한 다음 파일을 선택합니다.</p>
          </li>
          <li>
            <p>파일의 ID를 찾고 프로젝트의 ID를 모르는 경우 <b>[!UICONTROL Find Projects]</b>을(를) 클릭하고 파일이 연결된 프로젝트를 소유한 팀의 ID를 입력하거나 매핑합니다. 프로젝트를 선택한 다음 파일을 선택합니다.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Comment]</td>
      <td>주석의 텍스트를 입력합니다.</td>
    </tr>
  </tbody>
</table>


### 프로젝트 및 파일

* [파일 또는 이미지 가져오기](#get-a-file-or-image)

* [목록 파일 버전 기록](#list-file-version-history)

* [프로젝트 파일 나열](#list-project-files)

* [프로젝트 나열](#list-projects)


#### [!UICONTROL Get a file or image]

이 작업 모듈은 Figure 라이브러리에서 단일 파일 또는 이미지를 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>
        <p>검색할 객체 유형을 선택합니다.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL File]</b>
            </p>
            <p>모듈이 [!UICONTROL Key]에서 참조하는 문서를 JSON 개체로 반환합니다. 파일 키는 모든 Figma 파일 URL에서 구문 분석할 수 있습니다.</p>
            <p>필드에 대해서는 <a href="#get-a-file-or-image-file" class="MCXref xref" >[!UICONTROL Get a file or image: File]</a>을(를) 참조하십시오.</p>
          </li>
          <li>
            <p><b>[!UICONTROL File nodes]</b>
            </p>
            <p>ID에서 참조하는 노드를 JSON 개체로 반환합니다. [!UICONTROL Key]이(가) 참조하는 [!DNL Figma] 파일에서 노드를 검색했습니다.</p>
            <p>필드에 대해서는 <a href="#get-a-file-or-image-file-nodes" class="MCXref xref" >[!UICONTROL Get a file or image: File nodes]</a>을(를) 참조하십시오.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Image]</b>
            </p>
            <p>모듈은 파일의 이미지를 렌더링합니다.</p>
            <p>필드에 대해서는 <a href="#get-a-file-or-image-image" class="MCXref xref" >[!UICONTROL Get a file or image: Image]</a>을(를) 참조하십시오.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Image fills]</b>
            </p>
            <p>이 모듈은 문서의 이미지 채우기에 있는 모든 이미지에 대한 다운로드 링크를 반환합니다. 이미지 채우기는 [!DNL Figma]이(가) 사용자가 제공한 이미지를 나타내는 방식입니다. 이미지를 [!DNL Figma](으)로 드래그하면 [!DNL Figma]에서 이미지를 나타내는 단일 채우기로 사각형을 만들고 사용자는 사각형을 변형할 수 있습니다(및 채우기의 속성).</p>
            <p>필드에 대해서는 <a href="#get-a-file-or-image-image-fills" class="MCXref xref" >[!UICONTROL Get a file or image: Image fills]</a>을(를) 참조하십시오.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


##### 파일 또는 이미지 가져오기: 파일

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>JSON을 반환할 파일을 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version ID]</td>
      <td>모듈이 반환할 파일의 버전을 입력하거나 매핑합니다. 현재 모듈의 경우 이 필드를 비워 둡니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>문서의 하위 집합만 반환하려면 모듈이 반환할 노드를 입력합니다. 모듈은 나열된 노드, 해당 자식 및 루트 노드와 나열된 노드 사이의 모든 것을 반환합니다.</p>
        <p>반환할 각 노드에 대해 <b>[!UICONTROL Add]</b>을(를) 클릭하고 노드의 텍스트를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>결과를 반환할 문서 트리의 깊이를 나타내는 정수를 입력하거나 매핑합니다. </p>
        <div class="example"><span class="autonumber"><span><b>예: </b></span></span>
          <ul>
            <li>
              <p>페이지만 반환하려면 <code>1</code>을(를) 입력하십시오.</p>
            </li>
            <li>
              <p>페이지와 최상위 개체를 반환하려면 <code>2</code>을(를) 입력하십시오.</p>
            </li>
          </ul>
        </div>
        <p>모든 노드를 반환하려면 이 필드를 비워 둡니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>벡터 데이터를 반환하려면 <code>paths</code>을(를) 입력하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>플러그 인 ID 및/또는 문자열 "[!UICONTROL shared]"을(를) 쉼표로 구분한 목록입니다. 해당 플러그인이 작성한 문서에 있는 모든 데이터는 <code>pluginData</code> 및 <code>sharedPluginData</code> 속성의 결과에 포함됩니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Branch data]</td>
      <td>요청된 파일에 대한 분기 메타데이터를 반환하려면 이 옵션을 활성화하십시오. 파일이 분기인 경우 주 파일의 키가 반환된 응답에 포함됩니다. 파일에 분기가 있는 경우 해당 메타데이터가 반환된 응답에 포함됩니다. 기본값: <code>false</code>.</td>
    </tr>
  </tbody>
</table>

##### 파일 또는 이미지 가져오기: 파일 노드

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>JSON을 반환할 파일을 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>모듈이 반환하고 변환할 노드를 입력하십시오.</p>
        <p>반환할 각 노드에 대해 <b>[!UICONTROL Add]</b>을(를) 클릭하고 노드의 텍스트를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version ID]</td>
      <td>모듈이 반환할 파일의 버전을 입력하거나 매핑합니다. 현재 모듈의 경우 이 필드를 비워 둡니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Depth]</td>
      <td>
        <p>결과를 반환할 문서 트리의 깊이를 나타내는 정수를 입력하거나 매핑합니다. </p>
        <div class="example"><span class="autonumber"><span><b>예: </b></span></span>
          <ul>
            <li>
              <p>페이지만 반환하려면 <code>1</code>을(를) 입력하십시오.</p>
            </li>
            <li>
              <p>페이지와 최상위 개체를 반환하려면 <code>2</code>을(를) 입력하십시오.</p>
            </li>
          </ul>
        </div>
        <p>모든 노드를 반환하려면 이 필드를 비워 둡니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Geometry]</td>
      <td>벡터 데이터를 반환하려면 <code>paths</code>을(를) 입력하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plugin data]</td>
      <td>플러그인 ID 및/또는 문자열 "shared"를 쉼표로 구분한 목록입니다. 이러한 플러그인이 작성한 문서에 있는 모든 데이터는 pluginData 및 sharedPluginData 속성의 결과에 포함됩니다.</td>
    </tr>
  </tbody>
</table>


##### 파일 또는 이미지 가져오기: 이미지

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>JSON을 반환할 파일을 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Node IDs]</td>
      <td>
        <p>모듈을 렌더링할 노드를 입력합니다.</p>
        <p>렌더링할 각 노드에 대해 <b>[!UICONTROL Add]</b>을(를) 클릭하고 노드의 텍스트를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Scale]</td>
      <td>이미지의 크기를 조정하려면 크기 조정 요소를 입력하거나 매핑합니다. 이 숫자는 0.01에서 4 사이여야 합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Format]</td>
      <td>
        <p>이미지 출력 형식을 선택합니다.</p>
        <ul>
          <li>
            <p>JPG</p>
          </li>
          <li>
            <p>PNG</p>
          </li>
          <li>
            <p>SVG</p>
          </li>
          <li>
            <p>PDF</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - Include ID]</td>
      <td>모든 SVG 요소의 ID 속성을 포함하려면 이 옵션을 활성화합니다. 기본값: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SVG - Simplify Stroke]</td>
      <td>내부/외부 선을 단순화하고 가능한 경우 &lt;mask&gt; 대신 획 특성을 사용하려면 이 옵션을 활성화합니다. 기본값: [!UICONTROL true].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Use absolute bounds]</td>
      <td>잘리는지 또는 노드 주위의 공간이 비어 있는지에 관계없이 노드의 전체 차원을 사용하려면 이 옵션을 활성화합니다. 이 옵션을 사용하여 자르지 않고 텍스트 노드를 내보냅니다. 기본값: [!UICONTROL false].</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Version]</td>
      <td>모듈이 반환할 파일의 버전을 입력하거나 매핑합니다. 현재 모듈의 경우 이 필드를 비워 둡니다.</td>
    </tr>
  </tbody>
</table>

##### 파일 또는 이미지 가져오기: 이미지가 채워짐

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL File key]</td>
      <td>JSON을 반환할 파일을 선택합니다.</td>
    </tr>
  </tbody>
</table>

### [!UICONTROL List file version history]

이 검색 모듈은 [!UICONTROL Figma]에 있는 단일 파일의 버전 기록을 반환합니다.
<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>버전 기록을 검색할 파일의 파일 ID를 입력하거나 매핑합니다. </p>
        <ul>
          <li>
            <p>파일의 ID를 모를 경우 <b>[!UICONTROL Find Files]</b>을(를) 클릭하고 파일이 연결된 프로젝트의 ID를 입력하거나 매핑한 다음 파일을 선택합니다.</p>
          </li>
          <li>
            <p>파일의 ID를 찾고 프로젝트의 ID를 모르는 경우 <b>[!UICONTROL Find Projects]</b>을(를) 클릭하고 파일이 연결된 프로젝트를 소유한 팀의 ID를 입력하거나 매핑합니다. 프로젝트를 선택한 다음 파일을 선택합니다.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned files]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List project files]

이 검색 모듈은 지정된 프로젝트의 모든 파일 목록을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File ID]</td>
      <td>
        <p>파일을 검색할 프로젝트의 프로젝트 ID를 입력하거나 매핑합니다. </p>
        <ul>
          <li>
            <p>프로젝트의 ID를 모를 경우 <b>[!UICONTROL Find Projects]</b>을(를) 클릭하고 프로젝트가 연결된 팀의 ID를 입력하거나 매핑한 다음 프로젝트를 선택합니다.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned files]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List projects]

이 검색 모듈은 지정된 팀 내의 모든 프로젝트 목록을 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Team ID]</td>
      <td>파일을 검색할 프로젝트의 프로젝트 ID를 입력하거나 매핑합니다. 팀 ID는 Figma에 있는 팀 페이지의 URL에서 찾을 수 있습니다</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned projects]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>


### 구성 요소 및 스타일

#### [!UICONTROL Get a style or component]

이 작업 모듈은 단일 스타일 또는 구성 요소나 스타일 또는 구성 요소 집합을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    </tr>
    <tr>
      <td role="rowheader">개체&gt; 유형</td>
      <td>검색할 객체 유형을 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">&lt;[!UICONTROL Object> key]</td>
      <td>검색할 객체의 키(고유 식별자)를 입력합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Team ID]</td>
      <td>팀 구성 요소 또는 팀 구성 요소 집합을 검색하는 경우 레코드와 연결된 팀의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Page Size]</td>
      <td>팀 구성 요소 또는 팀 구성 요소 집합을 검색하는 경우 페이지당 반환할 횟수나 결과를 입력하거나 매핑합니다. 기본값: 30.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL After]</td>
      <td>
        <p>팀 구성 요소 또는 팀 구성 요소 집합을 검색하는 경우 결과 검색을 시작할 결과 번호를 입력하거나 매핑합니다. 이 항목을 [!UICONTROL Page Size] 필드와 결합하여 결과의 페이지를 매길 수 있습니다.</p>
        <p>이 값은 개체 ID와 일치하지 않습니다.</p>
        <p>이 필드는 [!UICONTROL Before] 필드와 함께 사용할 수 없습니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Before]</td>
      <td>
        <p>팀 구성 요소 또는 팀 구성 요소 집합을 검색하는 경우 결과 검색을 시작하기 전에 결과 번호를 입력하거나 매핑합니다. 이 항목을 [!UICONTROL Page Size] 필드와 결합하여 결과의 페이지를 매길 수 있습니다.</p>
        <p>이 값은 개체 ID와 일치하지 않습니다.</p>
        <p>이 필드는 [!UICONTROL After] 필드와 함께 사용할 수 없습니다.</p>
      </td>
    </tr>
  </tbody>
</table>


### 기타

* [API 호출 만들기](#make-an-api-call)

* [이벤트 보기](#watch-events)


#### [!UICONTROL Make an API call]

이 작업 모듈을 사용하면 인증을 통해 생각할 필요 없이 Figma API에 대한 사용자 지정 인증 호출을 만들 수 있습니다. 이렇게 하면 다른 Fi그마 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>[!DNL Figma] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">Figure에 연결 만들기</a>를 참조하십시오.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p><code>https://api.figma.com/v1/</code>과(와) 관련된 경로를 입력하십시오.</p>
        <p>For example: <code>[!DNL files/7179110/comments]</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Method]</td>
      <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 인증 헤더를 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]</td>
      <td>
        <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p>
        <p>For example: <code>{"name":"something-urgent"}</code></p>
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

#### [!UICONTROL Watch events]

이 트리거 모듈은 [!DNL Figma] 팀 공간의 특정 팀에 대해 다음 이벤트 중 하나가 발생하면 시나리오를 시작합니다.

* 파일 업데이트

* 파일 버전 업데이트

* 파일 삭제

* 라이브러리 게시

* 파일 주석

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>
        <p>모듈이 감시하는 웹후크를 선택합니다.</p>
        <p>새 Webhook를 추가하려면</p>
        <ol>
          <li>
            <p>[!UICONTROL Webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</p>
          </li>
          <li>
            <p>Webhook의 이름을 입력합니다.</p>
          </li>
          <li>
            <p>이 웹후크에 사용할 연결을 선택합니다. [!DNL Figma] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!UICONTROL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p>
          </li>
          <li>
            <p>모듈에서 볼 이벤트 유형을 선택합니다.</p>
          </li>
          <li>
            <p>웹후크에서 보려는 이벤트의 팀 ID를 입력합니다.</p>
          </li>
          <li>
            <p>웹후크를 활성화할지 또는 일시 중지할지 선택합니다.</p>
          </li>
          <li>
            <p>Webhook에 대한 설명을 입력합니다.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다.</p>
          </li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>
