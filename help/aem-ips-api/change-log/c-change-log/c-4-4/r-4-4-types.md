---
description: 說明IPS API 4.4版的新資料和變更資料型別。
solution: Experience Manager
title: 新增和修改的資料型別
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8800b15-b9a3-4497-8b6b-fd318458ab5a
TQID: 'https://experienceleague.adobe.com/M6caMx5DHaAFtDj-feUVEOQeHgr2--5R9gKmkoeQB1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 48
ht-degree: 2%

---

# 資料型別：新增和修改{#data-types-new-and-modified}

說明IPS API 4.4版的新資料和變更資料型別。

語法

## 新型別 {#section-b910343aff304ec9b4d74045a2596a74}

* `AssetMetadataFields`
* `AssetMetadataFieldsArray`
* `AssetSetInfo`
* `AutoSetCreationOptions`
* `ExcludeByproductCondition`
* `ExcludeByproductArray`
* `FontFieldUpdate`
* `FontFieldUpdateArray`
* `IccProfileFieldUpdate`
* `IccProfileFieldUpdateArray`

## 修改型別 {#section-dfd062062ad444b0876bbc951fb1560c}

**資產**

引數已新增：

* `subtype`
* `assetSetInfo`

**工作記錄檔**

引數已新增：

* `transferSuccessCount`
* `transferErrorCount`
* `transferWarningCount`

**PDFInfo**

引數已新增：

* `extractLinks`
