---
title: 層放置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 層放置{#layer-placement}

通過將圖層原點（原點=）與背景圖層原點對齊在pos=指定的偏移處來定點陣圖層。

如果未顯式指定影像層的圖層原點，則按以下方式計算：

1. 確定影像錨點。 使用 `anchor=`，或，如果未指定， `catalog::Anchor`。
1. 如果定義了影像錨點，則應用圖層轉換並 `extend=` 轉換為origin= value。
1. 如果未定義影像錨點，則圖層原點將放置在圖層矩形的中心（應用後） `extend=`)。

![圖層放置影像](assets/layerplacement.png)
