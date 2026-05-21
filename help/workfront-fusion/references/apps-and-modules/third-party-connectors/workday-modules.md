---
filename: workday-modules
title: Workday 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Workday]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
TQID: https://experienceleague.adobe.com/b-RlvqOsRRrFZMh8JrPFAS2pigkQP-6ugZ5kZl8AdZ8
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1063
ht-degree: 52%

---

# [!DNL Workday] 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Workday]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

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

[!DNL Workday] 모듈을 사용하려면 다음을 수행해야 합니다.

* [!DNL Workday] 계정이 있습니다.

* [!DNL Workday]에서 OAuth 응용 프로그램을 만듭니다. 자세한 내용은 [!DNL Workday] 설명서를 참조하십시오.

## Workday API 정보

Workday 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td><pre><code>https://&#123;&#123;connection.servicesUrl&#125;&#125;/api</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Workday]를 Workfront Fusion에 연결

1. Workfront Fusion 모듈에서 [!UICONTROL 연결] 필드 옆에 있는 [!UICONTROL 추가]를 클릭합니다

2. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL 연결 이름]</p>
                </td>
                <td>연결의 이름을 입력합니다.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Workday 호스트]</td>
                <td><code>https://</code> 없이 [!DNL Workday] 호스트의 주소를 입력하십시오. 예: <code>mycompany.workday.com</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Services URL]</td>
                <td><code>https://</code> 없이 [!DNL Workday] 웹 서비스의 주소를 입력하십시오. 예: <code>mycompany-services.workday.com</code>.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL 테넌트 이름]</td>
                <td>이 [!DNL Workday] 계정의 테넌트를 입력하십시오. 테넌트는 조직의 식별자이며, Workday에 로그인하는 데 사용하는 URL에서 볼 수 있습니다. 예: 주소 <code>https://www.myworkday.com/mycompany</code>에서 테넌트는 <code>mycompany</code>입니다.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
                <td>이 연결에서 사용하는 [!DNL Workday] 응용 프로그램의 클라이언트 ID를 입력하십시오. [!DNL Workday]에서 응용 프로그램을 만들 때 이 오류가 발생합니다.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL 클라이언트 암호]</td>
                <td>이 연결에서 사용하는 [!DNL Workday] 응용 프로그램의 클라이언트 암호를 입력하십시오. [!DNL Workday]에서 응용 프로그램을 만들 때 이 오류가 발생합니다.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL 세션 시간 초과(분)]</td>
                <td >인증 토큰이 만료된 후 시간(분)을 입력합니다.</td>
            </tr>
        </tbody>
    </table>


3. 연결을 저장하고 모듈로 돌아가려면 [!UICONTROL 계속]을 클릭하세요.

## [!DNL Workday] 모듈 및 해당 필드

[!DNL Workday] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL Workday] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#action)

* [검색](#search)


### 액션

* [[!UICONTROL 레코드 만들기]](#create-a-record)

* [[!UICONTROL 레코드 삭제]](#delete-a-record)

* [[!UICONTROL 사용자 정의 API 호출하기]](#make-a-custom-api-call)

* [[!UICONTROL 레코드 업데이트]](#update-a-record)


#### [!UICONTROL 레코드 만들기]

이 작업 모듈은 [!DNL Workday]에 단일 레코드를 만듭니다.

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL 연결]</td>
            <td>[!DNL Workday] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="#Connect" class="MCXref xref" >Workfront Fusion에 [!DNL Workday] 연결</a>을 참조하십시오.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 레코드 유형]</td>
            <td>만들려는 레코드 유형을 선택합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>만들려는 레코드의 ID를 입력하거나 매핑합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 하위 리소스 ID]</td>
            <td >만들려는 하위 리소스의 ID를 입력하거나 매핑합니다.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL 레코드 삭제]

이 작업 모듈은 [!DNL Workday]에서 단일 레코드를 삭제합니다.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL 연결]</td>
            <td>[!DNL Workday] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="#Connect" class="MCXref xref" >Workfront Fusion에 [!DNL Workday] 연결</a>을 참조하십시오.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 레코드 유형]</td>
            <td>삭제할 레코드 유형을 선택합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 특정 레코드 유형]</td>
            <td>삭제하려는 특정 레코드 유형을 선택합니다. 선택한 레코드 종류를 기반으로 합니다.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 하위 리소스 ID]</td>
            <td>삭제할 하위 리소스의 ID를 입력하거나 매핑합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >삭제할 레코드의 ID를 입력하거나 매핑합니다.</td>
        </tr>
    </tbody>
</table>


### [!UICONTROL 사용자 정의 API 호출하기]

이 액션 모듈을 사용하면 [!DNL Workday] API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Workday] 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

이 모듈은 API 호출의 헤더 및 본문과 함께 상태 코드를 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Connection]</p> </td> 
            <td>[!DNL Workday] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="#Connect" class="MCXref xref" >Workfront Fusion에 [!DNL Workday] 연결</a>을 참조하십시오.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code>과 관련된 경로를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion]가 사용자에게 인증 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>예: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:  <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 업데이트]

이 작업 모듈은 [!DNL Workday]의 단일 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL 연결]</td>
            <td>[!DNL Workday] 계정을 Workfront Fusion에 연결하는 방법은 <a href="#Connect" class="MCXref xref" >[!UICONTROL [!DNL Workday]을(를) Workfront Fusion에 연결</a>을 참조하십시오.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 레코드 유형]</td>
            <td>업데이트할 레코드 유형을 선택합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>업데이트할 레코드의 ID를 입력하거나 매핑합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 하위 리소스 ID]</td>
            <td >업데이트할 하위 리소스의 ID를 입력하거나 매핑합니다.</td>
        </tr>
    </tbody>
</table>

### 검색

* [[!UICONTROL 레코드 읽기]](#read-a-record)

* [[!UICONTROL 목록 레코드]](#list-records)


#### [!UICONTROL 레코드 읽기]

이 작업 모듈은 단일 레코드를 읽습니다.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL 연결]</td>
            <td>[!DNL Workday] 계정을 Workfront Fusion에 연결하는 방법은 <a href="#Connect" class="MCXref xref" >[!UICONTROL [!DNL Workday]을(를) Workfront Fusion에 연결</a>을 참조하십시오.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 레코드 유형]</td>
            <td>삭제할 레코드 유형을 선택합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 특정 레코드 유형]</td>
            <td>읽고자 하는 특정 레코드 유형을 선택합니다. 선택한 레코드 종류를 기반으로 합니다.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >삭제할 레코드의 ID를 입력하거나 매핑합니다.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL 목록 레코드]

이 검색 모듈은 지정된 유형의 레코드 목록을 검색합니다.

<table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">[!UICONTROL 연결]</td>
              <td>[!DNL Workday] 계정을 Workfront Fusion에 연결하는 방법은 <a href="#Connect" class="MCXref xref" >Workfront Fusion에 [!DNL Workday] 연결</a>을 참조하십시오.</td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL 레코드 유형]</td>
              <td>검색할 레코드 유형을 선택합니다.</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL 제한]</td>
              <td >
                  <p>각 시나리오 실행 주기 동안 모듈이 검색할 최대 레코드 수를 입력하거나 매핑합니다.</p>
              </td>
          </tr>
      </tbody>
  </table>
