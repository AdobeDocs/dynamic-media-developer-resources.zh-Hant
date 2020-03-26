---
description: 此版本- Image Serving 6.6.1和Image Rendering 6.6.1 —— 取代Image Serving 6.5.3和Image Rendering 6.5.3。
seo-description: 此版本- Image Serving 6.6.1和Image Rendering 6.6.1 —— 取代Image Serving 6.5.3和Image Rendering 6.5.3。
seo-title: 關於此版本
solution: Experience Manager
title: 關於此版本
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 關於此版本{#about-this-release}

此版本- Image Serving 6.6.1和Image Rendering 6.6.1 —— 取代Image Serving 6.5.3和Image Rendering 6.5.3。

## 已知問題和行為變更 {#section-9dbc05206187477f926a78e8108a34e1}

* 不再支援在資產ID中使用問號字元，即使該字元是URL編碼亦然。
* 不再支 `/xfl/flash/` 援動態橫幅請求，現在會傳回http 404錯誤碼。
* 不再支 `/is/agm/` 援W2P請求。
* 有些錯誤訊息不再呈現給瀏覽器。 因此，您需要查看跟蹤日誌以進行調試。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智慧色票
* 智慧裁切

## 錯誤修正 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修正RTF選項 `\qc` 後面加上空格時，導致請求無法呈現的問題。

