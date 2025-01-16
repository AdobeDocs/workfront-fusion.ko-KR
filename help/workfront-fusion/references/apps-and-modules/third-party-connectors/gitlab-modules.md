---
title: GitLab 모듈
description: Adobe Workfront Fusion에는 Adobe Workfront 라이센스 외에 Adobe Workfront Fusion 라이센스가 필요합니다.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3554'
ht-degree: 0%

---

# [!UICONTROL GitLab]개 모듈

Adobe Workfront Fusion에는 Adobe Workfront 라이센스 외에 Adobe Workfront Fusion 라이센스가 필요합니다.

[!DNL Adobe Workfront Fusion] 시나리오에서는 [!UICONTROL GitLab]을(를) 사용하는 워크플로를 자동화하고 여러 타사 응용 프로그램 및 서비스에 연결할 수 있습니다.

>[!NOTE]
>
>이 문서에서는 API 설명서 및 일반적으로 [!DNL GitLab] 기능에 대해 어느 정도 익숙할 것으로 예상합니다.

시나리오를 만드는 방법에 대한 지침은 [시나리오 만들기: 문서 인덱스](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)의 문서를 참조하십시오.

모듈에 대한 자세한 내용은 [모듈: 문서 인덱스](/help/workfront-fusion/references/modules/modules-toc.md)의 문서를 참조하십시오.

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

## [!DNL GitLab]을(를) [!DNL Workfront Fusion]에 연결 {#connect-gitlab-to-workfront-fusion}

1. [!DNL Workfront Fusion] [!DNL Gitlab] 모듈에서 연결 필드 옆의 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.
1. 다음 필드를 구성합니다.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td> <p>연결의 이름을 입력합니다.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL [!DNL GitLab] URL]</td> 
      <td>[!DNL GitLab] 인스턴스의 URL을 입력하십시오.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Access Token]</td> 
      <td><p>[!UICONTROL Private Token] 또는 [!UICONTROL Personal Access Token]을(를) 입력하십시오.</p><p>[!DNL GitLab]에서 개인 액세스 토큰을 찾거나 만드는 방법에 대한 자세한 내용은 [!DNL GitLab] 설명서의 <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">개인 액세스 토큰</a>에서 "개인 액세스 토큰 만들기"를 참조하십시오.</p></td> 
     </tr> 
    </tbody> 
   </table>


1. **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.
1. 연결을 만들고 모듈로 돌아가려면 **[!UICONTROL Authorize]**&#x200B;을(를) 클릭하십시오.

## [!DNL GitLab]개 모듈 및 해당 필드

[!DNL GitLab] 모듈을 구성할 때 [!DNL Workfront Fusion]에 아래 나열된 필드가 표시됩니다. 앱 또는 서비스의 액세스 수준과 같은 요소에 따라 이러한 필드와 함께 [!DNL GitLab] 필드가 추가로 표시될 수 있습니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

필드나 함수 위에 맵 단추가 표시되면 이 단추를 사용하여 해당 필드에 대한 변수와 함수를 설정할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![맵 전환](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 트리거

+++**[!UICONTROL Watch build status]**

이 즉시 트리거 모듈은 빌드의 상태가 변경되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 빌드 상태 변경을 감시할 프로젝트</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commit/MR/issue/snippet comments]**

이 인스턴트 트리거 모듈은 커밋, 병합 요청, 문제 또는 코드 조각에 대한 댓글이 있을 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 댓글을 확인할 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commits (pushes)]**

이 즉시 트리거 모듈은 커밋이 저장소에 푸시될 때 시나리오를 시작합니다. 이 모듈은 태그를 푸시할 때 시나리오를 시작하지 않습니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 커밋 여부를 확인할 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issue comment]**

이 즉시 트리거 모듈은 문제에 대한 댓글이 있을 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 문제 설명을 확인할 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issues]**

이 [!UICONTROL instant trigger] 모듈은 문제가 만들어지거나 기존 문제가 업데이트, 종료 또는 다시 열릴 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 문제를 확인하고자 하는 프로젝트</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge requests]**

이 인스턴스 트리거 모듈은 다음 중 하나가 발생하면 시나리오를 시작합니다.

* 새 병합 요청이 작성됨
* 기존 병합 요청이 업데이트, 병합 또는 종료되었습니다.
* 소스 분기에 커밋이 추가됨


<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 병합 요청을 감시할 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge request comments]**

이 인스턴스 트리거 모듈은 병합 요청에 대한 댓글이 있을 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 병합 요청 주석을 감시할 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch pipeline status]**

이 즉시 트리거 모듈은 파이프라인의 상태가 변경될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 파이프라인 상태 변경을 감시할 프로젝트</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch projects]**

이 예약된 트리거 모듈은 인증된 사용자가 멤버인 새 프로젝트가 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL GitLab] 계정을 [!DNL Workfront] Fusion에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">[!DNL GitLab]을(를) [!DNL Workfront] Fusion에 연결</a>을 참조하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">최대 결과</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 지켜볼 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository branches]**

이 예약된 트리거 모듈은 새 분기가 저장소에 추가되면 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL GitLab] 계정을 [!DNL Workfront] Fusion에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">[!DNL GitLab]을(를) [!DNL Workfront] Fusion에 연결</a>을 참조하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">최대 결과</td> 
   <td> <p>각 시나리오 실행 주기 동안 모듈이 지켜볼 최대 레코드 수를 입력하거나 매핑합니다.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository tags]**

이 즉시 트리거 모듈은 저장소에서 태그를 만들거나 삭제할 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 태그를 확인할 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch snippet comments]**

이 즉시 트리거 모듈은 코드 조각에 새 주석이 추가될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 댓글을 확인할 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch todos]**

이 예약된 트리거 모듈은 새로운 할 일이 추가되면 시나리오를 시작합니다. 필터가 적용되지 않은 경우 새 보류 중인 작업이 추가되면 트리거가 실행됩니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [할 일 목록 가져오기](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos)를 참조하십시오.

+++

+++**[!UICONTROL Watch wiki page]**

이 인스턴트 트리거 모듈은 위키 페이지가 만들어지거나 편집될 때 시나리오를 시작합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>이 트리거에 사용할 웹후크를 선택하거나 새 웹후크를 추가합니다. </p><p>새 웹후크를 추가하려면 <ol><li>[!UICONTROL webhook] 필드 옆의 <b>[!UICONTROL Add]</b>을(를) 클릭합니다.</li><li>다음을 입력합니다. <ul><li>Webhook 이름</li><li>이 웹후크에 사용할 연결입니다.</li><li>웹후크에서 Wiki 페이지를 볼 프로젝트입니다.</li></ul></li><li><b>[!UICONTROL Save]</b>을(를) 클릭하여 웹후크를 저장하고 모듈로 돌아갑니다. </td> 
   </tr> 
   </tbody> 
</table>

+++

### 액션

+++**[!UICONTROL Accept merge request]**

이 작업 모듈은 제출된 변경 사항을 지정된 병합 요청과 병합합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [병합 요청 수락](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr)을 참조하십시오.

+++

+++**[!UICONTROL Cancel a build]**

이 작업 모듈은 프로젝트의 단일 빌드를 취소합니다.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>[!DNL GitLab] 계정을 [!DNL Workfront] Fusion에 연결하는 방법에 대한 지침은 이 문서에서 <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">[!DNL GitLab]을(를) [!DNL Workfront] Fusion에 연결</a>을 참조하십시오.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>취소할 빌드가 포함된 프로젝트를 선택하거나 매핑합니다.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td>취소할 빌드를 선택하거나 매핑합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge commit message]</td> 
   <td> 병합에 대한 커밋 메시지를 입력하거나 매핑합니다.
    </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Should remove source branch]</td> 
   <td>병합이 완료되면 소스 분기를 제거할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge when build succeeds]</td> 
   <td>빌드가 완료되는 즉시 병합 요청을 병합할지 여부를 선택합니다.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL SHA]</td> 
   <td>존재하는 경우 이 SHA는 소스 분기의 HEAD과 일치해야 합니다. 일치하지 않으면 병합이 실패합니다.</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Cancel a pipeline's builds]**

이 작업 모듈은 단일 파이프라인에 대한 빌드를 취소합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [파이프라인 작업 취소](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs)를 참조하십시오.

+++

+++**[!UICONTROL Cancel merge when pipeline succeeds]**

파이프라인이 성공할 때 병합 요청이 병합으로 설정되면 이 작업 모듈은 해당 작업을 취소합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [파이프라인이 성공하면 병합 취소](https://docs.gitlab.com/ee/api/merge_requests.html)를 참조하십시오.

+++

+++**[!UICONTROL Cherry pick a commit]**

이 작업 모듈 체리는 지정된 분기에 대한 커밋을 선택합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [Cherry 커밋 선택](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit)을 참조하십시오.

+++

+++**[!UICONTROL Create a new label]**

이 작업 모듈은 지정된 저장소에 대한 새 레이블을 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [새 레이블 만들기](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label)를 참조하십시오.

+++

+++**[!UICONTROL Create a new pipeline]**

이 작업 모듈은 지정된 프로젝트에 대한 새 파이프라인을 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [새 파이프라인 만들기](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline)를 참조하십시오.

+++

+++**[!UICONTROL Create a new release]**

이 작업 모듈은 기존 git 태그에 릴리스 정보를 추가합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [릴리스 만들기](https://docs.gitlab.com/ee/api/releases/#create-a-release)를 참조하십시오.

+++

+++**[!UICONTROL Create a new tag]**

이 작업 모듈은 제공된 참조를 가리키는 새 태그를 저장소에 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [새 태그 만들기](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag)를 참조하십시오.

+++

+++**[!UICONTROL Create a todo]**

이 작업 모듈은 선택한 문제에 대한 현재 사용자의 할 일을 만듭니다. 현재 사용자는 이 모듈에 사용되는 연결에 대한 자격 증명으로 식별되는 사용자입니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [할 일 만들기](https://docs.gitlab.com/ee/api/issues.html#create-a-todo)를 참조하십시오.

+++

+++**[!UICONTROL Create a todo on a merge request]**

이 작업 모듈은 선택한 병합 요청에 대해 현재 사용자에 대한 작업을 만듭니다. 현재 사용자는 이 모듈에 사용되는 연결에 대한 자격 증명으로 식별되는 사용자입니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [할 일 만들기](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo)를 참조하십시오.

+++

+++**[!UICONTROL Create merge request]**

이 작업 모듈은 프로젝트에 대한 새 병합 요청을 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [병합 요청 만들기](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr)를 참조하십시오.

+++

+++**[!UICONTROL Create new file in repository]**

이 작업 모듈은 선택한 저장소에 새 파일을 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [저장소에 새 파일 만들기](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository)를 참조하십시오.

+++

+++**[!UICONTROL Create new issue note]**

이 작업 모듈은 단일 프로젝트 문제에 대한 문제 메모를 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [새 문제 메모 만들기](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note)를 참조하십시오.

+++

+++**[!UICONTROL Create new merge request note]**

이 작업 모듈은 단일 병합 요청에 대한 메모를 생성합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [새 병합 요청 메모 만들기](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note)를 참조하십시오.

+++

+++**[!UICONTROL Create a new milestone]**

이 작업 모듈은 프로젝트에 대한 새 이정표를 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [새 마일스톤 만들기](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone)를 참조하십시오.

+++

+++**[!UICONTROL Create new snippet note]**

이 작업 모듈은 단일 코드 조각에 대한 새 메모를 만듭니다. 코드 조각 노트는 사용자가 코드 조각에 게시할 수 있는 주석입니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [새 코드 조각 메모 만들기](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note)를 참조하십시오.

+++

+++**[!UICONTROL Create repository branch]**

이 작업 모듈은 단일 저장소 분기를 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [저장소 분기 만들기](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch)를 참조하십시오.

+++

+++**[!UICONTROL Create build variable]**

이 작업 모듈은 새 빌드 변수를 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [변수 만들기](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable)를 참조하십시오.

+++

+++**[!UICONTROL Delete a merge request]**

이 작업 모듈은 관리자 및 프로젝트 소유자만 사용할 수 있습니다. 문제가 되는 병합 요청이 삭제됩니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [병합 요청 삭제](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request)를 참조하십시오.

+++

+++**[!UICONTROL Delete existing file in repository]**

이 작업 모듈은 저장소에서 기존 파일을 삭제합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [저장소의 기존 파일 삭제](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository)를 참조하십시오.

+++

+++**[!UICONTROL Delete repository branch]**

이 작업 모듈은 저장소에서 분기를 삭제합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [저장소 분기 삭제](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch)를 참조하십시오.

+++

+++**[!UICONTROL Edit issue]**

이 작업 모듈은 기존 프로젝트 문제를 업데이트합니다. 이 호출은 문제를 종료로 표시하는 데에도 사용됩니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [문제 편집](https://docs.gitlab.com/ee/api/issues.html#edit-issue)을 참조하십시오.

+++

+++**[!UICONTROL Edit Milestone]**
이 작업 모듈은 기존 프로젝트 이정표를 업데이트합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [마일스톤 편집](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone)을 참조하세요.

+++

+++**[!UICONTROL Erase a build]**

이 작업 모듈은 프로젝트 빌드를 지웁니다(작업 아티팩트 및 작업 로그 제거).

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [작업 지우기](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job)를 참조하십시오.

+++

+++**[!UICONTROL Get a list of todos]**

이 검색 모듈은 할 일 항목의 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [할 일 목록 가져오기](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos)를 참조하십시오.

+++

+++**[!UICONTROL Get a single build]**

이 작업 모듈은 프로젝트의 단일 작업을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 작업 가져오기](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job)를 참조하십시오.

+++

+++**[!UICONTROL Get a single repository tag]**

이 작업 모듈은 해당 이름으로 결정된 특정 저장소 태그를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 저장소 태그 가져오기](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag)를 참조하십시오.

+++

+++**[!UICONTROL Get a specific deployment]**

이 작업 모듈은 특정 배포를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [특정 배포 가져오기](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment)를 참조하십시오.

+++

+++**[!UICONTROL Get all issues assigned to a single milestone]**

이 검색 모듈은 단일 프로젝트 마일스톤에 할당된 모든 문제를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 마일스톤에 할당된 모든 문제 가져오기](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone)를 참조하십시오.

+++

+++**[!UICONTROL Get file from repository]**

이 작업 모듈은 이름, 크기 또는 컨텐츠와 같은 저장소의 파일에 대한 정보를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [저장소에서 파일 가져오기](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository)를 참조하십시오.

+++

+++**[!UICONTROL Get project users]**

이 검색 모듈은 프로젝트의 사용자를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [프로젝트 사용자 가져오기](https://docs.gitlab.com/ee/api/projects.html#get-project-users)를 참조하십시오.

+++

+++**[!UICONTROL Get a single issue]**

이 작업 모듈은 문제 세부 정보를 검색합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>새 연결을 만들려면 이 문서에서 Workfront Fusion에 대한 <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab]</a>을(를) 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td> <p>세부 정보를 가져올 문제가 포함된 프로젝트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID]</td> 
   <td> <p>세부 정보를 검색할 문제의 이름을 입력하거나 매핑합니다.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Get single issue note]**

이 작업 모듈은 특정 프로젝트 문제에 대한 단일 메모를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 문제 메모 가져오기](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note)를 참조하십시오.

+++

+++**[!UICONTROL Get single merge request]**

이 작업 모듈은 단일 병합 요청에 대한 정보를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 병합 요청 가져오기](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr)를 참조하십시오.

+++

+++**[!UICONTROL Get single merge request changes]**

이 검색 모듈은 파일 및 변경 사항을 포함한 병합 요청에 대한 정보를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [단일 병합 요청 변경 사항 가져오기](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes)를 참조하십시오.

+++

+++**[!UICONTROL Get single merge request commits]**

이 작업 모듈은 병합 요청 커밋 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [단일 병합 요청 커밋 가져오기](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits)를 참조하십시오.

+++

+++**[!UICONTROL Get single merge request note]**

이 작업 모듈은 지정된 병합 요청에 대한 단일 메모를 반환합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [단일 병합 요청 메모 가져오기](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note)를 참조하십시오.

+++

+++**[!UICONTROL Get a Milestone]**

이 작업 모듈은 마일스톤 세부 정보를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [단일 마일스톤 가져오기](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone)를 참조하십시오.

+++

+++**[!UICONTROL Get single project]**

이 작업 모듈은 프로젝트 세부 정보를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 프로젝트 가져오기](https://docs.gitlab.com/ee/api/projects.html#get-single-project)를 참조하십시오.

+++

+++**[!UICONTROL Get single repository branch]**

이 작업 모듈은 저장소 분기 세부 정보를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 저장소 분기 가져오기](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch)를 참조하십시오.

+++

+++**[!UICONTROL Get snippet note]**

이 모듈은 지정된 코드 조각에 대한 단일 메모를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [단일 코드 조각 메모 가져오기](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note)를 참조하십시오.

+++

+++**[!UICONTROL Get the comments of a commit]**

이 검색 모듈은 프로젝트에서 커밋 주석을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [커밋 주석 가져오기](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit)를 참조하십시오.

+++

+++**[!UICONTROL Get the diff of a commit]**

이 작업 모듈은 프로젝트의 커밋 차이를 가져옵니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [커밋 비교](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit)를 참조하십시오.

+++

+++**[!UICONTROL Keep artifacts]**

만료 설정 시 아티팩트가 삭제되지 않도록 합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [아티팩트 보관](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts)을 참조하십시오.

+++

+++**[!UICONTROL List all merge request notes]**

이 검색 모듈은 단일 병합 요청에 대한 모든 메모 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [모든 병합 요청 메모 나열](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes)을 참조하세요.

+++

+++**[!UICONTROL List all snippet notes]**

이 모듈은 단일 코드 조각에 대한 모든 참고 목록을 가져옵니다. 코드 조각 노트는 사용자가 코드 조각에 게시할 수 있는 주석입니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [??](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes)을(를) 참조하십시오.

+++

+++**[!UICONTROL List commit builds]**

이 검색 모듈은 프로젝트의 특정 커밋에 대한 빌드 목록을 반환합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>새 연결을 만들려면 이 문서에서 Workfront Fusion에 대한 <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab]</a>을(를) 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>빌드를 나열할 커밋이 포함된 프로젝트를 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> 검색을 특정 상태로 빌드하도록 제한하려면 상태를 선택합니다. 이 필드를 비워 두면 커밋의 모든 빌드가 반환됩니다.  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL List issues]**

이 검색 모듈은 지정된 필터 설정에 따라 모든 문제를 반환합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [문제 나열](https://docs.gitlab.com/ee/api/issues.html#list-issues)을 참조하세요.

+++

+++**[!UICONTROL List Issues That Close on Merge]**

이 검색 모듈은 제공된 병합 요청을 병합하여 종결될 모든 문제를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [병합 시 닫히는 문제 나열](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge)을 참조하십시오.

+++

+++**[!UICONTROL List Labels]**

이 검색 모듈은 프로젝트의 모든 레이블을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [목록 레이블](https://docs.gitlab.com/ee/api/labels.html#list-labels)을 참조하십시오.

+++

+++**[!UICONTROL List merge requests]**

이 검색 모듈은 필터 설정별로 모든 병합 요청을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [병합 요청 나열](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests)을 참조하십시오.

+++

+++**[!UICONTROL List Owned Projects]**

이 검색 모듈은 인증된 사용자가 소유자로 설정된 프로젝트를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [사용자 프로젝트 나열](https://docs.gitlab.com/ee/api/projects.html#list-all-projects)을 참조하십시오.

+++

+++**[!UICONTROL List project builds]**

이 검색 모듈은 프로젝트의 빌드 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [프로젝트 작업 나열](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs)을 참조하십시오.

+++

+++**[!UICONTROL List project deployments]**

이 검색 모듈은 프로젝트의 배포 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [프로젝트 배포 나열](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments)을 참조하세요.

+++

+++**[!UICONTROL List project issue notes]**

이 검색 모듈은 단일 문제에 대한 모든 참고 사항 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [프로젝트 문제 메모 나열](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes)을 참조하십시오.

+++

+++**[!UICONTROL List project issues]**

이 검색 모듈은 지정된 프로젝트의 모든 문제를 반환합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [프로젝트 문제 나열](https://docs.gitlab.com/ee/api/issues.html#list-project-issues)을 참조하십시오.

+++

+++**[!UICONTROL List project milestones]**

이 검색 모듈은 프로젝트의 모든 이정표를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [프로젝트 마일스톤 나열](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones)을 참조하세요.

+++

+++**[!UICONTROL List project pipelines]**

이 검색 모듈은 프로젝트의 모든 파이프라인을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [프로젝트 파이프라인 나열](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines)을 참조하십시오.

+++

+++**[!UICONTROL List project repository tags]**

이 검색 모듈은 이름별로 알파벳 역순으로 정렬된 프로젝트에서 저장소 태그 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [프로젝트 저장소 태그 나열](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags)을 참조하세요.

+++

+++**[!UICONTROL List project variables]**

이 검색 모듈은 프로젝트 변수 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [프로젝트 변수 나열](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables)을 참조하십시오.

+++

+++**[!UICONTROL List projects]**

이 검색 모듈은 인증된 사용자가 멤버인 모든 프로젝트를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [모든 프로젝트 나열](https://docs.gitlab.com/ee/api/projects.html#list-all-projects)을 참조하세요.

+++

+++**[!UICONTROL List repository branches]**

이 모듈은 검색어로 저장소 분기를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [저장소 분기 나열](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches)을 참조하세요.

+++

+++**[!UICONTROL List repository commits]**

이 검색 모듈은 프로젝트의 저장소 커밋 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [저장소 커밋 나열](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits)을 참조하십시오.

+++

+++**[!UICONTROL List repository contributors]**

이 검색 모듈은 저장소 기여자 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [참가자](https://docs.gitlab.com/ee/api/repositories.html#contributors)를 참조하십시오.

+++

+++**[!UICONTROL List repository tree]**

이 검색 모듈은 프로젝트의 저장소 파일 및 디렉터리 목록을 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [목록 저장소 트리](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree)를 참조하십시오.

+++

+++**[!UICONTROL Mark a todo as done]**

이 작업 모듈은 현재 사용자에 대해 해당 ID로 지정된 단일 보류 중인 할 일 항목을 완료 상태로 표시합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [수행할 항목 표시](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done)를 참조하십시오.

+++

+++**[!UICONTROL Modify existing issue note]**

문제의 기존 메모를 수정합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [기존 문제 메모 수정](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note)을 참조하십시오.

+++

+++**[!UICONTROL Modify existing merge request note]**

병합 요청의 기존 메모를 수정합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [기존 병합 요청 메모 수정](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note)을 참조하십시오.

+++

+++**[!UICONTROL Modify existing snippet note]**

이 작업 모듈은 코드 조각의 기존 메모를 수정합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [기존 코드 조각 메모 수정](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note)을 참조하십시오.

+++

+++**[!UICONTROL New issue]**

이 작업 모듈은 새 프로젝트 문제를 만듭니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서에서 [새 문제](https://www.integromat.com/en/help/app/gitlab)를 참조하십시오.

+++

+++**[!UICONTROL Play a build]**

이 작업 모듈은 작업을 시작하는 수동 작업을 트리거합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [작업 재생](https://docs.gitlab.com/ee/api/jobs.html#play-a-job)을 참조하십시오.

+++

+++**[!UICONTROL Post comment to commit]**

이 작업 모듈은 커밋에 주석을 추가합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [커밋에 대한 댓글 게시](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit)을 참조하십시오.

+++

+++**[!UICONTROL Remove variable]**

이 작업 모듈은 프로젝트의 변수를 제거합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [변수 제거](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable)를 참조하십시오.

+++

+++**[!UICONTROL Retry a build]**

이 작업 모듈은 커밋에서 단일 빌드를 다시 시도합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>새 연결을 만들려면 이 문서에서 Workfront Fusion에 대한 <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab]</a>을(를) 참조하십시오.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>다시 시도할 빌드가 포함된 프로젝트를 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td> 다시 시도할 빌드를 선택합니다. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Retry Failed Jobs in a Pipeline]**

이 작업 모듈은 파이프라인에서 빌드를 다시 시도하지 못했습니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [파이프라인에서 작업 다시 시도](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline)를 참조하십시오.

+++

+++**[!UICONTROL Get a Variable]**

이 모듈은 프로젝트 특정 변수의 세부 정보를 검색합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [변수 세부 정보 표시](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details)를 참조하십시오.

+++

+++**[!UICONTROL Update a release]**

이 작업 모듈은 릴리스를 업데이트합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [릴리스 업데이트](https://docs.gitlab.com/ee/api/releases/#update-a-release)를 참조하십시오.

+++

+++**[!UICONTROL Update merge request]**

이 작업 모듈은 기존 병합 요청을 업데이트합니다. 대상 지점, 제목을 변경하거나 MR을 닫을 수 있습니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [병합 요청 업데이트](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr)를 참조하십시오.

+++

+++**[!UICONTROL Update a Variable]**

이 작업 모듈은 프로젝트의 변수를 업데이트합니다.

필드에 대한 자세한 내용은 [!DNL GitLab] 설명서의 [변수 업데이트](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable)를 참조하십시오.

+++
