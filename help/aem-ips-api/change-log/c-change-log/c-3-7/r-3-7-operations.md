---
description: 介紹IPS API 3.7版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 6%

---

# 操作：新建和修改{#operations-new-and-modified}

介紹IPS API 3.7版的新操作方法和更改的操作方法。

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

**搜索資產**

* 已刪除 `name` 的下界。
* 已新增 `excludeFieldArray`.

**getFolders**

* 已新增 `excludeFieldArray`.

**getFolderTree**

* 已添加 `excludeFieldArray` 和 `getUniqueMetadataValues`。
* 製作 `fieldHandle` 參數。
