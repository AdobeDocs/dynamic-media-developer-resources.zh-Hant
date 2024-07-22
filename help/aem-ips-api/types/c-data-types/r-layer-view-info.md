---
description: 圖層檢視屬性。
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

圖層檢視屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| url | `xsd:string` | 代表範本的影像伺服器URL。 結合`urlModifier`和`urlPostAp- plyModifier`欄位。 |
| urlModifier | `xsd:string` | 要在要求或`urlPostApplyModifier`命令之前套用的影像伺服通訊協定命令。 |
| urlPostApplyModifier | `xsd:string` | 要在`urlModifier`之後套用的影像伺服通訊協定命令和要求命令。 |
