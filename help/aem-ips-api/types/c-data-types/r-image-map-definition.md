---
description: 瀏覽器中點按動作的目標定義。
seo-description: 瀏覽器中點按動作的目標定義。
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Scene7 Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageMapDefinition{#imagemapdefinition}

瀏覽器中點按動作的目標定義。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`名稱`*` | `xsd:string` | 影像地圖定義的名稱。 |
| ` *`shapeType`*` | `xsd:string` | 區域形狀值之一。 |
| ` *`區域`*` | `xsd:string` | 影像地圖座標。 格式是以HTML標籤屬 `<area>` 性為基礎。 |
| ` *`操作`*` | `xsd:string` | HTML標籤中要包含的其 `<area>` 他屬性，包括 `href` URL。 |
| ` *`啟動`*` | `xsd:boolean` | 如果影像地圖已啟用，則返回true。 |

