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
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

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

