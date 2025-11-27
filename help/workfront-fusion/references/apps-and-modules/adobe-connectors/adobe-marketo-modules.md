---
title: Marketo 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Marketo]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '2237'
ht-degree: 100%

---

# [!DNL Marketo] 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Marketo]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

Marketo 커넥터에 대한 소개 비디오는 다음을 참조하십시오.

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

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

[!DNL Marketo] 모듈을 사용하려면 [!DNL Marketo] 계정이 있어야 합니다.

## Marketo API 정보

Marketo 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Marketo]를 Workfront Fusion에 연결 {#connect-marketo-to-workfront-fusion}

[!DNL Marketo] 모듈 내부에서 직접 [!DNL Marketo] 계정에 연결할 수 있습니다.

1. Marketo 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
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
          <p>새로운 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>
          <p>프로덕션 환경에 연결할지 비프로덕션 환경에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>
          <p>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 계정 / Munchkin ID]</td>
        <td>
          <p>[!DNL Marketo] 계정 또는 [!DNL Marketo] [!UICONTROL Munchkin] ID를 입력합니다. 계정에 할당된 기본 URL 또는 엔드포인트의 고유한 부분으로, [!UICONTROL REST] API를 통해 [!DNL Marketo]에 액세스하는 데 사용됩니다. 이 위치를 찾는 방법에 대한 자세한 내용은 [!DNL Marketo] 설명서의 [기본 URL](https://developers.marketo.com/rest-api/base-url/)을 참조하십시오.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>Marketo 클라이언트 ID를 입력합니다. 이 위치를 찾는 방법에 대한 자세한 내용은 [!DNL Marketo] 설명서의 [인증](https://developers.marketo.com/rest-api/authentication/)을 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>Marketo 클라이언트 암호를 입력합니다. 이들 위치를 찾는 방법에 대한 자세한 내용은 [!DNL Marketo] 설명서의 [인증](https://developers.marketo.com/rest-api/authentication/)을 참조하십시오.</td>
      </tr>
     </tbody>
    </table>

1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

## [!DNL Marketo] 모듈 및 해당 필드

[!DNL Marketo] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 수준과 같은 요인에 따라 추가적인 [!DNL Marketo] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

* [[!UICONTROL 이벤트 보기(인스턴트)]](#watch-events-instant)
* [[!UICONTROL 레코드 보기]](#watch-records)

#### [!UICONTROL 이벤트 보기(인스턴트)]

이 트리거 모듈은 레코드를 만들거나 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 웹후크]</p> </td> 
   <td> <p>모듈에서 사용할 웹후크를 입력합니다.</p> <p>웹후크에 대한 자세한 내용은 <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">웹후크</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 보기]

이 트리거 모듈은 레코드를 만들거나 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 활동]</strong> </p> <p>확인할 활동 유형을 선택합니다. </p> <p>모듈은 새 활동만 확인합니다.<br></p> </li> 
     <li> <p><strong>[!UICONTROL 리드]</strong> </p> <p><b>이벤트 유형</b> 필드에서 새 레코드, 업데이트된 레코드, 새 레코드 및 업데이트된 레코드 모두 또는 특정 필드 업데이트를 확인할지 여부를 선택합니다. 특정 필드 업데이트를 확인하도록 선택하는 경우 모듈이 확인할 필드를 선택합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL 프로그램]</strong> </p> <p><b>이벤트 유형</b> 필드에서 새 레코드, 업데이트된 레코드 또는 새 레코드 및 업데이트된 레코드 모두를 확인할지 여부를 선택합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL 목록에 리드 추가]](#add-leads-to-a-list)
* [[!UICONTROL 프로그램 복제]](#clone-a-program)
* [[!UICONTROL 레코드 만들기]](#create-a-record)
* [[!UICONTROL 사용자 정의 API 호출]](#custom-api-call)
* [[!UICONTROL 파일 다운로드]](#download-a-file)
* [[!UICONTROL 레코드 읽기]](#read-a-record)
* [[!UICONTROL 목록에서 리드 제거]](#remove-leads-from-a-list)
* [[!UICONTROL 캠페인 예약]](#schedule-a-campaign)
* [[!UICONTROL 레코드 업데이트]](#update-a-record)
* [[!UICONTROL 파일 업로드]](#upload-a-file)

#### [!UICONTROL 목록에 리드 추가]

이 액션 모듈은 리드 ID를 사용하여 하나 이상의 리드를 목록에 추가합니다. 한 번에 최대 300개의 리드를 추가할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 목록 ID]</td> 
   <td>리드를 추가할 목록의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 리드 ID]</td> 
   <td> <p>목록에 추가할 각 리드에 대해 <b>[!UICONTROL 추가]</b>를 클릭한 다음 추가할 리드의 ID를 입력하거나 매핑합니다. 목록에 추가할 해당 모듈에 최대 300개 리드까지 추가할 수 있습니다.</p> <p>토글 매핑을 클릭하여 목록에 추가할 기존 리드 컬렉션을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 프로그램 복제]

이 액션 모듈은 기존 프로그램의 ID를 사용하여 프로그램의 복사본을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 기존 프로그램 ID]</td> 
   <td>복사할 프로그램의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 새 프로그램 이름]</p> </td> 
   <td> <p>새 프로그램의 이름을 입력하거나 매핑합니다.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더 ID]</td> 
   <td>새 프로그램을 배치할 폴더의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 만들기]

이 액션 모듈은 [!DNL Marketo]에 새 레코드를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 회사]</p> </li> 
     <li> <p>[!UICONTROL 폴더]</p> </li> 
     <li> <p>[!UICONTROL 리드]</p> </li> 
     <li> <p>[!UICONTROL 프로그램]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 매핑할 필드 선택]</td> 
   <td>회사 또는 리드를 만드는 경우 새 레코드가 생성될 때 값을 설정할 필드를 선택한 다음 해당 필드에 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로그램 유형]</td> 
   <td>프로그램을 만드는 경우 만들려는 프로그램 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로그램 채널] </td> 
   <td>프로그램을 만드는 경우 프로그램을 만들려는 프로그램 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더] / [!UICONTROL 프로그램 이름]</td> 
   <td>폴더 또는 프로그램을 만드는 경우 새 레코드의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td> <p>폴더 또는 프로그램을 만드는 경우 새 레코드의 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 상위 폴더 ID]</td> 
   <td>폴더 또는 프로그램을 만드는 경우 새 레코드를 만들 상위 폴더의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 비용]</td> 
   <td>프로그램을 만드는 경우 비용을 추가합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 태그]</td> 
   <td>프로그램을 만드는 경우 태그를 추가합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 사용자 정의 API 호출]

이 액션 모듈을 사용하면 [!DNL Marketo] API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Marketo] 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td><code>https://{your-base-url}.mktorest.com/</code>과 관련된 경로를 입력합니다.</td> 
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
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td> <p>API 호출에 추가할 각 필드에 대해 <b>항목 추가</b>를 클릭하고 필드의 키와 값을 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 다운로드]

이 액션 모듈은 파일 ID를 사용하여 파일을 다운로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td>다운로드할 파일의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 읽기]

이 액션 모듈은 해당 ID를 사용하여 레코드에 대한 정보를 읽습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 캠페인]</p> </li> 
     <li> <p>[!UICONTROL 회사]</p> </li> 
     <li> <p>[!UICONTROL 리드]</p> </li> 
     <li> <p>[!UICONTROL 목록]</p> </li> 
     <li> <p>[!UICONTROL 프로그램]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>이 모듈의 출력 번들에 포함할 정보를 선택합니다. 필드는 선택한 [!UICONTROL 레코드 유형]을 기준으로 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;오브젝트&gt; ID]</td> 
   <td>정보를 가져올 오브젝트의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 목록에서 리드 제거]

이 액션 모듈은 리드 ID를 사용하여 목록에서 하나 이상의 리드를 제거합니다. 한 번에 최대 300개의 리드를 제거할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 목록 ID]</td> 
   <td>리드를 제거할 목록의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 리드 ID]</td> 
   <td> <p>목록에서 제거할 각 리드에 대해 <b>[!UICONTROL 항목 추가]</b>를 클릭한 다음 제거할 리드의 ID를 입력하거나 매핑합니다. 목록에서 제거할 해당 모듈에 최대 300개 리드까지 추가할 수 있습니다. </p> <p>토글 매핑을 클릭하여 목록에서 제거할 기존 리드 컬렉션을 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 캠페인 예약]

이 액션 모듈은 특정 날짜에 기존 캠페인을 예약합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 캠페인 ID]</td> 
   <td>예약할 캠페인의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 예약 날짜]</p> </td> 
   <td>캠페인을 실행할 날짜를 선택합니다. 이 필드를 비워두면 시나리오가 시작되고 5분 후에 캠페인이 실행됩니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 레코드 업데이트]

이 액션 모듈은 해당 ID를 사용하여 기존 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>만들려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 회사]</p> </li> 
     <li> <p>[!UICONTROL 리드]</p> </li> 
     <li> <p>[!UICONTROL 프로그램]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 회사] / [!UICONTROL 리드] / [!UICONTROL 프로그램 ID]</td> 
   <td>업데이트할 레코드의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 매핑할 필드 선택]</td> 
   <td>회사 또는 리드를 업데이트하는 경우 값을 업데이트할 필드를 선택한 다음 해당 필드에 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 프로그램 이름]</td> 
   <td>프로그램을 업데이트하는 경우 프로그램의 새 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td> <p>프로그램을 업데이트하는 경우 프로그램의 새 설명을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작 일자]</td> 
   <td>프로그램을 업데이트하는 경우 프로그램의 새 시작 일자를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 종료 일자]</td> 
   <td>프로그램을 업데이트하는 경우 프로그램의 새 종료 일자를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 비용]</td> 
   <td>프로그램을 업데이트하는 경우 비용을 추가합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 태그]</td> 
   <td>프로그램을 업데이트하는 경우 태그를 추가합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업로드]

이 액션 모듈은 새 파일을 [!UICONTROL Marketo]에 업로드합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더 ID]</td> 
   <td>새 파일을 배치할 폴더의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td>업로드한 파일에 대한 설명을 입력합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL 목록 레코드]](#list-records)
* [[!UICONTROL 검색 레코드]](#update-a-record)

#### [!UICONTROL 목록 레코드]

이 액션 모듈은 특정 유형의 모든 레코드를 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>목록에 넣으려는 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 모든 캠페인 읽기]</p> </li> 
     <li> <p>[!UICONTROL 모든 프로그램 읽기]</p> </li> 
     <li> <p>[!UICONTROL 리드 모두 읽기] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필드]</td> 
   <td>리드를 가져오기로 선택한 경우 목록에서 리드를 가져올지 프로그램에서 가져올지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td>이 모듈의 출력 번들에 포함할 정보를 선택합니다. 필드는 선택한 [!UICONTROL 레코드 유형]을 기준으로 사용할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 검색 레코드]

이 검색 모듈은 특정 검색 기준과 일치하는 레코드 목록을 가져옵니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 연결]</p> </td> 
   <td> <p>[!DNL Marketo] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL Marketo] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>검색할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL 캠페인]</p> </li> 
     <li> <p>[!UICONTROL 리드]</p> </li> 
     <li> <p>[!UICONTROL 프로그램]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 필드]</p> </td> 
   <td> <p>검색할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 값 / 값]</td> 
   <td>검색할 필드의 값을 입력합니다. 필드에서 여러 값을 검색할 수 있는 경우, 검색할 각 값에 대해 <b>[!UICONTROL 항목 추가]</b>를 클릭하고 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>
