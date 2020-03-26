---
description: 靜態內容目錄資料檔案路徑。 指定包含此目錄靜態內容資料的檔案。
seo-description: 靜態內容目錄資料檔案路徑。 指定包含此目錄靜態內容資料的檔案。
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

靜態內容目錄資料檔案路徑。 指定包含此目錄靜態內容資料的檔案。

靜態內容目錄資料檔案按指定順序載入。 如果相同 `static::Id` 的值出現在多個記錄（位於相同或不同的目錄檔案）中，則最後一個例項優先。

## 屬性 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

一或多個文字字串值，以逗號分隔。 選填。每個值都必須是相對於目錄資料夾的絕對檔案路徑或路徑。

## 預設 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空白，表示此影像目錄不包含任何靜態內容資料。

## 另請參閱 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
