---
description: 說明IPS API 4.5版新的和變更的作業方法。
solution: Experience Manager
title: 作業 — 新增和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: 'https://experienceleague.adobe.com/n4U8LW8otIaBBDalW1wRJFaweTAw3-0Sh0ckgIEADAI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 1%

---

# 作業：新增和已修改{#operations-new-and-modified}

說明IPS API 4.5版新的和變更的作業方法。

語法

## 新作業 {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## 已修改的作業 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset`包含`animatedGifInfo`、`swcInfo`、`cssInfo`和`javascriptInfo`引數。
* `createMetadataField`包含選用的`isHidden`引數。
* `saveMetadataField`包含選用的`isHidden`引數。
* `searchAssets`
* `renameFiles`引數已在先前的版本中被取代，並從`renameAsset`作業中移除。 虛擬檔案路徑會變更，以符合新的資產名稱（保留副檔名），而實體檔案路徑不受影響。 API使用者端在更新至新API版本時需要移除此引數的參考。
