---
title: Adobe Creative Cloud 라이브러리 모듈
description: ' [!DNL Adobe Workfront Fusion Adobe Creative Cloud] 라이브러리 모듈을 사용하면 요소 또는 라이브러리를 만들거나 업데이트할 때 시나리오를 시작할 수 있습니다. 요소를 업로드, 검색, 보관 또는 나열하거나  [!DNL Adobe Creative Cloud Libraries] API를 호출할 수도 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 85607e4e-538a-427f-8a99-a0ab65a75ac2
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1410'
ht-degree: 1%

---

# Adobe Creative Cloud 라이브러리 모듈

Adobe Workfront Fusion [!DNL Adobe Creative Cloud Libraries] 모듈을 사용하면 요소 또는 라이브러리를 만들거나 업데이트할 때 시나리오를 시작할 수 있습니다. 요소를 업로드, 검색, 보관 또는 나열하거나 [!DNL Adobe Creative Cloud Libraries] API를 호출할 수도 있습니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

>[!IMPORTANT]
>
>현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.

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

[!DNL Adobe Creative Cloud Libraries] 모듈을 사용하려면 [!UICONTROL Adobe Creative Cloud] 계정이 있어야 합니다.

## Adobe Creative Cloud Libraries API 정보

Adobe Creative Cloud 라이브러리 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>https://cc-libraries.adobe.io/api/v1</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.1.7</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Adobe Creative Cloud 라이브러리] 모듈 및 해당 필드

[!UICONTROL Adobe Creative Cloud 라이브러리] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Adobe Creative Cloud Libraries] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [요소](#elements)

* [라이브러리](#libraries)

* [기타](#other)


### 요소

* [[!UICONTROL 요소 보관]](#archive-an-element)

* [[!UICONTROL 요소 가져오기]](#get-an-element)

* [[!UICONTROL 요소 나열]](#list-elements)

* [[!UICONTROL 요소 업로드]](#upload-an-element)

* [!UICONTROL [라이브러리의 새 요소 보기]](#watch-new-element-in-library)

* [[!UICONTROL 업데이트된 요소 보기]](#watch-updated-elements)


#### [!UICONTROL 요소 보관]

이 작업 모듈은 라이브러리의 요소를 보관합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 라이브러리 ID]</td>
      <td >보관하려는 요소가 포함된 라이브러리를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 요소 ID]</td>
      <td>보관하려는 요소를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 요소 가져오기]

이 작업 모듈은 라이브러리에서 단일 요소를 반환합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 라이브러리 ID]</td>
      <td>검색할 요소가 포함된 라이브러리를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 요소 ID]</td>
      <td>검색할 요소의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>모듈이 반환하는 정보 유형을 선택합니다. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL 기본값]</b>
            </p>
            <p>기본 데이터</p>
          </li>
          <li>
            <p><b>[!UICONTROL 세부 정보]</b>
            </p>
            <p>사용 가능한 모든 데이터</p>
          </li>
          <li>
            <p><b>[!UICONTROL 표시]</b>
            </p>
            <p>라이브러리 요소와 연결된 병합된 자산 목록</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 요소 나열]

이 작업 모듈은 라이브러리의 요소 목록을 검색합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 라이브러리 ID]</td>
      <td >요소를 나열할 라이브러리를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Order by]</td>
      <td>결과를 이름별로 정렬할지 아니면 요소가 수정된 마지막 날짜별로 정렬할지 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 유형]</td>
      <td >MIME 유형을 입력하거나 매핑하여 지정된 MIME 유형으로 식별된 요소로 결과를 제한합니다. 예: <code>string</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selector]</td>
      <td>
        <p>모듈이 반환하는 정보 유형을 선택합니다. </p>
        <ul>
          <li>
            <p><b>[!UICONTROL 기본값]</b>
            </p>
            <p>기본 데이터</p>
          </li>
          <li>
            <p><b>[!UICONTROL 세부 정보]</b>
            </p>
            <p>사용 가능한 모든 데이터</p>
          </li>
          <li>
            <p><b>[!UICONTROL 표시]</b>
            </p>
            <p>라이브러리 요소와 연결된 병합된 자산 목록</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 라이브러리의 새 요소 보기]

이 트리거 모듈은 요소가 라이브러리에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 라이브러리 ID]</td>
      <td >업데이트된 요소를 검사할 라이브러리를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL 업데이트된 요소 보기]

이 트리거 모듈은 라이브러리의 요소가 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 라이브러리 ID]</td>
      <td >새 요소를 검사할 라이브러리를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

### 라이브러리

* [[!UICONTROL 새 라이브러리 보기]](#watch-new-libraries)

* [[!UICONTROL 업데이트된 라이브러리 보기]](#watch-updated-libraries)


#### [!UICONTROL 새 라이브러리 보기]

이 트리거 모듈은 새 라이브러리가 생성될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 업데이트된 라이브러리 보기]

이 트리거 모듈은 기존 라이브러리가 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]</td>
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

### 기타

* [API 호출 만들기](#make-an-api-call)
* [자산 업로드](#upload-an-asset)

#### [!UICONTROL API 호출 만들기]

이 모듈은 [!DNL Adobe Creative Cloud Libraries] API에 대한 사용자 지정 API 호출을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td> <p>Adobe Creative Cloud 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p><code>https://cc-libraries.adobe.io/api</code>과(와) 관련된 경로를 입력하십시오.</p>
    <p>예 <code>/v1/libraries</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL API version]</td>
      <td>
        <p>연결할 [!DNL Adobe Analytics] API의 버전을 선택하십시오.</p>
      </td>
    </tr>    <tr>
      <td role="rowheader">[!UICONTROL 메서드]</td>
      <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]</td>
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
       <tr>
      <td role="rowheader">[!UICONTROL 임시 문서 업로드]</td>
      <td>
      <p>임시 문서를 업로드하려면 업로드할 문서의 소스 파일을 입력합니다.</p>
      <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p>
    </td>
    </tr>
</tbody>
</table>


#### [!UICONTROL 자산 업로드]

이 작업 모듈은 작은 파일 에셋을 기존 라이브러리에 업로드합니다. 최대 파일 크기는 1GB입니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>기존 Creative Cloud Libraries 연결을 선택하십시오. 현재 Creative Cloud Libraries 커넥터에서는 연결을 만들 수 없습니다. 기존 연결이 예상대로 작동합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 라이브러리 ID]</td>
      <td >에셋을 업로드할 라이브러리를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 호출 모드]</td>
      <td>
        <p>이 요청 프로세스를 호출할 처리 모드를 선택하십시오.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL 동기화]</b>
            </p>
            <p>API 호출이 동기적으로 처리됩니다. 처리가 완료되면 응답이 전달됩니다(호출 제한 시간이 초과된 경우 제외).</p>
          </li>
          <li>
            <p><b>[!UICONTROL async]</b>
            </p>
            <p>비동기 모니터 응답이 즉시 반환되고 요청 처리가 비동기적으로 발생합니다. 호출은 완료될 때까지 끝점을 폴링합니다.</p>
          </li>
          <li>
            <p><b>[!UICONTROL sync,async]</b>(기본값)</p>
            <p>요청의 동기 처리를 시도했습니다. 처리가 5000ms를 초과할 경우 비동기 모니터 응답이 반환됩니다. 요청이 완료될 때까지 모니터 URL을 폴링해야 합니다.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 요소 유형]</td>
      <td >업로드할 요소의 유형을 선택합니다</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 파일 유형]</td>
      <td >업로드한 파일의 MIME 유형을 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Source 파일]</td>
      <td>
        <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>





