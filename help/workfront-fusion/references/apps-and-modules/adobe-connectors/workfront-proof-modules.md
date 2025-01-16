---
title: Workfront Proof 모듈
description: ' [!DNL Adobe Workfront Fusion] 시나리오에서는  [!DNL Workfront Proof]을(를) 사용하는 워크플로를 자동화할 수 있을 뿐만 아니라 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.'
author: Becky
feature: Workfront Fusion, Workfront Proof, Digital Content and Documents
exl-id: 9e556ae5-e672-4872-9c40-8c8e5f0305be
source-git-commit: 27c1d38d4c9e4b47d2d9da094b005a0e72ce9bd0
workflow-type: tm+mt
source-wordcount: '2664'
ht-degree: 0%

---

# [!DNL Workfront Proof]개 모듈

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!DNL Workfront Proof]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

특정 이벤트를 기반으로 증명을 업데이트하고 증명 수신자를 검색하는 등 현재 [!DNL Workfront] 또는 [!DNL Workfront Proof]에서 증명에서 지원되지 않는 작업을 실행해야 하는 경우 유용합니다.

[!DNL Workfront Proof] 커넥터는 조직에서 사용할 수 있는 활성 앱 수에 포함되지 않습니다. 모든 시나리오는 [!DNL Workfront Proof] 앱만 사용하더라도 조직의 총 시나리오 수에 대해 계산됩니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

## Workfront Proof 정보

Workfront Proof 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v21.3.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.8.92</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Workfront Proof]을(를) [!DNL Workfront Fusion]에 연결

[!DNL Workfront Fusion] 모듈 내에서 직접 [!DNL Workfront Proof] 계정에 연결할 수 있습니다.

1. [!DNL Workfront Fusion] 모듈에서 [!UICONTROL Connection] 필드 옆에 있는 [!UICONTROL **추가**]&#x200B;를 클릭합니다

2. 다음 필드를 채웁니다.

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>연결 이름 입력</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Environment]</td>
                <td>프로덕션 환경인지 미리 보기 또는 샌드박스와 같은 비프로덕션 환경인지 선택합니다.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Type]</td>
                <td>서비스 계정인지 개인 계정인지 선택합니다.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Email / Username]</td>
                <td>[!DNL Workfront Proof] 계정의 사용자 이름을 입력하십시오.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Password]</td>
                <td>[!DNL Workfront Proof] 계정의 암호를 입력하십시오.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant ID]</td>
                <td><strong>참고</strong>: BYOK를 사용하지 않는 고객은 이 필드를 비워 두어야 합니다. <p>이 계정의 테넌트 ID를 입력하십시오. 테넌트 ID를 찾는 데 도움이 필요한 경우 Workfront 고객 지원 센터에 문의하십시오.</p></td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Domain Extension]</td>
                <td>계정에 액세스하는 데 사용하는 URL의 확장을 입력합니다. <p>예: <code>com</code> 또는 <code>eu</code></p></td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Production, Preview, or Custom Environment]</td>
                <td>연결할 프로덕션, 미리보기 또는 사용자 지정 환경입니다.</td>
            </tr>
        </tbody>
    </table>


3. 연결을 저장하고 모듈로 돌아가려면 [!UICONTROL **계속**]&#x200B;을 클릭하세요.

## [!DNL Workfront Proof]개 모듈 및 해당 필드

[!DNL Workfront Proof] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL Workfront Proof] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [트리거](#triggers)
* [액션](#actions)
* [검색 결과](#searches)

### 트리거

* [PDF 요약 보기](#watch-for-pdf-summary)
* [[!UICONTROL Watch Proof Activity]](#watch-proof-activity)
* [증명 보기](#watch-proofs)

#### [!UICONTROL Watch for PDF Summary]

이 즉시 트리거 모듈은 누군가가 증명에 대한 PDF 요약을 만들 때 시나리오를 실행합니다.

이 모듈에는 웹후크가 필요합니다.

모듈은 증명과 연결된 모든 표준 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 또한 PDF 요약에 대한 새 이벤트 구독을 만들고 페이로드로 전송된 `pdf_url` 특성에서 콘텐츠를 출력합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook name]</td> 
   <td>새 웹후크의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proof Activity]

이 트리거 모듈은 증명 증명 시 지정된 활동이 발생하는 경우 시나리오를 실행합니다.

모듈은 증명과 연결된 모든 표준 필드와 연결이 액세스하는 모든 사용자 지정 필드 및 값을 반환합니다. 또한 PDF 요약에 대한 새 이벤트 구독을 만들고 페이로드로 전송된 `pdf_url` 특성에서 콘텐츠를 출력합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Activity type]</td> 
   <td>새 결정(증명 상태 변경 포함)을 감시할지 또는 전체 증명 상태 변경만 감시할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proofs]

이 예약된 트리거 모듈은 누군가가 증명을 만들거나 결정할 때 시나리오를 실행합니다.

모듈은 지정한 기간 동안 찾은 모든 레코드 목록과 함께 해당 유형을 반환합니다. 또한 지정한 필드의 값도 반환합니다. 증명에서 결정된 사항이 모듈에서 발견된 경우, 별도의 필드에 이전 값과 현재 값을 모두 포함합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 작업은 사용자가 지정한 정기적으로 예약된 간격으로 발생합니다.

이 정보를 검색하려면 [!DNL Workfront Proof]에서 증명 또는 증명에 액세스할 수 있는 충분한 권한이 있어야 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">레코드 유형</td> 
   <td>새 증명을 감시할지 또는 전체 증명 결정을 새로 감시할지 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">제한</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">페이지당 항목 수</td> 
   <td> <p>결과의 페이지에 페이지를 매기려면 결과의 각 페이지에 표시되어야 하는 반환된 결과 수를 입력하거나 매핑합니다. 이 숫자는 100보다 작거나 같아야 합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 액션

* [[!UICONTROL Create Proof]](#create-proof)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download Proof]](#download-proof)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Request PDF Summary]](#request-pdf-summary)
* [[!UICONTROL Update Proof]](#update-proof)
* [[!UICONTROL Upload File]](#upload-file)

#### [!UICONTROL Create Proof]

<!--Cannot test Jan 2025-->

이 작업 모듈은 [!DNL Workfront Proof]에 새 증명 또는 새 증명 버전을 만듭니다.

새 버전을 만드는 경우에는 새 증명에 대한 매개 변수를 지정하고 소스 증명에 대한 매개 변수를 지정합니다.

모듈이 새 증명 또는 증명 버전의 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Type]</td> 
   <td> <p>만들어진 증명에 기본 워크플로를 사용할지 [!UICONTROL Automated Workflow]을(를) 사용할지 지정합니다.</p> <p>그런 다음 선택한 증명 유형에 대해 표시되는 필드를 채웁니다. 예를 들어 [!UICONTROL Automated Workflow]을(를) 선택한 경우 <strong>[!UICONTROL Workflow Stages]</strong> 필드를 채워 단계를 구성합니다.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Allow original file to be downloaded]</td> 
   <td>증명을 만든 원본 파일을 다운로드하도록 허용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Classic Proof Viewer]</td> 
   <td>Classic Proof Viewer 사용 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Combine all files into single proof]</td> 
   <td>모든 파일을 하나의 다중 페이지 증명으로 결합하려면 이 옵션을 활성화합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create a new proof version]</td> 
   <td>모듈이 기존 증명의 새 버전을 만들도록 하려면 이 옵션을 선택합니다. 그런 다음 표시되는 <strong>[!UICONTROL Existing Proof ID]</strong> 필드에 증명의 고유 ID를 매핑하거나 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link Label]</td> 
   <td>사용자 정의 증명 링크에 대한 레이블을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link URL]</td> 
   <td>사용자 지정 링크에 대한 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>다음 숫자 중 하나를 입력하여 생성된 증명에 사용할 다음 기본 이메일 알림 설정 중 하나를 지정합니다.
    <ul>
     <li><strong>1</strong> - 새 댓글 및 답글 모두</li>
     <li><strong>2</strong> - 내 댓글에 답글 달기</li>
     <li><strong>3</strong> - 일별 요약</li>
     <li><strong>4</strong> - 시간별 요약</li>
     <li><strong>5</strong> - 결정 전용</li>
     <li><strong>9</strong> - 비활성화됨</li>
    </ul></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Excel Summary]</td> 
   <td>Excel 파일에 증명 설명을 다운로드하는 기능을 비활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable PDF Summary]</td> 
   <td>PDF 파일에 증명 주석을 다운로드하는 기능을 비활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>이 증명에 대한 구독 이메일을 비활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Embed Player]</td> 
   <td>이 증명에 대해 포함된 플레이어를 사용할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>참여자가 아닌 사람이 증명 구독을 허용할지 여부를 선택합니다.<br>이 옵션을 선택하면 이 표에 설명된 대로 구독자에 대한 기본 역할을 선택할 수도 있습니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>구독 이메일 유효성 검사를 활성화할지 여부를 선택합니다. 활성화된 경우 구독자가 증명에 액세스하려면 이메일의 링크를 클릭해야 합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>만들어진 증명에서 팀 URL을 숨기거나 표시할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Hash] <span style="font-weight: normal;">또는</span> [!UICONTROL File Hashes]</td> 
   <td>증명 또는 증명을 만들 파일의 ID를 추가합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Names]</td> 
   <td>생성된 증명에 대한 파일 이름 추가 필수 필드입니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>필요한 모든 결정을 수행한 후 만들어진 증명을 잠글 것인지 여부를 지정합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Notify recipients about this proof]</td> 
   <td>증명을 만들 때 수신자에게 알림을 보낼지 여부를 나타내는 옵션을 선택합니다.&gt;</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof name]</td> 
   <td>생성된 증명의 이름을 입력합니다. 필수 필드입니다. 여러 증명에 대한 이름을 구분하려면 파이프 기호(|)를 사용하십시오.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof owner ID]</td> 
   <td>증명 소유자의 ID를 입력하거나 매핑합니다. 이 필드를 비워 두면 증명 소유자가 현재 사용자로 설정됩니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reference ID]</td> 
   <td>증명에 대한 참조 ID를 입력합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require electronic signature]</td> 
   <td>증명에 대해 결정을 내리는 사람에게 전자 서명을 제출하도록 요구할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>생성된 증명에 로그인이 필요한지 여부를 지정합니다. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Resolution ID]</td> 
   <td>증명에 사용할 해상도의 ID를 입력합니다. 해결 ID 목록을 보려면 [!DNL Workfront Proof] <a href="https://api.proofhq.com/home/objects/soapworkflowproofobject.html">API 설명서</a>를 참조하십시오.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL SWF]</td> 
   <td>SWF 증명 유형을 입력합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Show] [item]</td> 
   <td>각 항목에 대해 증명에 표시할지 여부를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Workspace ID]</td> 
   <td>증명을 만들려는 작업 공간의 ID를 입력합니다. </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Recipients]</td> 
   <td>증명을 만들 수신자의 이메일 주소를 추가합니다 .</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>생성된 증명에 대해 원하는 기한을 지정합니다. 다음 날짜 형식을 사용하십시오.</p> <p><code>YYYY-MM-DD hh:mm</code></p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Custom API Call]

이 작업 모듈을 사용하면 [!DNL Workfront Proof] API에 대해 사용자 지정 인증된 호출을 수행할 수 있습니다. 이렇게 하면 다른 [!DNL Workfront Proof] 모듈에서 수행할 수 없는 데이터 흐름 자동화를 만들 수 있습니다.

모듈은 상태 코드, 헤더 및 본문을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Method]</td> 
   <td>API 호출에 대한 작업을 설정합니다. 사용 가능한 작업은 <a href="https://api.proofhq.com/">증명 API 설명서</a>를 참조하십시오.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Body (XML)]</td> 
   <td> <p>표준 JSON 개체의 형태로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>참고:  <p>JSON에서 <code>if</code>과(와) 같은 조건문을 사용할 때 따옴표를 조건문 외부에 넣으십시오.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**예:**
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/wfp-api-module-example-350x586.png)

#### [!UICONTROL Download Proof]

이 작업 모듈은 ID를 사용하여 식별하는 특정 증명의 소스 파일을 다운로드합니다.

증명의 ID를 지정합니다.

모듈은 증명을 만드는 데 사용된 소스 파일의 내용을 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 정보를 검색하려면 [!DNL Workfront Proof]의 레코드에 액세스할 수 있는 충분한 권한이 있어야 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>[!UICONTROL Proof Details] 페이지에 있는 증명의 고유 ID를 입력하십시오.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

이 작업 모듈은 [!DNL Workfront Proof]의 단일 증명에서 데이터를 읽습니다.

증명의 ID와 증명에서 원하는 정보를 지정합니다.

이 모듈은 증명에 대해 선택한 필드의 값과 해당 유형을 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 정보를 검색하려면 [!DNL Workfront Proof]의 레코드에 액세스할 수 있는 충분한 권한이 있어야 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>증명, 증명 주석 또는 증명 검토자를 읽을지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>모듈에서 읽을 레코드의 고유 [!DNL Workfront Proof] ID를 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Request PDF Summary]

이 작업 모듈은 [!DNL Workfront Proof]의 특정 증명에 대한 PDF 요약을 요청합니다.

증명의 ID를 지정합니다.

모듈은 PDF 요약 정보를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 정보를 검색하려면 [!DNL Workfront Proof]의 레코드에 액세스할 수 있는 충분한 권한이 있어야 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>PDF 요약을 요청할 증명의 고유 [!DNL Workfront Proof] ID를 입력하십시오.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Callback URL]</td> 
   <td>PDF 요약을 전송할 URL을 입력하거나 매핑합니다.</td> 
  </tr> 
 </tbody> 
</table>

##### 가능한 오류

* **오류**: &quot;[!UICONTROL You do not have privilege to perform this request. The stage must contain at least one recipient.]&quot;
* **솔루션**: 워크플로우의 단계에 할당된 유일한 솔루션이 아닌지 확인하십시오. 워크플로우의 단계에 할당된 다른 사용자가 있어야 합니다.

#### [!UICONTROL Update Proof]

이 작업 모듈은 [!DNL Workfront Proof]의 기존 증명을 업데이트합니다.

증명의 ID 및 레코드 유형과 출력에 포함할 필드를 지정합니다.

모듈은 연결에서 액세스하는 모든 사용자 지정 필드 및 값과 함께 레코드와 연결된 모든 표준 필드를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 정보를 검색하려면 [!DNL Workfront Proof]의 레코드에 액세스할 수 있는 충분한 권한이 있어야 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>[!UICONTROL Proof Details] 페이지에 있는 증명의 고유 ID를 입력하십시오. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>생성된 증명에 대해 원하는 기한을 지정합니다. 날짜 형식 <code>YYYY-MM-DD hh:mm</code>을(를) 사용합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>다음 기본 이메일 알림 설정 중 생성된 증명에 사용할 설정을 선택합니다.
    <ul>
     <li> [!UICONTROL All new comments and replies]</li>
     <li>[!UICONTROL Replies to my comments]</li>
     <li>[!UICONTROL Daily summary]</li>
     <li> [!UICONTROL Hourly summary]</li>
     <li> [!UICONTROL Decisions only]</li>
     <li> [!UICONTROL Disabled]</li>
    </ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default Role]</td> 
   <td>증명의 기본 역할을 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>이 증명에 대한 구독 이메일을 비활성화할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>참여자가 아닌 사람이 증명 구독을 허용할지 여부를 선택합니다.<br>이 옵션을 선택하면 [!UICONTROL Default Role] 필드에서도 옵션을 선택할 수 있습니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>구독 이메일 유효성 검사를 활성화할지 여부를 선택합니다. 활성화된 경우 구독자가 증명에 액세스하려면 이메일의 링크를 클릭해야 합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>만들어진 증명에서 팀 URL을 숨기거나 표시할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>필요한 모든 결정을 수행한 후 만들어진 증명을 잠글 것인지 여부를 지정합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Message]</td> 
   <td>증명과 함께 표시할 메시지를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID] </td> 
   <td>업데이트할 증명의 ID를 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Name]</td> 
   <td>업데이트할 증명의 이름을 입력하거나 매핑합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>생성된 증명에 로그인이 필요한지 여부를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show Versions Like]</td> 
   <td>이 증명의 다른 버전에 대한 링크를 표시할지 여부를 선택합니다.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>증명 제목 입력 또는 매핑</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File]

이 작업 모듈은 [!DNL Workfront Proof]의 [!UICONTROL Create Proof] 모듈에서 사용할 파일을 업로드합니다.

모듈이 업로드된 파일에 대한 해시 ID를 반환합니다. 이 정보는 시나리오의 후속 모듈에 매핑할 수 있습니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL List Workflow Templates]](#list-workflow-templates)
* [[!UICONTROL Search]](#search)

#### [!UICONTROL List Workflow Templates]

이 검색 모듈에는 사용 가능한 모든 워크플로우 템플릿이 나열됩니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>이 모듈에 대한 출력 번들에 포함할 정보를 선택합니다.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 템플릿 수를 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search]

이 검색 모듈은 지정한 검색 쿼리와 일치하는 [!DNL Workfront Proof]의 개체에서 레코드를 찾습니다.

증명을 검색하는 경우 모듈에서 증명 ID를 반환합니다. 또는 수신자를 검색할 경우 수신자의 사용자 ID, 이메일, 이름, 위치 및 이메일 별칭을 반환합니다. 시나리오의 후속 모듈에서 이 정보를 매핑할 수 있습니다.

이 정보를 검색하려면 [!DNL Workfront Proof]의 레코드에 액세스할 수 있는 충분한 권한이 있어야 합니다.

이 모듈을 구성할 때 다음 필드가 표시됩니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>[!DNL Workfront Proof] 계정을 [!DNL Workfront Fusion]에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">[!DNL Adobe Workfront Fusion]에 연결 만들기 - 기본 지침</a>을 참조하세요.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Search for]</td> 
   <td> <p>모듈에서 검색할 레코드 유형을 선택합니다.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Proof]</strong> </p> <p>검색할 증명의 증명 이름을 입력합니다.</p> </li> 
     <li> <p><strong>[!UICONTROL Recipient]</strong> </p> <p>검색할 수신자의 이메일 주소를 입력합니다.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Result Set]</td> 
   <td>모듈이 <strong>[!UICONTROL All Matching Records]</strong>을(를) 검색할지 <strong>[!UICONTROL First Matching Record]</strong>만 검색할지 여부를 나타냅니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort By]</td> 
   <td>결과를 정렬할 필드를 선택합니다.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sorting Direction]</td> 
   <td> <p>결과를 오름차순으로 정렬할지 아니면 내림차순으로 정렬할지 선택합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

