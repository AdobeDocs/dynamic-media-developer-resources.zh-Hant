---
description: 說明IPS API第6版新的和變更的作業方法。
solution: Experience Manager
title: 新作業和修改作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
TQID: 'https://experienceleague.adobe.com/DLA26IsxxpZ0TSSfQBrvZSl8mbcJCaTfnpK-bhhmglg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
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
