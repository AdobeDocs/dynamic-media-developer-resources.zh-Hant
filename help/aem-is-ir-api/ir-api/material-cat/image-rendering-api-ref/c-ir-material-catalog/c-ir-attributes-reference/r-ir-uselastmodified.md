---
title: UseLastModified
description: 啟用上次修改的回應標頭。 啟用或停用在影像演算發出的可快取HTTP回應中包含Last-Modified標頭。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

啟用上次修改的回應標頭。 啟用或停用在影像演算發出的可快取HTTP回應中包含Last-Modified標頭。

伺服器使用回應中涉及的所有暈映與材質目錄/目錄記錄的最新`vignette::TimeStamp`與`catalog::TimeStamp`值做為Last-Modified標頭值。

只有在使用的分散式快取網路（例如Akamai）不支援etag標題時，才應啟用。

>[!NOTE]
>
>在涉及多個影像提供/轉譯主機的負載均衡環境中使用Last-Modified標題時，務必謹慎。 如果由於某些原因，伺服器對於相同的目錄專案具有不同的時間戳記，使用者端快取可能會失敗且伺服器負載會增加。 這種情況可能會發生：

* 未定義`catalog::TimeStamp`、`vignette::TimeStamp`或`attribute::TimeStamp`，因此會使用[!DNL catalog.ini]檔案的修改時間作為`catalog::TimeStamp`的預設值。

* 每個伺服器在本機檔案系統上都有自己的目錄檔案執行個體，而不是透過網路掛載來共用素材目錄檔案。
* 相同[!DNL catalog.ini]檔案的兩個或多個執行個體有不同的檔案修改日期，可能是因為檔案複製不當所造成。

## 屬性 {#section-453952244193452caccfaf7f601007c1}

標幟。 0代表停用，1代表啟用Last-Modified HTTP標題。

## 預設 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

如果未定義或空白，則繼承自`default::UseLastModified`。

## 另請參閱 {#section-1536715169da48b0aecc4ab7326c86db}

[目錄：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ， [暈映：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
