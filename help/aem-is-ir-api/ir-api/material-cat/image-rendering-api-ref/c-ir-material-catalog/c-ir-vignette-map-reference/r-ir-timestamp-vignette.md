---
description: 修改時間戳。 指定上次修改此暈映的日期/時間。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---

# TimeStamp{#timestamp}

修改時間戳。 指定上次修改此暈映的日期/時間。

如果設定了`attribute::UseLastModified`，則暈映的最近`vignette::TimeStamp`和`catalog::TimeStamp`值以及請求中涉及的所有材料將在HTTP響應中作為上次修改的標題返回。

>[!NOTE]
>
>此目的不會使用暈映檔案的實際檔案時間。

`catalog::TimeStamp` 也用於目錄型快取驗證(請參閱 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`)。

## 屬性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

日期/時間值（Java格式）。 可以是自1970年1月1日午夜以來的整數毫秒數(UTC/GMT)，也可以是日期/時間字串值，其格式如下：

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:*[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* 在0到23之間。
* *[!DNL zzz]* 是3或4個字元的時區代碼，例如「GMT」或「PST」。日光節約時間必須計入時區代碼（例如太平洋標準時間為「PST」，太平洋日光節約時間為「PDT」）。
* *[!DNL offset]* 是以小時或小時：分鐘為單位的時區時差，相對於GMT。例如，「PDT」等同於「GMT -7」。

字串格式化日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值，並改用[!DNL *[!DNL catalog]*.ini]檔案的修改時間。

## 預設 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` 欄位為空或不存在。

## 另請參閱 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[屬性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) [，屬性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
