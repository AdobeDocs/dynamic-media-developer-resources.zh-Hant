---
description: 相對影像URL的根URL。 指定相對影像URL的根URL。 當src=值由{大括弧}括住時，會使用attribute RootUrl而非屬性RootPath。
seo-description: 相對影像URL的根URL。 指定相對影像URL的根URL。 當src=值由{大括弧}括住時，會使用attribute RootUrl而非屬性RootPath。
seo-title: RootUrl *
solution: Experience Manager
title: RootUrl *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aa10f210-4765-4b0e-9ce1-812b00cd8cf5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# RootUrl *{#rooturl}

相對影像URL的根URL。 指定相對影像URL的根URL。 attribute::RootUrl，而非attribute::RootPath，當src=值由{大括弧}括住時。

## 屬性 {#section-69cd0f71ea614770a8778c745d23197a}

文字字串值。 絕對URL根路徑，包括前導通訊協定識別碼。 支援下列通訊協定：HTTP、HTTPS和FTP。

## 預設 {#section-7a81569728474725a70f3a2cc4d48e85}

如果未定義，則繼承自`default::RootUrl`。 如果已定義但為空，則此材料目錄不支援相對URL。

## 另請參閱 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`，屬 [性：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
