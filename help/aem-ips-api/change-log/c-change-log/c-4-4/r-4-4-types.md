---
description: 說明IPS API 4.4版的新資料類型和已變更的資料類型。
solution: Experience Manager
title: 資料類型新增和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8800b15-b9a3-4497-8b6b-fd318458ab5a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---

# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API 4.4版的新資料類型和已變更的資料類型。

語法

## 新類型 {#section-b910343aff304ec9b4d74045a2596a74}

* `AssetMetadataFields`
* `AssetMetadataFieldsArray`
* `AssetSetInfo`
* `AutoSetCreationOptions`
* `ExcludeByproductCondition`
* `ExcludeByproductArray`
* `FontFieldUpdate`
* `FontFieldUpdateArray`
* `IccProfileFieldUpdate`
* `IccProfileFieldUpdateArray`

## 修改的類型 {#section-dfd062062ad444b0876bbc951fb1560c}

**資產**

新增參數：

* `subtype`
* `assetSetInfo`

**作業日誌**

新增參數：

* `transferSuccessCount`
* `transferErrorCount`
* `transferWarningCount`

**PDFInfo**

新增參數：

* `extractLinks`
