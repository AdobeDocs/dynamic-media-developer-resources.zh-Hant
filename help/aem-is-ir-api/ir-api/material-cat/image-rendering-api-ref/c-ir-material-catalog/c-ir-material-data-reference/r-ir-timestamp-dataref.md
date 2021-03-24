---
description: 檔案修改時間戳記。 指定附加到此目錄記錄的映像和／或資料檔案上次修改的日期／時間。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# TimeStamp{#timestamp}

檔案修改時間戳記。 指定附加到此目錄記錄的映像和／或資料檔案上次修改的日期／時間。

如果設定`attribute::UseLastModified`，則所有材料的`catalog::TimeStamp`和`vignette::TimeStamp`值的最新值以及請求中涉及的暈映會在HTTP回應中傳回為上次修改的標頭。

>[!NOTE]
>
>此目的絕不會使用附加至此目錄記錄的影像或資料檔案的實際檔案時間。

`catalog::TimeStamp` 也用於目錄型快取驗證(請參 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`閱)。

## 屬性 {#section-42f09e375e72492b87a3a486da7df808}

日期／時間值（Java格式）。 可以是自1970年1月1日午夜以來(UTC/GMT)的整數毫秒數，也可以是日期／時間字串值，其格式如下：

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* 在0到23的範圍內。
* *[!DNL zzz]* 是3或4個字元的時區代碼，例如「GMT」或「PST」。日光節約時間必須計入時區代碼（例如，太平洋標準時間為「PST」，太平洋日光節約時間為「PDT」）。
* *[!DNL offset]* 是以小時或小時：分鐘為單位的時區偏移，相對於GMT。例如，&#39;PDT&#39;等同於&#39;GMT -7&#39;。

字串格式化日期／時間值的所有元素都必須存在。 如果日期／時間值格式不正確，則會忽略它，並改用&#x200B;*catalog*.ini檔案的修改時間。

## 預設 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` 是欄位為空或不存在。

## 另請參閱 {#section-876f1d1b50dc4501b605820015a29451}

[屬性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ，屬 [性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)，屬性：:CacheValidationPolicy [,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4) [暈映：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
