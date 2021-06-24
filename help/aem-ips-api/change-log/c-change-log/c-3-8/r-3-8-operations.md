---
description: 說明IPS API 3.8版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---

# 操作：新增和修改{#operations-new-and-modified}

說明IPS API 3.8版的新操作方法和更改的操作方法。

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

**searchAssets**

* 選用的`publishState`參數可讓您搜尋`MarkedForPublish/NotMarkedForPublish`資產狀態。

**getJobLogs**

* 選用的`userHandle`參數可讓您擷取由特定使用者提交的工作記錄。
