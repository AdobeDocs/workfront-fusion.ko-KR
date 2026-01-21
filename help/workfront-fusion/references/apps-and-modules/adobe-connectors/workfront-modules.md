---
title: Adobe Workfront 모듈
description: Adobe Workfront Fusion Adobe Workfront 커넥터를 사용하여 Workfront 내에서 프로세스를 자동화할 수 있습니다. 작업 자동화 및 통합을 위한 Workfront Fusion 라이선스가 있는 경우, 이를 사용하여 서드파티 앱 및 서비스에 연결할 수도 있습니다.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: ab12dbf0dbad25a8300eb1201fa3e0fde9148acc
workflow-type: tm+mt
source-wordcount: '7366'
ht-degree: 99%

---

# Adobe Workfront 모듈

>[!IMPORTANT]
>
>이 문서에는 2025년 10월 22일에 릴리스된 신규 버전의 Workfront 커넥터에 대한 지침이 포함되어 있습니다. 이 새로운 커넥터는 Workfront API의 변경 사항을 반영합니다.
>
>새 커넥터는 “Workfront”로 표시되며, 이전에 사용 가능했던 커넥터는 “Workfront(이전)”로 표시됩니다
>
>권장 사항:
>
>* 시나리오를 만들거나 업데이트할 때 새 커넥터를 사용합니다.
>* 기존 모듈을 새 커넥터로 업그레이드하는 중입니다.
>
>이전 Workfront 커넥터는 28.4 릴리스(2028년 4월)와 함께 사용되지 않을 예정인 Workfront API 버전 20을 사용합니다. 이전 커넥터의 모듈은 해당 시간까지 계속 작동합니다.
>
>기존 모듈을 업그레이드하는 방법에 대한 지침은 신규 버전으로 모듈 업그레이드 문서에서 [Workfront 모듈을 신규 버전으로 업그레이드](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md)를 참조하십시오.
>
>경우에 따라 새 커넥터가 필요한 이유에 대한 자세한 내용은 [Fusion의 API 개요](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md)를 참조하십시오.

Adobe Workfront Fusion Adobe Workfront 커넥터를 사용하여 Workfront 내에서 프로세스를 자동화할 수 있습니다. Workfront를 다른 애플리케이션 및 서비스에 연결할 수도 있습니다.

시나리오 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 색인](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오. 모듈에 대한 자세한 내용은 [모듈: 문서 색인](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

+++

## Workfront을 Workfront Fusion에 연결

Workfront 커넥터는 OAuth 2.0을 사용하여 Workfront에 연결합니다.

Workfront Fusion 모듈 내에서 직접 Workfront 계정에 대한 연결을 만들 수 있습니다.

* [클라이언트 ID 및 클라이언트 암호를 사용하여 Workfront에 연결](#connect-to-workfront-using-client-id-and-client-secret)
* [서버 간 연결을 사용하여 Workfront에 연결](#connect-to-workfront-using-a-server-to-server-connection)

### 클라이언트 ID 및 클라이언트 암호를 사용하여 Workfront에 연결

1. 모든 Adobe Workfront 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
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
          <p><b>Adobe Workfront 인증 연결</b>을 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새로운 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>Workfront 클라이언트 ID를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. 연결할 특정 애플리케이션을 열어 클라이언트 ID를 확인합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>Workfront 클라이언트 암호를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. Workfront에 OAuth2 애플리케이션에 대한 클라이언트 암호가 없는 경우 다른 애플리케이션을 생성할 수 있습니다. 자세한 내용은 Workfront 설명서를 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인증 URL]</td>
        <td>이 값은 기본값으로 유지되거나 Workfront 인스턴스의 URL을 입력한 다음 <code>/integrations/oauth2</code>를 입력할 수 있습니다. <p>예: <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 호스트 접두사]</td>
        <td>대부분의 경우 이 값은 <code>origin</code>이어야 합니다.
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   Workfront에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인한 후 연결을 허용할 수 있습니다.

>[!NOTE]
>
>* OAuth 2.0의 Workfront API에 대한 연결은 더 이상 API 키에 사용하지 않습니다.
>* Workfront 샌드박스 환경에 연결하려면 해당 환경에서 OAuth2 애플리케이션을 만든 다음 해당 애플리케이션에서 생성한 클라이언트 ID와 클라이언트 암호를 연결에 사용해야 합니다.

### 서버 간 연결을 사용하여 Workfront에 연결

1. 모든 Adobe Workfront 모듈에서 연결 필드 옆에 있는 **추가**&#x200B;를 클릭합니다.
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
          <p><b>Adobe Workfront 서버 간 연결</b>을 선택합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 연결 이름]</td>
        <td>
          <p>새로운 연결의 이름을 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인스턴스 이름]</td>
        <td>
          <p>인스턴스 이름(도메인이라고도 함)을 입력합니다.</p><p>예: URL이 <code>https://example.my.workfront.com</code>인 경우 <code>example</code>을(를) 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 인스턴스 레인]</td>
        <td>
          <p>이 연결이 연결될 환경 유형을 입력합니다.</p><p>예: URL이 <code>https://example.my.workfront.com</code>인 경우 <code>my</code>을(를) 입력합니다.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>Workfront 클라이언트 ID를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. 연결할 특정 애플리케이션을 열어 클라이언트 ID를 확인합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>Workfront 클라이언트 암호를 입력합니다. 이는 Workfront의 설정 영역에 있는 OAuth2 애플리케이션 영역에서 찾을 수 있습니다. Workfront에 OAuth2 애플리케이션에 대한 클라이언트 암호가 없는 경우 다른 애플리케이션을 생성할 수 있습니다. 자세한 내용은 Workfront 설명서를 참조하십시오.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 범위]</td>
        <td>이 연결에 적용할 수 있는 범위를 입력합니다.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 호스트 접두사]</td>
        <td>대부분의 경우 이 값은 <code>origin</code>이어야 합니다.
      </tr>
    </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   Workfront에 로그인하지 않은 경우 로그인 화면으로 이동합니다. 로그인한 후 연결을 허용할 수 있습니다.

>[!NOTE]
>
>* OAuth 2.0의 Workfront API에 대한 연결은 더 이상 API 키에 사용하지 않습니다.
>* Workfront 샌드박스 환경에 연결하려면 해당 환경에서 OAuth2 애플리케이션을 만든 다음 해당 애플리케이션에서 생성한 클라이언트 ID와 클라이언트 암호를 연결에 사용해야 합니다.

## Workfront 모듈 및 해당 필드

Workfront 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 Workfront 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.


![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Workfront 모듈에서 최신 필드가 보이지 않는 경우, 이는 캐싱 문제 때문일 수 있습니다. 1시간 기다린 후 다시 시도해 보십시오.
>* Adobe Workfront의 HTTP 429 상태 코드는 비활성화를 일으키지 않고 시나리오에서 짧은 실행 중지를 트리거해야 합니다.

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL 이벤트 보기]**

이 트리거 모듈은 Workfront에서 특정 유형의 오브젝트가 추가, 업데이트 또는 삭제될 때 실시간으로 시나리오를 실행합니다.

모듈은 웹후크와 관련된 모든 이벤트 구독을 표시합니다. 여기에는 Fusion을 통해 생성된 이벤트 구독뿐만 아니라 API를 통해 직접 생성된 이벤트 구독도 포함됩니다. 이 이벤트 구독 보기는 이전 버전의 이벤트 보기 모듈에서 사용할 수 없습니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

1. **웹후크** 상자 오른쪽에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

1. 표시되는 **[!UICONTROL 후크 추가]** 상자에서 웹후크를 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL 웹후크 이름]</td> 
      <td>웹후크 이름을 입력합니다.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 연결]</td> 
      <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 레코드 유형]</td> 
      <td>모듈에서 볼 Workfront 레코드의 유형을 선택합니다.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 상태]</td> 
      <td>이전 상태를 볼 것인지 새 상태를 볼 것인지 선택합니다.<ul><li><p><b>[!UICONTROL 새 상태]</b></p><p>레코드가 지정된 값<b>으로</b> 변경되면 시나리오를 트리거합니다.</p><p>예를 들어, 상태가 [!UICONTROL 새 상태]로 설정되어 있고 필터가 [!UICONTROL 상태] [!UICONTROL 다음과 같음] [!UICONTROL 진행 중]으로 설정된 경우, 웹후크는 이전 상태와 관계없이 [!UICONTROL 상태]가 [!UICONTROL 진행 중]으로 변경되면 시나리오를 트리거합니다. </p></li><li><p><b>[!UICONTROL 이전 상태]</b></p><p>레코드가 지정된 값<b>에서</b> 변경되면 시나리오를 트리거합니다.</p><p>예를 들어, 상태가 [!UICONTROL 이전 상태]로 설정되어 있고 필터가 [!UICONTROL 상태] [!UICONTROL 다음과 같음] [!UICONTROL 진행 중]으로 설정된 경우, 현재 [!UICONTROL 진행 중]인 [!UICONTROL 상태]가 다른 상태로 변경되면 웹후크가 시나리오를 트리거합니다. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 이벤트 필터]</p> </td> 
      <td> <p>선택한 기준을 충족하는 레코드만 보도록 필터를 설정할 수 있습니다.</p> <p>각 필터에 대해 필터가 평가할 필드, 연산자, 필터를 허용하기 원하는 값을 입력합니다. AND 규칙을 추가하여 두 개 이상의 필터를 사용할 수 있습니다.</p> <p><b>메모</b>: 기존 Workfront 웹후크에서는 필터를 편집할 수 없습니다. Workfront 이벤트 구독에 대해 서로 다른 필터를 설정하려면 현재 웹후크를 제거하고 새 웹후크를 만듭니다.</p> <p>이벤트 필터에 대한 자세한 내용은 이 문서의 <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Workfront에서 이벤트 구독 필터 &gt; [!UICONTROL 이벤트 보기] 모듈</a>을 참조하십시오.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>이 연결에 의해 만들어진 이벤트 제외</td> 
      <td>이 트리거 모듈이 사용하는 동일한 커넥터를 사용하여 만들거나 업데이트된 이벤트를 제외하려면 이 옵션을 활성화합니다. 이렇게 하면 시나리오가 스스로 트리거되어 끝없이 반복되는 상황을 방지할 수 있습니다.<p><b>메모</b>: 할당 레코드 유형에 이 옵션이 포함되어 있지 않습니다.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 레코드 원본]</td> 
      <td>
       <p>시나리오를 [!UICONTROL 새 레코드만], [!UICONTROL 업데이트된 레코드만], [!UICONTROL 새 레코드 및 업데이트된 레코드] 또는 [!DNL Deleted Records Only] 중 어떻게 볼 것인지 선택합니다.</p>
       <p><b>메모</b>: [!UICONTROL 새 레코드 및 업데이트 레코드]를 선택하면, 웹후크 만들기에서 동일한 웹후크 주소에 대해 두 개의 이벤트 구독을 만듭니다.</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

웹후크가 생성된 후 이벤트가 전송되는 엔드포인트의 주소를 볼 수 있습니다.

자세한 내용은 Workfront 설명서의 이벤트 구독 API 문서에서 [이벤트 페이로드 예제](https://experienceleague.adobe.com/ko/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) 섹션을 참조하십시오.

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

+++

+++ **[!UICONTROL 필드 보기]**

이 트리거 모듈은 특정한 필드가 업데이트될 때 시나리오를 실행합니다. 모듈은 특정한 필드의 이전 값과 새 값을 모두 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형]</td> 
   <td> <p>모듈에서 볼 Workfront 레코드의 유형을 선택합니다.</p> <p>예를 들어, 작업에서 레코드 필드가 업데이트될 때마다 시나리오 실행을 시작하려면 [!UICONTROL 작업]를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 필드]</td> 
   <td>모듈이 업데이트를 확인할 필드를 선택합니다. 이러한 필드는 Workfront 관리자가 추적을 위해 설정한 필드를 반영합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 출력]</td> 
   <td>이 모듈의 출력 번들에 포함할 오브젝트 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

+++

+++ **[!UICONTROL 레코드 보기]**

이 트리거 모듈은 특정 유형의 오브젝트가 추가되거나 업데이트되거나 둘 다 사용될 때 시나리오를 실행합니다. 모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

출력에서 모듈은 각 레코드가 새로 추가되었는지 또는 업데이트되었는지 여부를 나타냅니다.

시나리오가 마지막으로 실행된 이후 추가 및 업데이트된 레코드는 새 레코드로 반환됩니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 필터]</td> 
   <td> <p>시나리오를 [!UICONTROL 새 레코드만], [!UICONTROL 업데이트된 레코드만] 또는 [!UICONTROL 새 레코드 및 업데이트된 레코드] 중 어떻게 볼 것인지 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 레코드 유형]</td> 
   <td> <p>모듈에서 볼 Workfront 레코드의 유형을 선택합니다.</p> <p>예를 들어, 새 프로젝트가 만들 때마다 시나리오를 시작하려면 [!UICONTROL 프로젝트]를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 참조]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 참조 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 출력]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 컬렉션 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 선택 필터]</td> 
   <td> <p>(고급) API 코드 문자열을 입력하여 기준을 개선할 추가 매개변수나 코드를 정의합니다. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제한]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

+++


### 액션

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL 오브젝트 변환]**

이 액션 모듈은 다음 중 하나를 변환합니다.

* 프로젝트로 문제 변환
* 작업으로 문제 변환
* 프로젝트로 작업 변환

>[!NOTE]
>
>2024년 7월부터 오브젝트를 변환할 때 사용자 정의 양식을 포함할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 오브젝트 유형]</td> 
   <td> <p>변환하려고 하는 오브젝트 유형을 선택합니다. 이는 오브젝트가 변환되기 전에 가지는 유형입니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 변환 대상]</td> 
   <td>변환할 오브젝트를 선택합니다. 이는 오브젝트가 변환되기 후에 가지는 유형입니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;오브젝트&gt; ID]</td> 
   <td> <p>오브젝트의 ID를 입력합니다. </p> <p>메모: 오브젝트의 ID를 입력할 때 오브젝트의 이름을 입력한 후 다음 목록에서 선택할 수 있습니다. 그러면 모듈이 해당 ID를 필드에 입력합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 템플릿 ID]</td> 
   <td> <p>프로젝트로 변환하는 경우 프로젝트에 사용할 템플릿 ID를 선택합니다.</p> <p>메모: 오브젝트의 ID를 입력할 때 오브젝트의 이름을 입력한 후 다음 목록에서 선택할 수 있습니다. 그러면 모듈이 해당 ID를 필드에 입력합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 사용자 정의 양식]</td> 
   <td>새로 변환된 오브젝트에 추가할 사용자 정의 양식을 선택한 다음, 사용자 정의 양식의 필드 값을 입력합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 선택 사항]</td> 
   <td> <p>오브젝트를 변환할 때 원하는 옵션을 활성화합니다. 어떤 오브젝트로 변환할지 또는 어떤 오브젝트에서 변환할지에 따라 옵션이 제공됩니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 기본 필드 복사]</td> 
   <td> <p>원본 오브젝트에서 새 오브젝트로 기본 필드를 복사하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 사용자 정의 양식 복사]</td> 
   <td> <p>원본 오브젝트에서 새 오브젝트로 기본 필드를 복사하려면 이 옵션을 활성화합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 레코드 만들기]** 

이 액션 모듈은 Workfront에서 프로젝트, 작업 또는 문제와 같은 오브젝트를 만들며, 새 오브젝트에 사용자 정의 양식을 추가할 수 있습니다. 모듈을 사용하면 모듈에서 사용할 수 있는 오브젝트의 필드를 선택할 수 있습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

최소 입력 필드 수를 입력해야 합니다. 예를 들어, 문제를 만들고 싶다면 프로젝트 ID 필드에 유효한 상위 프로젝트 ID를 제공하여 문제가 Workfront에서 발생해야 하는 위치를 표시해야 합니다. 매핑 패널을 사용하여 시나리오의 다른 모듈에서 이 정보를 매핑하거나 이름을 입력한 다음 목록에서 선택하여 수동으로 입력할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형]</td> 
   <td> <p>모듈에서 만들 Workfront 레코드의 유형을 선택합니다.</p> <p>예를 들어, 프로젝트를 만들고 싶다면 드롭다운 목록에서 [!UICONTROL 프로젝트]를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 매핑할 필드 선택]</td> 
   <td> <p>데이터 입력에 사용할 필드를 선택합니다. 이렇게 하면 필요 없는 필드를 스크롤할 필요 없이 이 필드를 사용할 수 있습니다. 그런 다음 이러한 필드에 데이터를 입력하거나 매핑할 수 있습니다.</p> <p>사용자 정의 양식의 필드는 <b>[!UICONTROL 사용자 정의 양식 첨부]</b> 필드를 사용합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 사용자 정의 양식 첨부]</td> 
   <td>새 오브젝트에 추가할 사용자 정의 양식을 선택하고 값을 입력할 필드를 선택한 다음 해당 필드에 값을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

>[!NOTE]
>
>* 오브젝트의 ID를 입력할 때 오브젝트의 이름을 입력한 후 다음 목록에서 선택할 수 있습니다. 그러면 모듈이 해당 ID를 필드에 입력합니다.
>* 사용자 정의 필드나 [!UICONTROL 메모] 오브젝트(댓글 또는 답장)의 텍스트를 입력할 때, [!UICONTROL 메모 텍스트] 필드의 HTML 태그를 사용하여 굵은 글씨나 기울임꼴과 같은 서식 있는 텍스트를 만들 수 있습니다.
>



>[!NOTE]
>
>사용자는 비활성화 및 승인 보류 중 상태로 생성됩니다. 조직이 Adobe Admin Console로 마이그레이션되고 승인 보류 중 배지가 몇 분 이내에 제거되지 않는 경우 사용자를 승인할 수 있습니다.
>
>* **개별 사용자 확인**
>
>      사용자 목록에서 개별 사용자를 확인할 수 있습니다.
>
>      1. 사용자 목록에서 사용자를 선택합니다.
>      1. 목록 헤더에서 세 개의 점 메뉴를 클릭합니다.
>      1. **승인**&#x200B;을 선택합니다.
>      1. 몇 분 후에 페이지를 새로 고침합니다.
>
>* **대규모 배치에 추가된 사용자 확인**
>
>   대규모 배치에 추가된 사용자를 확인하려면 Adobe Admin Console에 직접 사용자 배치를 추가할 수 있습니다.
>
>   지침은 Adobe 설명서의 [여러 사용자 관리 | 일괄 CSV 업로드](https://helpx.adobe.com/kr/enterprise/using/bulk-upload-users.html)를 참조하십시오.

+++

<!--

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Create a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module creates an object, such as a project, task, or issue in Workfront. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

Make sure you provide the minimum number of input fields. For example, if you want to create an issue, you need to provide a valid parent project ID in the Project ID field to indicate where the issue should live in Workfront. You can use the mapping panel to map this information from another module in your scenario, or you can enter it manually by typing in the name and then selecting it from the list.

This module does not attach custom forms when creating the object. To attach custom forms while creating an object, use the [!UICONTROL Create a record (attaching custom forms)] module.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to create.</p> <p>For example, if you want to create a Project, select [!UICONTROL Project] from the dropdown list.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL 사용자 정의 API 호출]**

이 액션 모듈을 사용하면 Workfront API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 Workfront 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

모듈은 다음 정보를 반환합니다.

* **[!UICONTROL 상태 코드]**(숫자): HTTP 요청의 성공 또는 실패를 나타냅니다. 이는 인터넷에서 찾을 수 있는 표준 코드입니다.
* **[!UICONTROL 헤더]**(오브젝트): 출력 본문과 관련이 없는 응답/상태 코드에 대한 상세한 컨텍스트입니다. 응답 헤더에 나타나는 모든 헤더가 응답 헤더인 것은 아니므로 일부 헤더는 유용하지 않을 수 있습니다.

  응답 헤더는 모듈을 구성할 때 선택한 HTTP 요청에 따라 달라집니다.

* **[!UICONTROL 본문]**(오브젝트): 모듈을 구성할 때 선택한 HTTP 요청에 따라 일부 데이터를 반환받을 수 있습니다. 해당 데이터, 예를 들어 GET 요청의 데이터는 이 오브젝트에 포함되어 있습니다.

시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p><code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>와 관련된 경로를 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API 버전]</td> 
   <td>모듈에서 사용할 Workfront API 버전을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion의 HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다. 요청의 콘텐츠 유형을 결정합니다.</p> <p>예:<code> {"Content-type":"application/json"}</code></p> <p>메모: 오류가 발생하고 원인을 파악하기 어렵다면 Workfront 설명서를 기반으로 헤더를 수정하는 것이 좋습니다. 사용자 정의 API 호출이 422 HTTP 요청 오류를 반환하는 경우 <code>"Content-Type":"text/plain"</code> 헤더를 사용해 보십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>예: <code>{"name":"something-urgent"}</code></p> <p>팁: 쿼리 매개변수 대신 JSON 본문을 통해 정보를 전송하는 것이 좋습니다.</p> </td> 
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

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

+++

+++ **[!UICONTROL 레코드 삭제]**

이 액션 모듈은 Workfront의 프로젝트, 작업 또는 문제와 같은 오브젝트를 삭제합니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 레코드의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 강제 삭제]</td> 
   <td>Workfront UI에서 삭제 확인을 요청하더라도 레코드가 삭제되도록 하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 비동기 삭제]</td> 
   <td>모듈이 비동기적으로 삭제하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>모듈이 삭제할 레코드의 고유한 Workfront ID를 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 오브젝트를 열고 URL 끝에 있는 텍스트를 “ID=” 뒤에 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형]</td> 
   <td>모듈에서 삭제할 Workfront 레코드의 유형을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

>[!NOTE]
>
>비동기 작업으로 인해 레코드가 삭제되지 않도록 다음 시나리오 구성을 권장합니다.
>
>1. 동기적으로 레코드를 삭제합니다.
>1. 레코드 삭제 모듈에 오류 처리를 추가하여 40초 시간 제한으로 인한 오류를 무시합니다.


+++

+++ **[!UICONTROL 문서 다운로드]**

이 액션 모듈은 Workfront에서 문서를 다운로드합니다.

레코드의 ID를 지정합니다.

모듈은 문서의 내용, 파일 이름, 파일 확장자 및 파일 크기를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 문서 ID]</td> 
   <td> <p>모듈을 다운로드할 문서의 고유한 Workfront ID를 매핑하거나 수동으로 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 오브젝트를 열고 URL 끝에 있는 텍스트를 “ID=” 뒤에 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

+++

### **미리 서명된 파일 URL 가져오기**

이 액션 모듈은 나중에 다른 API에서 사용할 수 있는 미리 서명된 파일 URL을 가져옵니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 문서 ID]</td> 
   <td> <p>미리 서명된 URL을 가져올 문서의 고유한 Workfront ID를 매핑하거나 수동으로 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 오브젝트를 열고 URL 끝에 있는 텍스트를 “ID=” 뒤에 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL 만료 시간]</td> 
   <td> <p>이 URL이 만료되기 전까지 존재하는 시간(분)을 입력하거나 매핑합니다. 기본값은 1분입니다.</p><p>이 값을 변경하려면 Workfront Fusion 팀에서 이 매개변수를 활성화해야 합니다. 활성화되지 않으면 입력한 숫자에 관계없이 값이 1분 동안 유지됩니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++ **[!UICONTROL 기타 액션]**

이 액션 모듈을 사용하면 API에 대한 액션을 수행할 수 있습니다.

>[!NOTE]
>
>2024년 7월부터 `convertToProject` 액션에 `copyCategories` 필드가 포함됩니다. `TRUE`로 설정하면 문제가 전환된 프로젝트에 모든 사용자 정의 양식이 포함됩니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 레코드 유형]</td> 
   <td> <p>모듈이 상호작용할 Workfront 레코드의 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 액션]</td> 
   <td> <p>모듈이 수행할 액션을 선택합니다.</p> <p>선택한 [!UICONTROL 레코드 유형]과 [!UICONTROL 액션]에 따라 추가 필드를 작성해야 할 수도 있습니다. 이 두 설정의 일부 조합은 레코드 ID만 필요할 수 있으며, 다른 조합(예: <strong>[!UICONTROL 레코드 유형]</strong> 프로젝트 및 [!UICONTROL 템플릿 첨부]는 <strong>[!UICONTROL 액션]</strong>에 대한 추가 정보(예: 오브젝트 ID 및 템플릿 ID)가 필요합니다.</p><p>일부 액션에 사용할 수 있는 옵션은 이 문서의 <a href="#misc-action-options" class="MCXref xref">기타 작업 옵션</a>을 참조하십시오.</p> <p>개별 필드에 대한 자세한 내용은 <a href="http://developer.workfront.com/">Workfront 개발자 설명서</a>를 참조하십시오. <p><strong>메모</strong>: 개발자 설명서 사이트에는 API 버전 14를 통해서만 정보가 포함되지만 API 호출에 대한 중요한 정보가 포함되어 있습니다. </p> 
    <ol> 
     <li value="1"> <p>Workfront 개발자 설명서 페이지의 왼쪽 탐색에서 레코드 유형을 선택합니다. 다음 유형은 자체 페이지를 가지고 있습니다.</p> 
      <ul> 
       <li> <p>[!UICONTROL 프로젝트]</p> </li> 
       <li> <p>[!UICONTROL 작업]</p> </li> 
       <li> <p>[!UICONTROL 문제]</p> </li> 
       <li> <p>[!UICONTROL 사용자]</p> </li> 
       <li> <p>[!UICONTROL 문서]</p> </li> 
      </ul> <p>다른 모든 레코드 유형의 경우 <b>[!UICONTROL 기타 오브젝트 및 엔드포인트]</b>를 선택하고 알파벳 순으로 정렬된 페이지에서 레코드 유형을 찾습니다.</p> </li> 
     <li value="2"> <p>적절한 레코드 유형의 페이지에서 액션(Ctrl-F 또는 Cmd-F)을 검색합니다.</p> </li> 
     <li value="3"> <p>선택한 액션 아래에서 사용 가능한 필드에 대한 설명을 확인합니다.</p> </li> 
    </ol> <p>메모:  <p>Workfront [!UICONTROL 기타 액션] 모듈을 통해 증명을 만들 때, 가장 좋은 방법은 고급 옵션 없이 증명을 만든 다음 [!DNL Workfront Proof] SOAP API를 사용하여 증명을 업데이트하는 것입니다.</p><p>이 모듈에서 사용하는 Workfront API로 증명을 만드는 방법에 대한 자세한 내용은 <a href="https://experienceleague.adobe.com/ko/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Adobe Workfront API를 통해 증명을 만들 때 고급 교정 옵션 추가</a>를 참조하십시오.</p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>모듈이 상호작용할 레코드의 고유한 Workfront ID를 입력하거나 매핑합니다.<p>ID를 가져오려면 브라우저에서 Workfront 오브젝트를 열고 URL 끝에 있는 텍스트를 “ID=” 뒤에 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

#### 기타 액션 옵션

##### 작업

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>액션</th> 
   <th>옵션</th> 
  </tr> 
  <tr> 
   <td>복사</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>이동</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### 문제

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>액션</th> 
   <th>옵션</th> 
  </tr> 
  <tr> 
   <td>복사</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>작업으로 전환</td> 
   <td>
   <ul>
   <li>preserveIssue<p>원래 문제를 유지하고 해결 방법을 이 작업에 연결</p></li>
   <li>preservePrimaryContact<p>이 작업에 대한 문제의 기본 연락처 액세스 허용</p></li>
   <li>preserveCompletionDate<p>문제의 계획된 완료 일자 유지</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>프로젝트로 전환</td> 
   <td>
   <ul>
   <li>preserveIssue<p>원래 문제를 유지하고 해결 방법을 이 작업에 연결</p></li>
   <li>preservePrimaryContact<p>이 작업에 대한 문제의 기본 연락처 액세스 허용</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### 프로젝트

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>액션</th> 
   <th>옵션</th> 
  </tr> 
  <tr> 
   <td>복사</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>템플릿 첨부 / 템플릿으로 저장</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>목표 지우기</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>재무 데이터 지우기</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>대기열 속성 및 문제 설정 지우기</p></li>
   <li>clearPredecessors</li>
   <li>clearRisk</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>미리 알림 지우기</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL 레코드 읽기]**

이 액션 모듈은 단일 레코드에서 데이터를 가져옵니다.

레코드의 ID를 지정합니다. 모듈이 읽을 관련 레코드를 지정할 수도 있습니다.

예를 들어, 모듈이 읽고 있는 레코드가 프로젝트인 경우 프로젝트의 작업을 읽도록 지정할 수 있습니다.

모듈은 지정한 출력 필드에서 데이터 배열을 반환합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL 연결]</td>
    <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 레코드 유형]</td>

<td>모듈이 읽을 Workfront 오브젝트 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 출력]</td>

<td> <p>이 모듈의 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 출력 사용자 정의 양식]</td>
     <td> <p>이 모듈의 출력 번들에 포함할 사용자 정의 양식을 선택한 다음, 출력에 포함할 사용자 정의 양식 중에서 특정 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 참조]</td>
   <td>출력에 포함할 참조 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 컬렉션]</td>
   <td>출력에 포함할 참조 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>모듈이 읽을 레코드의 고유한 Workfront ID를 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 오브젝트를 열고 URL 끝에 있는 텍스트를 “ID=” 뒤에 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

+++

<!--

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Read a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module retrieves data from a single record.

You specify the ID of the record. You can also specify which related records you want the module to read.

For example, if the record that the module is reading is a project, you can specify that you want the project's tasks read.

The module returns an array of data from the output fields you specified.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
  
   <td>Choose the Workfront object type that you want the module to read.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
  
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Enter the unique Workfront ID of the record that you want the module to read.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++

-->

+++ **이벤트 페이로드 버전 업데이트**

Workfront는 최근 이벤트 구독 서비스의 신규 버전을 출시했습니다. 신규 버전은 Workfront API의 변경이 아니라 이벤트 구독 기능의 변경입니다. 이 액션 모듈은 이 시나리오에 사용된 이벤트 페이로드 버전을 업데이트합니다.

새 이벤트 구독 버전에 대한 자세한 내용은 Workfront 설명서의 [이벤트 구독 버전 관리](https://experienceleague.adobe.com/ko/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning)를 참조하십시오.

웨비나 녹화를 포함한 이벤트 구독 업그레이드 중 Workfront Fusion 시나리오 유지에 대한 리소스는 [이벤트 구독 V2 업그레이드 중 Fusion 시나리오 유지](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182)를 참조하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 버전]</td> 
   <td> 이 페이로드에 사용할 이벤트 구독의 버전을 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **레코드 업데이트**


이 액션 모듈은 프로젝트, 작업 또는 문제와 같은 오브젝트를 업데이트합니다. 모듈을 사용하면 모듈에서 사용할 수 있는 오브젝트의 필드를 선택할 수 있습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 오브젝트의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>모듈을 업데이트할 레코드의 고유한 Workfront ID를 입력합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 오브젝트를 열고 URL 끝에 있는 텍스트를 “ID=” 뒤에 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>모듈을 업데이트할 Workfront 레코드의 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>데이터 입력에 사용할 필드를 선택합니다. 이렇게 하면 필요 없는 필드를 스크롤할 필요 없이 이 필드를 사용할 수 있습니다. 그런 다음 이러한 필드에 데이터를 입력하거나 매핑할 수 있습니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>새 레코드에서 필드 값을 제공할 사용자 정의 양식을 선택합니다. 양식을 선택한 후 해당 양식의 필드에 대한 데이터를 입력합니다.<p> 이 모듈에 첨부할 양식의 필드 값을 제공하려면 매핑할 필드 섹션에 사용자 정의 양식 ID를 포함합니다.</td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

>[!NOTE]
>
> 사용자 정의 필드나 [!UICONTROL 메모] 오브젝트(댓글 또는 답장)의 텍스트를 입력할 때, [!UICONTROL 메모 텍스트] 필드의 HTML 태그를 사용하여 굵은 글씨나 기울임꼴과 같은 서식 있는 텍스트를 만들 수 있습니다.


+++

<!--

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Update a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module updates an object, such as a project, task, or issue. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  object and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Enter the unique Workfront ID of the record that you want the module to update.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to update.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need. You can then enter or map data into these fields.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL 문서 업로드]**

이 액션 모듈은 프로젝트, 작업 또는 문제와 같은 Workfront 오브젝트에 문서를 업로드합니다. 이 모듈은 문서를 청크 단위로 업로드하므로 Workfront의 업로드 프로세스가 더 원활해집니다.

이 모듈은 이전 모듈보다 더 큰 파일을 처리할 수 있으며, Ultimate Workfront 패키지를 사용하는 조직에 대한 단계별 롤아웃의 일부입니다.

문서의 위치, 업로드할 파일, 그리고 파일의 새 이름(선택 사항)을 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 정의 필드 및 값과 함께 문서의 ID와 모든 연결된 필드를 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 관련 레코드 ID]</td> 
   <td>문서를 업로드할 레코드의 고유한 Workfront ID를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 관련 레코드 유형]</td> 
   <td>모듈이 문서를 업로드할 Workfront 레코드 유형을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 폴더 ID]</td> 
   <td>관련 레코드의 유형에 따라 폴더 ID를 입력하거나 매핑해야 할 수도 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

[각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형](#workfront-object-types-available-for-each-workfront-module)에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.

+++

<!--

+++ **[!UICONTROL Upload Document (Legacy)]**

This action module uploads a document to a Workfront object, such as a project, task, or issue. It uploads the entire document at once. 

You specify the location for the document, the file you want to upload, and an optional new name for the file.

The module returns the ID of the document and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Enter the unique Workfront ID of the record to which you want to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Select the type of Workfront record where you want the module to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Depending on the type of related record, you may need to enter or map a folder ID.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).


+++
-->

### 검색 결과

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL 관련 레코드 읽기]**

이 검색 모듈은 특정 상위 오브젝트에서 지정한 검색 쿼리와 일치하는 레코드를 읽습니다.

출력에 포함할 필드를 지정합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 레코드 유형]</td> 
   <td> <p>연결된 레코드를 읽을 상위 레코드(Workfront 오브젝트)의 유형을 선택합니다.</p> <p>이 문서의 <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">각 Workfront 모듈에서 사용할 수 있는 Workfront 오브젝트 유형</a>에서 이 모듈을 사용할 수 있는 Workfront 오브젝트 유형 목록을 확인하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 상위 레코드 ID]</td> 
   <td> <p>읽으려는 관련 레코드의 상위 레코드 ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 Workfront 오브젝트를 열고 URL 끝에 있는 텍스트를 “ID=” 뒤에 복사합니다. 예: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 컬렉션]</td> 
   <td>모듈이 읽을 하위 레코드 유형을 선택하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 출력]</td> 
   <td> <p>이 모듈의 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 검색]**

이 검색 모듈은 Workfront에서 지정한 검색 쿼리와 일치하는 오브젝트의 레코드를 찾습니다.

시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형]</td> 
   <td> <p>모듈이 검색할 Workfront 레코드 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 사용자 정의 양식 목록]</td> 
   <td> <p>하나 이상의 사용자 정의 양식을 선택합니다. 이러한 사용자 정의 양식의 필드는 검색 쿼리에 사용할 수 있습니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 결과 세트]</td> 
   <td>모듈이 검색 기준과 일치하는 첫 번째 결과를 가져올지 아니면 일치하는 모든 결과를 가져올지 지정하려면 옵션을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 최대]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 검색 기준 필드]</td> 
   <td> <p>검색 기준에 사용할 필드를 선택합니다. 이 필드는 검색 기준 드롭다운에서 사용할 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 검색 기준]</td> 
   <td> <p>검색할 필드, 쿼리에 사용할 연산자, 필드에서 검색할 값을 입력합니다.</p> <p>메모: 검색 기준에 <code>username </code>을 사용하지 마십시오. Workfront의 API 쿼리에 <code>username </code>을 포함시키면 사용자가 Workfront에 로그인하게 되며, 검색이 실패하게 됩니다.</p> <p>메모: <code>In</code> 및 <code>NotIn</code>은(는) 배열을 사용하여 작업합니다. 입력은 배열 형식이어야 합니다.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 출력]</td> 
   <td> <p>이 모듈의 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 참조]</td> 
   <td>검색에 포함할 참조 필드를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 컬렉션]</td> 
   <td>검색에 추가할 컬렉션을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 검색(이전)]**

>[!IMPORTANT]
>
>이 모듈은 검색 레코드 모듈로 교체되었습니다. 새로운 시나리오에서 해당 모듈을 사용하는 것이 좋습니다.
>이 모듈을 사용하는 기존 시나리오는 예상대로 계속 작동합니다. 이 모듈은 2025년 5월에 모듈 선택기에서 제거됩니다.

이 검색 모듈은 Workfront에서 지정한 검색 쿼리와 일치하는 오브젝트의 레코드를 찾습니다.

시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결]</td> 
   <td> <p>Workfront 앱을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서의 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Workfront을 Workfront Fusion에 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 레코드 유형]</td> 
   <td> <p>모듈이 검색할 Workfront 레코드 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 결과 세트]</td> 
   <td>모듈이 검색 기준과 일치하는 첫 번째 결과를 가져올지 아니면 일치하는 모든 결과를 가져올지 지정하려면 옵션을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 최대]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 검색 기준 필드]</td> 
   <td> <p>검색 기준에 사용할 필드를 선택합니다. 이 필드는 검색 기준 드롭다운에서 사용할 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 검색 기준]</td> 
   <td> <p>검색할 필드, 쿼리에 사용할 연산자, 필드에서 검색할 값을 입력합니다.</p> <p>메모: 검색 기준에 <code>username </code>을 사용하지 마십시오. Workfront의 API 쿼리에 <code>username </code>을 포함시키면 사용자가 Workfront에 로그인하게 되며, 검색이 실패하게 됩니다.</p> <p>메모: <code>In</code> 및 <code>NotIn</code>은(는) 배열을 사용하여 작업합니다. 입력은 배열 형식이어야 합니다.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 출력]</td> 
   <td> <p>이 모듈의 출력에 포함할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 참조]</td> 
   <td>검색에 포함할 참조 필드를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 컬렉션]</td> 
   <td>검색에 추가할 컬렉션을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## 각 Workfront 모듈에 사용할 수 있는 Workfront 오브젝트 유형

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**각 Workfront 트리거 모듈에 사용할 수 있는 오브젝트 유형**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 레코드 보기]</th> 
   <th>[!UICONTROL 필드 보기]</th> 
   <th>[!UICONTROL 이벤트 보기]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>승인 진행</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>할당</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>기준선</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 청구 기록 </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>과금 요율</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>회사</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>대시보드</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서 폴더</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문서 요청</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문서 버전</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>경비 유형</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>그룹</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>시간</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>시간 유형</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문제</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>반복</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업 역할</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>분개 기입</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤 경로</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>메모</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>메모 태그</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>포트폴리오</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로그램</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로젝트</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로젝트 사용자</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>교정쇄 승인</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>예약 시간* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>보고서</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>위험</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험 유형</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>단계 승인자</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>팀</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>템플릿 작업</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>타임시트</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>사용자</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>업데이트</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**각 Workfront 작업 모듈에 사용할 수 있는 오브젝트 유형**

>[!NOTE]
>
>[!UICONTROL 문서 다운로드] 모듈은 Workfront 오브젝트 유형이 구성에 포함되지 않기 때문에 이 테이블에 포함되지 않습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 레코드 만들기]</th> 
   <th>[!UICONTROL 레코드 업데이트]</th> 
   <th>[!UICONTROL 레코드 삭제]</th> 
   <th>[!UICONTROL 문서 업로드]</th> 
   <th>[!UICONTROL 레코드 읽기]</th> 
   <th>[!UICONTROL 사용자 정의 API 호출]</th> 
   <th>[!UICONTROL 기타 액션]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>승인 진행</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>할당</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>기준선</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>청구 기록</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>과금 요율</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>회사</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서 폴더</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서 버전</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>환율</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>경비 유형</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>외부 문서</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>그룹</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>시간</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>시간 유형</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문제</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>반복</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업 역할</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>분개 기입</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>마일스톤</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤 경로</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>메모</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>메모 태그</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>포트폴리오</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로그램</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로젝트</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로젝트 사용자</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>예약 시간* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험 유형</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>단계 승인자</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>팀</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿 작업</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>타임시트</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>사용자</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>업데이트</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**각 Workfront 검색 모듈에 사용할 수 있는 오브젝트 유형**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 검색]</th> 
   <th>[!UICONTROL 관련 레코드 읽기]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>승인 진행</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>할당</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>청구 기록</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>과금 요율</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>회사</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서 폴더</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>문서 버전</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>경비 유형</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>그룹</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>시간</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>시간 유형</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>문제</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>반복</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업 역할</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>분개 기입</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>마일스톤 경로</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>메모</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>메모 태그</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>포트폴리오</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로그램</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>프로젝트</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>프로젝트 사용자</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>예약 시간* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>위험 유형</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>단계 승인자</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>작업</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>팀</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>템플릿 작업</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>타임시트</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>사용자</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>사용자 위임</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

예상대로 작동하는지 다시 한 번 확인하는 것이 좋습니다.

+++

## Workfront > [!UICONTROL 이벤트 보기] 모듈의 이벤트 구독 필터

>[!NOTE]
>
>* [!UICONTROL 이벤트 보기] 모듈에서 이벤트 구독 필터를 사용하는 것이 좋습니다.
>
>* Workfront는 최근 이벤트 구독 서비스의 신규 버전을 출시했습니다. 신규 버전은 Workfront API의 변경이 아니라 이벤트 구독 기능의 변경입니다. 이 액션 모듈은 이 시나리오에 사용된 이벤트 페이로드 버전을 업데이트합니다.
>
>   새 이벤트 구독 버전에 대한 자세한 내용은 Workfront 설명서의 [이벤트 구독 버전 관리](https://experienceleague.adobe.com/ko/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning)를 참조하십시오.
>
>   웨비나 녹화를 포함한 이벤트 구독 업그레이드 중 Workfront Fusion 시나리오 유지에 대한 리소스는 [이벤트 구독 V2 업그레이드(https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182) 중 Fusion 시나리오 유지]를 참조하십시오.

Workfront [!UICONTROL 이벤트 보기] 모듈은 Workfront API에서 이벤트 구독을 만드는 웹후크를 기반으로 시나리오를 트리거합니다. 이벤트 구독은 웹후크로 전송되는 이벤트를 결정하는 데이터 세트입니다. 예를 들어, 문제를 확인하는 [!UICONTROL 이벤트 보기] 모듈을 설정하면 이벤트 구독은 문제와 관련된 이벤트만 전송합니다.

Fusion 사용자는 이벤트 구독 필터를 사용하여 사용 사례에 더 적합한 이벤트 구독을 만들 수 있습니다. 예를 들어, Workfront API에서 이벤트 구독을 설정하여 특정 프로젝트에 있는 문제만 웹후크로 전송하여 [!UICONTROL 이벤트 보기] 모듈이 해당 프로젝트의 문제만 트리거하도록 할 수 있습니다. 더 좁은 트리거를 만드는 기능은 관련 없는 트리거를 줄여 시나리오 설계를 개선합니다.

이는 Workfront Fusion 시나리오에서 필터를 설정하는 것과 다릅니다. 이벤트 구독 필터 없으면 웹후크는 선택한 오브젝트 유형과 관련된 모든 이벤트를 수신합니다. 이러한 이벤트의 대부분은 시나리오와 무관하므로 시나리오를 계속 진행하기 전에 필터링해야 합니다.

Workfront > 이벤트 보기 필터에서 다음 연산자를 사용할 수 있습니다.

* 다음과 같음
* 다음과 같지 않음
* 다음보다 큼
* 다음보다 작음
* 다음보다 크거나 같음
* 다음보다 작거나 같음
* 다음 포함
* 있음
   * 이 연산자는 값이 필요하지 않으며, 값 필드가 없습니다.
* 존재하지 않음
   * 이 연산자는 값이 필요하지 않으며, 값 필드가 없습니다.
* 변경됨
   * 이 연산자는 값이 필요하지 않으며, 값 필드가 없습니다.
   * 이 연산자는 상태 필드를 무시합니다.
   * `Changed`를 사용할 때, **레코드 원본** 필드에서 **업데이트된 이벤트만** 선택합니다.

>[!IMPORTANT]
>
>기존 Workfront 웹후크에서는 필터를 편집할 수 없습니다. Workfront 이벤트 구독에 대해 서로 다른 필터를 설정하려면 현재 웹후크를 제거하고 새 웹후크를 만듭니다.

>[!INFO]
>
>**예:** 특정 사용자인 Ana에게 할당된 새로운 문제를 처리하는 시나리오를 가정해 보겠습니다.
>
>### 이벤트 구독 필터를 사용하여 이벤트 필터링(권장)
>
>이벤트 필터를 사용하여 문제가 생성될 때 Ana에 문제가 할당되면 시나리오를 트리거하도록 웹후크를 설정할 수 있습니다. Ana에게는 userID b378489d8f7cd3cee0539260720a84b7이 있습니다.
>
>![이벤트 필터](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>하루에 100개의 문제가 만들어지지만 그 중 두 개만 Ana에 할당되면 시나리오는 두 번 실행됩니다.
>
>### 시나리오 내 이벤트 필터링(권장되지 않음)
>
>Ana에 할당된 문제만 처리되도록 이벤트를 필터링하려면 [!UICONTROL 이벤트 보기] 모듈 뒤에 필터를 만들 수 있습니다.
>
>![이벤트 필터 없음](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>하루에 100개의 문제가 만들어지지만 그 중 두 개만 Ana에 할당되면 시나리오는 100번 실행됩니다. 98개의 실행이 필터에서 멈추지만 트리거 모듈은 여전히 모든 실행에서 데이터를 소비하고 작업을 수행합니다.

Workfront 이벤트 구독에 대한 자세한 내용은 [FAQ - 이벤트 구독](https://experienceleague.adobe.com/ko/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq)을 참조하십시오.

웹후크에 대한 자세한 내용은 [Adobe Workfront Fusion의 인스턴트 트리거(웹후크)](/help/workfront-fusion/references/modules/webhooks-reference.md)를 참조하십시오.

시나리오의 필터에 대한 자세한 내용은 [시나리오에 필터 추가](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md)를 참조하십시오.
