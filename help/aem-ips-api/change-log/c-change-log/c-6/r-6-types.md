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

---


# 資料類型：新增和修改{#data-types-new-and-modified}

說明IPS API第6版的新類型和已變更類型。

語法

## 新類型 {#section-71ba6954339e4ba899acdf8a3212d6f3}

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

## 修改的類型 {#section-56b834b1a3b843279d8715b4a4f3890b}

**已新增**

* 已新 `numUrls` 增至 `UploadUrlsJob`。

* 新增 `fileName` 至 `Asset.`

* 已新 `isHidden` 增至 `MetadataField`。

* 已新 `taskState` 增至 `TaskProgress`。

* 已新 `exportJob` 增至 `ActiveJob` 和 `ScheduledJob`。

* 已添 `optmizedPath` 加 `optimizedFile` 和 `PsdInfo`。

* 已新 `contextHandle` 增至：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 將下列參數新增至 `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**將**

* 在中 `User`，已變 `role` 更為 `defaultRole`。

* 在中 `Folder`，已變 `permissions` 更為 `permissionsSetHandle`。

* 在中 `AssetSummary`, `type` 現在 `name` 是可選的。

