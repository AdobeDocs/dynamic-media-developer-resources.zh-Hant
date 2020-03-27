---
description: 屬於影像集的資產。
seo-description: 屬於影像集的資產。
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMember{#imagesetmember}

屬於影像集的資產。

頁面重設表示 [!DNL eCatalog] 應開始新頁面。 `RenderSet` 表示它是色票的一 `RenderSet` 部分。 值被強制用於 `true` 和 `eCatalog` 集 `RenderSet` 合。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`asset`*` | `type:Asset` | 影像集陣列中的資產。 |
| ` *`pageReset`*` | `xsd:boolean` | 開始新頁面。 設定會被忽略，且值會強制 `true` 用於 `eCatalog` 和 `RenderSet` 設定。 |

