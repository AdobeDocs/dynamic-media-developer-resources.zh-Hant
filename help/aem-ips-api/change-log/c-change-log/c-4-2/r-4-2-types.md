---
description: 說明IPS API 4.2版的新資料和變更資料型別。
solution: Experience Manager
title: 新增和修改的資料型別
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
TQID: 'https://experienceleague.adobe.com/2YCgrii3dF6Zq7NlXRI0vD3DtO-jWpSo4YKcpZsdFHU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 1%

---

# 資料型別：新增和修改{#data-types-new-and-modified}

說明IPS API 4.2版的新資料和變更資料型別。

語法

## 新型別 {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 修改型別 {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**資產**

引數已新增：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

引數已移除：

* `ImageSetInfo`
* `RenderSetInfo`

**重新處理資產工作**

引數已新增：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

引數已新增：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

引數已新增：

* `preservePublishState`
* `preserveCrop`
