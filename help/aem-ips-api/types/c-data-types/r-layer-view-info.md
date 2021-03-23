---
description: 圖層檢視屬性。
seo-description: 圖層檢視屬性。
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 10%

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

