---
description: 除了相對於層0調整大小(size=)和定位(pos=)圖層，並使用layer=命令指定合成順序（z階）外，還可以旋轉(rotate=)和翻轉(flip=)圖層。
solution: Experience Manager
title: 層操作
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# 層操作{#layer-operations}

除了相對於層0調整大小(size=)和定位(pos=)圖層，並使用layer=命令指定合成順序（z階）外，還可以旋轉(rotate=)和翻轉(flip=)圖層。

的 `origin=` 和 `anchor=` 當在模板中動態地更改影像或文本時，可以使用屬性來保持圖層之間所需的對齊。

的 `maskUse=` 命令可用於影像圖層訪問具有獨立蒙版的影像的背景區域。

`opac=` 可用於改變圖層不透明度， `hide=` 顯示或隱藏圖層。
