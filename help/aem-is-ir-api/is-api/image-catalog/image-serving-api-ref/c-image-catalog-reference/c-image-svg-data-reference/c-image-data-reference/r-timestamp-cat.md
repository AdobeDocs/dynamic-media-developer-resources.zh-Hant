---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# TimeStamp{#timestamp}

如果設定了`attribute::UseLastModified`，則在HTTP響應中將`catalog::TimeStamp`值作為上次修改的HTTP標頭返回。 即使未設定`attribute::UseLastModified`，仍一律會為靜態內容傳回上次修改的標題。

對於影像和SVG內容，`catalog::TimeStamp`還用於基於目錄的快取驗證（請參閱` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`）。

## 屬性 {#section-2298a384b5cb43929542655c5a49beb2}

日期/時間值（Java格式）。 可以是自1970年1月1日午夜以來的整數毫秒數(UTC/GMT)，也可以是日期/時間字串值，其格式如下：

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 在0 - 23範圍內。

*`zzz`* 是三個或四個字元的時區代碼，例如「GMT」或「PST」。在時區代碼中說明日光節約時間。 例如，太平洋標準時間為「PST」，太平洋日光節約時間為「PDT」)。

*`offset`* 是時區時差（以小時為單位），或 `hours:minutes`相對於GMT時差。例如，「PDT」等同於「GMT -7」。

字串格式化日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值，而會改用`*`catalog`*.ini`檔案的修改時間。

## 預設 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 如果欄位為空或不存在。

## 另請參閱 {#section-c42a427aa4794c548408dc4de028d578}

[屬性：:TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)，屬 [性：:UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，屬 [性：:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
