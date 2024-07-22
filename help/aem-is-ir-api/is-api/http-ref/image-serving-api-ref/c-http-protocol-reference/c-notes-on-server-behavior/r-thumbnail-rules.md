---
description: 請注意這些縮圖規則。
solution: Experience Manager
title: 縮圖規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# 縮圖規則{#thumbnail-rules}

請注意這些縮圖規則。

1. 如果是`catalog::ThumbType=Crop`，則（裁切的）影像會縮放至可能的最小尺寸，同時仍覆蓋整個目標矩形。 如果是`catalog::ThumbType=Fit`，則（裁切的）影像會縮放到可能的最大尺寸，同時仍然將整個影像配合目標矩形。 如果`catalog::ThumbType=Texture`，（裁切）影像會縮放成比例`catalog::ThumbRes`對`catalog::Resolution`。
1. 根據`attribute::ThumbHorizAlign`和`attribute::ThumbVertAlign`將縮放的影像與目標矩形對齊。
1. 裁切結果至目標矩形。
