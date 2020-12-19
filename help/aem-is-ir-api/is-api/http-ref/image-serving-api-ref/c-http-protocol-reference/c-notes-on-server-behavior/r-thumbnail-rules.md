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
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# 縮圖規則{#thumbnail-rules}

請注意這些縮圖規則。

1. 如果`catalog::ThumbType=Crop`，則（裁切的）影像會縮放至最小的大小，同時仍覆蓋整個目標。 如果`catalog::ThumbType=Fit`，則（裁切的）影像會縮放至最大尺寸，同時仍能將整個影像調整為目標方向。 如果`catalog::ThumbType=Texture`,（裁切）影像會縮放為`catalog::ThumbRes`與`catalog::Resolution`的比例。
1. 根據`attribute::ThumbHorizAlign`和`attribute::ThumbVertAlign`，將縮放的影像與目標對齊。
1. 將結果直接裁切至目標。

