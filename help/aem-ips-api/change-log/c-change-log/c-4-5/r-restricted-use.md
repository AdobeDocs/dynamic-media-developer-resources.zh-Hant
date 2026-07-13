---
description: 這些在Beta版WSDL中提供的全新或修改作業與資料型別，不得在Dynamic Media開發的應用程式之外使用。
solution: Experience Manager
title: 限制使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
TQID: 'https://experienceleague.adobe.com/X-Q28iVTM95SDSwlSy3yhmJcfJv0TC3LtxXPRv8RCpg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 限制使用{#restricted-use}

這些在Beta版WSDL中提供的全新或修改作業與資料型別，不得在Dynamic Media開發的應用程式之外使用。

這些作業和型別可能會因後續的系統更新而停用、變更或淘汰。

**新型別**

* AssetPublishContext
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**新作業**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContext
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* 更新資產集
* updateCompanyMetadata
* updateImageset
* updatePropertySetPermissions

**修改型別**

* 已變更`ActiveJob`以包含`createVideoSitemapJob`型別

* 已變更`ScheduledJob`以包含`createVideoSitemapJob`型別

* 已變更`ImageServingPublishJob`以包含選用的`contextHandle`

* 已變更`ImageRenderingPublishJob`以包含選用的`contextHandle`

* 已變更`MetadataField`以包含選用的`initialTagField`

* 將`MetadataCondition`變更為包含和選用的`caseSensitive`引數

* 變更`PropertySet`以包含選用的`PermissionArray`作為`permissions`

* 已變更`UploadDirectoryJob`以包含選用的`xmpKeywords`、`xmpTemplateId`和`xmpTemplateOverride`引數

* 已變更`VideoPublishJob`以包含選用的`contextHandle`

**已修改的作業**

* 已變更`createAssetSet`以包含選用的`thumbAssetHandle`

* 已變更`createImageSet`以包含選用的`thumbAssetHandle`

* 變更`createMetadataField`以包含選用的`initialTagValue`引數

* 變更`createPropertySet`以包含選用的`PermissionUpdateArray`作為`permissionArray`

* 變更`getImageServingPublishSettings`以包含選用的`contextHandle`引數

* 變更`getImageRenderingPublishSettings`以包含選用的`contextHandle`引數

* 變更`searchAssetsByFullText`以包含一系列選擇性引數：

   * `SearchFilter`作為`filters`引數

   * `sortBy`
   * `sortDirection`

* 變更`searchAssetsByMetadata`以包含一系列選擇性引數：

   * `SearchFilter`作為`filters`引數

   * `sortBy`
   * `sortDirection`
   * 七個引數的`haystackSearch`序列

* 變更`setAssetPublishState`以包含選用的`HandleArray`作為`contextHandleArray`

* 變更`setImageServingPublishSettings`以包含選用的`contextHandle`引數

* 變更`setImageRenderingPublishSettings`以包含選用的`contextHandle`引數

* 已變更`submitJob`以包含選用的`createVideoSitemap`工作型別

