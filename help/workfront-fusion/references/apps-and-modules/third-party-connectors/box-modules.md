---
title: 상자 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는 Box를 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다. 지정된 폴더를 모니터링하여 파일 변경 사항을 확인하거나, 기존 파일을 수정 및 삭제하거나, 새 파일을 폴더에 업로드합니다.'
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: f02c4df01c7fad6bb9cdf4911512eef97e71c82b
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 1%

---

# 상자 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Box]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다. 지정된 폴더를 모니터링하여 파일 변경 사항을 확인하거나, 기존 파일을 수정 및 삭제하거나, 새 파일을 폴더에 업로드합니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오. 모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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
   <p>현재: Workfront Fusion 라이선스 요구 사항 없음</p>
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

* [트리거](#triggers)
* [액션](#actions)

### 트리거

* [[!UICONTROL 새 이벤트]](#new-event)
* [[!UICONTROL 파일 보기]](#watch-files)

#### [!UICONTROL 새 이벤트]

이 즉시 트리거 모듈은 파일이 추가, 이동, 복사, 삭제, 잠김 또는 잠금 해제되면 시나리오를 시작합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>보내는 메시지를 보는 데 사용할 웹후크를 선택합니다. 웹후크를 추가하려면 <strong>[!UICONTROL 추가]</strong>를 클릭하고 웹후크의 이름과 연결을 입력하십시오.</p> <p> [!UICONTROL Workfront Fusion]에 [!UICONTROL Box] 계정을 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">서비스에 연결 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 반환되는 최대 이벤트 수]</p> </td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 이벤트 수를 입력합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 보기]

이 트리거 모듈은 새 파일이 추가되거나 감시되는 폴더에서 기존 파일이 업데이트될 때 시나리오를 시작합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">연결</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">폴더</td> 
   <td> <p>감시할 폴더를 선택합니다. 시나리오는 단일 폴더를 볼 수 있습니다.</p> 
   </td> 
  </tr> 
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

* [[!UICONTROL 파일 삭제]](#delete-a-file)
* [[!UICONTROL 파일 가져오기]](#get-a-file)
* [[!UICONTROL 파일 업데이트]](#update-a-file)
* [파일 [!UICONTROL 업로드]](#upload-a-file)

#### [!UICONTROL 파일 삭제]

이 작업 모듈은 파일을 삭제합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td>모듈에서 삭제할 파일의 고유 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 가져오기]

이 작업 모듈은 파일을 다운로드합니다.

파일의 ID를 지정합니다.

>[!NOTE]
>
>이 모듈은 파일을 후속 모듈에 제공하는 데 유용합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td>모듈에서 검색할 파일의 고유 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업데이트]

이 작업 모듈은 파일을 업데이트합니다.

파일의 ID를 지정합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL 파일 ID]</td> 
   <td>모듈에서 업데이트할 파일의 고유 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업로드]

이 작업 모듈은 파일을 업로드합니다.

파일을 지정합니다. 파일의 새 파일 이름을 제공할 수도 있습니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Box] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 폴더]</td> 
   <td> <p>파일을 업로드할 폴더를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 모듈이 성공하지 못한 경우 다음 사항을 고려하십시오.
>
>* 파일 크기가 [!DNL Box] 플랜의 최대 파일 크기 제한을 초과하거나 [!DNL Box] 계정의 저장소 할당량을 모두 사용했을 수 있습니다. 저장소 공간을 늘리려면 [!DNL Box]에서 기존 파일을 삭제하거나 [!DNL Box] 계정을 업그레이드하세요.
>* [!DNL Box]이(가) 같은 이름의 파일을 하나 이상의 폴더에 업로드하지 않습니다. 대상 폴더에 업로드되는 파일과 같은 이름의 파일이 포함되어 있으면 시나리오 실행이 오류와 함께 종료됩니다. 이 문제를 방지하려면 파일 이름을 바꾸십시오. 파일을 업데이트하려면 **[!UICONTROL 파일 업데이트]** 모듈을 사용하십시오.
