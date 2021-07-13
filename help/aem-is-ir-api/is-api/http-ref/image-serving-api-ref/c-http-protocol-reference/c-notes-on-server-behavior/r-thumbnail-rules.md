---
description: 請注意這些縮圖規則。
solution: Experience Manager
title: 縮圖規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 縮圖規則{#thumbnail-rules}

請注意這些縮圖規則。

1. 如果`catalog::ThumbType=Crop`，則（已裁切的）影像會縮放至盡可能小的大小，同時仍覆蓋整個目標。 如果`catalog::ThumbType=Fit`，則（已裁切的）影像會縮放至最大的大小，同時仍將整個影像擬合到目標正中。 如果`catalog::ThumbType=Texture`，（已裁切的）影像會縮放至`catalog::ThumbRes`與`catalog::Resolution`的比例。
1. 根據`attribute::ThumbHorizAlign`和`attribute::ThumbVertAlign`將縮放影像與目標直接對齊。
1. 將結果裁切至目標。
