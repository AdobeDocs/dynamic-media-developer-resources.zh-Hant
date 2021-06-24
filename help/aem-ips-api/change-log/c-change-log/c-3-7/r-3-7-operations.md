---
description: 說明IPS API 3.7版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 5%

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

* 移除`name`參數。
* 已新增 `excludeFieldArray`.

**getFolders**

* 已新增 `excludeFieldArray`.

**getFolderTree**

* 新增`excludeFieldArray`和`getUniqueMetadataValues`。
* 將`fieldHandle`設為必要參數。
