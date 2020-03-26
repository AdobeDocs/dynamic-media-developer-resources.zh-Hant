---
description: 說明IPS API 3.7版的新操作方法和更改的操作方法。
seo-description: 說明IPS API 3.7版的新操作方法和更改的操作方法。
seo-title: 操作新增和修改
solution: Experience Manager
title: 操作新增和修改
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 操作：新增和修改{#operations-new-and-modified}

說明IPS API 3.7版的新操作方法和更改的操作方法。

語法

## 新操作 {#section-c4d34a58f8194d548fbe26ab3764ea58}

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

## 修改的操作 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* 已移除 `name` 參數。
* 已新增 `excludeFieldArray`.

**getFolders**

* 已新增 `excludeFieldArray`.

**getFolderTree**

* 已新增 `excludeFieldArray` 和 `getUniqueMetadataValues`。
* 已設 `fieldHandle` 定必要參數。

