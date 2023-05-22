---
description: 介紹IPS API 4.2版的新資料類型和更改的資料類型。
solution: Experience Manager
title: 新建和修改的資料類型
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 1%

---

# 資料類型：新建和修改{#data-types-new-and-modified}

介紹IPS API 4.2版的新資料類型和更改的資料類型。

語法

## 新類型 {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 修改的類型 {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**資產**

添加的參數：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

刪除的參數：

* `ImageSetInfo`
* `RenderSetInfo`

**重新處理AssetsJob**

添加的參數：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**上載目錄作業**

添加的參數：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**上載Urls作業**

添加的參數：

* `preservePublishState`
* `preserveCrop`
