---
description: 瀏覽器中按一下操作的目標。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 13%

---

# 影像地圖{#imagemap}

瀏覽器中按一下操作的目標。

始終與影像關聯。 你可以 `ImageMap` 目標 `ImageInfo`。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 影像映射句柄。 |
| 名稱 | `xsd:string` | 影像映射名稱。 |
| 區域 | `xsd:string` | 影像地圖坐標。 格式基於HTML `<area>` 標籤屬性。 |
| 操作 | `xsd:string` | 要包括在HTML中的其他屬性 `<area>` 標籤，包括 `href` URL。 |
| 形狀類型 | `xsd:boolean` | A [!DNL RegionShape] 值。 |
| position | `xsd:string` | 以HTML格式定位 `<area>` 元素 [!DNL coords] 屬性。 例如: `coords ="0,0,84,128"`. |
| 啟動 | `xsd:boolean` | 如果啟用了影像映射，則為True。 |
| 上次修改時間 | `xsd:dateTime` | 上次修改影像映射的日期和時間。 |
