---
description: 介紹IPS API 4.5版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作 — 新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# 操作：新建和修改{#operations-new-and-modified}

介紹IPS API 4.5版的新操作方法和更改的操作方法。

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

* `Asset` 包括 `animatedGifInfo`。 `swcInfo`。 `cssInfo`, `javascriptInfo` 參數。
* `createMetadataField` 包括可選 `isHidden` 的下界。
* `saveMetadataField` 包括可選 `isHidden` 的下界。
* `searchAssets`
* 的 `renameFiles` 參數已棄用於以前的版本，並已從 `renameAsset` 的下界。 虛擬檔案路徑被更改以與新資產名稱匹配（保留檔案副檔名），而物理檔案路徑不受影響。 API客戶端在更新到新API版本時需要刪除對此參數的引用。
