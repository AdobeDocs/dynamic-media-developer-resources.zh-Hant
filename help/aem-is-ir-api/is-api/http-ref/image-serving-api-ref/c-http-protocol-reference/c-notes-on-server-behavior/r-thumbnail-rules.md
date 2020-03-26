---
description: 請注意這些縮圖規則。
seo-description: 請注意這些縮圖規則。
seo-title: 縮圖規則
solution: Experience Manager
title: 縮圖規則
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 縮圖規則{#thumbnail-rules}

請注意這些縮圖規則。

1. 如 `catalog::ThumbType=Crop`果，則（裁切的）影像會縮放至最小的大小，同時仍會覆蓋整個目標。 如 `catalog::ThumbType=Fit`果，則（裁切的）影像會縮放至最大大小，同時仍能將整個影像調整為目標正確。 如 `catalog::ThumbType=Texture`果，（已裁切）影像會縮放為比 `catalog::ThumbRes` 例 `catalog::Resolution`。
1. 根據和，將縮放的影像與目標對 `attribute::ThumbHorizAlign` 齊 `attribute::ThumbVertAlign`。
1. 將結果直接裁切至目標。

