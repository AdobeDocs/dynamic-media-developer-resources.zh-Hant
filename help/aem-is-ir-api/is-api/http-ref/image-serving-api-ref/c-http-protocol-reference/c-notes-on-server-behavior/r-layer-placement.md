---
title: 圖層放置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 圖層放置{#layer-placement}

通過將層原點(origin=)與背景層原點對準在由pos=指定的偏移處來定位層。

如果未為影像層顯式指定圖層原點，則計算如下：

1. 確定影像錨點。 使用`anchor=`，或者，如果未指定，則使用`catalog::Anchor`。
1. 如果已定義影像錨點，請應用圖層轉換，然後`extend=`將其轉換為origin=值。
1. 如果未定義影像錨點，則圖層原點將放置在圖層矩形的中心（在應用`extend=`之後）。

![圖層放置影像](assets/layerplacement.png)
