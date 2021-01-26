---
description: 說明IPS API 3.7版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新增和修改
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 6%

---


# 操作：新增和修改{#operations-new-and-modified}

說明IPS API 3.7版的新操作方法和更改的操作方法。

語法

## 新操作{#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## 修改的操作{#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* 已移除`name`參數。
* 已新增 `excludeFieldArray`.

**getFolders**

* 已新增 `excludeFieldArray`.

**getFolderTree**

* 已新增`excludeFieldArray`和`getUniqueMetadataValues`。
* 將`fieldHandle`設為必要參數。

