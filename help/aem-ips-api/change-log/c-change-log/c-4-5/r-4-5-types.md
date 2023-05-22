---
description: 介紹IPS API 4.5版的新資料類型和更改的資料類型。
solution: Experience Manager
title: 新建和修改的資料類型
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

---

# 資料類型：新建和修改{#data-types-new-and-modified}

介紹IPS API 4.5版的新資料類型和更改的資料類型。

語法

## 新類型 {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## 修改的類型 {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 資產包括新 `fileName` 返回虛擬檔案名的欄位。
* `AssetSummary` 返回 `type` 和 `name` 場

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要 `urlArray` 並添加可選 `numUrls` 計數
