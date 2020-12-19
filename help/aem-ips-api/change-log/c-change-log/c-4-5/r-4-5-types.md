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
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---


# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API 4.5版的新資料類型和變更的資料類型。

語法

## 新類型{#section-6941b228cf6747a987e98c3d6e4b6b17}

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

## 修改的類型{#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 資產包含新的`fileName`欄位，可傳回虛擬檔案名稱。
* `AssetSummary` 傳回 `type` 和欄 `name` 位

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要 `urlArray` 並新增選用計 `numUrls` 數

