---
description: 縮圖解析度。 指定縮圖影像的物件解析度。
solution: Experience Manager
title: 縮圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# 縮圖{#thumbres}

縮圖解析度。 指定縮圖影像的物件解析度。

僅在`catalog::ThumbType=3`時使用。

## 屬性 {#section-ee5cae086a3d4875805fa8a08756a586}

大於0的實數值。 必須有與`catalog::Resolution`相同的單位。

## 預設 {#section-f0e453fc8a7c451db21961c084eecabd}

如果欄位不存在、值為0或欄位為空，則會使用`attribute::ThumbRes`。

## 另請參閱 {#section-eb716bf647614db083020fe8ce453751}

[目錄:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ， [目錄：：Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)， [屬性：：ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501)， [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [縮圖縮放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
