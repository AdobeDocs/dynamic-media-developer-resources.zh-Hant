---
description: 此版本- Image Serving 6.6.1和Image Rendering 6.6.1 —— 取代Image Serving 6.5.3和Image Rendering 6.5.3。
seo-description: 此版本- Image Serving 6.6.1和Image Rendering 6.6.1 —— 取代Image Serving 6.5.3和Image Rendering 6.5.3。
seo-title: 關於此版本
solution: Experience Manager
title: 關於此版本
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# 關於此版本{#about-this-release}

此版本- Image Serving 6.6.1和Image Rendering 6.6.1 —— 取代Image Serving 6.5.3和Image Rendering 6.5.3。

## 已知問題和行為改變{#section-9dbc05206187477f926a78e8108a34e1}

* 不再支援在資產ID中使用問號字元，即使該字元是URL編碼亦然。
* 不再支援動態橫幅`/xfl/flash/`要求，現在會傳回http 404錯誤碼。
* 不再支援W2P `/is/agm/`要求。
* 有些錯誤訊息不再呈現給瀏覽器。 因此，您需要查看跟蹤日誌以進行調試。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智慧色票
* 智慧裁切

## 錯誤修正{#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修正`\qc` RTF選項後面加上空格導致請求無法呈現的問題。

