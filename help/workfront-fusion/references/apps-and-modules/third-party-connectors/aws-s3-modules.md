---
title: AWS S3 모듈
description: '[!DNL Adobe Workfront Fusion AWS] S3 모듈을 사용하면 S3 버킷에서 작업을 수행할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
TQID: 'https://experienceleague.adobe.com/FDkre6osF2kT7Kz-5VGradQLa7GPSJ6MHPH9-FgM-ag'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 7c25013f7a94000651e8331199ad985d40651ae3
workflow-type: tm+mt
source-wordcount: '2637'
ht-degree: 16%
---
# AWS S3 모듈

[!DNL Adobe Workfront Fusion AWS] S3 모듈을 사용하면 S3 버킷에서 작업을 수행할 수 있습니다.

## 액세스 요구 사항

+++ 이 문서의 기능에 대한 액세스 요구 사항을 보려면 확장하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 패키지</td> 
   <td> <p>모든 Adobe Workfront 워크플로 패키지 및 모든 Adobe Workfront 자동화 및 통합 패키지</p><p>Workfront Ultimate</p><p>Workfront Prime 및 Select 패키지 및 Workfront Fusion 추가 구매.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 라이선스</td> 
   <td> <p>표준</p><p>작업 이상</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 라이선스</td> 
   <td>
   <p>운영 기반: 운영 기반 라이센스가 있는 조직에서 사용 가능</p>
   <p>커넥터 기반(이전): 작업 자동화 및 통합을 위한 Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">제품</td> 
   <td>
   <p>조직에 Workfront 자동화 및 통합이 포함되지 않은 Select 또는 Prime Workfront 패키지가 있는 경우 Adobe Workfront Fusion을 구매해야 합니다.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

이 테이블의 정보에 대한 자세한 내용은 [설명서의 액세스 요구 사항](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)을 참조하십시오.

Adobe Workfront Fusion 라이선스에 대한 자세한 내용은 [Adobe Workfront Fusion 라이선스](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)를 참조하십시오.

+++

## 전제 조건

[!UICONTROL AWS S3] 모듈을 사용하려면 [!DNL Amazon Web Service] 계정이 있어야 합니다.

## AWS S3 API 정보

AWS S3 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">기본 URL</td> 
   <td><pre><code>https://s3.&#123;&#123;parameters.region&#125;&#125;.amazonaws.com</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL AWS]를 Workfront Fusion에 연결 {#connect-aws-to-workfront-fusion}

* [페더레이션 연결을 사용하여 AWS을 Workfront Fusion에 연결](#connect-aws-to-workfront-fusion-using-a-federated-connection)
* [API 사용자를 사용하여 AWS을 Workfront Fusion에 연결](#connect-aws-to-workfront-fusion-using-an-api-user)

### 페더레이션 연결을 사용하여 AWS을 Workfront Fusion에 연결

+++ 를 확장하여 이 연결 유형에 대한 지침을 봅니다.

* [페더레이션 연결을 사용하여 AWS을 Workfront Fusion에 연결하기 위한 사전 요구 사항](#prerequisites-to-connecting-aws-to-workfront-fusion-using-a-federated-connection)
* [AWS에서 ID 공급자로 Workfront Fusion 추가](#add-workfront-fusion-as-an-identity-provider-in-aws)
* [IAM 역할 만들기](#create-the-iam-role)
* [Workfront Fusion에서 연결 만들기](#create-the-connection-in-workfront-fusion)
* [역할의 트러스트 정책에 연결 추가](#add-the-connection-to-the-roles-trust-policy)
* [연결 확인](#verify-the-connection)
* [문제 해결](#troubleshooting)

페더레이션 연결을 사용하면 IAM 사용자를 생성하거나 Fusion에 액세스 키를 저장하지 않고도 Workfront Fusion이 AWS 계정에 액세스할 수 있습니다.
대신 Workfront Fusion을 AWS 계정에 신뢰할 수 있는 ID 공급자로 등록하고 특정 IAM 역할을 사용할 수 있는 단일 Fusion 연결을 구성합니다. 연결이 실행되면 Fusion은 짧은 기간 동안 ID 증명을 제공하고 AWS은 자체 만료 예정인 임시 자격 증명을 반환합니다. 오래 지속되는 키를 만들거나 저장하거나 회전시킬 수 없습니다.

>[!NOTE]
>
>이 연결을 설정하려면 AWS 콘솔에 대한 두 번의 방문이 필요합니다. 먼저 역할을 만든 다음 Workfront Fusion에서 연결을 만든 다음 AWS으로 돌아가 트러스트 정책을 완료합니다. 이는 트러스트 정책의 일부가 하나의 특정 연결을 식별하며 해당 식별자가 연결을 만들 때까지 존재하지 않기 때문입니다.

#### 페더레이션 연결을 사용하여 AWS을 Workfront Fusion에 연결하기 위한 사전 요구 사항

이 연결을 만들려면 다음이 필요합니다.

* ID 공급자를 만들고 역할을 만들고 편집할 수 있는 AWS IAM의 권한입니다. 이는 일반적으로 정책 또는 이에 준하는 것을 의미합니다. 이 액세스 권한이 없는 경우 클라우드에 있는 사용자에게 질문하거나
보안 팀이 AWS 단계를 완료합니다.
* Workfront Fusion에서 연결을 만드는 기능입니다.


#### AWS에서 ID 공급자로 Workfront Fusion 추가

이 단계는 AWS에 Workfront Fusion에서 발급한 토큰을 신뢰할 수 있음을 알려줍니다. AWS 계정당 한 번 수행합니다. 조직의 누군가가 이미 이 공급자를 추가한 경우 [IAM 역할 만들기](#create-the-iam-role)로 건너뜁니다.

1. AWS 콘솔에 로그인하고 **IAM** > **ID 공급자**(으)로 이동합니다.
1. **공급자 추가**&#x200B;를 선택하십시오.
1. 공급자 형식에는 **OpenID 연결**&#x200B;을 선택하세요.
1. 공급자 URL에서 다음을 입력한 다음 **지문 가져오기**&#x200B;를 선택합니다.

   ```
   https://oidc.automations.adobe.com
   ```

1. Audience에서 다음을 입력합니다.

   ```
   sts.amazonaws.com
   ```

1. **공급자 추가**&#x200B;를 선택하십시오.
1. [IAM 역할 만들기](#create-the-iam-role)를 계속합니다.

#### IAM 역할 만들기

역할은 AWS 계정에서 연결이 수행할 수 있는 작업을 정의합니다. 각 연결의 액세스 권한을 독립적으로 부여하고 취소할 수 있도록 연결당 하나의 역할을 만듭니다.

1. IAM에서 **역할**(으)로 이동하여 **역할 만들기**&#x200B;를 선택합니다.
1. 신뢰할 수 있는 엔터티 형식의 경우 **웹 ID**&#x200B;을(를) 선택하십시오.
1. ID 공급자에서 `oidc.automations.adobe.com`을(를) 선택합니다.
1. 대상자에서 `sts.amazonaws.com`을(를) 선택합니다.
1. **다음**&#x200B;을 선택한 다음 이 연결에 필요한 권한 정책을 첨부하십시오.
연결에 실제로 사용하는 권한만 부여합니다. (예: 다음에서만 읽는 연결)
버킷 하나에 `AmazonS3FullAccess`이(가) 필요하지 않습니다.
1. 역할에 인식할 수 있는 명확한 이름을 지정합니다. 예: `WorkfrontFusionFederatedConnection`.
1. **역할 만들기**&#x200B;를 선택합니다.
1. 방금 생성한 역할을 열고 요약 영역에서 해당 ARN을 복사합니다. 다음과 같습니다. `arn:aws:iam::123456789012:role/WorkfrontFusionFederatedConnection`

1. [Workfront Fusion에서 연결 만들기](#create-the-connection-in-workfront-fusion)를 계속합니다.

#### Workfront Fusion에서 연결 만들기

1. 모듈의 연결 설정 화면에서 통합 연결 유형을 선택합니다.
1. [IAM 역할 만들기](#create-the-iam-role)에서 복사한 역할 ARN을 입력하십시오.
1. Select **Create**.
Workfront Fusion에는 세 가지 값이 표시됩니다. 다음 절차에서 사용합니다.

<table>
  <tr>
    <td>발급자</td>
    <td>항상 <code>https://oidc.automations.adobe.com</code>입니다. AWS에서 추가한 ID 공급자와 일치합니다.</td>
  </tr>
  <tr>
    <td>제목</td>
    <td>이 하나의 연결을 식별합니다. <code>fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964</code>(으)로 보입니다. 만드는 모든 연결에 대해 다릅니다.</td>
  </tr>
  <tr>
    <td>대상자</td>
    <td>항상 <code>sts.amazonaws.com</code>입니다.</td>
  </tr>
</table>

1. 이 패널을 연 상태로 두고 제목 값을 복사합니다.

   >[!NOTE]
   >
   >패널을 닫거나 취소를 선택하지 마십시오. 나머지 절차를 완료할 때까지 연결이 완료되지 않습니다. 패널을 닫으면 새 연결에 새 제목 이 표시되므로 연결을 삭제하고 다시 시작해야 합니다.

1. 계속해서 [역할의 트러스트 정책에 연결을 추가](#add-the-connection-to-the-roles-trust-policy)합니다.

#### 역할의 트러스트 정책에 연결 추가

이 절차를 완료할 때까지 이 역할은 일반적으로 Workfront Fusion을 신뢰하지만 아직 이 특정 연결에서 이를 사용할 수는 없습니다.

1. 새 브라우저 탭에서 AWS 콘솔로 돌아가서 만든 역할을 엽니다.
1. **트러스트 관계** 탭을 선택한 다음 **트러스트 정책 편집**&#x200B;을 선택합니다.
1. 정책을 고유한 값으로 대체하여 다음과 같이 바꿉니다.

   * `123456789012`을(를) AWS 계정 ID로 바꾸기
   * `sub` 값을 Workfront Fusion에서 복사한 제목으로 바꿉니다.


   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow", 
         "Principal": {
           "Federated": "arn:aws:iam::123456789012:oidc-provider/oidc.automations.adobe.com"
       },
       "Action": "sts:AssumeRoleWithWebIdentity", "Condition": {
        "StringEquals": {
          "oidc.automations.adobe.com:sub": "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", 
          "oidc.automations.adobe.com:aud": "sts.amazonaws.com"
        }
       }
      }
    ]
   }
   ```

1. **정책 업데이트**&#x200B;를 선택하십시오.
1. [연결 확인](#verify-the-connection)을 계속합니다.

>[!TIP]
>
>두 개 이상의 연결에서 동일한 역할을 사용할 수 있도록 하려면 제목을 배열로 나열합니다. AWS에서는 토큰이 목록의 값과 일치하는 경우 역할을 사용할 수 있습니다.
>
>```
>"oidc.automations.adobe.com:sub": [ "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:29011"
>]
>```
>
>하위 값을 와일드카드로 바꾸지 마십시오. 이렇게 하면 나중에 다른 사용자가 만든 연결을 포함하여 조직의 모든 연결에서 역할을 사용할 수 있습니다


#### 연결 확인

1. 연결 패널이 열려 있는 Workfront Fusion 브라우저 탭으로 돌아갑니다.
1. **저장**&#x200B;을 클릭합니다.

   Workfront Fusion은 AWS에 문의하여 트러스트 정책을 확인하고 임시 자격 증명을 반환합니다. 모든 것이 올바르게 설정된 경우 연결이 성공적으로 검증되고 모듈 설정을 계속할 수 있습니다.
   확인에 실패하면 패널이 열린 상태로 유지되며 오류가 표시됩니다. AWS에서 문제를 수정하고 [저장]을 다시 선택합니다. 연결을 다시 만들 필요가 없으며 주제도 변경되지 않습니다.

이 시점에서부터 연결은 자체 자격 증명을 갱신합니다. 회전할 키가 없으며 유지 관리해야 하는 만료도 없습니다.

#### 문제 해결


<table>
  <tr>
    <th>오류</th>
    <th>의미</th>
    <th>확인할 사항</th>
  </tr>
  <tr>
    <td>InvalidIdentityToken</td>
    <td>AWS에서 토큰을 등록된 id 공급자와 일치시킬 수 없습니다.</td>
    <td>Workfront Fusion 추가에 설명된 ID 공급자를 AWS의 ID 공급자로 추가하고 해당 URL이 정확히 https://oidc.automations.adobe.com이며 뒤에 슬래시가 없는지 확인합니다.</td>
  </tr>
  <tr>
    <td>역할을 가정할 때 AccessDenied</td>
    <td>ID 공급자가 등록되었지만 트러스트 정책이 이 연결과 일치하지 않습니다.</td>
    <td>트러스트 정책의 하위 값이 Workfront Fusion에 표시된 주제와 동일한 문자 대 문자이고 aud가 sts.amazonaws.com인지 확인합니다. 다른 연결에서 복사된 제목 이 가장 일반적인 원인입니다.</td>
  </tr>
  <tr>
    <td>연결이 작동하면 나중에 실패합니다</td>
    <td> </td>
    <td>역할의 권한 정책이 변경되었는지 또는 역할이 삭제되고 다시 만들어졌는지 확인합니다. 역할을 다시 생성해도 ARN은 변경되지 않지만 트러스트 정책은 재설정됩니다.</td>
  </tr>
</table>

+++

### API 사용자를 사용하여 AWS을 Workfront Fusion에 연결

+++ 를 확장하여 이 연결 유형에 대한 지침을 봅니다.

[!DNL AWS S3]을(를) Workfront Fusion에 연결하려면 [!DNL AWS] 계정을 Workfront Fusion에 연결해야 합니다. 이렇게 하려면 먼저 [!DNL AWS] [!UICONTROL IAM]에서 API 사용자를 만들어야 합니다.

1. [!DNL AWS] [!UICONTROL IAM] 계정에 로그인합니다.
1. **[!UICONTROL ID 및 액세스 관리]** > **[!UICONTROL 액세스 관리]** > **[!UICONTROL 사용자]**(으)로 이동합니다.

1. **[!UICONTROL 사용자 추가]**&#x200B;를 클릭합니다.
1. 새 사용자의 이름을 입력하고 [!UICONTROL 액세스 형식] 섹션에서 **[!UICONTROL 프로그래밍 방식 액세스]** 옵션을 선택합니다.
1. **[!UICONTROL 기존 정책을 직접 첨부]**&#x200B;를 클릭한 다음 검색 창에서 **[!UICONTROL AmazonS3FullAccess]**&#x200B;를 검색합니다. 나타나면 클릭한 다음 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. 다른 대화 상자 화면을 계속 진행하고 **[!UICONTROL 사용자 만들기]**&#x200B;를 클릭합니다.
1. 제공된 **[!UICONTROL 액세스 키 ID]** 및 **[!UICONTROL 비밀 액세스 키]**&#x200B;를 복사합니다.

1. Workfront Fusion으로 이동하여 [!DNL AWS S3] 모듈의 **[!UICONTROL 연결 만들기]** 대화 상자를 엽니다.
1. 7단계의 각 필드에 [!UICONTROL 액세스 키 ID] 및 [!UICONTROL 비밀 액세스 키]를 입력하고 **[!UICONTROL 계속]**&#x200B;을 클릭하여 연결을 설정하십시오.

연결이 설정되었습니다. 모듈 설정을 진행할 수 있습니다.

+++

## [!DNL AWS S3] 모듈 및 해당 필드

* [액션](#actions)
* [검색 결과](#searches)

[!DNL AWS S3] 모듈을 구성할 때 Workfront Fusion은 아래 나열된 필드를 표시합니다. 이와 함께 앱 또는 서비스의 액세스 레벨과 같은 요인에 따라 추가적인 [!DNL AWS S3] 필드가 표시될 수 있습니다. 모듈의 굵은 글씨 제목은 필수 필드를 나타냅니다.

필드 또는 함수 위에 있는 맵 버튼을 보면 해당 필드의 변수와 함수를 설정하는 데 사용할 수 있습니다. 자세한 내용은 [한 모듈에서 다른 모듈로 정보 매핑](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)을 참조하십시오.

![토글 매핑](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [액션](#actions)
* [검색 결과](#searches)

### 액션

* [[!UICONTROL 버킷 만들기]](#create-bucket)
* [[!UICONTROL 파일 가져오기]](#get-file)
* [[!UICONTROL API 호출 만들기]](#make-an-api-call)
* [[!UICONTROL 파일 업로드]](#upload-file)

#### [!UICONTROL 버킷 만들기]

이 작업 모듈은 AWS에서 버킷을 만듭니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL AWS] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL AWS] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 이름] </td> 
   <td> <p>새 버킷의 이름을 입력합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 영역] </td> 
   <td> <p>지역 끝점을 선택합니다. 자세한 내용은 AWS 설명서에서 <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">지역 끝점</a>을 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 가져오기]

이 작업 모듈은 버킷에서 파일을 다운로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL AWS] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL AWS] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 영역] </td> 
   <td> <p>지역 끝점을 선택합니다. 자세한 내용은 [!DNL AWS] 설명서의 <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">지역 끝점</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 버킷] </td> 
   <td> <p>파일을 다운로드할 버킷을 선택합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 경로]</p> </td> 
   <td> <p>파일 경로를 입력합니다. 예: <code>/photos/2019/February/image023.jpg</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL API 호출 만들기]

이 작업 모듈은 AWS S3 API에 대한 사용자 지정 호출을 만듭니다.

[!DNL Amazon S3] API에 대한 자세한 내용은 [[!DNL Amazon S3] [!UICONTROL REST] API 소개](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html)를 참조하십시오.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 연결] </td> 
   <td> <p>[!DNL AWS] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL AWS] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 영역] </td> 
   <td> <p>지역 끝점을 선택합니다. 자세한 내용은 [!DNL AWS] 설명서의 <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">지역 끝점</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>호스트 URL을 입력합니다. 경로는 <code> https://s3.&lt;selected-region>.amazonaws.com/</code>에 상대적이어야 합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 메서드]</td> 
   <td> <p>API 호출을 구성하는 데 필요한 [!UICONTROL HTTP] 요청 메서드를 선택합니다. 자세한 내용은 Adobe Workfront Fusion의 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">[!UICONTROL HTTP] 요청 메서드</a>를 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 헤더]</td> 
   <td> <p>요청 헤더를 추가합니다. 추가할 각 헤더에 대해 <b>항목 추가</b>를 클릭하고 헤더를 입력하십시오. 다음과 같은 일반적인 요청 헤더를 사용할 수 있습니다. 추가 요청 헤더는 <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3] API 설명서</a>를 참조하십시오.</p> <p>Workfront Fusion은 자동으로 인증 헤더를 추가합니다.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>헤더 이름</th> 
       <th> <p> 설명</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Length]</p> </td> 
       <td> <p>RFC 2616에 따른 메시지 길이(헤더 없음). 이 헤더는 로깅 및 ACL과 같이 XML을 로드하는 작업 및 [!UICONTROL PUT]에 필요합니다.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Type]</p> </td> 
       <td> <p>요청 콘텐츠가 본문에 있는 경우 리소스의 콘텐츠 유형입니다. 예: <code>text/plain</code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>Base64는 RFC 1864에 따라 메시지의 128비트 MD5 다이제스트(헤더 없음)를 인코딩했습니다. 이 헤더를 메시지 무결성 검사로 사용하여 데이터가 원래 전송된 데이터와 동일한지 확인할 수 있습니다. 선택 사항이지만 [!UICONTROL Content-MD5] 메커니즘을 엔드 투 엔드 무결성 검사로 사용하는 것이 좋습니다. [!UICONTROL REST] 요청 인증에 대한 자세한 내용은 AWS 설명서의 <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">REST 요청 서명 및 인증</a>을 참조하십시오.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL 날짜]</p> </td> 
       <td> <p>요청자에 따른 현재 날짜 및 시간입니다. 예: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. <code>Authorization </code>헤더를 지정할 때는 <code>x-amz-date</code> 또는 <code>Date </code>헤더를 지정해야 합니다.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Expect]</p> </td> 
       <td> <p>애플리케이션이 [!UICONTROL 100-continue]를 사용하는 경우 승인을 받을 때까지 요청 본문을 전송하지 않습니다. 헤더를 기반으로 메시지가 거부되면 메시지 본문이 전송되지 않습니다. 본문을 보내는 경우에만 이 헤더를 사용할 수 있습니다.</p> <p>유효한 값: [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL 호스트]</p> </td> 
       <td> <p>경로 스타일 요청의 경우 값은 <code>s3.amazonaws.com</code>입니다. 가상 스타일 요청의 경우 값은 <code>BucketName.s3.amazonaws.com</code>입니다. 자세한 내용은 AWS 설명서에서 <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">가상 호스팅</a>을 참조하십시오.</p> <p>이 헤더는 HTTP 1.1에 필요합니다(대부분의 도구 키트에서 이 헤더를 자동으로 추가). HTTP/1.0 요청에는 선택 사항입니다.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>서명 버전 4를 사용하여 요청을 인증할 때 이 헤더는 요청 페이로드의 해시를 제공합니다. 개체를 청크로 업로드할 때 서명에서 헤더만 다루고 페이로드가 없음을 나타내려면 값을 <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code>(으)로 설정하십시오. 자세한 내용은 AWS 설명서의 <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">인증 헤더에 대한 서명 계산</a>을 참조하십시오.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-date]</p> </td> 
       <td> <p>요청자에 따른 현재 날짜 및 시간입니다. 예: <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. <code>Authorization </code>헤더를 지정할 때는 <code>x-amz-date</code> 또는 <code>Date </code>헤더를 지정해야 합니다. 둘 다 지정하면 <code>x-amz-date</code> 헤더에 지정된 값이 우선합니다.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>이 헤더는 다음 시나리오에서 사용할 수 있습니다.</p> 
        <ul> 
         <li>[!DNL Amazon DevPay] 작업에 대한 보안 토큰을 제공합니다. [!DNL Amazon DevPay]을(를) 사용하는 각 요청에는 두 개의 <code>x-amz-security-token</code> 헤더가 필요합니다. 하나는 제품 토큰에 사용되고 다른 하나는 사용자 토큰에 사용됩니다. [!DNL Amazon S3]이(가) 인증된 요청을 받으면 계산된 서명을 제공된 서명과 비교합니다. 서명을 계산하는 데 사용되는 형식이 올바르지 않은 다중 값 헤더로 인해 인증 문제가 발생할 수 있습니다.</li> 
         <li>임시 보안 자격 증명을 사용할 때 보안 토큰을 제공합니다. IAM에서 가져온 임시 보안 자격 증명을 사용하여 요청할 때 이 헤더를 사용하여 보안 토큰을 제공해야 합니다. 임시 보안 자격 증명에 대한 자세한 내용을 보려면 요청 만들기를 참조하십시오.</li> 
        </ul> <p>이 헤더는 [!DNL Amazon DevPay]을(를) 사용하는 요청과 임시 보안 자격 증명을 사용하여 서명된 요청에 필요합니다.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 쿼리 문자열]</td> 
   <td> <p>매개 변수 또는 양식 필드 등 원하는 쿼리 문자열을 추가합니다.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 본문]</td> 
   <td> <p>표준 JSON 오브젝트 형식으로 API 호출에 대한 본문 콘텐츠를 추가합니다.</p> <p>메모:   <p>JSON에서 <code>if</code>와 같은 조건문을 사용할 때는 따옴표를 조건문 외부에 배치해야 합니다.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 파일 업로드]

이 작업 모듈은 AWS S3 버킷에 파일을 업로드합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL AWS] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL AWS] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 영역] </td> 
   <td> <p>지역 끝점을 선택합니다. 자세한 내용은 [!DNL AWS] 설명서의 <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">지역 끝점</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 폴더] </p> </td> 
   <td> <p>파일을 업로드할 대상 폴더를 지정합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 소스 파일]</td> 
   <td> <p>이전 모듈에서 소스 파일을 선택하거나 소스 파일의 이름과 데이터를 매핑합니다.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers] (선택 사항)</p> </td> 
   <td> <p> 추가할 각 헤더에 대해 <b>항목 추가</b>를 클릭하고 헤더의 키와 값을 입력합니다.</p><p> 사용 가능한 머리글에 대해서는 AWS 설명서에서 <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>를 참조하십시오.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 검색 결과

* [[!UICONTROL 목록 파일]](#list-files)
* [[!UICONTROL 폴더 나열]](#list-folders)

#### [!UICONTROL 목록 파일]

지정된 위치의 파일 목록을 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL AWS] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL AWS] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 영역] </td> 
   <td> <p>지역 끝점을 선택합니다. 자세한 내용은 [!DNL AWS] 설명서의 <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">지역 끝점</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 버킷] </td> 
   <td> <p>파일을 검색할 [!DNL Amazon S3] 버킷을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 접두사]</p> </td> 
   <td> <p> 파일을 조회할 폴더의 경로를 입력합니다. 예: <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 폴더 나열]

지정된 위치의 폴더 목록을 반환합니다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 연결] </td> 
   <td> <p>[!DNL AWS] 계정을 Workfront Fusion에 연결하는 방법에 대한 자세한 내용은 이 문서의 <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Workfront Fusion에 [!DNL AWS] 연결</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 영역] </td> 
   <td> <p>지역 끝점을 선택합니다. 자세한 내용은 [!DNL AWS] 설명서의 <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">지역 끝점</a>을 참조하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 버킷] </td> 
   <td> <p>폴더를 검색할 [!DNL Amazon S3] 버킷을 선택하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (선택 사항)</p> </td> 
   <td> <p> 폴더를 조회할 폴더 경로(예: ) <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
