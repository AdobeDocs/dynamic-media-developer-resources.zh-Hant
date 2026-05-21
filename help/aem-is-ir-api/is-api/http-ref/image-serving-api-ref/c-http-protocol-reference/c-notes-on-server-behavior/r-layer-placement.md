---
title: 圖層位置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# 圖層位置{#layer-placement}

將圖層原點(origin=)與背景圖層原點對齊於pos=所指定的位移來放置圖層。

如果未明確指定影像圖層的圖層原點，則計算方式如下：

1. 決定影像錨點。 使用`anchor=`，如果未指定，則使用`catalog::Anchor`。
1. 如果已定義影像錨點，請套用圖層轉換和`extend=`以將其轉換為origin=值。
1. 如果未定義影像錨點，圖層原點會放置在圖層矩形的中心（套用`extend=`之後）。

![圖層位置影像](assets/layerplacement.png)
