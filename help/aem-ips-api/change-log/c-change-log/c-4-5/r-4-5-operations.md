---
description: 說明IPS API 4.5版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新增和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 操作：新增和修改{#operations-new-and-modified}

說明IPS API 4.5版的新操作方法和更改的操作方法。

語法

## 新操作{#section-a3be679d8e9345aba2e97699c3a537b9}

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

## 修改的操作{#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 包含 `animatedGifInfo`、 `swcInfo`、 `cssInfo`和參 `javascriptInfo` 數。

* `createMetadataField` 包含可選 `isHidden` 參數。

* `saveMetadataField` 包含可選 `isHidden` 參數。

* `searchAssets`
* 
* `renameFiles`參數已在舊版中過時，並已從`renameAsset`操作中移除。 虛擬檔案路徑會變更為符合新資產名稱（保留副檔名），而物理檔案路徑則不受影響。 API用戶端在更新至新API版本時，必須移除此參數的參考。

