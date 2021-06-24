---
description: 預設修改時間戳。 為目錄TimeStamp和暈映TimeStamp提供預設值。 如果未指定，則伺服器將使用此catalog.ini檔案的修改日期/時間。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# TimeStamp{#timestamp}

預設修改時間戳。 提供目錄：:TimeStamp和暈映：:TimeStamp的預設值。 如果未指定，則伺服器將使用此catalog.ini檔案的修改日期/時間。

## 屬性 {#section-910e2562b41c47b78ee6216deeabbbd5}

日期/時間值（Java格式）。 可以是自1970年1月1日午夜以來的整數毫秒數(UTC/GMT)，也可以是日期/時間字串值，其格式如下：

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* 在0到23之間。

*[!DNL zzz]* 是3或4個字元的時區代碼，例如「GMT」或「PST」。日光節約時間必須計入時區代碼（例如太平洋標準時間為「PST」，太平洋日光節約時間為「PDT」）。

*[!DNL offset]* 是以小時或小時：分鐘為單位的時區時差，相對於GMT。例如，「PDT」等同於「GMT -7」。

字串格式化日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值，並改用[!DNL *[!DNL catalog]*.ini]檔案的修改時間。

## 預設 {#section-65fb29a9ea2044df8cb9fe295eb14872}

如果為空或未定義，則伺服器將使用此[!DNL *[!DNL catalog]*.ini]檔案的檔案修改時間。

## 另請參閱 {#section-764188f9b1734ad1a6270f5fecd28532}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [暈映：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [屬性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [屬性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
