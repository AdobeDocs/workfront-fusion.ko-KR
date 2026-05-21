---
title: NetSuite 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL NetSuite]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 9bf67fc4-d93b-4868-ad1a-021c98637905
TQID: https://experienceleague.adobe.com/IUhCQh11M9IWrk8DsyUlcdUmDil2UOiqpKGB3GPHgM0
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 593
ht-degree: 83%

---

# [!DNL NetSuite] 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL NetSuite]를 사용하는 워크플로를 자동화할 수 있으며 여러 제3자 애플리케이션 및 서비스에 연결할 수 있습니다.

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

[!DNL NetSuite] 모듈을 사용하려면 [!DNL NetSuite] 계정이 있어야 합니다.

## NetSuite API 정보

NetSuite 커넥터는 다음을 사용합니다.

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
   <td>v1.0.10</td> 
  </tr>
 </tbody> 
 </table>

## NetSuite에 대한 연결 만들기

사용자의 [!DNL NetSuite] 모듈에 연결하려면:

1. [!DNL NetSuite] 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

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
            <p>이 연결의 이름을 입력합니다.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 유형] </td>
          <td>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</p>
        </tr>
       <tr>
          <td role="rowheader">[!UICONTROL 계정 ID] </td>
          <td>NetSuite 계정의 ID를 입력합니다.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
          <td>NetSuite 계정의 클라이언트 ID를 입력합니다. NetSuite 클라이언트 자격 증명에서 찾을 수 있습니다.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
          <td>NetSuite 계정의 클라이언트 암호를 입력합니다.</p>
        </tr>
        </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

## [!DNL NetSuite] 모듈 및 해당 필드

[!DNL NetSuite] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL NetSuite] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


### [!UICONTROL 사용자 정의 API 호출]

이 액션 모듈을 사용하면 [!DNL NetSuite] API에 인증된 사용자 정의 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL NetSuite] 모듈로는 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

작업은 지정한 엔티티 유형(Allocadia 객체 유형)을 기반으로 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결]</td> 
   <td> <p>[!DNL NetSuite] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-netsuite" class="MCXref xref">[!DNL NetSuite]</a>에 연결 만들기 를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>다음 URL 형식을 사용하십시오.</p> <p><code>https://{accountID}.suitetalk.api.netsuite.com/services/rest/record/{version}/{resource}?{query-parameters}</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 헤더]</td> 
   <td> <p>표준 JSON 오브젝트 형태로 요청의 헤더를 추가합니다.</p> <p>예: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
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
