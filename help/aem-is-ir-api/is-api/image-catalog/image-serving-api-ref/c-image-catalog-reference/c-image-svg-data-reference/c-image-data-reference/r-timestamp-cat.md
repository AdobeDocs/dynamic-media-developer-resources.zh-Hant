---
title: 時間戳記
description: 如果設定「attribute：：UseLastModified」，則「catalog：：TimeStamp」值會在HTTP回應中傳回為Last-Modified HTTP標頭。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---

# 時間戳記{#timestamp}

如果設定`attribute::UseLastModified`，則HTTP回應中會傳回`catalog::TimeStamp`值作為Last-Modified HTTP標頭。 系統會一律傳回靜態內容的Last-Modified標頭，即使未設定`attribute::UseLastModified`亦然。

對於影像和SVG內容，`catalog::TimeStamp`也用於目錄型快取驗證（請參閱[attribute：：CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md)）。

## 屬性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期/時間值。 可以是自午夜、1970 UTC/GMT年1月1日以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* GMT *`offset`*

*`hh`*&#x200B;在0到23的範圍內。

*`zzz`*&#x200B;是三或四個字元的時區代碼，例如&#39;GMT&#39;或&#39;PST&#39;。 時區代碼中的日光節約時間帳戶。 例如，「PST」代表太平洋標準時間，「PDT」代表太平洋日光節約時間)。

*`offset`*&#x200B;是以小時為單位的時區位移，或相對於GMT的`hours:minutes`。 例如，「PDT」等於「GMT -7」。

必須存在字串格式化的日期/時間值的所有元素。 如果日期/時間值的格式不正確，則會忽略該值，並改用`*`目錄`*.ini`檔案的修改時間。

## 預設 {#section-0cbf801401ff4857bdda168fd12358af}

如果欄位空白或不存在，`attribute::TimeStamp`。

## 另請參閱 {#section-c42a427aa4794c548408dc4de028d578}

[屬性：：TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)，[屬性：：UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，[屬性：：CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
