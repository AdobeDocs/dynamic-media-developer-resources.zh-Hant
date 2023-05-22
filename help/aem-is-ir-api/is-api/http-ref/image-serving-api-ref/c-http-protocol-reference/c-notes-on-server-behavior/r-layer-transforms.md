---
description: 轉換應用於源影像和文本圖層。
solution: Experience Manager
title: 圖層轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# 圖層轉換{#layer-transforms}

轉換應用於源影像和文本圖層。

以下操作按給定順序應用於源影像，以實現與層0的所需空間關係：

1. 應用 `crop=`，如果已指定。
1. 基於 `size=` 或 `size=` 未指定，基於 `scale=`，或 `scale=` 未指定，基於 `res=`，或 `res=`未指定，請使用全解析度源影像。
1. 應用 `flip=`，如果已指定。
1. 應用 `rotate=`，如果已指定。
1. 應用 `extend=`，如果已指定。
1. 根據 `origin=` 和 `pos=` （見下文）。

以下轉換應用於文本圖層：

1. 文本框大小由 `size=`，或文本寬度和高度，如果 `size=` 只提供部分或完全不提供。 文本使用rtf文本對齊屬性在文本框內對齊。 文本可以被文本框裁剪。
1. 根據指定的解析度縮放文本內容 `textAttr=`。
1. 應用 `rotate=`，如果已指定。
1. 應用 `extend=`，如果已指定。
1. 根據 `origin=` 和 `pos=`（見下文）。

對於影像和文本圖層，在畫布中對圖層進行最後一步定位並不適用於圖層0，因為圖層0有效地構成了畫布。
