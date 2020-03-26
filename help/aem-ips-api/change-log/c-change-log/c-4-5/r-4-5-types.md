---
description: 說明IPS API 4.5版的新資料類型和變更的資料類型。
seo-description: 說明IPS API 4.5版的新資料類型和變更的資料類型。
seo-title: 資料類型新增和修改
solution: Experience Manager
title: 資料類型新增和修改
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API 4.5版的新資料類型和變更的資料類型。

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

* 資產包含可傳 `fileName` 回虛擬檔案名稱的新欄位。
* `AssetSummary` 返回 `type` 和字 `name` 段

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要並 `urlArray` 新增選用計 `numUrls` 數

