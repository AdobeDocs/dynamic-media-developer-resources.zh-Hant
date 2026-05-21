---
title: RootUrl
description: 相對影像URL的根URL。 指定相對影像URL的根URL。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
TQID: 'https://experienceleague.adobe.com/1wKgvbd1t4HyDlz-CTDkp2gQuryBJYfMyDG7SmVgNwE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# RootUrl{#rooturl}

相對影像URL的根URL。 指定相對影像URL的根URL。 當`src=`值由{curly braces}括住時，會使用`attribute::RootUrl`而非`attribute::RootPath`。

## 屬性 {#section-69cd0f71ea614770a8778c745d23197a}

文字字串值。 絕對URL根路徑，包括前導通訊協定識別碼。 支援下列通訊協定：HTTP、HTTPS和FTP。

## 預設 {#section-7a81569728474725a70f3a2cc4d48e85}

如果未定義，則繼承自`default::RootUrl`。 如果已定義但空白，此材質目錄不支援相對URL。

## 另請參閱 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ， `mask=`， [屬性:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
