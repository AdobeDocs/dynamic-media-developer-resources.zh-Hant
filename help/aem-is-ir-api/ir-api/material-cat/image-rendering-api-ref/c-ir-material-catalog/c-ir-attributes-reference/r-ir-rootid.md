---
title: RootId
description: 目錄識別碼。 HTTP路徑元素，用來在HTTP要求的暈映、材質或ICC設定檔物件規範中識別此目錄。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cc34087a-8a19-4ead-b510-f2466efc44a9
TQID: 'https://experienceleague.adobe.com/Aglu-ZeC1g0LLlAwLDK5RZcgqBRyEE2NbmPodlRiJZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 4%

---

# RootId{#rootid}

目錄識別碼。 HTTP路徑元素，用來在HTTP要求的暈映、材質或ICC設定檔物件規範中識別此目錄。

## 屬性 {#section-c33266223d5b47029df756caa4e0df0c}

文字字串值。 可包含http路徑中有效的任何字元。

## 預設 {#section-e0ed902557684345850b86672b5dbe5b}

無。 每個目錄都必須有唯一的`catalog::RootId`值。 default.ini通常有空的`catalog::RootId`。

## 另請參閱 {#section-4670832574f54f9080bb485b047efd5b}

[目錄：：Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85) ， [暈映：：Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-id-vignette.md#reference-2a7ba758924b4757b3234942304db7fd)， [profile::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-name.md#reference-63b663d2052545ffab030a23e7060b1e)， [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
