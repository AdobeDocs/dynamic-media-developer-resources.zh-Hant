---
description: 測試版WSDL中提供的這些新或修改的作業和資料類型，在Scene7開發的應用程式外部不會使用。
seo-description: 測試版WSDL中提供的這些新或修改的作業和資料類型，在Scene7開發的應用程式外部不會使用。
seo-title: 限制使用
solution: Experience Manager
title: 限制使用
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 限制使用{#restricted-use}

測試版WSDL中提供的這些新或修改的作業和資料類型，在Scene7開發的應用程式外部不會使用。

這些操作和類型可能會在後續系統更新中禁用、更改或取代。

**新類型**

* AssetPublishContexts
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**新操作**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimiliary
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**修改的類型**

* 變更 `ActiveJob` 為包含類 `createVideoSitemapJob` 型

* 變更 `ScheduledJob` 為包含類 `createVideoSitemapJob` 型

* 已變 `ImageServingPublishJob` 更為包含選用 `contextHandle`

* 已變 `ImageRenderingPublishJob` 更為包含選用 `contextHandle`

* 已變 `MetadataField` 更為包含選用 `initialTagField`

* 已變 `MetadataCondition` 更為包含和選用參 `caseSensitive` 數

* 已變 `PropertySet` 更為包含可選 `PermissionArray` 項 `permissions`

* 已變 `UploadDirectoryJob` 更為包含 `xmpKeywords`可選 `xmpTemplateId` 和參 `xmpTemplateOverride` 數

* 已變 `VideoPublishJob` 更為包含選用 `contextHandle`

**修改的操作**

* 已變 `createAssetSet` 更為包含選用 `thumbAssetHandle`

* 已變 `createImageSet` 更為包含選用 `thumbAssetHandle`

* 變更 `createMetadataField` 為包含可選參 `initialTagValue` 數

* 已變 `createPropertySet` 更為包含可選 `PermissionUpdateArray` 項 `permissionArray`

* 變更 `getImageServingPublishSettings` 為包含可選參 `contextHandle` 數

* 變更 `getImageRenderingPublishSettings` 為包含可選參 `contextHandle` 數

* 已變 `searchAssetsByFullText` 更為包含一系列可選參數：

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`

* 已變 `searchAssetsByMetadata` 更為包含一系列可選參數：

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7個參數序列

* 已變 `setAssetPublishState` 更為包含可選 `HandleArray` 項 `contextHandleArray`

* 變更 `setImageServingPublishSettings` 為包含可選參 `contextHandle` 數

* 變更 `setImageRenderingPublishSettings` 為包含可選參 `contextHandle`數

* 已變 `submitJob` 更為包含可選作 `createVideoSitemap` 業類型

