---
description: 修改時間戳。 指定上次修改此視圖的日期/時間。
solution: Experience Manager
title: 時間戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 時間戳{#timestamp}

修改時間戳。 指定上次修改此視圖的日期/時間。

如果 `attribute::UseLastModified` 已設定，最近 `vignette::TimeStamp` 和 `catalog::TimeStamp`vignette的值和請求中涉及的所有材料在HTTP響應中作為上次修改的標頭返回。

>[!NOTE]
>
>vignette檔案的實際檔案時間從未用於此目的。

`catalog::TimeStamp` 也用於基於目錄的快取驗證(請參見 [屬性：:CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)。

## 屬性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java格式的日期/時間值。 可以是自1970年1月1日午夜以來的整數毫秒數，也可以是日期/時間字串值，其格式如下：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:*[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* 在0到23之間。
* *[!DNL zzz]* 是3或4個字元的時區代碼，如「GMT」或「PST」。 夏令時必須在時區代碼中入帳（例如，太平洋標準時間為「PST」，而太平洋夏令時為「PDT」）。
* *[!DNL offset]* 是相對於GMT的時區偏移（小時或小時：分鐘）。 例如，「PDT」等效於「GMT -7」。

字串格式化日期/時間值的所有元素必須存在。 如果日期/時間值的格式不正確，則忽略該值，並修改[!DNL]的時間 *[!DNL catalog]*&#x200B;改用.ini]檔案。

## 預設 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` 欄位為空或不存在。

## 另請參閱 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[屬性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) 。 [目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)。 [屬性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
