---
description: 預設縮圖解析度。 提供縮圖物件解析度的預設值，以防特定目錄記錄不包含有效的目錄ThumbRes值。
seo-description: 預設縮圖解析度。 提供縮圖物件解析度的預設值，以防特定目錄記錄不包含有效的目錄ThumbRes值。
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4a77d673-9d2e-4e62-a014-c99fa3df294a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# ThumbRes{#thumbres}

預設縮圖解析度。 提供縮圖物件解析度的預設值，以防特定目錄記錄不包含有效的目錄：:ThumbRes值。

僅用於縮圖請求(`req=tmb`)和`catalog::ThumbType=3`時。

## 屬性 {#section-88d37d0e030f4879a9e584dd2cc780f3}

實數，大於0。通常以每英吋像素表示，但也可以以其他單位表示，例如每米像素。

## 預設 {#section-86588899ec9b4276a98b03d7faf64003}

如果未定義或為空，則繼承自`default::ThumbRes`。

## 另請參閱 {#section-a6d2cce2e404441a996dba98a95c8e16}

[目錄：:ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
