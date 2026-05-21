---
description: 預設縮圖解析度。 提供縮圖物件解析度的預設值，以防止特定目錄記錄未包含有效的目錄ThumbRes值。
solution: Experience Manager
title: 縮圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
TQID: 'https://experienceleague.adobe.com/xMGMMjCIDWQJbJtLzatEiSEgdD5hQOkaOhKJbMYUyB0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 3%

---

# 縮圖{#thumbres}

預設縮圖解析度。 提供縮圖物件解析度的預設值，以防止特定目錄記錄未包含有效的目錄：：ThumbRes值。

僅用於縮圖要求(`req=tmb`)及`catalog::ThumbType=3`時。

## 屬性 {#section-88d37d0e030f4879a9e584dd2cc780f3}

實數，大於0。通常以每英吋畫素表示，但也可能以其他單位表示，例如每米的畫素。

## 預設 {#section-86588899ec9b4276a98b03d7faf64003}

如果未定義或空白，則繼承自`default::ThumbRes`。

## 另請參閱 {#section-a6d2cce2e404441a996dba98a95c8e16}

[目錄：：ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
