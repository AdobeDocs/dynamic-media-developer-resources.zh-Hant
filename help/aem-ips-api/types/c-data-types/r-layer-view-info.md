---
description: 圖層視圖屬性。
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 11%

---

# LayerViewInfo{#layerviewinfo}

圖層視圖屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`url`*` | `xsd:string` | 代表範本的影像伺服器URL。 結合`urlModifier`和`urlPostAp- plyModifier`欄位。 |
| `*`urlModifier`*` | `xsd:string` | 在請求或`urlPostApplyModifier`命令之前應用的影像伺服協定命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 要在`urlModifier`和請求命令後應用的影像伺服協定命令。 |
