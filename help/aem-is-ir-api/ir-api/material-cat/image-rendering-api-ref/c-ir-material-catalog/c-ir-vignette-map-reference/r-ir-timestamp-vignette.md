---
title: 時間戳記
description: 修改時間戳記。 指定上次修改此暈映的日期/時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# 時間戳記{#timestamp}

修改時間戳記。 指定上次修改此暈映的日期/時間。

如果設定`attribute::UseLastModified`，則在HTTP回應中會傳回暈映以及要求中涉及的所有材質的最新`vignette::TimeStamp`和`catalog::TimeStamp`值，做為上次修改的標頭。

>[!NOTE]
>
>絕對不會將暈映檔案的實際檔案時間用於此用途。

`catalog::TimeStamp`也用於目錄型快取驗證。 請參閱[屬性：：CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)。

## 屬性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java™格式的日期/時間值。 可以是自午夜、1970年1月1日UTC/GMT以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]*&#x200B;在0到23的範圍內。
* *[!DNL zzz]*&#x200B;是三或四個字元的時區代碼，例如&#39;GMT&#39;或&#39;PST&#39;。 日光節約時間必須在時區代碼中計算（例如，太平洋標準時間是「PST」，而太平洋日光節約時間是「PDT」）。
* *[!DNL offset]*&#x200B;是相對於GMT的時區位移（以小時或小時：分鐘為單位）。 例如，「PDT」等於「GMT -7」。

字串格式日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值，並改用[!DNL *[!DNL catalog]*.ini]檔案的修改時間。

## 預設 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp`是空白或不存在的欄位。

## 另請參閱 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ， [catalog：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)， [attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
