---
title: Adobe Journey Optimizer 모듈
description: Adobe Workfront Fusion 시나리오에서는  [!DNL Adobe Journey Optimizer]을(를) 사용하는 워크플로를 자동화하고 여러 타사 애플리케이션 및 서비스에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: 1d0ccf4d-9f06-4210-86ec-7da7970f6a47
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '3747'
ht-degree: 0%

---

# [!DNL Adobe Journey Optimizer]개 모듈

Adobe Workfront Fusion 시나리오에서는 [!DNL Adobe Journey Optimizer]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다. [!DNL Adobe Journey Optimizer] 모듈을 사용하면 레코드를 만들거나, 읽거나, 업데이트하거나, 삭제할 수 있으며, [!DNL Adobe Journey Optimizer] API에 대한 사용자 지정 API 호출을 수행할 수 있습니다.


시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Adobe Workfront 플랜*</td>
      <td>
        <p>[!UICONTROL Pro] 이상</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront 라이센스*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront Fusion 라이센스**</td>
      <td>
   <p>현재 라이선스 요구 사항: Workfront Fusion 라이선스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시 라이선스 요구 사항: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">제품</td>
      <td>
   <p>현재 제품 요구 사항: [!UICONTROL Select] 또는 [!UICONTROL Prime] Adobe Workfront 플랜이 있는 경우 조직에서 이 문서에 설명된 기능을 사용하려면 Adobe Workfront Fusion과 Adobe Workfront을 구입해야 합니다. Workfront Fusion은 [!UICONTROL Ultimate] Workfront 플랜에 포함되어 있습니다.</p>
   <p>또는</p>
   <p>레거시 제품 요구 사항: 조직에서 이 문서에 설명된 기능을 사용하려면 Adobe Workfront Fusion과 Adobe Workfront을 구입해야 합니다.</p>
   </td>
    </tr>
  </tbody>
</table>


보유 중인 플랜, 라이선스 유형 또는 액세스 권한을 확인하려면 Workfront 관리자에게 문의하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!DNL Adobe Journey Optimizer] 커넥터를 사용하려면 먼저 다음 전제 조건을 충족하는지 확인해야 합니다.

* 활성 [!DNL Adobe Journey Optimizer] 계정이 있어야 합니다.

## Adobe Journey Optimizer API 정보

Adobe Journey Optimizer 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td>{{connection.url}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.7.11</td> 
  </tr>
 </tbody> 
 </table>

## Adobe Journey Optimizer에 대한 연결 만들기

모든 Adobe Journey Optimizer 모듈에서 연결을 만들 수 있습니다.

1. 모든 모듈에서 연결 상자 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

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
          <p>이 연결의 이름을 입력하십시오.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 환경]</td>
        <td>프로덕션 환경에 연결할지 아니면 비프로덕션 환경에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 유형]</td>
        <td>서비스 계정에 연결할지 또는 개인 계정에 연결할지 선택합니다.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 ID]</td>
        <td>[!UICONTROL Adobe] [!UICONTROL 클라이언트 ID]를 입력합니다. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 클라이언트 암호]</td>
        <td>[!DNL Adobe] [!UICONTROL 클라이언트 암호]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 조직 ID]</td>
        <td>[!DNL Adobe] [!UICONTROL 조직 ID]를 입력하십시오. 이 로그는 의 [!UICONTROL 자격 증명] 세부 정보 섹션에서 찾을 수 있습니다. [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 샌드박스 이름]</td>
        <td>이 연결에 사용할 샌드박스의 이름을 입력합니다.</td>
        </tr>
      </tbody>
    </table>



   <!--Markdown 0032 placeholder-->


## [!DNL Adobe Journey Optimizer]개 모듈 및 해당 필드

[!DNL Adobe Journey Optimizer] 모듈을 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Adobe Journey Optimizer] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [구성 관리](#configuration-management)
* [패키지 관리](#package-management)
* [기록 관리](#record-management)
* [메시지 관리](#message-management)
* [상태 확인](#status-checks)
* [검색 결과](#searches)
* [기타](#other)




### 구성 관리

* [구성 만들기](#create-a-configuration)
* [구성 배포](#deploy-a-configuration)
* [구성 업데이트](#update-a-configuration)
* [구성 배포 취소](#undeploy-a-configuration)
* [구성을 배포할 수 있는지 확인](#check-if-configuration-can-be-deployed)
* [구성 삭제](#delete-a-configuration)
* [구성 가져오기](#get-a-configuration)

#### 구성 만들기

이 작업 모듈은 제한 끝점 또는 제한 구성을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>최대 가용량 구성을 만들거나 제한 구성을 만드는지 선택합니다.<ul><li><p><b>상한 설정</b></p><a href="#capping-fields" class="MCXref xref" >필드 제한</a>을 계속합니다.</li><li><p><b>조절</b></p><a href="#throttling-fields" class="MCXref xref" >필드 조절</a>을 계속합니다.</li></ul></td> 
  </tr> 
   </tbody> 
</table>

##### 필드 캡핑

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>구성할 끝점의 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IMS 조직 ID]</td> 
   <td>조직의 Adobe IMS ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td>이 구성에서 사용할 메서드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service]</td> 
   <td>이 구성에 대해 작업을 사용하는지 아니면 데이터 소스를 사용하는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 최대 HTTP 연결]</td> 
   <td>이 끝점에 최대 동시 연결 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 최대 호출]</td> 
   <td>기간 필드에 지정된 기간에 수행할 최대 호출 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 기간(밀리초)]</td> 
   <td>최대 호출 수 필드와 관련된 밀리초 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

##### 제한 필드

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL 이름]</td> 
   <td>이 구성의 이름을 입력하거나 매핑합니다.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td>이 구성에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL URL pattern]</td> 
   <td>스로틀링할 끝점의 URL을 입력하거나 매핑하십시오.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메서드]</td> 
   <td>이 구성에서 사용할 메서드를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 최대 처리량]</td> 
   <td>이 구성에 대해 작업을 사용하는지 아니면 데이터 소스를 사용하는지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 최대 HTTP 연결]</td> 
   <td>이 끝점에 최대 동시 연결 수를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 최대 호출]</td> 
   <td>이 끝점에 대해 원하는 최대 처리량을 입력하거나 매핑합니다. 이 값은 200에서 5000 사이여야 합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 구성 배포

이 작업 모듈은 지정된 제한 또는 제한 구성을 배포합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>최대 가용량 구성을 배포할지 또는 제한 구성을 배포할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 ID]</td> 
   <td>배포하려는 구성의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 구성 업데이트

이 작업 모듈은 지정된 제한 또는 제한 구성을 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>최대 가용량 구성을 업데이트할지 또는 제한 구성을 업데이트할지 선택합니다.<ul><li><p><b>상한 설정</b></p>필드의 경우 이 문서의 구성 만들기 섹션에서 <a href="#capping-fields" class="MCXref xref" >필드 가용량</a>을(를) 참조하십시오.</li><li><p><b>조절</b></p>필드의 경우 이 문서의 구성 만들기 섹션에서 <a href="#throttling-fields" class="MCXref xref" >필드 조절</a>을(를) 참조하십시오.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

#### 구성 배포 취소

이 작업 모듈은 최대 가용량 또는 제한 구성을 배포하지 않습니다. 구성 상태가 배포 이전 상태(`created` 또는 `updated`)로 다시 변경되었습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>최대 가용량 구성을 배포 취소할지 또는 제한 구성을 배포 취소할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 ID]</td> 
   <td>배포를 취소할 구성의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 구성을 배포할 수 있는지 확인

이 작업 모듈은 최대 가용량 구성이나 제한 구성을 배포할 수 있는지 확인합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>최대 가용량 구성을 검사할지 또는 제한 구성을 검사할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 ID]</td> 
   <td>확인할 구성의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 구성 삭제

이 작업 모듈은 최대 가용량 끝점 또는 제한 구성을 삭제합니다.

구성이 배포된 경우 삭제하기 전에 배포를 취소해야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>최대 가용량 구성을 삭제할지 또는 제한 구성을 삭제할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 ID]</td> 
   <td>삭제하려는 구성의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 구성 가져오기

이 작업 모듈은 지정된 ID로 식별되는 제한 또는 제한 구성을 반환합니다. 최신 정의가 반환됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>최대 가용량 구성을 검색할지 제한 구성을 검색할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 ID]</td> 
   <td>검색할 구성의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>




### 패키지 관리

* [패키지 만들기](#create-a-package)
* [패키지 업데이트](#update-a-package)
* [패키지 삭제](#delete-a-package)
* [패키지 조회](#look-up-a-package)
* [패키지 가져오기](#import-a-package)
* [패키지 게시](#publish-a-package)
* [가져오기 제출](#submit-an-import)



#### 패키지 만들기

이 작업 모듈은 다중 아티팩트 패키지를 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이름]</td> 
   <td>패키지의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td>패키지에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 만료일]</td> 
   <td>패키지의 만료 날짜를 정의하는 타임스탬프를 입력하거나 매핑합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 유형]</td> 
   <td>만들려는 패키지 유형을 선택합니다.<ul><li><p><b>전체</b></p>패키지에는 모든 아티팩트가 포함됩니다</p></li><li><p><b>부분</b></p><p>패키지에는 추가한 아티팩트만 포함됩니다. </p></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 아티팩트]</td> 
   <td>부분 패키지를 만드는 경우 추가할 각 아티팩트에 대해 <b>아티팩트 추가</b>를 클릭하고 아티팩트의 ID, 유형 및 제목을 지정합니다. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Sandbox]</td> 
   <td>패키지에 포함할 항목이 포함된 샌드박스의 이름 및 IMS 조직 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 패키지 업데이트

이 작업 모듈은 패키지에서 아티팩트를 추가 또는 삭제하거나 패키지 메타데이터를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select action]</td> 
   <td>수행할 작업을 선택합니다.<ul><li><p><b>아티팩트 추가</b></p><p>추가할 각 아티팩트에 대해 <b>아티팩트 추가</b>를 클릭하고 아티팩트의 ID, 유형 및 제목을 지정한 다음 패키지의 만료 날짜를 입력하거나 매핑하십시오. </p></li><li><p><b>아티팩트 삭제</b></p><p>삭제할 각 아티팩트에 대해 <b>아티팩트 추가</b>를 클릭하고 아티팩트의 ID, 유형 및 제목을 지정합니다. </p></li><li><p><b>메타데이터 업데이트</b></p><p>이름, 설명 또는 소스 샌드박스 이름 또는 IMS 조직 ID에 대한 새 값을 입력합니다.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

#### 패키지 삭제

이 작업 모듈은 다중 아티팩트 패키지를 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 ID]</td> 
   <td>삭제하려는 패키지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 패키지 조회

이 작업 모듈은 지정된 패키지의 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 ID]</td> 
   <td>세부 정보를 반환할 패키지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 패키지 가져오기

이 작업 모듈은 지정된 대상 샌드박스에서 충돌하는 개체를 가져옵니다. 충돌하는 오브젝트는 대상 샌드박스에 이미 존재하는 유사한 오브젝트를 나타냅니다.

패키지를 가져오려면 먼저 게시해야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 ID]</td> 
   <td>가져올 패키지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target 샌드박스]</td> 
   <td>패키지를 가져올 샌드박스의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 패키지 게시

패키지를 가져오려면 먼저 게시해야 합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 ID]</td> 
   <td>게시하려는 패키지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 가져오기 제출

이 작업 모듈은 충돌을 검토하고 대체 기능을 제공한 후 패키지에 대한 가져오기를 제출합니다. 결과는 페이로드로 제공되며, 페이로드에 지정된 대로 대상 샌드박스에 대한 가져오기 작업을 시작합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 ID]</td> 
   <td>게시하려는 패키지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이름]</td> 
   <td>가져오기 작업의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td>가져오기 작업의 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (대상 샌드박스) 이름]</td> 
   <td>가져오기를 제출할 샌드박스의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (대상 샌드박스) IMS 조직 ID]</td> 
   <td>가져오기를 제출할 샌드박스의 Adobe IMS 조직 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source 샌드박스) ID]</td> 
   <td>게시하려는 패키지가 포함된 샌드박스의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source 샌드박스) 유형]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source 샌드박스) 링크]</td> 
   <td>게시하려는 패키지에 대한 링크를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>


<!--

### Artifact management

* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)

#### Copy artifacts synchronously

This action module copies artifacts from a source sandbox into a destination sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination sandbox]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to copy, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

#### Export Artifacts asynchronously

This action module exports artifacts from the specified sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to export, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



#### Import Artifacts asynchronously

This action module imports a snapshot containing artifacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Snapshot ID]</td> 
   <td>Enter or map the ID of the snapshot you want to import.</td> 
  </tr> 
 </tbody> 
</table>

-->

### 기록 관리

* [레코드 만들기](#create-a-record)
* [레코드 업데이트](#update-a-record)
* [레코드 삭제](#delete-a-record)
* [레코드 패치](#patch-a-record)
* [레코드 가져오기](#get-a-record)

#### 레코드 만들기

이 작업 모듈은 새 콘텐츠 템플릿 또는 콘텐츠 조각을 만듭니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 콘텐츠 유형 선택]</td> 
   <td>콘텐츠 템플릿을 만들거나 콘텐츠 조각을 만들지 선택합니다.<ul><li><p><b>콘텐츠 템플릿</b></p><a href="#template-fields" class="MCXref xref" >템플릿 필드</a>을(를) 계속합니다.</li><li><p><b>컨텐츠 조각</b></p><a href="#fragment-fields" class="MCXref xref" >조각 필드</a>을(를) 계속합니다.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

##### 템플릿 필드

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL 이름]</td> 
   <td>이 콘텐츠 템플릿의 이름을 입력하거나 매핑하십시오.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td>이 컨텐츠 템플릿에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL 유형]</td> 
   <td>만들려는 템플릿 유형을 선택합니다.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널]</td> 
   <td>이 템플릿에 포함된 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content template origin]</td> 
   <td>이 템플릿의 소스를 선택하십시오.</td>  
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메타데이터]</td> 
   <td>새 템플릿에 사용자 지정 속성을 포함하려면 "메타데이터 추가"를 선택하고 메타데이터의 키 및 값을 입력하거나 매핑합니다. 포함하려는 각 사용자 정의 필드에 대해 이 작업을 반복합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email HTML]</td> 
   <td>이 템플릿에 포함된 이메일의 HTML을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>이메일에 사용자 정의 속성을 포함하려면 "편집기 컨텍스트 추가"를 선택하고 컨텍스트의 키 및 값을 입력하거나 매핑합니다. 포함하려는 각 사용자 정의 필드에 대해 이 작업을 반복합니다.</td> 
  </tr> 
 </tbody> 
</table>

##### 조각 필드

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL 이름]</td> 
   <td>이 콘텐츠 조각의 이름을 입력하거나 매핑합니다.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL 설명]</td> 
   <td>이 컨텐츠 조각에 대한 설명을 입력하거나 매핑합니다.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL 유형]</td> 
   <td>만들려는 템플릿 유형을 선택합니다.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 채널]</td> 
   <td>이 템플릿에 포함된 채널을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 콘텐츠 조각 원본]</td> 
   <td>이 조각의 소스를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메타데이터]</td> 
   <td>새 템플릿에 사용자 지정 속성을 포함하려면 "메타데이터 추가"를 선택하고 메타데이터의 키 및 값을 입력하거나 매핑합니다. 포함하려는 각 사용자 정의 필드에 대해 이 작업을 반복합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td>조각의 콘텐츠를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>이메일에 사용자 정의 속성을 포함하려면 "편집기 컨텍스트 추가"를 선택하고 컨텍스트의 키 및 값을 입력하거나 매핑합니다. 포함하려는 각 사용자 정의 필드에 대해 이 작업을 반복합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 업데이트

이 작업 모듈은 컨텐츠 템플릿 또는 조각을 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 콘텐츠 유형 선택]</td> 
   <td>최대 가용량 구성을 업데이트할지 또는 제한 구성을 업데이트할지 선택합니다.<ul><li><p><b>템플릿</b></p>필드의 경우 이 문서의 레코드 만들기 섹션에서 <a href="#template-fields" class="MCXref xref" >템플릿 필드</a>을(를) 참조하십시오.</li><li><p><b>조각</b></p>필드의 경우 이 문서의 레코드 만들기 섹션에서 <a href="#fragment-fields" class="MCXref xref" >조각 필드</a>을(를) 참조하십시오.</li></ul></td> 
  </tr> 
  </tbody> 
  </table>

#### 레코드 삭제

이 작업 모듈은 컨텐츠 템플릿 또는 컨텐츠 조각을 삭제합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 콘텐츠 유형 선택]</td> 
   <td>콘텐츠 템플릿을 삭제할지 또는 콘텐츠 조각을 삭제할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 템플릿/조각 ID]</td> 
   <td>삭제할 템플릿 또는 조각의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 패치

이 작업 모듈은 JSON 포인터 형식이 있는 PATCH을 사용하여 레코드를 업데이트합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 콘텐츠 유형 선택]</td> 
   <td>콘텐츠 템플릿을 패치할지 또는 콘텐츠 조각을 패치할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 템플릿/조각 ID]</td> 
   <td>패치할 템플릿 또는 조각의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 페이로드 데이터]</td> 
   <td>이 패치의 페이로드에 레코드를 추가하려면 다음 작업을 수행하십시오. <ol><li><b>레코드 추가</b>를 클릭합니다.</li><li>추가, 제거 또는 바꾸기 작업을 선택합니다.</li><li>경로 필드에서 이름 또는 설명에 패치를 적용할지 여부를 선택합니다.</li><li> From 필드에 JSON 포인터 값이 포함된 문자열을 입력하거나 매핑합니다.</li><li>값 필드에 공정에 사용할 값을 입력합니다.</li></ol></td> 
  </tr> 
 </tbody> 
</table>

#### 레코드 가져오기

이 작업 모듈은 지정된 ID로 식별되는 콘텐츠 템플릿 또는 콘텐츠 조각을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 콘텐츠 유형 선택]</td> 
   <td>콘텐츠 템플릿을 검색할지 또는 콘텐츠 조각을 검색할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 템플릿/조각 ID]</td> 
   <td>검색할 템플릿 또는 조각의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>


### 메시지 관리

* [단일 메시지 실행 트리거](#trigger-a-unitary-message-execution)
* [대상자 기반 메시지 트리거](#trigger-an-audience-based-message)
* [대상 기반 메시지의 상태 확인](#check-the-status-for-audience-based-message)



#### 단일 메시지 실행 트리거

이 작업 모듈은 사용자가 지정하는 수신자에게 단일 메시지를 트리거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 요청 ID]</td> 
   <td>이 메시지와 연결된 요청의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 캠페인 ID]</td> 
   <td>이 메시지와 연결된 캠페인의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipients]</td> 
   <td>이 메시지를 받을 각 받는 사람에 대해 <b>받는 사람 추가</b>를 클릭하고 다음을 입력하십시오.
   <ul>
   <li><p><b>유형</b></p><code>aep</code>를 선택합니다.</li>
   <li><p><b>사용자 ID</b></p>수신자의 Adobe Experience Platform 프로필 식별자를 입력하거나 매핑합니다.</li>
   <li><p><b>네임스페이스</b></p>수신자의 Adobe Experience Platform 프로필 네임스페이스를 입력하거나 매핑합니다.</li>
   <li><p><b>이메일 주소</b></p></li>
   <li><p><b>휴대폰 번호</b></p></li>
   <li><p><b>이름</b></p></li>
   <li><p><b>성</b></p></li>
   <li><p><b>제품</b></p>이 메시지와 연관된 제품을 입력하거나 매핑합니다. 메시지 콘텐츠의 동적 변수 대체에 사용됩니다.</li>
   </ul></td> 
  </tr> 
 </tbody> 
</table>

#### 대상자 기반 메시지 트리거

이 작업 모듈은 지정한 요청 및 캠페인에 따라 대상 기반 메시지의 실행을 트리거합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 요청 ID]</td> 
   <td>이 메시지와 연결된 요청의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 캠페인 ID]</td> 
   <td>이 메시지와 연결된 캠페인의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 제품]</td> 
   <td>이 메시지와 연관된 제품을 입력하거나 매핑합니다. 메시지 콘텐츠의 동적 변수 대체에 사용됩니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 대상 기반 메시지의 상태 확인

이 작업 모듈은 대상 기반 일괄 처리 메시지의 상태를 확인합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 메시지 실행 ID]</td> 
   <td>확인할 메시지 실행 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 상태 확인

<!--* [Check service health](#check-service-health)-->
* [가져오기 종속성 확인](#check-the-import-dependencies)
* [가져오기 작업의 상태 확인](#check-the-status-of-an-import-job)

<!--

#### Check service health

This action module checks that the service represented by the connection is running.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
 </tbody> 
</table>

-->

#### 가져오기 종속성 확인

이 작업 모듈은 패키지 아티팩트에 대한 종속성을 확인합니다. 이렇게 하면 패키지 아티팩트를 가져올 수 있는 권한이 있는지 확인할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 ID]</td> 
   <td>권한을 확인할 패키지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Target 샌드박스]</td> 
   <td>패키지를 가져올 샌드박스의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 가져오기 작업의 상태 확인

이 작업 모듈은 가져오기 작업의 성공 여부를 확인합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 작업 ID]</td> 
   <td>데이터를 검색할 작업의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [모든 종속 개체 나열](#list-all-dependent-objects)
* [목록 구성](#list-configurations)
* [내보내기 및 가져오기 작업 나열](#list-export-and-import-jobs)
* [패키지 나열](#list-packages)
* [목록 레코드](#list-records)

#### 모든 종속 개체 나열

이 검색 모듈은 지정된 패키지의 개체에 대한 모든 종속 개체를 나열합니다

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 개체]</td> 
   <td>종속 개체를 반환할 패키지의 각 개체에 대해 <b>개체 추가</b>를 클릭하고 개체의 이름과 형식을 입력하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 패키지 ID]</td> 
   <td>종속 개체를 나열할 패키지의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target 샌드박스]</td> 
   <td>종속 개체를 나열할 패키지가 포함된 샌드박스의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 목록 구성

이 작업 모듈에는 모든 제한 또는 제한 구성이 나열됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 구성 유형 선택]</td> 
   <td>제한 구성을 나열할지 또는 제한 구성을 나열할지 선택합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### 내보내기 및 가져오기 작업 나열

이 검색 모듈에는 현재 내보내기 및 가져오기 작업이 나열됩니다. 쿼리 매개 변수를 사용하여 목록을 필터링할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 결과 수]</td> 
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>결과를 만든 날짜별로 정렬할지 또는 수정한 날짜별로 정렬할지 여부를 선택합니다.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 매개 변수]</td> 
   <td>필터링할 각 쿼리 매개 변수에 대해 <b>쿼리 매개 변수 추가</b>를 클릭한 다음 필드 및 연산자를 선택하고 필터의 필드 값을 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>



#### 패키지 나열

이 검색 모듈은 조직의 모든 패키지를 나열합니다. 쿼리 매개 변수를 사용하여 목록을 필터링할 수 있습니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 반환되는 최대 결과 수]</td> 
      <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>결과를 만든 날짜별로 정렬할지 또는 수정한 날짜별로 정렬할지 여부를 선택합니다.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL 쿼리 매개 변수]</td> 
   <td>필터링할 각 쿼리 매개 변수에 대해 <b>쿼리 매개 변수 추가</b>를 클릭한 다음 필드 및 연산자를 선택하고 필터의 필드 값을 입력하십시오.</td> 
  </tr> 
 </tbody> 
</table>

#### 목록 레코드

이 검색 모듈에는 제한 또는 제한 구성이 모두 나열됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 콘텐츠 유형 선택]</td> 
   <td>콘텐츠 템플릿을 검색할지 또는 콘텐츠 조각을 검색할지 선택합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>이 목록을 정렬하려는 매개 변수 이름을 입력하거나 매핑합니다. 내림차순 또는 오름차순으로 정렬하려면 <code>-</code> 또는 <code>+</code>을(를) 추가하십시오. 기호를 지정하지 않으면 목록이 내림차순으로 정렬됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 시작]</td> 
   <td>이 필드는 페이지 매김에 사용됩니다. [정렬 기준] 필드에 지정된 속성과 관련된 다음 페이지의 기준을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>이 목록을 정렬하려는 매개 변수 이름을 입력하거나 매핑합니다. 내림차순 또는 오름차순으로 정렬하려면 <code>-</code> 또는 <code>+</code>을(를) 추가하십시오. 기호를 지정하지 않으면 목록이 내림차순으로 정렬됩니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by property]</td> 
   <td>추가할 각 속성 필터에 대해 <b>항목 추가</b>를 클릭하고 속성의 키와 값을 입력하십시오. 속성에 대해 지정된 값을 포함하는 레코드가 목록에 포함됩니다.</td> 
  </tr> 
 </tbody> 
</table>


### 기타


#### 사용자 지정 API 호출 만들기

이 작업 모듈은 Adobe Journey Optimizer API에 대한 사용자 지정 API 호출을 만듭니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>[!DNL Adobe Journey Optimizer]에 대한 연결을 만드는 방법에 대한 지침은 이 문서에서 <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >[!DNL Adobe Journey Optimizer]</a>에 대한 연결 만들기 를 참조하십시오.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>기본 URL에 상대적인 경로를 입력합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
      </td>
   <td> <p>API 호출을 구성하는 데 필요한 HTTP 요청 메서드를 선택합니다. 자세한 내용은 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 요청 메서드</a>를 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 인증, <code>x-api-key</code> 및 <code>x-gw-ims-org-id</code> 헤더를 자동으로 추가합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 쿼리 문자열]  </td>
      <td>
        <p>요청 쿼리 문자열을 입력합니다.</p>
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







<!--

* [Check if configuration can be deployed](#check-if-configuration-can-be-deployed)
* [Check service health](#check-service-health)
* [Check the import dependencies](#check-the-import-dependencies)
* [Check the status for audience-based message](#status-for-audience-based-message)
* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Create a configuration](#create-a-configuration)
* [Create a package](#create-a-package)
* [Create a record](#create-a-record)
* [Delete a configuration](#delete-a-configuration)
* [Delete a package](#delete-a-package)
* [Delete a record](#delete-a-record)
* [Deploy a configuration](#deploy-a-configuration)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Get a configuration](#get-a-configuration)
* [Get a record](#get-a-record)
* [Import a package](#import-a-package)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)
* [List all dependent objects](#list-all-dependent-objects)
* [List export and import jobs](#list-import-and-export-jobs)
* [Look up a package](#look-up-a-package)
* [Make a custom API call](#make-a-custom-api-call)
* [Patch a record](#patch-a-record)
* [Publish a package](#publish-a-package)
* [Submit an import](#submit-an-import)
* [Trigger a unitary message execution](#trigger-a-unitary-message-execution)
* [Trigger an audience-based message](#trigger-an-audience-based-message)
* [Undeploy a configuration](#undeploy-a-configuration)
* [Update a configuration](#update-a-configuration)
* [Update a package](#update-a-package)
* [Update a record](#update-a-record)
* [List configurations](#list-configurations)
* [List packages](#list-packages)
* [List records](#list-records)

-->
