---
description: 說明IPS API 4.5版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# 操作：新增和修改{#operations-new-and-modified}

說明IPS API 4.5版的新操作方法和更改的操作方法。

語法

## 新操作 {#section-a3be679d8e9345aba2e97699c3a537b9}

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

## 修改的操作 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 包括 `animatedGifInfo`、  `swcInfo`、 `cssInfo`和參 `javascriptInfo` 數。

* `createMetadataField` 包含選用 `isHidden` 參數。

* `saveMetadataField` 包含選用 `isHidden` 參數。

* `searchAssets`
* 
* 先前版本已棄用`renameFiles`參數，並從`renameAsset`操作中移除。 虛擬檔案路徑會變更，以符合新資產名稱（保留副檔名），而物理檔案路徑則不受影響。 更新至新API版本時，API用戶端需要移除此參數的參考。
