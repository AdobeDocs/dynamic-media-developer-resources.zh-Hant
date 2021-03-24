---
description: 屬於影像集的資產。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media經典，SDK/API，影像集
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

屬於影像集的資產。

頁面重設表示[!DNL eCatalog]應該啟動新頁面。 `RenderSet` 表示它是色票的一 `RenderSet` 部分。對於`eCatalog`和`RenderSet`集，該值被強制為`true`。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 影像集陣列中的資產。 |
| `*`pageReset`*` | `xsd:boolean` | 開始新頁面。 設定被忽略，並且`eCatalog`和`RenderSet`集的值被強制為`true`。 |

