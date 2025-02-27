---
title: SOAP 모듈
description: SOAP 모듈을 사용하여 Adobe Workfront Fusion의 SOAP API에 연결할 수 있습니다.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: 3a27a51e10438e6cf8862bf28b1d58273bbaff36
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# [!UICONTROL SOAP] 모듈

[!UICONTROL SOAP] 모듈을 사용하여 [!UICONTROL Adobe Workfront Fusion]의 [!UICONTROL SOAP] API에 연결할 수 있습니다.

## SOAP 모듈 및 해당 필드

SOAP 커넥터에는 하나의 모듈인 SOAP 실행 작업만 포함됩니다

### SOAP 작업 실행

이 작업 모듈은 지정된 SOAP 작업을 실행합니다.



## 액세스 요구 사항

+++ 을 확장하여 이 문서의 기능에 대한 액세스 요구 사항을 봅니다.

이 문서의 기능을 사용하려면 다음 액세스 권한이 있어야 합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>임의</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>새로운 기능: 표준</p><p>또는</p><p>현재: 작업 시간 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이센스**</td> 
   <td>
   <p>현재: Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
   <p>또는</p>
   <p>레거시: 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>신규:</p> <ul><li>또는 Prime Workfront 패키지 선택: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</li><li>Ultimate Workfront 패키지: Workfront Fusion이 포함됩니다.</li></ul>
   <p>또는</p>
   <p>현재: 조직은 Adobe Workfront Fusion을 구매해야 합니다.</p>
   </td> 
  </tr>
 </tbody> 
</table>

이 표의 정보에 대한 자세한 내용은 설명서에서 [액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

[!DNL Adobe Workfront Fusion] 라이선스에 대한 자세한 내용은 [[!DNL Adobe Workfront Fusion] 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하세요.

+++

## SOAP 모듈 및 해당 필드

SOAP 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다.  모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### SOAP 작업 실행

이 작업 모듈은 지정한 WSDL을 기반으로 SOAP 작업을 실행합니다.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> 모듈에서 사용할 WSDL을 선택합니다. WSDL을 만들려면 필드 옆에 있는 <b>추가</b>를 클릭하고 필드를 채웁니다. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTTP headers]</td> 
   <td> 추가할 각 HTTP 헤더에 대해 <b>항목 추가</b>를 클릭하고 헤더의 이름과 값을 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SOAP headers]</td> 
   <td> 추가할 각 SOAP 헤더에 대해 <b>항목 추가</b>를 클릭하고 헤더의 이름, 값, 네임스페이스 및 XMLNS를 입력합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Force SOAP headers]</td> 
   <td> SOAP 1.2용 헤더를 구성하려면 이 옵션을 활성화합니다. </td> 
  </tr> 
  </tbody> 
</table>

## [!UICONTROL SOAP] 모듈의 제한 사항

>[!NOTE]
>
>WDSL을 로드하는 동안 리디렉션이 비활성화됩니다. 이는 보안 기능이지만 모듈을 실행할 때 확인되지 않은 리디렉션이 차단됨을 의미할 수 있습니다.

[!UICONTROL SOAP] 모듈은 현재 베타 버전이며 다음을 지원하지 않습니다.

* 요소 재정의
* 소수 자릿수 제한
* 총 자릿수 제한
* 공백 제한
* 입력 및 출력 메시지의 여러 부분. 단일 부분 메시지만 지원됩니다.
* SOAP 인코딩 스키마 및 요소의 도움으로 정의된 사용자 지정 XML 스키마 요소.

>[!BEGINSHADEBOX]

**예:**

[!UICONTROL Workfront Fusion]이(가) 다음 내용을 올바르게 인식하지 못합니다.

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

이 예에는 [!UICONTROL Workfront Fusion]에서 아직 지원되지 않는 `soapenc:Array`, `soapenc:arrayType` 및 `wsdl:arrayType` 참조가 포함되어 있습니다.

>[!ENDSHADEBOX]

## 해결 방법

[!UICONTROL SOAP] 모듈이 WSDL 파일 처리를 거부하거나 모듈 구성에 다양한 오류가 발생하면 대신 범용 **[!UICONTROL HTTP]>[!UICONTROL Make a request]** 모듈을 사용할 수 있습니다.

1. [!DNL Workfront Fusion]에서 새 시나리오를 만듭니다.
1. 시나리오에 **[!UICONTROL HTTP]>[!UICONTROL Make a request]** 모듈을 삽입합니다.
1. 모듈의 구성을 열고 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td> <p>[!UICONTROL Raw]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Parse response]</td> 
      <td>[!UICONTROL Enabled]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. 새 웹 브라우저 창 또는 탭을 엽니다.
1. 웹 브라우저의 주소 표시줄에 WSDL URL을 붙여 넣고 XML 파일을 가져옵니다.

   WSDL URL은 대개 `?wsdl`(으)로 끝나지만 `http://voip.ms/api/v1/server.wsdl`과 같은 형식일 필요는 없습니다.

1. WSDL 파일이 웹 브라우저에 직접 표시되지 않으면 다운로드한 파일을 텍스트 편집기에서 엽니다.
1. `<service>` 또는 `<wsdl:service>` 태그 검색:

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. 찾으면 `location` 특성에서 URL을 복사합니다.
1. [!DNL Workfront Fusion]에서 HTTP 모듈의 URL 필드에 URL을 붙여 넣습니다.
1. 새 웹 브라우저 창/탭에서 [온라인 [!UICONTROL SOAP] 클라이언트](https://wsdlbrowser.com/)를 엽니다.
1. WSDL URL을 WSDL URL 필드에 붙여넣습니다.
1. **[!UICONTROL Browse]**&#x200B;을(를) 클릭합니다.
1. 왼쪽에 있는 함수 목록(예: `getLanguages`)에서 선택하십시오.
1. [!UICONTROL Request XML] 텍스트 영역의 콘텐츠를 복사합니다.
1. [!UICONTROL Workfront Fusion]에서 복사한 콘텐츠를 모듈의 URL 필드에 붙여넣습니다.
1. 물음표를 실제 값으로 대체하여 선택한 매개 변수의 값을 제공합니다.

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 모듈의 구성을 닫습니다.
1. 시나리오 또는 모듈을 실행합니다.
