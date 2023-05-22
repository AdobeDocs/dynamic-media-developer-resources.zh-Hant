---
description: 請注意這些縮略圖規則。
solution: Experience Manager
title: 縮略圖規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# 縮略圖規則{#thumbnail-rules}

請注意這些縮略圖規則。

1. 如果 `catalog::ThumbType=Crop`，然後將（裁剪）影像縮放到盡可能小的大小，同時仍覆蓋整個目標矩。 如果 `catalog::ThumbType=Fit`，然後將（裁剪的）影像縮放到盡可能大的大小，同時仍將整個影像擬合到目標矩形中。 如果 `catalog::ThumbType=Texture`，將（裁剪）影像縮放為 `catalog::ThumbRes` 至 `catalog::Resolution`。
1. 根據 `attribute::ThumbHorizAlign` 和 `attribute::ThumbVertAlign`。
1. 將結果裁剪到目標目錄。
