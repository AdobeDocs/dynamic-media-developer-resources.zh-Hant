---
description: 在瀏覽器中鎖定點擊動作。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 11%

---

# 影像地圖{#imagemap}

在瀏覽器中鎖定點擊動作。

始終與影像關聯。 您可以從`ImageInfo`取得`ImageMap`目標。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 影像地圖控制代碼。 |
| `*`名稱`*` | `xsd:string` | 影像地圖名稱。 |
| `*`區域`*` | `xsd:string` | 影像地圖座標。 格式以HTML `<area>`標籤屬性為基礎。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`標籤中的其他屬性，包括`href` URL。 |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape]值。 |
| `*`位置`*` | `xsd:string` | 以HTML `<area>`元素的[!DNL coords]屬性格式放置。 例如: `coords ="0,0,84,128"`. |
| `*`啟動`*` | `xsd:boolean` | 如果已啟用影像映射，則為true。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改影像映射的日期和時間。 |
