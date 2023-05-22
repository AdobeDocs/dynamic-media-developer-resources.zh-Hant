---
description: 時間戳
solution: Experience Manager
title: 時間戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# 時間戳{#timestamp}

如果 `attribute::UseLastModified` 設定， `catalog::TimeStamp` 值在HTTP響應中作為上次修改的HTTP標頭返回。 對於靜態內容，始終返回上次修改的標頭，即使 `attribute::UseLastModified` 未設定。

對於影像和SVG內容， `catalog::TimeStamp` 也用於基於目錄的快取驗證(請參見 [屬性：:CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md)。

## 屬性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期/時間值。 可以是自1970年1月1日午夜以來的整數毫秒數，也可以是日期/時間字串值，其格式如下：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 在0 - 23範圍內。

*`zzz`* 是3或4個字元的時區代碼，如「GMT」或「PST」。 時區代碼中夏令時帳戶。 例如，「太平洋標準時間」為「PST」，「太平洋夏令時」為「PDT」)。

*`offset`* 是時區偏移(以小時或 `hours:minutes`，相對於GMT。 例如，「PDT」等效於「GMT -7」。

字串格式化日期/時間值的所有元素必須存在。 如果日期/時間值的格式不正確，則忽略該值，並修改 `*`目錄`*.ini` 檔案。

## 預設 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 欄位為空或不存在。

## 另請參閱 {#section-c42a427aa4794c548408dc4de028d578}

[屬性：:TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)。 [屬性：:UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)。 [屬性：:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
