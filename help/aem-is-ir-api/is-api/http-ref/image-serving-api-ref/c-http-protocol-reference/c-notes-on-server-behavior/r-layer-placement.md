---
description: 通過將層原點（原點=）與背景層原點對準在pos=指定的偏移處來定位層。
solution: Experience Manager
title: 圖層放置
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# 圖層放置{#layer-placement}

通過將層原點（原點=）與背景層原點對準在pos=指定的偏移處來定位層。

如果未為影像圖層顯式指定圖層原點，則計算如下：

1. 確定影像錨點。 使用`anchor=`，或者，如果未指定，則使用`catalog::Anchor`。
1. 如果已定義影像錨點，請套用圖層變形和`extend=`，將其轉換為原點=值。
1. 如果未定義影像錨點，圖層原點會置於圖層矩形的中心（在套用`extend=`後）。

![](assets/layerplacement.png)

