---
title: Salesforce 모듈
description: Adobe Workfront Fusion 시나리오에서는 Salesforce을 사용하는 워크플로를 자동화할 뿐만 아니라 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2603'
ht-degree: 0%

---

# [!DNL Salesforce]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Salesforce]을(를) 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.

Salesforce 커넥터에 대한 비디오 소개는 다음을 참조하십시오.

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

>[!NOTE]
>
>* [!DNL Salesforce]의 모든 버전에 API 액세스 권한이 있는 것은 아닙니다. 자세한 내용은 [!DNL Salesforce] 커뮤니티 사이트에서 API 액세스 권한이 있는 [!DNL Salesforce] 버전에 대한 정보를 참조하십시오.
>* [!DNL Salesforce] API에서 반환된 특정 오류에 대한 자세한 내용은 [!DNL Salesforce] API 문서를 참조하십시오. [!DNL Salesforce] API의 상태를 통해 가능한 서비스 중단을 확인할 수도 있습니다.
>

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

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

보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 [!DNL Workfront] 관리자에게 문의하세요.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

## 전제 조건

[!DNL Salesforce] 모듈을 사용하려면 [!DNL Salesforce] 계정이 있어야 합니다.

## Salesforce API 정보

Salesforce 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> {{connection.instanceUrl}}</td>
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v46.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Salesforce]개 개체 검색 정보

객체를 검색할 때 개별 검색어를 입력하거나 와일드카드 및 연산자를 사용하여 보다 복잡한 질의를 생성할 수 있습니다.

* 별표 와일드카드(\*)를 0개 이상의 문자 대용으로 사용합니다. 예를 들어 Ca\*를 검색하면 Ca로 시작하는 항목이 검색됩니다
* 물음표 와일드카드(?) 사용 단일 문자의 대용품입니다. 예를 들어 Jo?n을 검색하면 John 또는 Joan이라는 용어가 있지만 Jon은 아닌 항목이 검색됩니다
* 따옴표 연산자(&quot; &quot;)를 사용하여 정확한 구문 일치를 찾습니다. 예: &quot;Monday meeting&quot;

검색 가능성에 대한 자세한 내용은 SOQL 및 SOSL에 대한 [!DNL Salesforce] 개발자 설명서를 참조하십시오.

## [!DNL Salesforce]개 모듈 및 해당 필드

* [트리거](#triggers)
* [작업](#actions)
* [검색 결과](#searches)

### 트리거

* [[!UICONTROL Watch for Records]](#watch-for-records)
* [[!UICONTROL Watch Outbound Messages]](#watch-outbound-messages)
* [[!UICONTROL Watch a field]](#watch-a-field)

#### [!UICONTROL Watch for Records]

이 트리거 모듈은 오브젝트 내의 레코드가 생성되거나 업데이트될 때 시나리오를 실행한다. 모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드 또는 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>모듈을 감시할 [!DNL Salesforce] 레코드 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Fields]</td> 
   <td>모듈에서 조사할 필드를 선택합니다. 사용 가능한 필드는 레코드 유형에 따라 다릅니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>선택한 유형의 새 레코드만 시나리오에 표시할지, 선택한 유형의 새 레코드와 해당 유형의 다른 모든 레코드 변경 사항을 시나리오에 표시할지 여부를 결정합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Outbound Messages]

이 트리거 모듈은 누군가가 메시지를 보낼 때 시나리오를 실행합니다. 모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드 또는 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈에는 추가 설정이 필요합니다.

1. [!DNL Salesforce] 설정 페이지로 이동합니다.

   설정 페이지에 액세스하려면 [!DNL Salesforce] 계정의 오른쪽 상단 모서리에서 &quot;[!UICONTROL Setup]&quot; 단추를 찾아 클릭합니다. [!DNL Salesforce] 설정 페이지에서 왼쪽의 &quot;[!UICONTROL Quick Find / Search]&quot; 막대를 찾습니다. &quot;[!UICONTROL Workflow Rules]&quot;을(를) 검색합니다.

1. **[!UICONTROL Workflow Rules]**&#x200B;을(를) 클릭합니다.
1. 표시되는 [!UICONTROL Workflow Rules] 페이지에서 **[!UICONTROL New Rule]**&#x200B;을(를) 클릭하고 규칙이 적용될 개체 유형을 선택합니다(예: Opportunity 레코드에 대한 업데이트를 모니터링하는 경우 &quot;[!UICONTROL Opportunity]&quot;).
1. **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.
1. 규칙 이름, 평가 기준 및 규칙 기준을 설정한 다음 **[!UICONTROL Save]** 및 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.
1. 새로 만든 워크플로 규칙에서 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Add Workflow Action]** 드롭다운 목록에서 **[!UICONTROL New Outbound Message]**&#x200B;을(를) 선택합니다.

1. 새 아웃바운드 메시지에 포함할 이름, 설명, 끝점 URL 및 필드를 지정한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   **[!UICONTROL Endpoint URL]** 필드에 [!DNL Workfront Fusion]의 [!DNL Salesforce] [!UICONTROL Outbound Message]에 제공된 URL이 포함되어 있습니다.

1. [!UICONTROL Outbound Message] 이벤트로 시작하는 시나리오를 구성하십시오.

1. 오른쪽 하단에 있는 **&lt;/>** 아이콘을 클릭하고 제공된 URL을 복사합니다.
1. **[!UICONTROL Workflow Rules]** 페이지로 돌아가서 새로 만든 규칙을 찾은 다음 **[!UICONTROL Activate]**&#x200B;을(를) 클릭합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>보내는 메시지를 보는 데 사용할 웹후크를 선택합니다. 웹후크를 추가하려면 <strong>[!UICONTROL Add]</strong>을(를) 클릭하고 웹후크의 이름과 연결을 입력하십시오.</p> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!UICONTROL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>모듈에서 보내는 메시지를 확인할 [!DNL Salesforce] 레코드 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fields]</td> 
   <td> <p>모듈에서 보내는 메시지를 확인할 필드를 선택합니다. 사용 가능한 필드는 레코드 유형에 따라 다릅니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### *[!UICONTROL Watch a field]*

이 트리거 모듈은 [!DNL Salesforce]에서 필드를 업데이트할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>모듈에서 조사할 필드가 포함된 레코드 유형을 선택합니다. [!DNL Salesforce] 설정에서 [!UICONTROL Field History]이(가) 켜진 레코드 종류를 선택해야 합니다. 자세한 내용은 [!DNL Salesforce] 설명서의 <a href="https://help.salesforce.com/articleView?id=tracking_field_history.htm&amp;type=5">필드 기록 추적</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td> <p>모듈에서 변경 사항을 감시할 필드를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 필드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Upload Attachment/Document]](#upload-attachmentdocument)
* [[!UICONTROL Download Attachment/Document]](#download-attachmentdocument)
* [파일 업로드](#upload-file)

#### [!UICONTROL Create a Record]

이 작업 모듈은 개체에 새 레코드를 만듭니다.

모듈을 사용하면 모듈에서 사용할 수 있는 개체 필드를 선택할 수 있습니다. 이렇게 하면 모듈을 설정할 때 스크롤해야 하는 필드의 수가 줄어듭니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>모듈을 만들 [!DNL Salesforce] 레코드 형식을 선택하십시오. [!UICONTROL Record Type] 필드에서 선택한 레코드 유형에 따라 필드를 사용할 수 있습니다. 이 필드는 [!DNL Salesforce] API를 기반으로 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>새 레코드를 만들 때 모듈에서 구성할 필드를 선택합니다. 필수 필드는 목록의 맨 위에 있습니다. </p> <p>선택한 필드는 이 필드 아래에 열립니다. 이제 이러한 필드에 값을 입력할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

이 작업 모듈은 [!DNL Salesforce]의 단일 개체에서 데이터를 읽습니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Record Type]</td>
    <td>모듈에서 [action].read를 실행할 [!DNL Salesforce] 레코드의 형식을 선택하십시오.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Record Fields]</td>
    <td>모듈에서 읽을 필드를 선택합니다. 필드를 하나 이상 선택해야 합니다.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>모듈에서 읽을 레코드의 고유 [!DNL Salesforce] ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 [!DNL Salesforce] 개체를 열고 마지막 슬래시(/) 뒤의 URL 끝에 있는 텍스트를 복사합니다. For example: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Record]

이 작업 모듈은 오브젝트의 기존 레코드를 삭제합니다.

레코드의 ID를 지정합니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>모듈을 삭제할 [!DNL Salesforce] 레코드의 형식을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>모듈에서 삭제할 레코드의 고유 [!DNL Salesforce] ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 [!DNL Salesforce] 개체를 열고 마지막 슬래시(/) 뒤의 URL 끝에 있는 텍스트를 복사합니다. For example: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

이 작업 모듈을 사용하면 [!DNL Salesforce] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Salesforce] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

모듈은 다음을 반환합니다.

* **[!UICONTROL Status Code]**(숫자): HTTP 요청의 성공 또는 실패를 나타냅니다. 이것은 인터넷에서 찾아볼 수 있는 표준 코드입니다.
* **[!UICONTROL Headers]**(개체): 출력 본문과 관련이 없는 응답/상태 코드에 대한 자세한 컨텍스트입니다. 응답 헤더에 표시되는 일부 헤더가 응답 헤더는 아니므로 유용하지 않을 수 있습니다.

  응답 헤더는 모듈을 구성할 때 선택한 HTTP 요청에 따라 다릅니다.

* **[!UICONTROL Body]**(개체): 모듈을 구성할 때 선택한 HTTP 요청에 따라 일부 데이터를 다시 받을 수 있습니다. [!UICONTROL GET] 요청의 데이터와 같은 데이터가 이 개체에 포함되어 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p><code> &lt;Instance URL&gt;/services/data/v46.0/</code>에 상대적인 경로를 입력하십시오.</p> <p>사용 가능한 끝점 목록은 <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Salesforce REST API 개발자 안내서</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형식으로 요청의 헤더를 추가합니다(예: <code>{"Content-type":"application/json"}</code>). Workfront Fusion은 사용자에게 권한 부여 헤더를 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체의 형식으로 API 호출에 대한 쿼리를 추가합니다.예: <code>{"name":"something-urgent"}</code></p> </td> 
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

>[!INFO]
>
>**예:** 다음 API 호출은 [!DNL Salesforce] 계정의 모든 사용자 목록을 반환합니다.
>
>* **URL**: `query`
>
>* **메서드**: [!UICONTROL GET]
>
>* **쿼리 문자열**:
>
>* **키**: `q`
>
>* **값**: `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`
>
>검색 일치 항목은 모듈의 출력에서 **[!UICONTROL Bundle]> [!UICONTROL Body] >[!UICONTROL records]** 아래에 있습니다.
>
>이 예에서는 6명의 사용자가 반환되었습니다.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)


#### [!UICONTROL Upload Attachment/Document]

이 작업 모듈은 파일을 업로드하여 지정한 레코드에 첨부하거나 문서를 업로드합니다.

모듈은 연결이 액세스하는 사용자 지정 필드 및 값과 함께 첨부 파일 또는 문서의 ID와 관련 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type of Upload]</td> 
   <td>모듈에서 첨부 파일을 업로드할지 문서를 업로드할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>첨부 파일을 업로드할 오브젝트의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td>모듈을 업로드할 파일이 포함된 폴더를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download Attachment/Document]

이 작업 모듈은 레코드에서 문서 또는 첨부 파일을 다운로드합니다.

레코드의 ID와 원하는 다운로드 유형을 지정합니다.

모듈은 연결이 액세스하는 사용자 지정 필드 및 값과 함께 첨부 파일 또는 문서의 ID와 관련 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Type of Download]</td>
    <td> <p>Salesforce에서 다운로드할 파일 유형을 지정합니다.</p> 
     <ul> 
      <li>[!UICONTROL Attachment]</li> 
      <li>[!UICONTROL Document]</li> 
      <li>[!UICONTROL ContentDocument] [!DNL Saleforce CRM Content] 또는 [!DNL Salesforce Files]의 라이브러리에 업로드된 문서입니다.</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL Attachment ID] / </p> <p>[!UICONTROL ContentDocument ID]</p> </td>
    <td> <p>모듈을 다운로드할 레코드의 고유 [!DNL Salesforce] ID를 입력하거나 매핑합니다.</p> <p>ID를 가져오려면 브라우저에서 [!DNL Salesforce] 개체를 열고 마지막 슬래시(/) 뒤의 URL 끝에 있는 텍스트를 복사합니다. For example: <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Update a Record]

이 작업 모듈은 오브젝트의 레코드를 편집합니다.

모듈을 사용하면 모듈에서 사용할 수 있는 개체 필드를 선택할 수 있습니다. 이렇게 하면 모듈을 설정할 때 스크롤해야 하는 필드의 수가 줄어듭니다.

모듈은 연결에서 액세스하는 사용자 지정 필드 및 값과 함께 레코드 및 관련 필드의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>업데이트할 레코드의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>모듈을 업데이트할 [!DNL Salesforce] 레코드의 형식을 선택하십시오. 필드는 레코드 유형 필드에서 선택한 레코드 유형에 따라 사용할 수 있습니다. 이 필드는 [!DNL Salesforce] API를 기반으로 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>새 레코드를 만들 때 모듈에서 구성할 필드를 선택합니다. 필수 필드는 목록의 맨 위에 있습니다. </p> <p>선택한 필드는 이 필드 아래에 열립니다. 이제 이러한 필드에 값을 입력할 수 있습니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 파일 업로드

이 작업 모듈은 단일 파일을 Salesforce에 업로드합니다.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">연결 만들기[!DNL  Adobe Workfront Fusion] - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document linking]</td> 
   <td>콘텐츠 문서 링크를 적용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL linkedEntityId]</td> 
   <td>문서 연결을 사용하는 경우 연결된 개체의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ShareType]</td> 
   <td>문서 연결을 사용하는 경우 파일에 대한 권한을 선택합니다.<ul><li><b>뷰어 권한</b><p>사용자는 파일을 볼 수 있습니다.</p></li><li><b>공동 작업자 권한</b><p>사용자는 파일을 보고 편집할 수 있습니다.</p></li><li><b>권한 유추</b><p>권한은 라이브러리와 같은 관련 레코드에 대한 사용자의 권한을 기반으로 합니다.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>문서 연결을 사용하는 경우 문서의 가시성을 입력하거나 매핑합니다.<ul><li><b>모든 사용자</b><p>권한이 있는 모든 사용자가 사용할 수 있습니다.</p></li><li><b>내부 사용자</b><p>권한이 있는 내부 사용자가 사용할 수 있습니다.</p></li><li><b>공유 사용자</b><p>파일이 게시된 피드를 볼 수 있는 사용자가 사용할 수 있습니다.</p></li></ul></td> 
  </tr>

### 검색 결과

#### [!UICONTROL Search with Query]

이 검색 모듈은 지정한 검색 쿼리와 일치하는 [!DNL Salesforce]의 개체에서 레코드를 찾습니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search Type]</td> 
   <td> <p>모듈에서 수행할 검색 유형을 선택합니다.</p> 
    <ul> 
     <li> <p>[!UICONTROL Simple]</p> </li> 
     <li> <p>[!UICONTROL Using SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Using SOQL (Salesforce Object Query Language)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>단순 검색 유형을 선택한 경우 모듈에서 검색할 [!DNL Salesforce] 레코드의 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] / [!UICONTROL SOSL Query] / [!UICONTROL SOQL Query]</td> 
   <td> <p>검색할 쿼리를 입력합니다.</p> <p>SOSL에 대한 자세한 내용은 [!DNL Salesforce] 설명서의 <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm">Salesforce SOSL(개체 검색 언어)</a>을 참조하십시오.</p> <p>SOQL에 대한 자세한 내용은 [!DNL Salesforce] 설명서에서 <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm">Salesforce SOQL(개체 쿼리 언어)</a>을(를) 참조하십시오.</p> <p>참고: 매개 변수 <code>RETURNING </code>의 값은 모듈의 출력에 영향을 줍니다. <code>LIMIT</code>을(를) 사용하는 경우 [!DNL Fusion]이(가) [!UICONTROL Maximal count of records] 필드의 설정을 무시합니다. 제한을 설정하지 않으면 값 [!UICONTROL LIMIT = Maximal count of records]이(가) 삽입됩니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search]

이 작업 모듈은 지정된 조건을 충족하는 모든 레코드를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Salesforce] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">연결 만들기[!DNL  Adobe Workfront Fusion] - 기본 지침</a>을 참조하세요.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>검색할 객체 유형을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>검색할 필드, 쿼리에 사용할 연산자 및 필드에서 검색할 값을 선택합니다. AND 또는 OR를 사용하여 쿼리를 연결할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>모듈의 출력에 포함할 필드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>모듈이 모든 일치 레코드를 반환할지, 첫 번째 일치 레코드만 반환할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 검색할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>
