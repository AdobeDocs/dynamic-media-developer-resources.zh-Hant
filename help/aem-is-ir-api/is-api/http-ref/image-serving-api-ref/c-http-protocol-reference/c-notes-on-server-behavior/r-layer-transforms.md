---
description: 變形會套用至原始影像和文字圖層。
seo-description: 變形會套用至原始影像和文字圖層。
seo-title: 圖層轉換
solution: Experience Manager
title: 圖層轉換
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 層變換{#layer-transforms}

變形會套用至原始影像和文字圖層。

以下操作按給定順序應用於源影像，以實現與圖層0的所需空間關係：

1. 如果已指定，則應用`crop=`。
1. 根據`size=`或，如果未指定`size=`，則根據`scale=`，或者，如果未指定`scale=`，則根據`res=`，或者，如果未指定`res=`，則使用完整解析度來源影像。
1. 如果已指定，則應用`flip=`。
1. 如果已指定，則應用`rotate=`。
1. 如果已指定，則應用`extend=`。
1. 根據`origin=`和`pos=`將圖層定位在畫布中（請參閱下面）。

下列變形會套用至文字圖層：

1. 文本框大小由`size=`決定，或文本寬度和高度（如果`size=`僅提供部分或完全不提供）決定。 文本使用RTF文本對齊屬性在文本框中對齊。 文字可能會被文字方塊裁切。
1. 根據以`textAttr=`指定的解析度縮放文字內容。
1. 如果已指定，則應用`rotate=`。
1. 如果已指定，則應用`extend=`。
1. 根據`origin=`和`pos=`將圖層定位在畫布中（請參閱下面）。

對於影像和文字圖層，畫布中的圖層最後一個步驟定位不適用於圖層0，因為圖層0有效地構成畫布。
