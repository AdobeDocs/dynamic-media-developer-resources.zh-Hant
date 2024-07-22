---
description: 說明IPS API 4.5版的新資料和變更資料型別。
solution: Experience Manager
title: 新增和修改的資料型別
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# 資料型別：新增和修改{#data-types-new-and-modified}

說明IPS API 4.5版的新資料和變更資料型別。

語法

## 新型別 {#section-6941b228cf6747a987e98c3d6e4b6b17}

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

## 修改型別 {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 資產包含傳回虛擬檔案名稱的新`fileName`欄位。
* `AssetSummary`傳回`type`和`name`欄位

* `MetadataField`包含`isHidden`

* `MetadataUpdate`
* `UploadUrlsJob`需要`urlArray`並新增選用的`numUrls`計數
