---
description: 除了相對於圖層0調整大小(size=)和定位(pos=)圖層，並使用layer=指令指定合成順序（z順序）之外，圖層還可以旋轉(rotate=)和翻轉(flip=)。
solution: Experience Manager
title: 圖層作業
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 圖層作業{#layer-operations}

除了相對於圖層0調整大小(size=)和定位(pos=)圖層，並使用layer=指令指定合成順序（z順序）之外，圖層還可以旋轉(rotate=)和翻轉(flip=)。

當範本中的影像或文字動態變更時，`origin=`和`anchor=`屬性可用來維持圖層間所需的對齊方式。

`maskUse=`指令可供影像圖層存取具有個別遮色片之影像的背景區域。

`opac=`可用來改變圖層不透明度，`hide=`可用來顯示或隱藏圖層。
