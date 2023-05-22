---
description: 映像資料檔案路徑。 指定包含此目錄的影像資料的檔案。
solution: Experience Manager
title: 目錄檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---

# 目錄檔案{#catalogfile}

映像資料檔案路徑。 指定包含此目錄的影像資料的檔案。

影像資料檔案按指定的順序載入。 如果相同 `catalog::Id` 值在多條記錄（在同一或不同的目錄檔案中）中出現，最後一個實例佔上風。

## 屬性 {#section-6da55f145ecd4e31a5de52637a436983}

一個或多個文本字串值，用逗號分隔。 選擇性. 每個值必須是相對於目錄資料夾的絕對檔案路徑或路徑。

## 預設 {#section-80f91cd7a6b2479ebb310319e9c74da7}

空，表示此影像目錄不包含任何影像資料。

## 另請參閱 {#section-910b67c5041d44d99a105ad43ff63a37}

[目錄資料欄位](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
