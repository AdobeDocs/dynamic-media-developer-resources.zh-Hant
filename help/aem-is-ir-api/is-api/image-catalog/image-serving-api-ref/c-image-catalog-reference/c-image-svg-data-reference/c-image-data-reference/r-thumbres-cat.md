---
description: 縮圖解析度。 指定縮圖影像的物件解析度。
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---


# ThumbRes{#thumbres}

縮圖解析度。 指定縮圖影像的物件解析度。

僅在`catalog::ThumbType=3`時使用。

## 屬性 {#section-ee5cae086a3d4875805fa8a08756a586}

實數值大於0。 必須與`catalog::Resolution`具有相同的單位。

## 預設 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` 如果欄位不存在、值為0或欄位空白，則會使用。

## 另請參閱 {#section-eb716bf647614db083020fe8ce453751}

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , catalog [::](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)Resolution [, attribute: ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) [, Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
