---
description: 說明IPS API 3.7版新的和變更的作業方法。
solution: Experience Manager
title: 新作業和修改作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---

# 作業：新增和已修改{#operations-new-and-modified}

說明IPS API 3.7版新的和變更的作業方法。

語法

## 新作業 {#section-c4d34a58f8194d548fbe26ab3764ea58}

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

## 已修改的作業 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* 已移除`name`引數。
* 已新增`excludeFieldArray`。

**getFolders**

* 已新增`excludeFieldArray`。

**getFolderTree**

* 已新增`excludeFieldArray`和`getUniqueMetadataValues`。
* 將`fieldHandle`設為必要引數。
