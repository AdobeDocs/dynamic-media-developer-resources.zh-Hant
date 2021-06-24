---
description: 說明IPS API 4.5版的新資料類型和已變更的資料類型。
solution: Experience Manager
title: 資料類型新增和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API 4.5版的新資料類型和已變更的資料類型。

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

* 資產包含新的`fileName`欄位，可傳回虛擬檔案名稱。
* `AssetSummary` 傳回 `type` 和欄 `name` 位

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要 `urlArray` 並新增選用計 `numUrls` 數
