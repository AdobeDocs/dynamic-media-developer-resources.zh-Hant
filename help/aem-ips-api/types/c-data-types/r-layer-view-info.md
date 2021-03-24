---
description: 圖層檢視屬性。
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

---


# LayerViewInfo{#layerviewinfo}

圖層檢視屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`url`*` | `xsd:string` | 代表範本的影像伺服器URL。 組合`urlModifier`和`urlPostAp- plyModifier`欄位。 |
| `*`urlModifier`*` | `xsd:string` | 在請求或`urlPostApplyModifier`命令之前應用的影像服務協定命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 在`urlModifier`和request命令之後應用的影像服務協定命令。 |

