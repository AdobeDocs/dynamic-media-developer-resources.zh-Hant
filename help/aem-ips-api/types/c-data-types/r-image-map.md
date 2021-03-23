---
description: 定位以在瀏覽器中執行點按動作。
seo-description: 定位以在瀏覽器中執行點按動作。
seo-title: 影像地圖
solution: Experience Manager
title: 影像地圖
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 11%

---


# 影像地圖{#imagemap}

定位以在瀏覽器中執行點按動作。

一律與影像關聯。 您可從`ImageInfo`取得`ImageMap`目標。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 影像地圖控點。 |
| `*`名稱`*` | `xsd:string` | 影像地圖名稱。 |
| `*`區域`*` | `xsd:string` | 影像地圖座標。 格式以HTML `<area>`標籤屬性為基礎。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`標籤中的其他屬性，包括`href` URL。 |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape]值。 |
| `*`位置`*` | `xsd:string` | 以HTML `<area>`元素的[!DNL coords]屬性格式定位。 例如: `coords ="0,0,84,128"`. |
| `*`啟動`*` | `xsd:boolean` | 如果影像地圖已啟用，則返回true。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改影像地圖的日期和時間。 |

