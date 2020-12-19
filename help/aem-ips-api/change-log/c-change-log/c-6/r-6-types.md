---
description: 說明IPS API第6版的新類型和已變更類型。
seo-description: 說明IPS API第6版的新類型和已變更類型。
seo-title: 資料類型新增和修改
solution: Experience Manager
title: 資料類型新增和修改
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---


# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API第6版的新類型和已變更類型。

語法

## 新類型{#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## 修改的類型{#section-56b834b1a3b843279d8715b4a4f3890b}

**已新增**

* 已將`numUrls`新增至`UploadUrlsJob`。

* 將`fileName`新增至`Asset.`

* 已將`isHidden`新增至`MetadataField`。

* 已將`taskState`新增至`TaskProgress`。

* 將`exportJob`新增至`ActiveJob`和`ScheduledJob`。

* 將`optmizedPath`和`optimizedFile`新增至`PsdInfo`。

* 將`contextHandle`新增至：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 已將下列參數新增至`Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**將**

* 在`User`中，將`role`變更為`defaultRole`。

* 在`Folder`中，將`permissions`變更為`permissionsSetHandle`。

* 在`AssetSummary`中，`type`和`name`現在是可選的。

