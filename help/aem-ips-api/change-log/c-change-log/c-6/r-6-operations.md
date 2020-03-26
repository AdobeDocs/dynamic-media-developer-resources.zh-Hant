---
description: 說明IPS API第6版的新操作方法和更改的操作方法。
seo-description: 說明IPS API第6版的新操作方法和更改的操作方法。
seo-title: 操作新增和修改
solution: Experience Manager
title: 操作新增和修改
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 操作：新增和修改{#operations-new-and-modified}

說明IPS API第6版的新操作方法和更改的操作方法。

語法

## 新操作 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 修改的操作 {#section-f4e8755527444266ae806e3f4c851ae6}

**已新增**

* 新增 `isHidden` 及 `initialTagValue` 至：

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 已新 `thumbAssetHandle` 增至：

   * `createImageSet`
   * `createAssetSet`
   已新 `companyHandle` 增至：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   已新 `contextHandle` 增至：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* 將includeInactive新增至：

   * `getUsers`.
   * `getUserChars`.

* 已新 `permissionArray` 增至 `createPropertySet`。

* 已新 `exportJob` 增至 `submitJob`。

**將**

* 在 `addUser` 和 `setUser`中， `role` 更改為 `defaultRole`。

* 在中 `getCompanyMembers`，已變 `userArray` 更為 `memberArray`。

* 在中 `getCompanyMembership`，已變 `companyArray` 更為 `membershipArray`。

* In `addUser`、 `setCompanyMembership`和 `addCompanyMembership`，已變 `membershipArray` 更為 `companyHandleArray`。

* 在中 `getCompanyMembership`，已變 `companyArray` 更為 `membershipArray`。

* 在中 `getUserChars`, `includeInvalid` 現在是可選的。

**已移除**

* 已從 `renameFiles` 移除 `renameAsset`。

* 已移除 `getXMPPanelViewDefinition`.
* 已移 `searchAssetsByFulltext` 除 `searchAssetsBySimilarity`。

