---
description: 介紹IPS API版本6的新類型和更改的類型。
solution: Experience Manager
title: 新建和修改的資料類型
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# 資料類型：新建和修改{#data-types-new-and-modified}

介紹IPS API版本6的新類型和更改的類型。

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

* 已添加 `numUrls` 至 `UploadUrlsJob`。

* 已添加 `fileName` 至 `Asset.`

* 已添加 `isHidden` 至 `MetadataField`。

* 已添加 `taskState` 至 `TaskProgress`。

* 已添加 `exportJob` 至 `ActiveJob` 和 `ScheduledJob`。

* 已添加 `optmizedPath` 和 `optimizedFile` 至 `PsdInfo`。

* 已添加 `contextHandle` 至：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 已將以下參數添加到 `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**將**

* 在 `User`已更改 `role` 至 `defaultRole`。

* 在 `Folder`已更改 `permissions` 至 `permissionsSetHandle`。

* 在 `AssetSummary`。 `type` 和 `name` 選項。
