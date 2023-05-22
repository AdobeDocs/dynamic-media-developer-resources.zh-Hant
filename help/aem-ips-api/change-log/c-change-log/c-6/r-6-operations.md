---
description: 介紹IPS API版本6的新操作方法和已更改的操作方法。
solution: Experience Manager
title: 操作新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---

# 操作：新建和修改{#operations-new-and-modified}

介紹IPS API版本6的新操作方法和已更改的操作方法。

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

* 已添加 `isHidden` 和 `initialTagValue` 至：

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 已添加 `thumbAssetHandle` 至：

   * `createImageSet`
   * `createAssetSet`

   已添加 `companyHandle` 至：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   已添加 `contextHandle` 至：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* 已將includeInactive添加到：

   * `getUsers`.
   * `getUserChars`.

* 已添加 `permissionArray` 至 `createPropertySet`。

* 已添加 `exportJob` 至 `submitJob`。

**將**

* 在 `addUser` 和 `setUser`已更改 `role` 至 `defaultRole`。

* 在 `getCompanyMembers`已更改 `userArray` 至 `memberArray`。

* 在 `getCompanyMembership`已更改 `companyArray` 至 `membershipArray`。

* 在 `addUser`。 `setCompanyMembership`, `addCompanyMembership`已更改 `membershipArray` 至 `companyHandleArray`。

* 在 `getCompanyMembership`已更改 `companyArray` 至 `membershipArray`。

* 在 `getUserChars`。 `includeInvalid` 選項。

**已移除**

* 已刪除 `renameFiles` 從 `renameAsset`。

* 已移除 `getXMPPanelViewDefinition`.
* 已刪除 `searchAssetsByFulltext` 和 `searchAssetsBySimilarity`。
