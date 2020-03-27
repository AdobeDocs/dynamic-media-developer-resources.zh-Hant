---
description: 'null'
seo-description: 'null'
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 3148cc25-3b9a-499a-b0da-1ebe9ae99f69
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# TimeStamp{#timestamp}

如果 `attribute::UseLastModified` 已設定，則在HTTP `catalog::TimeStamp` 回應中會傳回值，作為「上次修改的HTTP」標題。 即使未設定，靜態內容一律會傳回「上次修改 `attribute::UseLastModified` 的」標題。

對於影像和SVG內容， `catalog::TimeStamp` 也會用於目錄型快取驗證(請參 ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`閱)。

## 屬性 {#section-2298a384b5cb43929542655c5a49beb2}

日期／時間值（Java格式）。 可以是自午夜、1970年1月1日UTC/GMT以來的毫秒整數，也可以是日期／時間字串值，其格式如下：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`**`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 在0 - 23範圍內。

*`zzz`* 是3或4個字元的時區代碼，例如「GMT」或「PST」。 在時區代碼中考慮夏令時。 例如，「太平洋標準時間」為「PST」，而「太平洋日光節約時間」為「PDT」)。

*`offset`* 是時區相對於GMT的時區偏 `hours:minutes`移（以小時為單位）。 例如，&#39;PDT&#39;等同於&#39;GMT -7&#39;。

字串格式化日期／時間值的所有元素都必須存在。 如果日期／時間值格式不正確，則會忽略它，並改用目錄 ` *`檔`*.ini` 的修改時間。

## 預設 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 欄位為空或不存在。

## 另請參閱 {#section-c42a427aa4794c548408dc4de028d578}

[屬性：:TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)，屬 [性：:UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，屬 [性：:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
