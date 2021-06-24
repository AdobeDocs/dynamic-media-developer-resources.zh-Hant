---
description: 說明IPS API 6版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新建和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# 操作：新增和修改{#operations-new-and-modified}

說明IPS API 6版的新操作方法和更改的操作方法。

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

* 將`isHidden`和`initialTagValue`新增至：

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 將`thumbAssetHandle`新增至：

   * `createImageSet`
   * `createAssetSet`

   將`companyHandle`新增至：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   將`contextHandle`新增至：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* 將includeInactive新增至：

   * `getUsers`.
   * `getUserChars`.

* 將`permissionArray`新增至`createPropertySet`。

* 將`exportJob`新增至`submitJob`。

**將**

* 在`addUser`和`setUser`中，將`role`變更為`defaultRole`。

* 在`getCompanyMembers`中，將`userArray`變更為`memberArray`。

* 在`getCompanyMembership`中，將`companyArray`變更為`membershipArray`。

* 在`addUser`、`setCompanyMembership`和`addCompanyMembership`中，將`membershipArray`變更為`companyHandleArray`。

* 在`getCompanyMembership`中，將`companyArray`變更為`membershipArray`。

* 在`getUserChars`中，`includeInvalid`現在為選用。

**已移除**

* 從`renameAsset`移除`renameFiles`。

* 已移除 `getXMPPanelViewDefinition`.
* 移除`searchAssetsByFulltext`和`searchAssetsBySimilarity`。
