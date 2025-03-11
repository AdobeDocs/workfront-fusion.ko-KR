---
title: 암호화기
description: Adobe Workfront Fusion Encryptor 모듈을 사용하면 모든 텍스트 데이터를 암호화할 수 있습니다. 현재 AES256 및 PGP(OpenPGP)를 통해 메시지 암호화를 지원합니다.
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 0689cfee7cf546a6c1f5f72c79a1e7be9df85a8c
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# 암호화기

[!DNL Adobe Workfront Fusion] [!UICONTROL Encryptor] 모듈을 사용하면 모든 텍스트 데이터를 암호화할 수 있습니다. 현재 AES256 및 PGP([!UICONTROL OpenPGP])를 통해 메시지 암호화를 지원합니다.

이러한 모듈에서는 암호화 프로세스에 대해 어느 정도 숙지해야 합니다.

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
   <p>Workfront Fusion 라이센스 요구 사항이 없습니다.</p>
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

## PGP를 이용한 메시지 암호화 및 복호화

PGP를 통해 암호화 및 복호화할 때 키체인을 사용하고 개인 또는 공개 키(또는 둘 다)를 생성해야 한다.

공개 키와 개인 키에 대한 자세한 내용은 [Adobe Workfront Fusion 용어집](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md)을 참조하십시오.

키에 대한 자세한 내용은 [키](/help/workfront-fusion/references/modules/keys.md)를 참조하십시오.

## [!UICONTROL 암호기] 모듈 및 해당 필드

[!UICONTROL Encryptor] 모듈을 구성할 때 다음 필드가 표시됩니다. 모듈의 굵은 제목은 필수 필드를 나타냅니다.

### AES 암호 해독(고급)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 키]</td>
        <td>모듈에서 사용할 키를 선택합니다. 키를 만들려면 <b>추가</b>를 클릭하고 키 이름, 키 및 인코딩 형식을 입력하십시오.</td>
    </tr>
    <tr>
        <td>비트</td>
        <td>모듈에서 128비트 암호화를 사용할지 256비트 암호화를 사용할지 선택합니다.</td>
    </tr>
    <tr>
        <td>입력 인코딩</td>
        <td>사용할 입력 인코딩 유형을 선택합니다.
        <ul>
        <li>이진</li>
        <li>기본 64</li>
        <li>16진수</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>데이터</td>
        <td>해독할 데이터를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
        <td>출력 인코딩</td>
        <td>사용할 출력 인코딩 유형을 선택합니다.
        <ul>
        <li>ASCII</li>
        <li>이진</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>암호 알고리즘</td>
        <td>사용할 암호 알고리즘을 선택합니다.
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>초기화 벡터 인코딩</td>
        <td>사용할 초기화 벡터 인코딩을 선택합니다.
        <ul>
        <li>UTF-8</li>
        <li>이진</li>
        <li>기본 64</li>
        <li>헥사아데시말</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>인증 태그 인코딩</td>
        <td>사용할 인증 태그 인코딩을 선택합니다.
        <ul>
        <li>UTF-8</li>
        <li>이진</li>
        <li>기본 64</li>
        <li>헥사아데시말</li>
        </ul>
        </td>
    </tr>
</table>

### AES 암호 해독(단순)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 키]</td>
        <td>모듈에서 사용할 키를 선택합니다. 키를 만들려면 <b>추가</b>를 클릭하고 키 이름, 키 및 인코딩 형식을 입력하십시오.</td>
    </tr>
   <tr>
        <td>입력 인코딩</td>
        <td>사용할 입력 인코딩 유형을 선택합니다.
        <ul>
        <li>이진</li>
        <li>기본 64</li>
        <li>16진수</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>데이터</td>
        <td>해독할 데이터를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
        <td>출력 인코딩</td>
        <td>사용할 출력 인코딩 유형을 선택합니다.
        <ul>
        <li>ASCII</li>
        <li>이진</li>
        <li>UTF-8</li>
        </ul>
        </td>
     </tr>
    <tr>
        <td>비밀 키</td>
        <td>사용할 비밀 키를 입력하거나 매핑합니다.</td>
    </tr>
</table>

### AES 암호화(고급)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 키]</td>
        <td>모듈에서 사용할 키를 선택합니다. 키를 만들려면 <b>추가</b>를 클릭하고 키 이름, 키 및 인코딩 형식을 입력하십시오.</td>
    </tr>
    <tr>
        <td>비트</td>
        <td>모듈에서 128비트 암호화를 사용할지 256비트 암호화를 사용할지 선택합니다.</td>
    </tr>
    <tr>
        <td>입력 인코딩</td>
        <td>사용할 입력 인코딩 유형을 선택합니다.
        <ul>
        <li>이진</li>
        <li>ASCII</li>
        <li>16진수</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>데이터</td>
        <td>암호화할 데이터를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
        <td>출력 인코딩</td>
        <td>사용할 출력 인코딩 유형을 선택합니다.
        <ul>
        <li>ASCII</li>
        <li>이진</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>암호 알고리즘</td>
        <td>사용할 암호 알고리즘을 선택합니다.
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>초기화 벡터 인코딩</td>
        <td>사용할 인증 태그 인코딩을 선택합니다.
        <ul>
        <li>UTF-8</li>
        <li>이진</li>
        <li>기본 64</li>
        <li>헥사아데시말</li>
        </ul>
        </td>
    </tr>
</table>

### AES 암호화(단순)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 키]</td>
        <td>모듈에서 사용할 키를 선택합니다. 키를 만들려면 <b>추가</b>를 클릭하고 키 이름, 키 및 인코딩 형식을 입력하십시오.</td>
    </tr>
   <tr>
        <td>입력 인코딩</td>
        <td>사용할 입력 인코딩 유형을 선택합니다.
        <ul>
        <li>이진</li>
        <li>ASCII</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>데이터</td>
        <td>암호화할 데이터를 입력하거나 매핑합니다.</td>
    </tr>
    <tr>
        <td>출력 인코딩</td>
        <td>사용할 출력 인코딩 유형을 선택합니다.
        <ul>
        <li>기본 64</li>
        <li>이진</li>
        <li>16진수</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>비밀 키</td>
        <td>사용할 비밀 키를 입력하거나 매핑합니다.</td>
    </tr>
</table>


### 디지털 서명 만들기

이 모듈에서는 공개 및 개인 키를 사용하여 메시지의 암호를 해독할 수 있습니다.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 개인 키]</td>
        <td>이 서명에 사용할 개인 키를 선택하십시오. 개인 키를 추가하려면 <b>추가</b>를 클릭하고 키 이름, 키 텍스트 및 암호를 입력하십시오.</td>
    </tr>
    <tr>
        <td>알고리즘 </td>
        <td>RSA-SHA1을 사용할지 RSA-SHA256을 사용할지 선택합니다. </td>
    </tr>
   <tr>
        <td>입력 인코딩</td>
        <td>사용할 입력 인코딩 유형을 선택합니다.
        <ul>
        <li>ASCII</li>
        <li>이진</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>출력 인코딩</td>
        <td>사용할 출력 인코딩 유형을 선택합니다.
        <ul>
        <li>기본 64</li>
        <li>16진수</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>데이터</td>
        <td>서명을 생성할 데이터를 입력하거나 매핑합니다.</td>
    </tr>
</table>

### PGP 메시지 암호 해독

이 모듈에서는 공개 및 개인 키를 사용하여 메시지의 암호를 해독할 수 있습니다.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 개인 키]</td>
        <td>이 메시지에 사용할 수신자의 개인 키를 선택합니다. 개인 키를 추가하려면 <b>추가</b>를 클릭하고 키 이름, 키 텍스트 및 암호를 입력하십시오.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 공개 키]</td>
        <td>보낸 사람의 공개 키를 입력합니다. 발신자의 신원을 인증할 수 있습니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>해독할 메시지를 매핑합니다.</td>
    </tr>
</table>

### PGP 메시지 암호화

이 모듈에서는 공개 및 개인 키를 사용하여 메시지를 암호화할 수 있습니다.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 개인 키]</td>
        <td>보낸 사람의 개인 키를 입력합니다. 발신자의 신원을 인증할 수 있습니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL 공개 키]</td>
        <td>수신자의 공개 키를 입력합니다.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>암호화할 메시지를 입력합니다.</td>
    </tr>
    </table>
