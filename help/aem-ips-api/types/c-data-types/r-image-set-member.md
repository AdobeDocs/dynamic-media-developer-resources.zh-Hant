---
description: 屬於影像集的資產。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,Administrator
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# ImageSetMember{#imagesetmember}

屬於影像集的資產。

頁面重設表示[!DNL eCatalog]應該啟動新頁面。 `RenderSet` 表示它是色票的一 `RenderSet` 部分。對於`eCatalog`和`RenderSet`集，值被強制為`true`。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 影像集陣列中的資產。 |
| `*`pageReset`*` | `xsd:boolean` | 開始新頁面。 忽略設定，且對於`eCatalog`和`RenderSet`集，值強制為`true`。 |
