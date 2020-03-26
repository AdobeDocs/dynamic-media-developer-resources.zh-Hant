---
description: 啟用上次修改的回應標題。 啟用或停用「影像演算」所發出可快取HTTP回應中包含「上次修改」標題。
seo-description: 啟用上次修改的回應標題。 啟用或停用「影像演算」所發出可快取HTTP回應中包含「上次修改」標題。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

啟用上次修改的回應標題。 啟用或停用「影像演算」所發出可快取HTTP回應中包含「上次修改」標題。

伺服器會使用回應中 `vignette::TimeStamp` 所有暈映和 `catalog::TimeStamp` 材質目錄／目錄記錄的最新和值，做為「上次修改」標題值。

只有當使用不支援etag標題的分散式快取網路（例如Akamai）時，才應啟用。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>在包含多部影像伺服／轉換主機的負載平衡環境中使用「上次修改」標題時，請務必小心。 如果由於某些原因，伺服器對同一目錄條目具有不同的時間戳記，則可能會打敗客戶端快取並增加伺服器負載。 這種情況可能發生如下：

* 既 `catalog::TimeStamp`未定義 `vignette::TimeStamp`、 `attribute::TimeStamp` 也未定義，因此檔案的修改時間 [!DNL catalog.ini] 將用作預設值 `catalog::TimeStamp`。

* 每台伺服器在本地檔案系統上都有自己的目錄檔案實例，而不是通過網路裝載共用物料目錄檔案。
* 同一檔案的兩個或多個實例具 [!DNL catalog.ini] 有不同的檔案修改日期，這可能是由於不正確複製檔案所致。

## 屬性 {#section-453952244193452caccfaf7f601007c1}

標幟. 若要停用，請使用1啟用「上次修改的HTTP」標題。

## 預設 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

繼承自 `default::UseLastModified` （如果未定義或為空）。

## 另請參閱 {#section-1536715169da48b0aecc4ab7326c86db}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [暈映：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
