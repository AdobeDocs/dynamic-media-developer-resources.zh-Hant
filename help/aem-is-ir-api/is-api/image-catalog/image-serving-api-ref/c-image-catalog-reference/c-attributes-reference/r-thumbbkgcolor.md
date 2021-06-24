---
description: 縮圖的預設背景顏色。 RGB值，用於填充輸出縮略圖影像的區域，該影像不包含實際影像資料。
solution: Experience Manager
title: ThumbBkgColor
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 88acf5ad-2973-42f9-9aaa-901e66b07f53
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# ThumbBkgColor{#thumbbkgcolor}

縮圖的預設背景顏色。 RGB值，用於填充輸出縮略圖影像的區域，該影像不包含實際影像資料。

僅用於縮圖請求(`req=tmb`)，以及當`catalog::ThumbType`設為2或3時。

## 屬性 {#section-a73e82c950cc4319bc3bccec14764c25}

色彩.

## 預設 {#section-b02bb56dda684ff9969806ce82ba00c2}

如果未定義或為空，則從`default::ThumbBkgColor`繼承。

## 另請參閱 {#section-27983dc885424dfbba8c8e4192f3f88d}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [req=tmb](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
