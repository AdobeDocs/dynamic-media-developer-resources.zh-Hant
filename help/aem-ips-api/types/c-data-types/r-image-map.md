---
description: 定位以在瀏覽器中執行點按動作。
seo-description: 定位以在瀏覽器中執行點按動作。
seo-title: 影像地圖
solution: Experience Manager
title: 影像地圖
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 影像地圖{#imagemap}

定位以在瀏覽器中執行點按動作。

一律與影像關聯。 您可以從中獲 `ImageMap` 取目標 `ImageInfo`。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | 影像地圖控點。 |
| ` *`名稱`*` | `xsd:string` | 影像地圖名稱。 |
| ` *`區域`*` | `xsd:string` | 影像地圖座標。 格式是以HTML標籤屬 `<area>` 性為基礎。 |
| ` *`操作`*` | `xsd:string` | HTML標籤中要包含的其 `<area>` 他屬性，包括 `href` URL。 |
| ` *`shapeType`*` | `xsd:boolean` | 值 [!DNL RegionShape] 。 |
| ` *`位置`*` | `xsd:string` | 在HTML元素屬性格 `<area>` 式中的位 [!DNL coords] 置。 例如: `coords ="0,0,84,128"`. |
| ` *`啟動`*` | `xsd:boolean` | 如果影像地圖已啟用，則返回true。 |
| ` *`lastModified`*` | `xsd:dateTime` | 上次修改影像地圖的日期和時間。 |

