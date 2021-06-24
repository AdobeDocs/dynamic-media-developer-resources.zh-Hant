---
description: 瀏覽器中點按動作的目標定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# ImageMapDefinition{#imagemapdefinition}

瀏覽器中點按動作的目標定義。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`名稱`*` | `xsd:string` | 影像映射定義的名稱。 |
| `*`shapeType`*` | `xsd:string` | 區域形狀值之一。 |
| `*`區域`*` | `xsd:string` | 影像地圖座標。 格式以HTML `<area>`標籤屬性為基礎。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`標籤中的其他屬性，包括`href` URL。 |
| `*`啟動`*` | `xsd:boolean` | 若已啟用影像對應，則為true。 |
