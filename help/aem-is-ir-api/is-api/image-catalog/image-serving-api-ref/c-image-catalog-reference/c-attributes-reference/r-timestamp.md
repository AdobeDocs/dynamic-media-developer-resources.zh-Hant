---
title: 時間戳記
description: 預設影像修改時間戳記。 它提供目錄TimeStamp的預設值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---

# 時間戳記{#timestamp}

預設影像修改時間戳記。 提供catalog：：TimeStamp的預設值。

如果未指定，則伺服器會使用此專案的修改日期/時間 [!DNL *`catalog`*.ini] 檔案。

## 屬性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期/時間值。 可以是自午夜、1970年1月1日UTC/GMT以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

日期/時間值 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss zzz`*

日期/時間值 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* GMT *`offset`*

時間值 *`hh`* 介於0到23之間。

時間值 *`zzz`* 是三個或四個字元的時區代碼，例如 `GMT` 或 `PST`. 日光節約時間必須在時區代碼中計算(例如， `PST` 太平洋標準時間，與 `PDT` （適用於太平洋日光節約時間）。

時間值 *`offset`* 是相對於GMT的時區位移，單位為時數或小時：分鐘。 例如， `PDT` 相當於 `GMT -7`.

字串格式日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值，而修改時間 [!DNL *`catalog`*.ini] 會改用檔案。

## 預設 {#section-ac465313c97943ed97d41ea852329177}

如果為空白或未定義，則伺服器會使用此檔案的修改時間 `*`目錄`*.ini` 檔案。

## 另請參閱 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog：：TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ， [attribute：：UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)， [attribute：：CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
