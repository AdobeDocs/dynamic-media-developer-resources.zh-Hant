---
description: 轉換會套用至來源影像和文字圖層。
solution: Experience Manager
title: 圖層轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 圖層轉換{#layer-transforms}

轉換會套用至來源影像和文字圖層。

下列作業會依指定順序套用至來源影像，以取得與圖層0的所需空間關係：

1. 套用`crop=` （若已指定）。
1. 以`size=`為基礎進行縮放；如果未指定`size=`，則以`scale=`為基礎；如果未指定`scale=`，則以`res=`為基礎；如果未指定`res=`，則使用完整解析度的來源影像。
1. 套用`flip=` （若已指定）。
1. 套用`rotate=` （若已指定）。
1. 套用`extend=` （若已指定）。
1. 根據`origin=`和`pos=`將圖層放置在畫布中（請參閱下文）。

下列轉換會套用至文字圖層：

1. 如果`size=`僅部分提供或未提供，則文字方塊大小由`size=`或文字寬度和高度決定。 文字會使用rtf文字對齊屬性，在文字方塊內對齊。 文字方塊可能會裁切文字。
1. 根據以`textAttr=`指定的解析度縮放文字內容。
1. 套用`rotate=` （若已指定）。
1. 套用`extend=` （若已指定）。
1. 根據`origin=`和`pos=`將圖層放置在畫布中（請參閱下文）。

對於影像和文字圖層，最後一個步驟在畫布中定點陣圖層不會套用至圖層0，因為圖層0有效地構成畫布。
