---
title: Microsoft Dynamics 365 재무 및 운영 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Microsoft Dynamics 365 재무 및 운영을 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Microsoft Dynamics 365]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

>[!NOTE]
>
>[!DNL Microsoft Dynamics 365 Finance and Operations] 커넥터가 [!DNL Dynamics 365]을(를) 지원하지 않습니다.
>
>Microsoft Dynamics 365 모듈의 경우 [[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md)을(를) 참조하십시오.



시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 연결 만들기

Microsoft Dynamics 365 Finance and Operations 모듈에 대한 연결을 만들려면 다음을 수행하십시오.

1. Microsoft Dynamics 365 재무 및 작업 모듈에서 연결 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

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
          <p>표준 Dynamics Finance and Operations 연결을 만드는지 아니면 인증 코드를 사용하여 연결을 만드는지 선택하십시오.</p>
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
        <td>Dynamics Finance and Operations [!UICONTROL Client ID]을(를) 입력하십시오.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Dynamics Finance and Operations [!UICONTROL Client Secret]을(를) 입력하십시오. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tenant ID]</td>
        <td>Dynamics Finance and Operations 테넌트 ID를 입력합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">리소스</td>
        <td>Dynamics Finance and Operations 계정의 URL을 입력하십시오(https:// 제외).</td>
        </tr>
      </tbody>
    </table>

1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.



## Microsoft Dynamics 365 재무 및 운영 모듈 및 해당 필드

>[!IMPORTANT]
>
>Dynamics 365 F&amp;O API를 통해 사용할 수 있는 데이터 엔터티는 인스턴스에 따라 다를 수 있습니다. API를 통해 사용할 수 있는 엔티티를 잘 모르는 경우 &quot;데이터&quot; 엔드포인트를 사용하여 인스턴스의 엔티티를 살펴보는 것이 좋습니다. Dynamics 365 Finance and Operations의 &quot;데이터&quot; 끝점은 OData 서비스에 액세스하기 위한 루트 URL입니다. 이 끝점을 사용하면 표준 OData 프로토콜을 사용하여 시스템에 의해 노출된 다양한 데이터 엔티티와 상호 작용할 수 있습니다.
>
>사용자 지정 API 호출 모듈을 사용하여 이러한 엔티티를 검색할 수 있습니다.
>
><!--For more information -->



### 엔티티 항목 만들기

이 작업 모듈은 Microsoft Dynamics 365 Finance and Operations에서 새 엔티티 항목을 만듭니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Microsoft Dynamics 365 Finance and Operations를 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection" class="MCXref xref">연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>생성할 Dynamics Finance and Operations 엔터티 유형을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>새 엔티티 항목에 포함할 데이터가 포함된 JSON 본문을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>



### 엔티티 항목 삭제

이 작업 모듈은 Dynamics Finance and Operations에서 엔티티 항목을 삭제합니다. 항목은 기본 키 필드로 식별됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Microsoft Dynamics 365 Finance and Operations를 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection" class="MCXref xref">연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>삭제할 Dynamics Finance and Operations 엔티티 유형을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> 기본 키 필드는 항목을 식별합니다. 제공하려는 각 기본 키 필드에 대해 <b>항목 추가</b>를 클릭하고 해당 항목을 식별하는 고유 키 및 값을 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

### 사용자 지정 API 호출 만들기

이 작업 모듈은 Dynamics Finance and Operations API를 사용자 지정 호출합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>Microsoft Dynamics 365 Finance and Operations를 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection" class="MCXref xref">연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Dynamics Finance and Operations URL과 관련된 경로를 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 요청의 콘텐츠 유형을 결정합니다.</p> <p>For example,<code> {"Content-type":"application/json"}</code></p> <p>참고: 오류가 발생하여 원래 위치를 확인하기 어려운 경우 [!DNL Workfront] 설명서를 기반으로 헤더를 수정하는 것이 좋습니다. 사용자 지정 API 호출이 422 HTTP 요청 오류를 반환하는 경우 <code>"Content-Type":"text/plain"</code> 헤더를 사용해 보십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>For example: <code>{"name":"something-urgent"}</code></p> <p>팁: 쿼리 매개 변수보다는 JSON 본문을 통해 정보를 전송하는 것이 좋습니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>



### 엔티티 항목 읽기

이 작업 모듈은 엔티티 항목에서 데이터를 반환합니다. 항목은 기본 키 필드로 식별됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Microsoft Dynamics 365 Finance and Operations를 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection" class="MCXref xref">연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>읽으려는 Dynamics Finance and Operations 엔티티 유형을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> 기본 키 필드는 항목을 식별합니다. 제공하려는 각 기본 키 필드에 대해 <b>항목 추가</b>를 클릭하고 해당 항목을 식별하는 고유 키 및 값을 입력하거나 매핑합니다. </td> 
  </tr> 
 </tbody> 
</table>

### 엔티티 항목 업데이트

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Microsoft Dynamics 365 Finance and Operations를 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서의 <a href="#create-a-connection" class="MCXref xref">연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>갱신할 Dynamics Finance and Operations 엔티티 유형을 입력하거나 매핑합니다.</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> 기본 키 필드는 항목을 식별합니다. 제공하려는 각 기본 키 필드에 대해 <b>항목 추가</b>를 클릭하고 해당 항목을 식별하는 고유 키 및 값을 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>새 엔티티 항목에 포함할 데이터가 포함된 JSON 본문을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색

이 검색 모듈은 사용자가 지정하는 기준에 따라 결과를 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">[!DNL Workfront]을(를) [!DNL Workfront Fusion]</a>에 연결 을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entity]</td> 
   <td>검색할 Dynamics Finance and Operations 엔티티 유형을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>검색할 필드, 쿼리에 사용할 연산자 및 검색할 값을 필드에 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort by]</td> 
   <td> <p>결과를 정렬할 필드를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!--

### List All

This module lists all records for a given entity.  The item is identified by its Primary key fields.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
     <td>Choose the Dynamics Finance and Operations entity type that you want the module to list.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
     <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Watch Record

This trigger module starts a scenario when a record of the given type is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of [!DNL Workfront] record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to [!DNL Workfront] logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->
