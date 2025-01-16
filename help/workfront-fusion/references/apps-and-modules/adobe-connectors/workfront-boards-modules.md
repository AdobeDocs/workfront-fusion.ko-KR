---
title: Adobe Workfront 보드 모듈
description: Adobe Workfront Boards 커넥터를 사용하여 Workfront Boards 내에서 프로세스를 자동화하고 서드파티 앱 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: dcc5044d-8fdf-4a74-b664-e965e714ce92
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '2440'
ht-degree: 1%

---

# [!DNL Adobe Workfront] 보드 모듈

>[!NOTE]
>
>Boards Fusion 커넥터가 베타 상태입니다. 그 결과, 이 커넥터에 대한 지원은 제한되고 보드의 향후 개발로 인해 변경될 수 있습니다. 또한 Fusion 커넥터 프로세스에 영향을 줄 수 있는 공지 없이 GraphQL API가 변경될 수 있습니다.

Adobe Workfront 보드는 열과 카드가 포함된 공유 보드에 대한 액세스를 제공하여 팀 공동 작업을 허용하는 유연한 도구입니다.

Adobe Workfront 보드 모듈을 사용하여 레코드를 읽거나 업데이트하거나, Workfront 보드 API에 대한 API 호출을 수행하거나, 보드에서 작업이 발생할 때 시나리오를 트리거할 수 있습니다.

<!--For general information on Workfront Boards, see [Boards overview](/help/quicksilver/agile/boards-overview.md).-->

## 액세스 요구 사항

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 패키지</td>
  <td> <p>임의</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 라이센스</td>
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: [!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 라이센스</td> 
   <td>
   <p>현재 라이선스 요구 사항: [!DNL Workfront Fusion] 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: 작업 자동화 및 통합의 경우 [!UICONTROL [!DNL Workfront Fusion], 작업 자동화의 경우 [!UICONTROL [!DNL Workfront Fusion]]</p>
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

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.


## 전제 조건

연결하려면 먼저 Adobe Workfront에서 보드를 구성해야 합니다.

## Adobe Workfront 보드 API 정보

Adobe Workfront 보드 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.23.6</td> 
  </tr>
 </tbody> 
 </table>

## Workfront 보드에 대한 연결 만들기

>[!NOTE]
>
>Workfront 연결을 사용하여 Workfront 보드에 연결하거나 별도의 Workfront 보드 연결을 만들 수 있습니다.

Workfront 보드 연결을 만들려면 다음 작업을 수행하십시오.

1. [!DNL Adobe Workfront Boards] 모듈에서 연결 상자 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

1. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>이 연결의 이름을 입력하십시오.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>서비스 계정에 연결할지 개인 계정에 연결할지 선택합니다.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(선택 사항)</p></td>
          <td>[!DNL Adobe] [!UICONTROL Client ID]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(선택 사항)</p></td>
          <td>[!DNL Adobe] [!UICONTROL Client Secret]을(를) 입력하십시오. [!DNL Adobe Developer Console]의 [!UICONTROL Credentials details] 섹션에서 찾을 수 있습니다.
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(선택 사항)</p></td>
          <td>Workfront 인스턴스가 이 연결을 인증하는 데 사용할 URL을 입력하십시오. <p>기본값은 <code>https://oauth.my.workfront.com/integrations/oauth2</code>입니다.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>호스트 접두사를 입력합니다.<p>기본값은 <code>origin-</code>입니다.</p>
        </tr>
      </tbody>
    </table>
1. 연결을 저장하고 모듈로 돌아가려면 **[!UICONTROL Continue]**&#x200B;을(를) 클릭하십시오.

## Adobe Workfront 보드 모듈 및 해당 필드

Workfront 보드 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준 등의 요소에 따라 추가 Workfront 보드 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [카드](#cards)
* [보드](#boards)
* [열](#columns)
* [태그](#tags)
* [댓글](#comments)
* [기타](#other)

<!--

### Watch

#### Watch events

This trigger module starts a scenario when an event occurs on a board.

1. Click **[!UICONTROL Add]** to the right of the **Webhook** box.

1. Configure the webhook in the **[!UICONTROL Add a hook]** box that displays.

   When you are configuring this module, the following fields display.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook name]</td> 
      <td>(Optional) Type a new name for the webhook</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>You can use an existing Workfront connection to connect to Workfront Boards, or you can use a specific Workfront Boards connection. </p><p>For instructions about connecting your [!DNL Workfront] app to [!DNL Workfront Fusion], see <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Create a connection to Workfront Boards</a> in this article.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Object type]</td> 
      <td>Select the type of [!DNL Workfront] object that you want the module to watch.</td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Objects to watch]</p> </td> 
      <td> Select whether you want to trigger a scenario when there is a new object, an updated object, a new or updated object, or a deleted object. </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Exclude events made by this connection</td> 
      <td>Enable this option to exclude events created or updated using the same connector that this trigger module uses. This can prevent situations where a scenario might trigger itself, causing it to repeat in an endless loop.</td> 
     </tr> 
    </tbody> 
   </table>

After the webhook is created, you can view the address of the endpoint that events are sent to.

-->

### 카드

* [체크리스트 항목 추가](#add-checklist-item)
* [하위 작업 추가](#add-subtask)
* [카드 만들기](#create-a-card)
* [카드 이동](#move-a-card)
* [카드 읽기](#read-a-card)
* [카드 업데이트](#update-a-card)

#### 체크리스트 항목 추가

이 작업 모듈은 지정된 카드에 체크리스트 항목을 추가합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>체크리스트 항목을 추가할 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Checklist items]</td> 
   <td>추가하려는 각 체크리스트 항목에 대해 항목 추가를 누르고 체크리스트 항목의 이름을 입력한 다음 항목의 완료 여부를 선택합니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 하위 작업 추가

이 작업 모듈은 보드의 카드에 하위 작업을 추가합니다. 카드가 연결된 카드여야 합니다. 하위 작업은 카드가 나타내는 Workfront 작업에도 추가됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Parent card ID]</td> 
   <td>하위 작업을 추가할 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>하위 작업을 추가할 카드가 포함된 보드 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>새 하위 작업의 이름을 입력하거나 매핑합니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 카드 만들기

이 작업 모듈은 Workfront 보드에 새 카드를 만듭니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>카드를 추가할 보드 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>하위 작업을 추가할 열의 ID를 입력하거나 매핑합니다.<p>보드 읽기 모듈에서 반환된 정보에서 열 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>새 카드의 이름을 입력하거나 매핑합니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 카드 이동

이 작업 모듈은 카드를 동일한 보드의 다른 열로 이동합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>이동할 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>이동할 카드가 포함된 게시판의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination column ID]</td> 
   <td>카드를 이동할 열의 ID를 입력하거나 매핑합니다.<p>보드 읽기 모듈에서 반환된 정보에서 열 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To index]</td> 
   <td>새 열에서 카드에 지정할 위치를 입력하거나 매핑합니다.<p>인덱스 0에서 열의 상위 위치입니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 카드 읽기

이 작업 모듈은 특정 카드에 대한 정보를 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>읽으려는 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 카드 업데이트

이 작업 모듈은 지정한 카드에 대한 정보를 업데이트합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>업데이트할 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>업데이트하려는 카드가 포함된 게시판의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>카드의 새 이름을 입력하거나 매핑합니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>카드에 대한 새 설명을 입력하거나 매핑합니다.</p></td> 
  </tr> 
 </tbody> 
</table>

### 보드

* [보드 만들기](#create-a-board)
* [게시판 읽기](#read-a-board)

#### 보드 만들기

이 작업 모듈은 Workfront에서 보드를 만듭니다. 만들려는 보드 유형을 지정할 수 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board name]</td> 
   <td>새 게시판의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type]</td> 
   <td>생성할 보드 유형을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 게시판 읽기

이 작업 모듈은 보드 카드, 열, 태그 및 멤버와 같은 단일 보드에 대한 정보를 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>정보를 검색할 게시판의 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
 </tbody> 
</table>

### 열

* [열 만들기](#create-a-column)
* [열 검색](#search-for-a-column)
* [열 업데이트](#update-a-column)

#### 열 만들기

이 작업 모듈은 지정된 보드에 새 열을 만듭니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>열을 추가할 게시판의 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>업데이트할 열의 ID를 입력하거나 매핑합니다.<p>보드 읽기 모듈에서 반환된 정보에서 열 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column name]</td> 
   <td>열의 새 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL WIP Limit]</td> 
   <td>열에 대한 신규 WIP 한도를 입력하거나 맵핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 열 검색

이 검색 모듈은 지정된 이름의 열에 대한 정보를 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>검색할 열이 포함된 보드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>검색할 열의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 열 업데이트

이 조치 모듈은 지정된 열의 이름 또는 WIP 한도를 갱신합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>검색할 열이 포함된 보드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Name]</td> 
   <td>검색할 열의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 태그

* [카드에 태그 추가](#add-card-tag)
* [태그 만들기](#create-a-tag)

#### 카드에 태그 추가

이 작업 모듈은 카드에 태그를 추가합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>태그를 추가할 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>태그를 추가할 카드가 포함된 보드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag ID]</td> 
   <td>추가할 태그의 ID를 입력하거나 매핑합니다.<p>보드 읽기 모듈에서 반환된 정보에서 태그 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 태그 만들기

이 작업 모듈은 새 태그를 만들고 색상을 지정합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>태그를 만들 보드 ID를 입력하거나 매핑합니다.<p>Workfront에서 게시판을 볼 때 URL에서 게시판 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag name]</td> 
   <td>새 태그의 이름을 입력하거나 매핑합니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag Color]</td> 
   <td>이 태그의 색상을 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 댓글

* [댓글 만들기](#create-a-comment)
* [카드 댓글 읽기](#read-card-comments)

#### 댓글 만들기

이 작업 모듈은 지정된 카드에 주석을 만들었습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>댓글을 추가할 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>추가할 댓글의 텍스트를 입력하거나 매핑합니다.</p></td> 
  </tr> 
 </tbody> 
</table>

#### 카드 댓글 읽기

이 작업 모듈은 지정된 카드에서 주석을 검색합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>댓글을 검색할 카드의 ID를 입력하거나 매핑합니다.<p>Workfront에서 카드를 볼 때 URL에서 카드 ID를 찾을 수 있습니다.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>한 실행 주기에서 모듈이 반환할 최대 주석 수를 입력합니다.</p></td> 
  </tr> 
 </tbody> 
</table>

### 기타

#### 사용자 지정 API 호출 만들기

이 작업 모듈은 Workfront 보드 API에 대한 사용자 지정 호출을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>기존 Workfront 연결을 사용하여 Workfront 보드에 연결하거나 특정 Workfront 보드 연결을 사용할 수 있습니다. </p><p>[!DNL Workfront] 앱을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Workfront 보드에 연결 만들기</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p><code> https://&lt;WORKFRONT_DOMAIN&gt;/boards-service/graphql?</code>에 상대적인 경로를 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 [!DNL Adobe Workfront Fusion]</a>에서 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드를 참조하십시오.</p><p>대부분의 보드에서 를 호출하는 방법은 POST입니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다. 요청의 콘텐츠 유형을 결정합니다.</p> <p>For example,<code> { "Content-type":"application/json-stringify()"}</code></p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>표준 JSON 개체 형식으로 API 호출에 대한 쿼리를 추가합니다.</p> <p>Workfront 보드의 경우 이 섹션은 일반적으로 비어 있습니다.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>JSON 임베드된 Graphql 형식으로 API 호출에 대한 본문 콘텐츠 추가 </p> <p>예:</p><p>이 예에서는 열 이름을 업데이트합니다. 이전 모듈에서 하드 코딩되거나 매핑된 GUID로 <code>boardId</code> 및 <code>columnId</code>을(를) 포함할 수 있습니다.<p><pre>{<br> "query": "mutation { updateColumn(boardId: \"\", columnId: \"\", updateColumnInput: { name: \"\" }) { id name }}"<br>}</pre><p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
