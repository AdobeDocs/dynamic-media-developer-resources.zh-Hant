---
description: 靜態內容目錄資料檔案路徑。 指定包含此目錄的靜態內容資料的檔案。
solution: Experience Manager
title: 靜態內容目錄檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# 靜態內容目錄檔案{#staticcontentcatalogfile}

靜態內容目錄資料檔案路徑。 指定包含此目錄的靜態內容資料的檔案。

靜態內容目錄資料檔案按指定的順序載入。 如果相同 `static::Id` 值在多條記錄（在同一或不同的目錄檔案中）中出現，最後一個實例佔上風。

## 屬性 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

一個或多個文本字串值，用逗號分隔。 選擇性. 每個值必須是相對於目錄資料夾的絕對檔案路徑或路徑。

## 預設 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空，表示此影像目錄不包含任何靜態內容資料。

## 另請參閱 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
