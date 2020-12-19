---
description: 除了相對於圖層0調整(size=)和定位(pos=)圖層，並使用layer=命令指定複合順序（z階）外，圖層還可以旋轉(rotate=)和翻轉(flip=)。
seo-description: 除了相對於圖層0調整(size=)和定位(pos=)圖層，並使用layer=命令指定複合順序（z階）外，圖層還可以旋轉(rotate=)和翻轉(flip=)。
seo-title: 圖層操作
solution: Experience Manager
title: 圖層操作
topic: Scene7 Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 層操作{#layer-operations}

除了相對於圖層0調整(size=)和定位(pos=)圖層，並使用layer=命令指定複合順序（z階）外，圖層還可以旋轉(rotate=)和翻轉(flip=)。

當在範本中動態變更影像或文字時，`origin=`和`anchor=`屬性可用來維持圖層之間的所需對齊方式。

`maskUse=`命令可用於影像圖層訪問具有獨立遮色片的影像的背景區域。

`opac=` 可用來變更圖層的不透明度，以 `hide=` 及顯示或隱藏圖層。
