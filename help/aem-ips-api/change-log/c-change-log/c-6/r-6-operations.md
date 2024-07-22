---
description: 說明IPS API第6版新的和變更的作業方法。
solution: Experience Manager
title: 新作業和修改作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# 作業：新增和已修改{#operations-new-and-modified}

說明IPS API第6版新的和變更的作業方法。

語法

## 新作業 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 已修改的作業 {#section-f4e8755527444266ae806e3f4c851ae6}

**已新增**

* 已新增`isHidden`和`initialTagValue`至：

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 已新增`thumbAssetHandle`至：

   * `createImageSet`
   * `createAssetSet`

  已新增`companyHandle`至：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  已新增`contextHandle`至：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* 將includeInactive新增至：

   * `getUsers`.
   * `getUserChars`.

* 已新增`permissionArray`至`createPropertySet`。

* 已新增`exportJob`至`submitJob`。

**已變更**

* 在`addUser`和`setUser`中，將`role`變更為`defaultRole`。

* 在`getCompanyMembers`中，將`userArray`變更為`memberArray`。

* 在`getCompanyMembership`中，將`companyArray`變更為`membershipArray`。

* 在`addUser`、`setCompanyMembership`和`addCompanyMembership`中，將`membershipArray`變更為`companyHandleArray`。

* 在`getCompanyMembership`中，將`companyArray`變更為`membershipArray`。

* 在`getUserChars`中，`includeInvalid`現在是選用專案。

**已移除**

* 已從`renameAsset`移除`renameFiles`。

* 已移除`getXMPPanelViewDefinition`。
* 已移除`searchAssetsByFulltext`和`searchAssetsBySimilarity`。
