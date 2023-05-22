---
description: 此版本(影像服6.6.1和影像渲染)6.6.1取代影像服6.5.3和影像渲染6.5.3。
solution: Experience Manager
title: 關於此版本
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---

# 關於此版本{#about-this-release}

此版本(影像服6.6.1和影像渲染)6.6.1取代影像服6.5.3和影像渲染6.5.3。

## 已知問題和行為更改 {#section-9dbc05206187477f926a78e8108a34e1}

* 不再支援在資產ID中使用問號字元，即使該字元是URL編碼的。
* 動態橫幅 `/xfl/flash/` 不再支援請求，現在返回http 404錯誤代碼。
* W2P `/is/agm/` 不再支援請求。
* 某些錯誤消息不再呈現給瀏覽器。 因此，您需要查看要調試的跟蹤日誌。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智慧色板
* 智慧裁剪

## 錯誤修復 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 已修復問題 `\qc` RTF選項後跟空格導致請求未呈現。
