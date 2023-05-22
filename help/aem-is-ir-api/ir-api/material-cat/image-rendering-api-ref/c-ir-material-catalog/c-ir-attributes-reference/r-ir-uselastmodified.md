---
title: 使用上次修改時間
description: 啟用上次修改的響應標頭。 啟用或禁用在影像呈現所發出的可快取HTTP響應中包含上次修改的標頭。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# 使用上次修改時間{#uselastmodified}

啟用上次修改的響應標頭。 啟用或禁用在影像呈現所發出的可快取HTTP響應中包含上次修改的標頭。

伺服器使用最新 `vignette::TimeStamp` 和 `catalog::TimeStamp` 響應中涉及的所有vignette和material目錄/目錄記錄的值，作為「上次修改的」標題值。

僅當使用不支援etag頭的分佈式快取網路（如Akamai）時才應啟用。

>[!NOTE]
>
>在涉及多個影像服務/呈現主機的負載平衡環境中使用上次修改的標頭時，必須小心。 如果由於某種原因，伺服器對同一目錄項具有不同的時間戳，則客戶端快取可能會失敗，伺服器負載會增加。 這種情況可能發生如下：

* `catalog::TimeStamp`。 `vignette::TimeStamp`或 `attribute::TimeStamp` 未定義，因此修改時間 [!DNL catalog.ini] 檔案用作 `catalog::TimeStamp`。

* 每個伺服器不是通過網路裝載來共用材料目錄檔案，而是在本地檔案系統上具有其自己的目錄檔案實例。
* 兩個或多個相同實例 [!DNL catalog.ini] 檔案的檔案修改日期不同，可能是由於檔案複製不當所致。

## 屬性 {#section-453952244193452caccfaf7f601007c1}

標幟. 0禁用，1啟用上次修改的HTTP標頭。

## 預設 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

繼承自 `default::UseLastModified` 或為空。

## 另請參閱 {#section-1536715169da48b0aecc4ab7326c86db}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) 。 [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
