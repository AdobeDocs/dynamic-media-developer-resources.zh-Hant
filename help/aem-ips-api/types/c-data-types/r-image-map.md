---
description: 在瀏覽器中鎖定點擊動作。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---

# [!DNL ImageMap]{#imagemap}

在瀏覽器中鎖定點擊動作。

始終與影像關聯。 您可以取得 `ImageMap` 目標從 `ImageInfo`.

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 影像地圖控制代碼。 |
| [!DNL name] | `xsd:string` | 影像地圖名稱。 |
| [!DNL region] | `xsd:string` | 影像地圖座標。 格式以HTML為基礎 `<area>` 標籤屬性。 |
| [!DNL action] | `xsd:string` | 要包含在HTML中的其他屬性 `<area>` 標籤，包括 `href` URL。 |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] 值。 |
| [!DNL position] | `xsd:string` | 以HTML格式定位 `<area>` 元素 [!DNL coords] 屬性。 例如: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | 如果已啟用影像映射，則為true。 |
| lastModified | `xsd:dateTime` | 上次修改影像映射的日期和時間。 |
