---
description: 屬於影像集的Assets。
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

屬於影像集的Assets。

頁面重設表示[!DNL eCatalog]應開始新頁面。 `RenderSet`指出它是`RenderSet`色票的一部分。 值已強製為`true`和`eCatalog`組的`RenderSet`。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| asset | `type:Asset` | 影像集陣列中的Assets。 |
| pageReset | `xsd:boolean` | 開始新頁面。 已忽略設定，且已強制將`true`和`eCatalog`集的值設為`RenderSet`。 |
