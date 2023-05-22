---
description: 屬於映像集的資產。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

屬於映像集的資產。

頁面重置表示 [!DNL eCatalog] 應該開始新頁面。 `RenderSet` 表示它是 `RenderSet` 樣式。 值被強制 `true` 為 `eCatalog` 和 `RenderSet` 設定。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| asset | `type:Asset` | 映像集陣列中的資產。 |
| 頁面重置 | `xsd:boolean` | 啟動新頁面。 設定被忽略，值被強制 `true` 為 `eCatalog` 和 `RenderSet` 設定。 |
