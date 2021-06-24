---
description: 說明IPS API 4.2版的新資料類型和已變更的資料類型。
solution: Experience Manager
title: 資料類型新增和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 3%

---

# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API 4.2版的新資料類型和已變更的資料類型。

語法

## 新類型 {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 修改的類型 {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**資產**

新增參數：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

移除的參數：

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

新增參數：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

新增參數：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

新增參數：

* `preservePublishState`
* `preserveCrop`
