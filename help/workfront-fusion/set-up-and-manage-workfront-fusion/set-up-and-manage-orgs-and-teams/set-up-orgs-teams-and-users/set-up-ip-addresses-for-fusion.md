---
title: 조직의 허용 목록에 추가하다에서 Fusion에 대한 IP 주소 구성
description: Fusion은 웹 통신에 특정 IP 주소 및 도메인을 사용합니다. 조직에서 Workfront을 사용하려면 먼저 조직의 허용 목록에 추가하다에 추가해야 합니다.
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# 조직의 허용 목록에 추가하다에서 Fusion에 대한 IP 주소 구성

Adobe Workfront Fusion은 조직의 네트워크와 통신하므로 해당 통신을 허용하도록 조직의 방화벽을 구성해야 합니다. 방화벽은 인터넷으로부터 조직의 네트워크를 분리하여 기능하는 매우 효과적인 보안 조치입니다. 선택한 데이터 및 네트워크 트래픽만 조직의 네트워크로 이동하거나 네트워크의 외부로 이동할 수 있습니다. 방화벽은 데이터를 전송하거나 수신하는 사이트를 기준으로 데이터를 허용하거나 차단합니다. Fusion 관리자는 Fusion으로 보내거나 받은 데이터가 조직 방화벽을 통과할 수 있는지 확인해야 합니다.

이는 본질적으로 방화벽을 통해 데이터를 전송하거나 수신할 수 있는 사이트의 &quot;목록&quot;인 허용 목록에 추가하다를 통해 수행됩니다. 사이트는 다음 두 가지 방법 중 하나로 식별할 수 있습니다.

* **IP 주소**: 52.31.132.175과(와) 같은 일련의 숫자
* **도메인**: URL의 일부(예: `thisdomain`의 `www.thisdomain.com`)

Fusion은 웹 통신에 특정 IP 주소 및 도메인을 사용합니다. 조직에서 Workfront을 사용하려면 먼저 조직의 허용 목록에 추가하다에 추가해야 합니다.

일반적으로 네트워크 관리자가 허용 목록을 구성합니다. 조직의 네트워크 관리자와 협력하여 방화벽에서 이러한 IP 주소를 허용하는지 확인하십시오. 네트워크 관리자가 누구인지 모르는 경우 조직의 IT 부서에서 올바른 방향을 가리킬 수 있습니다.

>[!IMPORTANT]
>
>Fusion 관리자는 이러한 IP 주소 및 도메인이 조직의 허용 목록에 추가하다에 추가되었는지 확인해야 합니다. 직접 추가하지 않더라도 마찬가지입니다. Fusion에서 조직의 허용 목록에 추가하다를 구성할 수 없습니다.

모든 Fusion IP 주소 및 도메인을 허용 목록에 추가하다에 추가하거나, 클러스터를 찾아 해당 클러스터의 IP 주소 및 도메인만 추가할 수 있습니다.

## 모든 Fusion IP 주소 및 도메인 추가

다음 IP 주소를 허용 목록에 추가합니다.

* 52.30.133.50
* 54.220.93.204
* 34.254.76.122
* 54.244.142.219
* 52.39.217.230
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28
* 20.81.156.240/28
* 172.172.84.48/28

또한 조직에서 아웃바운드 네트워크 필터링을 사용하는 경우 허용 목록에 추가하다에 다음 도메인을 추가하여 시스템이 Workfront Fusion에 액세스할 수 있도록 합니다.

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## 클러스터에 대해서만 Fusion IP 주소 및 도메인 추가

### 데이터 센터 식별

IP 주소는 데이터가 저장되는 위치에 따라 다릅니다.

URL을 통해 Fusion에 액세스하는 경우 URL을 검사하여 데이터 센터를 찾을 수 있습니다.

| URL | 데이터 센터 |
| --- | --- |
| `https://app.workfrontfusion.com` | 미국 데이터 센터 |
| `https://app-eu.workfrontfusion.com` | EU 데이터 센터 |
| `https://app-az.workfrontfusion.com` | Azure 클러스터 |

`experience.adobe.com`을(를) 통해 Fusion에 액세스하는 경우 브라우저에서 네트워크 탭을 확인하여 데이터 센터를 식별할 수 있습니다.

| URL | 데이터 센터 |
| --- | --- |
| `https://fusion.adobe.com`에 대한 호출 | 미국 데이터 센터 |
| `https://eu.fusion.adobe.com`에 대한 호출 | EU 데이터 센터 |
| `https://az.fusion.adobe.com`에 대한 호출 | Azure 클러스터 |

### 데이터 센터의 IP 주소 및 도메인 추가

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront EU 데이터 센터</td> 
   <td> 
    <ul> 
     <li>52.30.133.50</li> 
     <li>54.220.93.204</li> 
     <li>34.254.76.122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront 미국 데이터 센터</p> </td> 
   <td> 
    <ul> 
     <li>54.244.142.219</li> 
     <li>52.39.217.230</li> 
     <li>44.241.82.96</li>
     <li>100.20.126.137</li>
     <li>34.223.32.4</li>
     <li>52.39.176.220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Microsoft Azure 클러스터의 Adobe Workfront Fusion</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

또한 조직에서 아웃바운드 네트워크 필터링을 사용하는 경우 허용 목록에 추가하다에 다음 도메인을 추가하여 시스템이 Workfront Fusion에 액세스할 수 있도록 합니다. 웹후크에 사용된다.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront EU 데이터 센터</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Adobe Workfront 미국 데이터 센터</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Microsoft Azure 클러스터의 Adobe Workfront Fusion</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>아웃바운드 네트워크 필터링은 흔하지 않습니다. 네트워크 관리자에게 문의하여 허용 목록에 추가하다를 업데이트해야 하는지 확인하십시오.
