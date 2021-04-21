---
description: 啟用上次修改的回應標題。 啟用或停用「影像演算」所發出可快取HTTP回應中包含「上次修改」標題。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# UseLastModified{#uselastmodified}

啟用上次修改的回應標題。 啟用或停用「影像演算」所發出可快取HTTP回應中包含「上次修改」標題。

伺服器將響應中涉及的所有暈映和物料目錄／目錄記錄的最新`vignette::TimeStamp`和`catalog::TimeStamp`值用作「上次修改」標題值。

只有當使用不支援etag標題的分散式快取網路（例如Akamai）時，才應啟用。

>[!NOTE]
>
>在包含多部影像伺服／轉換主機的負載平衡環境中使用「上次修改」標題時，請務必小心。 如果由於某些原因，伺服器對同一目錄條目具有不同的時間戳記，則可能會打敗客戶端快取並增加伺服器負載。 這種情況可能發生如下：

* `catalog::TimeStamp`、`vignette::TimeStamp`和`attribute::TimeStamp`都未定義，因此[!DNL catalog.ini]檔案的修改時間用作`catalog::TimeStamp`的預設時間。

* 每台伺服器在本地檔案系統上都有自己的目錄檔案實例，而不是通過網路裝載共用物料目錄檔案。
* 相同[!DNL catalog.ini]檔案的兩個或兩個以上執行個體的檔案修改日期不同，可能是因為不當複製檔案所致。

## 屬性 {#section-453952244193452caccfaf7f601007c1}

標幟. 若要停用，請使用1啟用「上次修改的HTTP」標題。

## 預設 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

如果未定義或為空，則繼承自`default::UseLastModified`。

## 另請參閱 {#section-1536715169da48b0aecc4ab7326c86db}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ，暈 [映：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
