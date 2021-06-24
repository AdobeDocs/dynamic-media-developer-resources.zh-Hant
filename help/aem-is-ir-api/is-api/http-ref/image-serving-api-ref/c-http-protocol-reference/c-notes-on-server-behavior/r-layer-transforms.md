---
description: 轉換會套用至來源影像和文字層。
solution: Experience Manager
title: 圖層轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 圖層轉換{#layer-transforms}

轉換會套用至來源影像和文字層。

以下操作按給定順序應用於源影像，以實現與第0層的所需空間關係：

1. 如果指定，則應用`crop=`。
1. 根據`size=`或，如果未指定`size=`，則根據`scale=`；如果未指定`scale=`，則根據`res=`，或者，如果未指定`res=`，則使用完全解析度源影像。
1. 如果指定，則應用`flip=`。
1. 如果指定，則應用`rotate=`。
1. 如果指定，則應用`extend=`。
1. 根據`origin=`和`pos=`在畫布中定點陣圖層（請參閱下方）。

下列轉換會套用至文字層：

1. 如果`size=`僅部分提供或完全未提供，則文本框大小由`size=`或文本寬度和高度確定。 文本在文本框內使用rtf文本對齊屬性對齊。 文本框可以裁切文本。
1. 根據使用`textAttr=`指定的解析度縮放文本內容。
1. 如果指定，則應用`rotate=`。
1. 如果指定，則應用`extend=`。
1. 根據`origin=`和`pos=`在畫布中定點陣圖層（請參閱下方）。

對於影像層和文本層，在畫布中定點陣圖層的最後一個步驟不適用於圖層0，因為圖層0有效地構成了畫布。
