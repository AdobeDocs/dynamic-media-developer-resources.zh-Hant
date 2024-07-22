---
description: 色彩轉換遞色。 指定在沒有icc=明確選取時，是否應使用遞色來改善色彩轉換的感應品質。
solution: Experience Manager
title: Icc遞色
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4b444f0f-2313-4477-8a22-7840b4783c88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 3%

---

# Icc遞色{#iccdither}

色彩轉換遞色。 指定在沒有icc=明確選取時，是否應使用遞色來改善色彩轉換的感應品質。

## 屬性 {#section-b7ba44d2d5de43f5a0841fe4cac29d35}

標幟。 設為0可停用遞色，或設為1可啟用遞色。

## 預設 {#section-86c4230a16454464880f64d4ab5ad533}

如果未定義或空白，則繼承自`default::IccDither`。

## 另請參閱 {#section-fe119006eb414a618b6ec9edbed8fe94}

[attribute：：IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md) &#42;，[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
