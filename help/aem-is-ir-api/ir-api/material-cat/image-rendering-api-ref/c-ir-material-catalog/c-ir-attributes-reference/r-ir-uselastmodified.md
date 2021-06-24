---
description: 啟用上次修改的回應標題。 啟用或停用將上次修改的標題包含在影像呈現所發出的可快取HTTP回應中。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---

# UseLastModified{#uselastmodified}

啟用上次修改的回應標題。 啟用或停用將上次修改的標題包含在影像呈現所發出的可快取HTTP回應中。

伺服器將響應中涉及的所有暈映和物料目錄/目錄記錄的最新`vignette::TimeStamp`和`catalog::TimeStamp`值用作上次修改的標題值。

只有在使用不支援etag標頭的分佈式快取網路（例如Akamai）時，才應啟用。

>[!NOTE]
>
>在涉及多個影像提供/轉譯主機的負載平衡環境中使用上次修改的標題時，請務必小心。 如果伺服器對相同目錄項目有不同的時間戳記，則可能會失敗用戶端快取並增加伺服器負載。 這種情況可能發生如下：

* 未定義`catalog::TimeStamp`、`vignette::TimeStamp`和`attribute::TimeStamp`，因此[!DNL catalog.ini]檔案的修改時間用作`catalog::TimeStamp`的預設時間。

* 每個伺服器在本地檔案系統上具有其自己的目錄檔案實例，而不是通過網路裝載共用資料目錄檔案。
* 同一[!DNL catalog.ini]檔案的兩個或多個實例具有不同的檔案修改日期，這可能是由於檔案的複製不當所致。

## 屬性 {#section-453952244193452caccfaf7f601007c1}

標幟. 若要停用，請使用1啟用上次修改的HTTP標題。

## 預設 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

如果未定義或為空，則從`default::UseLastModified`繼承。

## 另請參閱 {#section-1536715169da48b0aecc4ab7326c86db}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [暈映：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
