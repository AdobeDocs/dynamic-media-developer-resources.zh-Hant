---
description: 說明IPS API 4.2版的新資料類型和變更的資料類型。
solution: Experience Manager
title: 資料類型新增和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 3%

---


# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API 4.2版的新資料類型和變更的資料類型。

語法

## 新類型{#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 修改的類型{#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**資產**

已新增參數：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

已移除參數：

* `ImageSetInfo`
* `RenderSetInfo`

**重新處理AssetsJob**

已新增參數：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

已新增參數：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

已新增參數：

* `preservePublishState`
* `preserveCrop`

