---
description: 測試版WSDL中提供的這些新操作或修改的操作和資料類型，在Dynamic Media開發的應用程式之外不可使用。
solution: Experience Manager
title: 限制使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# 限制使用{#restricted-use}

測試版WSDL中提供的這些新操作或修改的操作和資料類型，在Dynamic Media開發的應用程式之外不可使用。

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

* 已將`ActiveJob`變更為包含`createVideoSitemapJob`類型

* 已將`ScheduledJob`變更為包含`createVideoSitemapJob`類型

* 已將`ImageServingPublishJob`變更為包含選用的`contextHandle`

* 已將`ImageRenderingPublishJob`變更為包含選用的`contextHandle`

* 已將`MetadataField`變更為包含選用的`initialTagField`

* 已將`MetadataCondition`變更為包含和選用`caseSensitive`參數

* 已將`PropertySet`變更為包含選用`PermissionArray`為`permissions`

* 已將`UploadDirectoryJob`變更為包含可選`xmpKeywords`、`xmpTemplateId`和`xmpTemplateOverride`參數

* 已將`VideoPublishJob`變更為包含選用的`contextHandle`

**修改的操作**

* 已將`createAssetSet`變更為包含選用的`thumbAssetHandle`

* 已將`createImageSet`變更為包含選用的`thumbAssetHandle`

* 已將`createMetadataField`變更為包含選用的`initialTagValue`參數

* 已將`createPropertySet`變更為包含選用`PermissionUpdateArray`為`permissionArray`

* 已將`getImageServingPublishSettings`變更為包含選用的`contextHandle`參數

* 已將`getImageRenderingPublishSettings`變更為包含選用的`contextHandle`參數

* 已變更`searchAssetsByFullText`以包含一系列可選參數：

   * `SearchFilter` as參 `filters` 數

   * `sortBy`
   * `sortDirection`

* 已變更`searchAssetsByMetadata`以包含一系列可選參數：

   * `SearchFilter` as參 `filters` 數

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7個參數序列

* 已將`setAssetPublishState`變更為包含選用`HandleArray`為`contextHandleArray`

* 已將`setImageServingPublishSettings`變更為包含選用的`contextHandle`參數

* 已將`setImageRenderingPublishSettings`變更為包含選用的`contextHandle`參數

* 已將`submitJob`變更為包含可選`createVideoSitemap`作業類型

