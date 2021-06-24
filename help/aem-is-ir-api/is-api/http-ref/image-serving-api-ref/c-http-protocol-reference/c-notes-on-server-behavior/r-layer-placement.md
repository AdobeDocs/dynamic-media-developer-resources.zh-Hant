---
description: 通過將層原點(origin=)與背景層原點對準在由pos=指定的偏移處來定位層。
solution: Experience Manager
title: 圖層放置
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# 圖層放置{#layer-placement}

通過將層原點(origin=)與背景層原點對準在由pos=指定的偏移處來定位層。

如果未為影像層顯式指定圖層原點，則計算如下：

1. 確定影像錨點。 使用`anchor=`，或者，如果未指定，則使用`catalog::Anchor`。
1. 如果已定義影像錨點，請應用圖層轉換，然後`extend=`將其轉換為origin=值。
1. 如果未定義影像錨點，則圖層原點將放置在圖層矩形的中心（在應用`extend=`之後）。

![](assets/layerplacement.png)
