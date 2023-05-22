---
description: 介紹IPS API 3.8版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---

# 操作：新建和修改{#operations-new-and-modified}

介紹IPS API 3.8版的新操作方法和更改的操作方法。

語法

## 新操作 {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 修改的操作 {#section-25eee732b69c49d0a27b1f3290f8654a}

**搜索資產**

* 可選 `publishState` 參數，用於搜索 `MarkedForPublish/NotMarkedForPublish` 資產狀態。

**getJobLogs**

* 可選 `userHandle` 參數用於檢索特定用戶提交的作業日誌。
