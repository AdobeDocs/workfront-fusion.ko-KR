---
title: Power BI 모듈
description: Adobe Workfront Fusion에는 Adobe Workfront 라이센스 외에 Adobe Workfront Fusion 라이센스가 필요합니다.
author: Becky
feature: Workfront Fusion
exl-id: 73eb70e1-3f3d-419d-9cde-3ec3cda224f8
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2600'
ht-degree: 0%

---

# [!DNL Power BI]개 모듈

[!DNL Power BI]은(는) 관련자들에게 데이터를 시각화하고 제공할 수 있는 애플리케이션입니다. 다양한 소스에서 데이터를 가져올 수 있습니다.

>[!NOTE]
>
>Workfront Fusion은 데이터 소스가 아닙니다. Workfront Fusion은 데이터 소스를 만들고 사용할 수 있지만 데이터를 저장하지 않습니다.


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

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## Microsoft Power BI API 정보

Microsoft Power BI 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td> https://api.powerbi.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 버전</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.0.2</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Power BI]개 모듈 및 해당 필드

[!DNL Power BI]을(를) 구성하면 Workfront Fusion에 아래 나열된 필드가 표시됩니다. 이러한 필드와 함께 앱이나 서비스의 액세스 수준과 같은 요소에 따라 추가 필드가 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [Adobe Workfront Fusion에서 한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [대시보드](#dashboards)
* [보고서](#reports)
* [데이터 세트](#dataset)
* [앱](#apps)
* [기타](#other)

### 대시보드

* [대시보드 만들기](#create-a-dashboard)
* [대시보드 가져오기](#get-a-dashboard)
* [대시보드 타일 가져오기](#get-a-dashboard-tile)
* [목록 대시보드 타일](#list-dashboard-tiles)
* [목록 대시보드](#list-dashboards)

#### [!UICONTROL 대시보드 만들기]

이 작업 모듈은 새 대시보드를 만듭니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 이름]</td>
      <td>대시보드의 이름을 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>새 대시보드를 소유할 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 대시보드 가져오기]

이 작업 모듈은 지정된 대시보드의 메타데이터를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 대시보드 ID 입력]</td>
      <td>
        <p>옵션을 선택하거나 매핑하여 메타데이터를 검색할 대시보드를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 대시보드 ID]</td>
      <td>
        <p>메타데이터를 검색할 대시보드의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>메타데이터를 검색할 대시보드를 소유한 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 대시보드 타일 가져오기]

이 작업 모듈은 지정된 대시보드 타일의 메타데이터를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 대시보드 ID 입력]</td>
      <td>
        <p>옵션을 선택하거나 매핑하여 검색할 대시보드 세부 정보를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 대시보드 ID]</td>
      <td>
        <p>세부 정보를 검색할 대시보드의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 타일 ID]</td>
      <td>세부 정보를 검색할 [!DNL Power BI] 타일의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>검색할 타일을 소유한 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 대시보드 타일 나열]

이 검색 모듈은 대시보드 타일 목록을 검색합니다.

<table>
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 대시보드 ID 입력]</td>
    <td>
      <p>옵션을 선택하거나 매핑하여 타일을 나열할 대시보드를 선택합니다.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 대시보드 ID]</td>
    <td>
      <p>나열할 타일이 포함된 대시보드의 ID를 입력하거나 매핑합니다.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
    <td>나열할 타일이 포함된 대시보드를 소유한 그룹의 ID를 선택하거나 매핑합니다.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 제한]  </td>
    <td>
      <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
    </td>
  </tr>
</tbody>
</table>

#### [!UICONTROL 대시보드 나열]

이 검색 모듈은 대시보드 목록을 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>
        <p>나열할 대시보드를 소유한 그룹의 ID를 선택하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]  </td>
      <td>
        <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

### 보고서

* [보고서 복사](#copy-a-report)
* [보고서 삭제](#delete-a-report)
* [보고서 가져오기](#get-a-report)
* [목록 보고서](#list-reports)

#### [!UICONTROL 보고서 복사]

이 작업 모듈은 기존 보고서를 복사합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID 입력]</td>
      <td>
        <p>옵션을 선택하거나 매핑하여 복사할 보고서를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID]</td>
      <td>
        <p>복사할 보고서의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>복사할 보고서를 소유한 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 새로 복사된 보고서 이름]</td>
      <td>새 보고서의 이름을 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 보고서 삭제]

이 작업 모듈은 보고서를 삭제합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID 입력]</td>
      <td>
        <p>옵션을 선택하거나 매핑하여 삭제할 보고서를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID]</td>
      <td>
        <p>삭제할 보고서의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>삭제할 보고서를 소유한 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 보고서 가져오기]

이 작업 모듈은 지정된 보고서의 메타데이터를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID 입력]</td>
      <td>
        <p>옵션을 선택하거나 매핑하여 메타데이터를 검색할 보고서를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID]</td>
      <td>
        <p>메타데이터를 검색할 보고서의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>메타데이터를 검색할 보고서를 소유한 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 보고서 나열]

이 검색 모듈은 보고서 목록을 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>
        <p>나열할 보고서를 소유하는 그룹의 ID를 선택하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]  </td>
      <td>
        <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>


### 데이터 세트

* [데이터 세트 테이블에서 행 추가/삭제](#add-or-delete-rows-in-a-dataset-table)
* [데이터 세트 만들기](#create-a-dataset)
* [데이터 세트 삭제](#delete-a-dataset)
* [데이터 세트 가져오기](#get-a-dataset)
* [데이터 세트 나열](#list-datasets)
* [데이터 세트 새로 고침](#refresh-a-dataset)

#### [!UICONTROL 데이터 집합 테이블에서 행 추가 또는 삭제]

이 작업 모듈은 지정된 푸시 데이터 세트 테이블의 행을 추가하거나 삭제합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 테이블 입력]</td>
      <td>옵션을 선택하거나 매핑하여 조정할 테이블이 포함된 데이터 세트를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 데이터 세트 ID]</td>
      <td>추가하거나 삭제할 행이 포함된 데이터 세트의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 테이블 이름]  </td>
      <td>
        <p>추가하거나 삭제할 행이 포함된 테이블의 이름을 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>데이터 세트를 소유하는 그룹의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 작업 선택]</td>
      <td>
        <p>수행할 작업을 선택하거나 매핑합니다.</p>
        <ul>
          <li>
            <p>[!UICONTROL 행 추가]</p>
          </li>
          <li>
            <p>[!UICONTROL 모든 행 삭제]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 행]</td>
      <td>
        <p>행 필드를 추가합니다.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL 키]</b>
            </p>
            <p>키 이름을 입력하거나 매핑합니다.</p>
          </li>
          <li>
            <p><b>[!UICONTROL 필드 형식]</b>
            </p>
            <p>필드 유형을 선택하거나 매핑합니다.</p>
            <ul>
              <li>
                <p>부울</p>
              </li>
              <li>
                <p>Date</p>
              </li>
              <li>
                <p>텍스트</p>
              </li>
              <li>
                <p>숫자</p>
              </li>
            </ul>
          </li>
          <li>
            <p>[!UICONTROL 값]</p>
            <p>키 값을 입력하거나 매핑합니다.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 데이터 집합 만들기]

이 작업 모듈은 새 데이터 세트를 만듭니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 이름]</td>
      <td>데이터 세트의 이름을 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>새 데이터 세트를 소유할 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 기본 모드]</td>
      <td>
        <p>데이터 세트에 대한 기본 모드 선택 또는 매핑:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL As Azure]</b>: 다음에 대한 실시간 연결이 있는 데이터 집합 [!DNL Azure Analysis Service]</p>
          </li>
          <li>
            <p><b>[!UICONTROL As On Prem]</b>: [!DNL On-premise Analysis] 서비스에 대한 실시간 연결이 있는 데이터 집합입니다.</p>
          </li>
          <li>
            <p><b>[!DNL Push]</b>: 로 데이터를 푸시하기 위해 프로그래밍 방식으로 액세스할 수 있는 데이터 세트 [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Push Streaming]</b>: 데이터 스트리밍을 지원하고 데이터를 로 푸시하기 위해 프로그래밍 방식으로 액세스할 수 있는 데이터 세트입니다 [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Streaming]</b>: 데이터 스트리밍을 지원하는 데이터 세트</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 테이블]</td>
      <td>데이터 세트에 테이블을 추가합니다. 필드의 경우 <a href="#Table" class="MCXref_0">테이블 필드</a>를 참조하십시오.</td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Data sources]</td>
      <td>데이터 소스를 추가합니다. 필드의 경우 <a href="#Data" class="MCXref_0">데이터 원본 필드</a>를 참조하세요.</td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Default Retention Policy]  </td>
      <td>
        <p>데이터 세트에 대한 의도적인 정책을 선택하거나 매핑합니다.</p>
        <ul>
          <li>
            <p>[!UICONTROL 없음]</p>
          </li>
          <li>
            <p>[!UICONTROL 기본 FIFO]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### 테이블 필드

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 이름]</td>
      <td>
        <p>  테이블 이름을 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 열]</td>
      <td>
        <p>열을 추가합니다.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL 이름]</b>
            </p>
            <p>열 이름을 입력(매핑)합니다.</p>
          </li>
          <li>
            <p><b>[!UICONTROL 데이터 형식]</b>
            </p>
            <p>데이터 유형 선택 또는 매핑:</p>
            <ul>
              <li>
                <p>[!UICONTROL String]</p>
              </li>
              <li>
                <p>[!UICONTROL 정수]</p>
              </li>
              <li>
                <p>[!UICONTROL 부울]</p>
              </li>
              <li>
                <p>[!UICONTROL Date Time]</p>
              </li>
            </ul>
          </li>
          <li>
            <p><b>[!UICONTROL 형식 문자열]</b>
            </p>
            <p>형식 문자열을 입력(매핑)합니다.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 행]</td>
      <td>행 세부 정보를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 측정값]</td>
      <td>테이블에 대한 측정값을 추가합니다.</td>
    </tr>
  </tbody>
</table>

##### 데이터 소스 필드

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 데이터베이스]  </td>
      <td>
        <p>사용할 데이터베이스를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Server]  </td>
      <td>
        <p>사용할 서버의 이름을 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]  </td>
      <td>
        <p>사용할 URL을 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 데이터 소스 ID]</td>
      <td>
        <p>  데이터 소스의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 데이터 소스 유형]  </td>
      <td>
        <p>데이터 소스 유형을 선택하거나 매핑합니다. 예: SQL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 게이트웨이 ID]  </td>
      <td>사용할 게이트웨이의 ID를 입력하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 데이터 집합 삭제]

이 작업 모듈은 데이터 세트를 삭제합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID 입력]</td>
      <td>
        <p>옵션을 선택하거나 매핑하여 삭제할 데이터 세트를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID]</td>
      <td>
        <p>삭제할 데이터 세트의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>삭제하려는 데이터 세트를 소유하는 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 데이터 세트 가져오기]

이 작업 모듈은 지정된 데이터 세트의 메타데이터를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID 입력]</td>
      <td>
        <p>옵션을 선택하거나 매핑하여 메타데이터를 검색할 보고서를 선택합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID]</td>
      <td>
        <p>메타데이터를 검색할 데이터 세트의 ID를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>메타데이터를 검색할 데이터 세트를 소유하는 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 데이터 세트 나열]

이 검색 모듈은 데이터 세트 목록을 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>메타데이터를 검색할 보고서를 소유한 그룹의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]</td>
      <td>
        <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 데이터 집합 새로 고침]

이 작업 모듈은 지정된 데이터 세트를 새로 고칩니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 데이터 세트 입력]</td>
      <td>옵션을 선택하거나 매핑하여 새로 고칠 데이터 세트를 선택합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 데이터 세트 ID]</td>
      <td>새로 고침할 데이터 세트의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 테이블 이름]  </td>
      <td>
        <p>추가하거나 삭제할 행이 포함된 테이블의 이름을 입력하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 그룹 ID]  </td>
      <td>데이터 세트를 소유하는 그룹의 ID를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 알림 옵션]  </td>
      <td>
        <p>알림 옵션을 선택하거나 매핑합니다.</p>
        <ul>
          <li>
            <p>완료 시 [!UICONTROL Mail]</p>
          </li>
          <li>
            <p>[!UICONTROL 실패 시 메일]</p>
          </li>
          <li>
            <p>[!UICONTROL 알림 없음]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### 앱

* [앱 가져오기](#get-an-app)
* [앱의 대시보드 가져오기](#get-an-apps-dashboard)
* [앱의 보고서 가져오기](#get-an-apps-report)
* [앱 대시보드 나열](#list-apps-dashboards)
* [앱 보고서 나열](#list-apps-reports)
* [목록 앱](#list-apps)
* [앱 시청](#watch-apps)

#### [!UICONTROL 앱 가져오기]

이 작업 모듈은 지정된 앱의 메타데이터를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 앱 ID]  </td>
      <td>
        <p>검색할 앱의 ID를 선택하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 앱의 대시보드 가져오기]

이 작업 모듈은 지정된 앱 대시보드의 메타데이터를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 앱 ID]  </td>
      <td>
        <p>검색할 대시보드가 포함된 앱의 ID를 선택하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID]</td>
      <td>
        <p>  검색할 대시보드의 ID를 선택하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 앱의 보고서 가져오기]

이 작업 모듈은 지정된 앱 보고서의 메타데이터를 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 앱 ID]  </td>
      <td>
        <p>검색할 보고서가 포함된 앱의 ID를 선택하거나 매핑합니다.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 보고서 ID]</td>
      <td>
        <p>  검색할 보고서의 ID를 선택하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 앱 나열]

이 검색 모듈은 설치된 모든 앱 목록을 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]  </td>
      <td>
        <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 앱 대시보드 나열]

이 검색 모듈은 지정된 앱에서 대시보드 목록을 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 앱 ID]</td>
      <td>대시보드를 나열할 앱의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]  </td>
      <td>
        <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 앱 보고서 나열]

이 검색 모듈은 지정된 앱에서 모든 보고서 목록을 검색합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 앱 ID]</td>
      <td>보고서를 나열할 앱의 ID를 선택하거나 매핑합니다.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]  </td>
      <td>
        <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 앱 시청]

이 트리거 모듈은 앱이 업데이트될 때 시나리오를 시작합니다.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 제한]  </td>
      <td>
        <p>각 시나리오 실행 주기 동안 모듈이 반환할 최대 레코드 수를 입력하거나 매핑합니다.</p>
      </td>
    </tr>
  </tbody>
</table>

### 기타

#### [!UICONTROL API 호출 만들기]

이 작업 모듈은 [!DNL Power BI] API에 대한 API 호출을 수행합니다.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>[!DNL Power BI] 계정을 Workfront Fusion에 연결하는 방법에 대한 지침은 <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 연결 만들기 - 기본 지침</a>을 참조하십시오.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 경로]</p>
      </td>
      <td>
        <p><code>https://api.powerbi.com</code>과(와) 관련된 경로를 입력하십시오. 예: <code>/v1.0/myorg/datasets</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 메서드]</p>
      </td>
      <td>
        <p>API 호출을 구성하는 데 필요한 [!UICONTROL HTTP] 요청 메서드를 선택합니다. 자세한 내용은 [!UICONTROL HTTP] 요청 메서드를 참조하십시오.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>표준 JSON 개체 형태로 요청의 헤더를 추가합니다.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion은 인증 헤더와 x-api-key 헤더를 자동으로 추가합니다.</p>
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
