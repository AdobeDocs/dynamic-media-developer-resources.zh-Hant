---
description: 預設影像修改時間戳記。 提供目錄TimeStamp的預設值。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 2%

---


# TimeStamp{#timestamp}

預設影像修改時間戳記。 提供目錄的預設值：:TimeStamp。

如果未指定，伺服器將使用此&#x200B;[!DNL *`catalog`*.ini]檔案的修改日期／時間。

## 屬性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期／時間值。 可以是自1970年1月1日午夜以來(UTC/GMT)的整數毫秒數，也可以是日期／時間字串值，其格式如下：

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 在0到23的範圍內。

*`zzz`* 是3或4個字元的時區代碼，例如 `GMT` 或 `PST`。日光節約時間必須計入時區代碼(例如`PST`表示太平洋標準時間，而`PDT`表示太平洋日光節約時間)。

*`offset`* 是以小時或小時：分鐘為單位的時區偏移，相對於GMT。例如，`PDT`等效於`GMT -7`。

字串格式化日期／時間值的所有元素都必須存在。 如果日期／時間值格式不正確，則會忽略它，並改用&#x200B;[!DNL *`catalog`*.ini]檔案的修改時間。

## 預設 {#section-ac465313c97943ed97d41ea852329177}

如果定義為空或未定義，則伺服器使用此`*`catalog`*.ini`檔案的檔案修改時間。

## 另請參閱 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog:::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ，屬 [性：:UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，屬 [性：:CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
