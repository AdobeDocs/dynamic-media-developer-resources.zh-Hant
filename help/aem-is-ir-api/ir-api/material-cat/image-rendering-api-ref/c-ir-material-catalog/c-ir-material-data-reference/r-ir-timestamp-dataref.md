---
title: 時間戳記
description: 檔案修改時間戳記。 指定上次修改附加至此目錄記錄的影像和/或資料檔案的日期/時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# 時間戳記{#timestamp}

檔案修改時間戳記。 指定上次修改附加至此目錄記錄的影像和/或資料檔案的日期/時間。

如果設定`attribute::UseLastModified`，則在HTTP回應中會傳回所有材質及請求中相關暈映的`catalog::TimeStamp`與`vignette::TimeStamp`值中最近的值，做為上次修改的標頭。

>[!NOTE]
>
>絕對不會將附加至此目錄記錄的影像或資料檔案的實際檔案時間用於此目的。

`catalog::TimeStamp`也用於目錄型快取驗證（請參閱[attribute：：CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)）。

## 屬性 {#section-42f09e375e72492b87a3a486da7df808}

Java™格式的日期/時間值。 可以是自午夜、1970年1月1日UTC/GMT以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]*&#x200B;在0到23的範圍內。
* *[!DNL zzz]*&#x200B;是三或四個字元的時區代碼，例如&#39;GMT&#39;或&#39;PST&#39;。 日光節約時間必須在時區代碼中計算。 例如，「PST」代表太平洋標準時間，「PDT」代表太平洋日光節約時間。
* *[!DNL offset]*&#x200B;是相對於GMT的時區位移（以小時或小時：分鐘為單位）。 例如，「PDT」等於「GMT -7」。

字串格式日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值，並改用&#x200B;*catalog*.ini檔案的修改時間。

## 預設 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp`是空白或不存在的欄位。

## 另請參閱 {#section-876f1d1b50dc4501b605820015a29451}

[attribute：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ， [attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)， [attribute：：CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)， [vignette：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
