---
title: HTTP 요청 메서드
description: 모듈에서 API 호출을 구성할 때는 HTTP 요청 메서드를 선택해야 합니다. 이 문서에서는 사용 가능한 방법 및 각 방법을 선택하는 이유를 설명합니다.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# HTTP 요청 메서드

모듈에서 API 호출을 구성할 때는 HTTP 요청 메서드를 선택해야 합니다. 이 문서에서는 사용 가능한 방법 및 각 방법을 선택하는 이유를 설명합니다.

## HTTP 메서드

다음 HTTP 메서드 중 하나를 사용합니다.

* **[!UICONTROL GET]**: 매개 변수를 기반으로 웹 서버에서 데이터를 검색합니다. [!UICONTROL GET]이(가) 지정된 리소스의 표현을 요청하고 성공하면 요청된 콘텐츠와 함께 [!UICONTROL 200 OK] 응답 메시지를 받습니다.
* **[!UICONTROL POST]**: 매개 변수를 기반으로 웹 서버에 데이터를 보냅니다. [!UICONTROL POST]개의 요청에 파일 업로드와 같은 작업이 포함되어 있습니다. 여러 [!UICONTROL POST]을(를) 사용하면 단일 [!UICONTROL POST]과(와) 다른 결과가 발생할 수 있으므로 실수로 여러 [!UICONTROL POST]을(를) 보내는 것에 주의하십시오. [!UICONTROL POST]이(가) 성공하면 [!UICONTROL 200 OK] 응답 메시지를 받습니다.
* **[!UICONTROL PUT]**: 매개 변수를 기반으로 웹 서버의 위치로 데이터를 보냅니다. [!UICONTROL PUT]개의 요청에 파일 업로드와 같은 작업이 포함되어 있습니다. [!UICONTROL PUT]과(와) [!UICONTROL POST]의 차이점은 PUT이 멱등 행렬이라는 것입니다. 즉, 하나의 성공한 [!UICONTROL PUT]의 결과가 동일한 [!UICONTROL PUT]의 수와 동일합니다. PUT이 성공하면 200개의 응답 메시지(일반적으로 201 또는 204)를 받습니다.
* **[!UICONTROL PATCH]**: (일부 API 호출 모듈에는 사용할 수 없음) 매개 변수를 기반으로 웹 서버의 리소스에 부분 수정 사항을 적용합니다. [!UICONTROL PATCH]은(는) idempotent가 아닙니다. 즉, 여러 [!UICONTROL PATCH]의 결과가 의도하지 않은 결과를 초래할 수 있습니다. [!UICONTROL PATCH]이(가) 성공하면 200개의 응답 메시지(일반적으로 204개)를 받게 됩니다.
* **[!UICONTROL DELETE]**: 매개 변수를 기반으로 웹 서버에서 지정된 리소스를 삭제합니다(리소스가 있는 경우). [!UICONTROL DELETE]이(가) 성공하면 200 OK 응답 메시지가 표시됩니다.
