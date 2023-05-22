---
description: 預設影像修改時間戳。 為目錄TimeStamp提供預設值。
solution: Experience Manager
title: 時間戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# 時間戳{#timestamp}

預設影像修改時間戳。 為目錄：:TimeStamp提供預設值。

如果未指定，伺服器將使用此的修改日期/時間 [!DNL *`catalog`*.ini] 的子菜單。

## 屬性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期/時間值。 可以是自1970年1月1日午夜以來的整數毫秒數，也可以是日期/時間字串值，其格式如下：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 在0到23之間。

*`zzz`* 是3或4個字元的時區代碼，如 `GMT` 或 `PST`。 夏令時必須在時區代碼中計算(例如， `PST` 用於太平洋標準時間，與 `PDT` （適用於太平洋夏令時）。

*`offset`* 是相對於GMT的時區偏移（小時或小時：分鐘）。 比如說， `PDT` 等於 `GMT -7`。

字串格式化日期/時間值的所有元素必須存在。 如果日期/時間值的格式不正確，則忽略該值，並修改 [!DNL *`catalog`*.ini] 檔案。

## 預設 {#section-ac465313c97943ed97d41ea852329177}

如果為空或未定義，則伺服器將使用此時間的檔案修改時間 `*`目錄`*.ini` 的子菜單。

## 另請參閱 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[目錄：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) 。 [屬性：:UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)。 [屬性：:CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
