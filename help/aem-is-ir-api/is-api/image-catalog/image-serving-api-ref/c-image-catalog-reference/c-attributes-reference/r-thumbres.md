---
description: 預設縮圖解析度。 提供縮圖對象解析的預設值，以備特定目錄記錄不包含有效的目錄ThumbRes值時使用。
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# ThumbRes{#thumbres}

預設縮圖解析度。 提供縮圖對象解析的預設值，以防特定目錄記錄不包含有效目錄：:ThumbRes值。

僅用於縮圖請求(`req=tmb`)和`catalog::ThumbType=3`時。

## 屬性 {#section-88d37d0e030f4879a9e584dd2cc780f3}

實數，大於0。通常以每英吋像素表示，但也可以以其他單位表示，如每米像素。

## 預設 {#section-86588899ec9b4276a98b03d7faf64003}

如果未定義或為空，則從`default::ThumbRes`繼承。

## 另請參閱 {#section-a6d2cce2e404441a996dba98a95c8e16}

[目錄：:ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
