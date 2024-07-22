---
description: 瀏覽器中點選動作的目標。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

瀏覽器中點選動作的目標。

永遠與影像相關聯。 您可以從`ImageInfo`取得`ImageMap`目標。

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 影像地圖控制代碼。 |
| [!DNL name] | `xsd:string` | 影像地圖名稱。 |
| [!DNL region] | `xsd:string` | 影像地圖座標。 格式是以`<area>`標籤屬性HTML為基礎。 |
| [!DNL action] | `xsd:string` | 要包含在HTML`<area>`標籤中的其他屬性，包括`href` URL。 |
| shapetype | `xsd:boolean` | [!DNL RegionShape]值。 |
| [!DNL position] | `xsd:string` | 以HTML`<area>`專案的[!DNL coords]屬性格式放置位置。 例如： `coords ="0,0,84,128"`。 |
| [!DNL enabled] | `xsd:boolean` | 如果啟用影像地圖，則為True。 |
| lastModified | `xsd:dateTime` | 上次修改影像地圖的日期和時間。 |
