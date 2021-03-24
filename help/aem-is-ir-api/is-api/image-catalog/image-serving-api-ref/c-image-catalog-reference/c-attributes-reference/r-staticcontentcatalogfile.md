---
description: 靜態內容目錄資料檔案路徑。 指定包含此目錄靜態內容資料的檔案。
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

靜態內容目錄資料檔案路徑。 指定包含此目錄靜態內容資料的檔案。

靜態內容目錄資料檔案按指定順序載入。 如果相同的`static::Id`值出現在多個記錄中（位於相同或不同的目錄檔案中），則最後一個例項優先。

## 屬性 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

一或多個文字字串值，以逗號分隔。 選填。每個值都必須是相對於目錄資料夾的絕對檔案路徑或路徑。

## 預設 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空白，表示此影像目錄不包含任何靜態內容資料。

## 另請參閱 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
