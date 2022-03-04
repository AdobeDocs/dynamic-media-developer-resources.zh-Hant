---
description: 預設修改時間戳。 為目錄TimeStamp和vignette TimeStamp提供預設值。 如果未指定，伺服器將使用此catalog.ini檔案的修改日期/時間。
solution: Experience Manager
title: 時間戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---

# 時間戳{#timestamp}

預設修改時間戳。 為目錄：:TimeStamp和vignette::TimeStamp提供預設值。 如果未指定，伺服器將使用此catalog.ini檔案的修改日期/時間。

## 屬性 {#section-910e2562b41c47b78ee6216deeabbbd5}

Java格式的日期/時間值。 可以是自1970年1月1日午夜以來的整數毫秒數，也可以是日期/時間字串值，其格式如下：

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* 在0到23之間。

*[!DNL zzz]* 是3或4個字元的時區代碼，如「GMT」或「PST」。 夏令時必須在時區代碼中入帳（例如，太平洋標準時間為「PST」，而太平洋夏令時為「PDT」）。

*[!DNL offset]* 是相對於GMT的時區偏移（小時或小時：分鐘）。 例如，「PDT」等效於「GMT -7」。

字串格式化日期/時間值的所有元素必須存在。 如果日期/時間值的格式不正確，則忽略該值，並修改[!DNL]的時間 *[!DNL catalog]*&#x200B;改用.ini]檔案。

## 預設 {#section-65fb29a9ea2044df8cb9fe295eb14872}

如果為空或未定義，則伺服器將使用此[!DNL]的檔案修改時間 *[!DNL catalog]*.ini]檔案。

## 另請參閱 {#section-764188f9b1734ad1a6270f5fecd28532}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) 。 [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)。 [屬性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)。 [屬性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
