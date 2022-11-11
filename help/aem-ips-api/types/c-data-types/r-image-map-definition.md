---
description: 瀏覽器中點按動作的目標定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

瀏覽器中點按動作的目標定義。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 名稱 | `xsd:string` | 影像映射定義的名稱。 |
| shapeType | `xsd:string` | 區域形狀值之一。 |
| 區域 | `xsd:string` | 影像地圖座標。 格式以HTML為基礎 `<area>` 標籤屬性。 |
| 操作 | `xsd:string` | 要包含在HTML中的其他屬性 `<area>` 標籤，包括 `href` URL。 |
| 啟動 | `xsd:boolean` | 若已啟用影像對應，則為true。 |
