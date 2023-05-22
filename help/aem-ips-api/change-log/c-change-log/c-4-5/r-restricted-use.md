---
description: 這些測試版WSDL中提供的新操作或已修改的操作和資料類型不在Dynamic Media開發的應用程式之外使用。
solution: Experience Manager
title: 限制使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 限制使用{#restricted-use}

這些測試版WSDL中提供的新操作或已修改的操作和資料類型不在Dynamic Media開發的應用程式之外使用。

這些操作和類型可能會在後續系統更新時禁用、更改或棄用。

**新類型**

* 資產發佈上下文
* 資產發佈上下文陣列
* 公司元資料資訊
* 公司元資料資訊陣列
* CreateVideoSitemapJob
* 發佈上下文
* 發佈上下文陣列
* 搜索篩選器
* 長陣列

**新操作**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* 刪除掩碼
* removePropertySetPermissions
* searchAssetsBySimility
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* 更新資產集
* updateCompanyMetadata
* 更新映像集
* updatePropertySetPermissions

**修改的類型**

* 已更改 `ActiveJob` 包括 `createVideoSitemapJob` 類型

* 已更改 `ScheduledJob` 包括 `createVideoSitemapJob` 類型

* 已更改 `ImageServingPublishJob` 包含可選 `contextHandle`

* 已更改 `ImageRenderingPublishJob` 包含可選 `contextHandle`

* 已更改 `MetadataField` 包含可選 `initialTagField`

* 已更改 `MetadataCondition` 包括和可選 `caseSensitive` 參數

* 已更改 `PropertySet` 包含可選 `PermissionArray` 如 `permissions`

* 已更改 `UploadDirectoryJob` 包括可選 `xmpKeywords`。 `xmpTemplateId` 和 `xmpTemplateOverride` 參數

* 已更改 `VideoPublishJob` 包含可選 `contextHandle`

**修改的操作**

* 已更改 `createAssetSet` 包含可選 `thumbAssetHandle`

* 已更改 `createImageSet` 包含可選 `thumbAssetHandle`

* 已更改 `createMetadataField` 包含可選 `initialTagValue` 參數

* 已更改 `createPropertySet` 包含可選 `PermissionUpdateArray` 如 `permissionArray`

* 已更改 `getImageServingPublishSettings` 包含可選 `contextHandle` 參數

* 已更改 `getImageRenderingPublishSettings` 包含可選 `contextHandle` 參數

* 已更改 `searchAssetsByFullText` 要包括一系列可選參數：

   * `SearchFilter` 如 `filters` 參數

   * `sortBy`
   * `sortDirection`

* 已更改 `searchAssetsByMetadata` 要包括一系列可選參數：

   * `SearchFilter` 如 `filters` 參數

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 七個參數序列

* 已更改 `setAssetPublishState` 包含可選 `HandleArray` 如 `contextHandleArray`

* 已更改 `setImageServingPublishSettings` 包含可選 `contextHandle` 參數

* 已更改 `setImageRenderingPublishSettings` 包含可選 `contextHandle`參數

* 已更改 `submitJob` 包含可選 `createVideoSitemap` 作業類型
