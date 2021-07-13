---
description: 縮圖影像。 請求使用目錄縮圖條件格式化和調整大小的影像資料。
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

縮圖影像。 請求使用目錄縮圖條件格式化和調整大小的影像資料。

`req=tmb`

回覆資料格式和回應MIME類型由`fmt=`決定。 支援除`fit=`之外的所有命令。

請參閱[縮圖縮放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)。

您可以根據`catalog::Expiration`透過TTL快取HTTP回應。
