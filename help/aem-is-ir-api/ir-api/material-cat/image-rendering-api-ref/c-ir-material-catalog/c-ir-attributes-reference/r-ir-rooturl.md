---
title: RootUrl
description: 相對影像URL的根URL。 指定相對影像URL的根URL。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# RootUrl{#rooturl}

相對影像URL的根URL。 指定相對影像URL的根URL。 當`attribute::RootUrl`值由`attribute::RootPath`括住時，會使用`src=`而非{curly braces}。

## 屬性 {#section-69cd0f71ea614770a8778c745d23197a}

文字字串值。 絕對URL根路徑，包括前導通訊協定識別碼。 支援下列通訊協定：HTTP、HTTPS和FTP。

## 預設 {#section-7a81569728474725a70f3a2cc4d48e85}

如果未定義，則繼承自`default::RootUrl`。 如果已定義但空白，此材質目錄不支援相對URL。

## 另請參閱 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ， `mask=`， [屬性:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
