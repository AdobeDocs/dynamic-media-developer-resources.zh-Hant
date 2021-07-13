---
description: 除了相對於層0調整(size=)和定位(pos=)層以及使用layer=命令指定複合順序（z階）外，層還可以旋轉(rotate=)和翻轉(flip=)。
solution: Experience Manager
title: 層操作
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# 層操作{#layer-operations}

除了相對於層0調整(size=)和定位(pos=)層以及使用layer=命令指定複合順序（z階）外，層還可以旋轉(rotate=)和翻轉(flip=)。

當在模板中動態地更改影像或文本時，`origin=`和`anchor=`屬性可用於保持圖層之間的所需對齊方式。

`maskUse=`命令可用於影像層訪問具有獨立遮罩的影像的背景區域。

`opac=` 可用於更改圖層不透明度，以 `hide=` 及顯示或隱藏圖層。
