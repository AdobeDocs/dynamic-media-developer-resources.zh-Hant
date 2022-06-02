---
description: 檔案修改時間戳。 指定上次修改附加到此目錄記錄的映像和/或資料檔案的日期/時間。
solution: Experience Manager
title: 時間戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 時間戳{#timestamp}

檔案修改時間戳。 指定上次修改附加到此目錄記錄的映像和/或資料檔案的日期/時間。

如果 `attribute::UseLastModified` 是設定， `catalog::TimeStamp` 和 `vignette::TimeStamp` 在HTTP響應中，將請求中涉及的所有材料和vignette的值作為上次修改的標頭返回。

>[!NOTE]
>
>附加到此目錄記錄的影像或資料檔案的實際檔案時間永遠不會用於此目的。

`catalog::TimeStamp` 也用於基於目錄的快取驗證(請參見 [屬性：:CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md))。

## 屬性 {#section-42f09e375e72492b87a3a486da7df808}

Java格式的日期/時間值。 可以是自1970年1月1日午夜以來的整數毫秒數，也可以是日期/時間字串值，其格式如下：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* 在0到23之間。
* *[!DNL zzz]* 是3或4個字元的時區代碼，如「GMT」或「PST」。 夏令時必須在時區代碼中入帳（例如，太平洋標準時間為「PST」，而太平洋夏令時為「PDT」）。
* *[!DNL offset]* 是相對於GMT的時區偏移（小時或小時：分鐘）。 例如，「PDT」等效於「GMT -7」。

字串格式化日期/時間值的所有元素必須存在。 如果日期/時間值的格式不正確，則忽略該值，並修改 *目錄*&#x200B;改用.ini檔案。

## 預設 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` 欄位為空或不存在。

## 另請參閱 {#section-876f1d1b50dc4501b605820015a29451}

[屬性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) 。 [屬性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)。 [屬性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)。 [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
