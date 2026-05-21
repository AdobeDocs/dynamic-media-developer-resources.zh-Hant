---
description: 請注意這些縮圖規則。
solution: Experience Manager
title: 縮圖規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# 縮圖規則{#thumbnail-rules}

請注意這些縮圖規則。

1. 如果是`catalog::ThumbType=Crop`，則（裁切的）影像會縮放至可能的最小尺寸，同時仍覆蓋整個目標矩形。 如果是`catalog::ThumbType=Fit`，則（裁切的）影像會縮放到可能的最大尺寸，同時仍然將整個影像配合目標矩形。 如果`catalog::ThumbType=Texture`，（裁切）影像會縮放成比例`catalog::ThumbRes`對`catalog::Resolution`。
1. 根據`attribute::ThumbHorizAlign`和`attribute::ThumbVertAlign`將縮放的影像與目標矩形對齊。
1. 裁切結果至目標矩形。
