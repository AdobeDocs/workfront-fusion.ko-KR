---
title: 수학 변수
description: '[!DNL Adobe Workfront Fusion mapping] 패널에서 다음 수학 변수를 사용할 수 있습니다.'
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
TQID: 'https://experienceleague.adobe.com/7vPwofVyFGdTGAXXuqbP5mmpPgSEK0JqimFqWu-UlJU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 11%
---
# 수학 변수

## pi

수학 기호 $\pi$를 나타냅니다.

## [!UICONTROL random]

[`0`,`1`] 범위의 부동 소수점 의사 난수를 반환합니다(`0` 포함, `1` 제외).

[`min`,`max`] 범위의 정수 의사 난수를 생성하려면 다음 수식을 사용하십시오(`min` 및 `max` 모두 포함).

![Random](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
