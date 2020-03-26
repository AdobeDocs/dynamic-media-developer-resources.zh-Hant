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

---


# 圖層轉換{#layer-transforms}

變形會套用至原始影像和文字圖層。

以下操作按給定順序應用於源影像，以實現與圖層0的所需空間關係：

1. 如果 `crop=`已指定，則套用。
1. 如果未指 `size=` 定，則根據或 `size=` ，或者，如果未指定，則根據或，如果未指定，則根據或，如果未指定，則 `scale=``scale=``res=``res=`使用全解析度源影像。
1. 如果 `flip=`已指定，則套用。
1. 如果 `rotate=`已指定，則套用。
1. 如果 `extend=`已指定，則套用。
1. 根據和（請參閱下面）將圖 `origin=` 層放 `pos=` 置在畫布中。

下列變形會套用至文字圖層：

1. 文本框大小由文本寬 `size=`度和高度決定(如果僅提供部 `size=` 分或完全不提供)。 文本使用RTF文本對齊屬性在文本框中對齊。 文字可能會被文字方塊裁切。
1. 根據指定的解析度縮放文字內容 `textAttr=`。
1. 如果 `rotate=`已指定，則套用。
1. 如果 `extend=`已指定，則套用。
1. 根據和(請參閱下 `origin=` 面 `pos=`)在畫布中定點陣圖層。

對於影像和文字圖層，畫布中的圖層最後一個步驟定位不適用於圖層0，因為圖層0有效地構成畫布。
