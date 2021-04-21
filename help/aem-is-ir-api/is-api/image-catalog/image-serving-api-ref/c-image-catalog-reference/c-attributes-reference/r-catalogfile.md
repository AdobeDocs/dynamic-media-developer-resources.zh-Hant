---
description: 影像資料檔案路徑。 指定包含此目錄映像資料的檔案。
solution: Experience Manager
title: 目錄檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---


# CatalogFile{#catalogfile}

影像資料檔案路徑。 指定包含此目錄映像資料的檔案。

影像資料檔案會依指定順序載入。 如果相同的`catalog::Id`值出現在多個記錄中（位於相同或不同的目錄檔案中），則最後一個例項優先。

## 屬性 {#section-6da55f145ecd4e31a5de52637a436983}

一或多個文字字串值，以逗號分隔。 選填。每個值都必須是相對於目錄資料夾的絕對檔案路徑或路徑。

## 預設 {#section-80f91cd7a6b2479ebb310319e9c74da7}

空白，表示此影像目錄不包含任何影像資料。

## 另請參閱 {#section-910b67c5041d44d99a105ad43ff63a37}

[目錄資料欄位](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
