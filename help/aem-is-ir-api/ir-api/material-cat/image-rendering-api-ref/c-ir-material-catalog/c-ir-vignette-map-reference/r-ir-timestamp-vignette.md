---
description: 修改時間戳記。 指定此暈映上次修改的日期／時間。
seo-description: 修改時間戳記。 指定此暈映上次修改的日期／時間。
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# TimeStamp{#timestamp}

修改時間戳記。 指定此暈映上次修改的日期／時間。

如果設定`attribute::UseLastModified`，則會在HTTP回應中傳回暈映的最近`vignette::TimeStamp`和`catalog::TimeStamp`值，以及請求中涉及的所有材料，作為上次修改的標題。

>[!NOTE]
>
>暈映檔案的實際檔案時間絕不會用於此目的。

`catalog::TimeStamp` 也用於目錄型快取驗證(請參 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`閱)。

## 屬性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

日期／時間值（Java格式）。 可以是自1970年1月1日午夜以來(UTC/GMT)的整數毫秒數，也可以是日期／時間字串值，其格式如下：

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:*[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* 在0到23的範圍內。
* *[!DNL zzz]* 是3或4個字元的時區代碼，例如「GMT」或「PST」。日光節約時間必須計入時區代碼（例如，太平洋標準時間為「PST」，太平洋日光節約時間為「PDT」）。
* *[!DNL offset]* 是以小時或小時：分鐘為單位的時區偏移，相對於GMT。例如，&#39;PDT&#39;等同於&#39;GMT -7&#39;。

字串格式化日期／時間值的所有元素都必須存在。 如果日期／時間值格式不正確，則會忽略該值，並改用[!DNL *[!DNL catalog]*.ini]檔案的修改時間。

## 預設 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` 是欄位為空或不存在。

## 另請參閱 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[屬性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)，屬 [性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
