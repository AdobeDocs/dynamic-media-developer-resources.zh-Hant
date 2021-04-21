---
description: 定位以在瀏覽器中執行點按動作。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '104'
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

