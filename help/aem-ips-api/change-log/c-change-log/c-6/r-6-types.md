---
description: 說明IPS API第6版的新型別和變更型別。
solution: Experience Manager
title: 新增和修改的資料型別
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

---

# 資料型別：新增和修改{#data-types-new-and-modified}

說明IPS API第6版的新型別和變更型別。

語法

## 新型別 {#section-71ba6954339e4ba899acdf8a3212d6f3}

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

## 修改型別 {#section-56b834b1a3b843279d8715b4a4f3890b}

**已新增**

* 已新增`numUrls`至`UploadUrlsJob`。

* 已新增`fileName`至`Asset.`

* 已新增`isHidden`至`MetadataField`。

* 已新增`taskState`至`TaskProgress`。

* 已新增`exportJob`至`ActiveJob`和`ScheduledJob`。

* 已新增`optmizedPath`和`optimizedFile`至`PsdInfo`。

* 已新增`contextHandle`至：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 已將下列引數新增至`Asset`：

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**已變更**

* 在`User`中，將`role`變更為`defaultRole`。

* 在`Folder`中，將`permissions`變更為`permissionsSetHandle`。

* 在`AssetSummary`中，`type`和`name`現在是選用專案。
