---
title: 상자 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Box를 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다. 지정된 폴더를 모니터링하여 파일 변경 사항을 확인하거나, 기존 파일을 수정 및 삭제하거나, 새 파일을 폴더에 업로드합니다.'
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 0%

---

# 상자 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Box]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다. 지정된 폴더를 모니터링하여 파일 변경 사항을 확인하거나, 기존 파일을 수정 및 삭제하거나, 새 파일을 폴더에 업로드합니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오. 모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

[!DNL Box] 모듈을 사용하려면 [!DNL Box] 계정이 있어야 합니다.

## Box API 정보

Box 커넥터에서는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box]개 모듈 및 해당 필드

[!DNL Box] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Box] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 트리거

* [[!UICONTROL New event]](#new-event)
* [[!UICONTROL Watch files]](#watch-files)

#### [!UICONTROL New event]

이 즉시 트리거 모듈은 파일이 추가, 이동, 복사, 삭제, 잠김 또는 잠금 해제되면 시나리오를 시작합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>보내는 메시지를 보는 데 사용할 웹후크를 선택합니다. 웹후크를 추가하려면 <strong>[!UICONTROL Add]</strong>을(를) 클릭하고 웹후크의 이름과 연결을 입력하십시오.</p> <p> [!UICONTROL Box] 계정을 [!UICONTROL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">서비스에 연결 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Maximum number of returned events]</p> </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 이벤트 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch files]

이 트리거 모듈은 새 파일이 추가되거나 감시되는 폴더에서 기존 파일이 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">시청</td> 
   <td> <p>보려는 파일 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>새 파일만</strong> </p> <p>새 파일이 추가되면 시나리오가 시작됩니다.</p> </li> 
     <li> <p><strong>새 파일 및 모든 변경 내용</strong> </p> <p>이 시나리오는 파일이 추가되거나 파일 콘텐츠 또는 파일 속성(예: 이름)이 수정될 때 시작됩니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>다운로드한 최대 파일 수</p> </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 파일 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL Upload] 파일](#upload-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)

#### [!UICONTROL Upload a file]

이 작업 모듈은 파일을 업로드합니다.

파일을 지정합니다. 파일의 새 파일 이름을 제공할 수도 있습니다.

모듈은 파일의 ID와 연결된 필드, 그리고 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 모듈이 성공하지 못한 경우 다음 사항을 고려하십시오.
>
>* 파일 크기가 [!DNL Box] 플랜의 최대 파일 크기 제한을 초과하거나 [!DNL Box] 계정의 저장소 할당량을 모두 사용했을 수 있습니다. 저장소 공간을 늘리려면 [!DNL Box]에서 기존 파일을 삭제하거나 [!DNL Box] 계정을 업그레이드하세요.
>* [!DNL Box]이(가) 같은 이름의 파일을 하나 이상의 폴더에 업로드하지 않습니다. 대상 폴더에 업로드되는 파일과 같은 이름의 파일이 포함되어 있으면 시나리오 실행이 오류와 함께 종료됩니다. 이 문제를 방지하려면 파일 이름을 바꾸십시오. 파일을 업데이트하려면 **[!UICONTROL Update a file]** 모듈을 사용하십시오.

#### [!UICONTROL Update a file]

이 작업 모듈은 파일을 업데이트합니다.

파일의 ID를 지정합니다.

모듈은 파일의 ID와 연결된 필드, 그리고 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>모듈에서 업데이트할 파일의 고유 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

이 작업 모듈은 파일을 삭제합니다.

파일의 ID를 지정합니다.

모듈은 파일의 ID와 연결된 필드, 그리고 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>모듈에서 업데이트할 파일의 고유 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

이 작업 모듈은 파일을 다운로드합니다.

파일의 ID를 지정합니다.

모듈은 파일의 ID와 연결된 필드, 그리고 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

>[!NOTE]
>
>이 모듈은 파일을 후속 모듈에 제공하는 데 유용합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>모듈에서 업데이트할 파일의 고유 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

<!--
<h2>Possible problems</h2>

<p style="color: #ff1493;">This is drafted out because we don't have a download module for Box yet</p>


<h3>Watch files trigger module doesn't download a file contained in the folder.</h3>

<p>There are several situations when downloading a file fails:</p>



  <li>The current file lock setting does not allow the file to be downloaded or the downloading of the file is disabled. In this case, the file is ignored.</li>



  <li>When the scenario started, the file was being uploaded to the server and was not ready to be downloaded. The scenario run gets stopped and Workfront Fusion tries downloading the file again during the next execution of the scenario.</li>
  
-->
