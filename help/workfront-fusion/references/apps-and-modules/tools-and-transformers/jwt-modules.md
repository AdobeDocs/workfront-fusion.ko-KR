---
title: JWT 모듈
description: Adobe Workfront Fusion [!UICONTROL JWT] 앱은 제공된 알고리즘을 기반으로 JWT 토큰을 생성하는 모듈을 제공합니다.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# [!UICONTROL JWT] 모듈

Adobe Workfront Fusion [!UICONTROL JWT] 앱은 제공된 알고리즘을 기반으로 JWT 토큰을 생성하는 모듈을 제공합니다.

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
   <p>Workfront Fusion 라이센스 요구 사항 없음</p>
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

## JWT API 정보

JWT 커넥터는 다음을 사용합니다.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">API 태그</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## JWT 모듈 및 해당 필드

### JWT 생성

이 모듈은 선택한 알고리즘을 기반으로 JWT를 생성합니다.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 알고리즘]</td> 
   <td> <p>JWT를 생성할 알고리즘을 선택합니다.</p> <ul>
   <li><b>HS256</b>: SHA-256 해시 알고리즘을 사용하는 HMAC</li>
   <li><b>HS384</b>: SHA-384 해시 알고리즘을 사용하는 HMAC</li>
   <li><b>HS512</b>: SHA-512 해시 알고리즘을 사용하는 HMAC</li>
   <li><b>RS256</b>: SHA-256 해시 알고리즘을 사용하는 RSASSA-PKCS1-v1_5</li>
   <li><b>RS384</b>: SHA-384 해시 알고리즘을 사용하는 RSASSA-PKCS1-v1_5</li>
   <li><b>RS512</b>: SHA-512 해시 알고리즘을 사용하는 RSASSA-PKCS1-v1_5</li>
   <li><b>PS256</b>: SHA-256 해시 알고리즘을 사용하는 RSASSA-PSS(노드 ^6.12.0 또는 &gt;=8.0.0만)</li>
   <li><b>PS384</b>: SHA-384 해시 알고리즘을 사용하는 RSASSA-PSS(노드 ^6.12.0 또는 &gt;=8.0.0만)</li>
   <li><b>PS512</b>: SHA-512 해시 알고리즘을 사용하는 RSASSA-PSS(노드 ^6.12.0 또는 &gt;=8.0.0만)</li>
   <li><b>ES256</b>: P-256 곡선 및 SHA-256 해시 알고리즘을 사용하는 ECDSA</li>
   <li><b>ES384</b>: P-384 곡선 및 SHA-384 해시 알고리즘을 사용하는 ECDSA</li>
   <li><b>ES512</b>: P-521 곡선 및 SHA-512 해시 알고리즘을 사용하는 ECDSA</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>추가할 각 페이로드 항목에 대해 <b>항목 추가</b>를 클릭하고 항목의 키와 값을 입력하십시오.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Options] </td> 
   <td> <p>추가할 각 옵션 항목에 대해 <b>항목 추가</b>를 클릭하고 항목의 키와 값을 입력하십시오.</p> <p>다음 키를 사용할 수 있습니다.
   <ul>
   <li><b>알고리즘</b>: (기본값: RS256)</li>
   <li><b>expiresIn</b>: 초 단위 또는 시간 범위(예: 2일, 10h, 7d)를 설명하는 문자열로 표시됩니다. 숫자 값은 초 수로 해석됩니다. 문자열을 사용하는 경우 시간 단위(일, 시간 등)를 제공해야 합니다. 그렇지 않으면 밀리초 단위가 기본적으로 사용됩니다(120은 120밀리초와 같음).</li>
   <li><b>notBefore</b>: 초 단위 또는 시간 범위(예: 2일, 10h, 7d)를 설명하는 문자열로 표시됩니다. 숫자 값은 초 수로 해석됩니다. 문자열을 사용하는 경우 시간 단위(일, 시간 등)를 제공해야 합니다. 그렇지 않으면 밀리초 단위가 기본적으로 사용됩니다(120은 120밀리초와 같음).
</li>
   <li><b>대상자</b></li>
   <li><b>발급자</b></li>
   <li><b>jwtid</b></li>
   <li><b>제목</b></li>
   <li><b>no타임스탬프</b></li>
   <li><b>머리글</b></li>
   <li><b>keyid</b></li>
   <li><b>mutatePayload</b>: <code>true</code>이면 서명 함수에서 페이로드 개체를 직접 수정합니다. 이 기능은 호출이 적용된 후 토큰으로 인코딩되기 전에 페이로드에 대한 원시 참조가 필요한 경우 유용합니다.</li>
   <li><b>allowInsecureKeySizes</b>: <code>true</code>인 경우 RSA에 2048 미만의 모듈러스를 사용하는 개인 키를 사용할 수 있습니다.</li>
   <li><b>allowInvalidAsymmetricKeyTypes</b>: <code>true</code>인 경우 지정된 알고리즘과 일치하지 않는 비대칭 키를 허용합니다. 이 옵션은 이전 버전과의 호환성을 위한 것이므로 피해야 합니다.</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>
