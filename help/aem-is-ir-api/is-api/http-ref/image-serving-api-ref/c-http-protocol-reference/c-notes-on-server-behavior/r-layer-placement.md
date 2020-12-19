---
description: 通過將層原點（原點=）與背景層原點對準在pos=指定的偏移處來定位層。
seo-description: 通過將層原點（原點=）與背景層原點對準在pos=指定的偏移處來定位層。
seo-title: 圖層放置
solution: Experience Manager
title: 圖層放置
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# 圖層放置{#layer-placement}

通過將層原點（原點=）與背景層原點對準在pos=指定的偏移處來定位層。

如果未為影像圖層顯式指定圖層原點，則計算如下：

1. 確定影像錨點。 使用`anchor=`，或者，如果未指定，則使用`catalog::Anchor`。
1. 如果已定義影像錨點，請套用圖層變形和`extend=`，將其轉換為原點=值。
1. 如果未定義影像錨點，圖層原點會置於圖層矩形的中心（在套用`extend=`後）。

![](assets/layerplacement.png)

