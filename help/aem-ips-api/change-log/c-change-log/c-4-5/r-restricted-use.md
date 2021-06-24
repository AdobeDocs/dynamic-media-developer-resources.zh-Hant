---
description: 這些測試版WSDL中可用的新操作或修改的操作和資料類型，在Dynamic Media開發的應用程式之外不可使用。
solution: Experience Manager
title: 限制使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 限制使用{#restricted-use}

這些測試版WSDL中可用的新操作或修改的操作和資料類型，在Dynamic Media開發的應用程式之外不可使用。

這些操作和類型可能會隨著後續的系統更新而禁用、更改或淘汰。

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
* searchAssetsBySimility
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**修改的類型**

* 將`ActiveJob`變更為包含`createVideoSitemapJob`類型

* 將`ScheduledJob`變更為包含`createVideoSitemapJob`類型

* 將`ImageServingPublishJob`變更為包含選用`contextHandle`

* 將`ImageRenderingPublishJob`變更為包含選用`contextHandle`

* 將`MetadataField`變更為包含選用`initialTagField`

* 將`MetadataCondition`變更為包含和選用`caseSensitive`參數

* 將`PropertySet`變更為將選用`PermissionArray`包含為`permissions`

* 將`UploadDirectoryJob`變更為包含選用`xmpKeywords`、`xmpTemplateId`和`xmpTemplateOverride`參數

* 將`VideoPublishJob`變更為包含選用`contextHandle`

**修改的操作**

* 將`createAssetSet`變更為包含選用`thumbAssetHandle`

* 將`createImageSet`變更為包含選用`thumbAssetHandle`

* 變更`createMetadataField`以包含選用的`initialTagValue`參數

* 將`createPropertySet`變更為將選用`PermissionUpdateArray`包含為`permissionArray`

* 變更`getImageServingPublishSettings`以包含選用的`contextHandle`參數

* 變更`getImageRenderingPublishSettings`以包含選用的`contextHandle`參數

* 已變更`searchAssetsByFullText`以包含一系列選用參數：

   * `SearchFilter` 作為參 `filters` 數

   * `sortBy`
   * `sortDirection`

* 已變更`searchAssetsByMetadata`以包含一系列選用參數：

   * `SearchFilter` 作為參 `filters` 數

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 七參數序列

* 將`setAssetPublishState`變更為將選用`HandleArray`包含為`contextHandleArray`

* 變更`setImageServingPublishSettings`以包含選用的`contextHandle`參數

* 變更`setImageRenderingPublishSettings`以包含選用的`contextHandle`參數

* 將`submitJob`變更為包含可選`createVideoSitemap`作業類型
