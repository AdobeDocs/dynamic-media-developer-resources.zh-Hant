---
description: 瀏覽器中點按動作的目標定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# ImageMapDefinition{#imagemapdefinition}

瀏覽器中點按動作的目標定義。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`名稱`*` | `xsd:string` | 影像地圖定義的名稱。 |
| `*`shapeType`*` | `xsd:string` | 區域形狀值之一。 |
| `*`區域`*` | `xsd:string` | 影像地圖座標。 格式以HTML `<area>`標籤屬性為基礎。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`標籤中的其他屬性，包括`href` URL。 |
| `*`啟動`*` | `xsd:boolean` | 如果影像地圖已啟用，則返回true。 |

