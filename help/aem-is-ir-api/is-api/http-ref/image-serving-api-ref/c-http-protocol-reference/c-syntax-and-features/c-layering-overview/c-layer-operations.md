---
description: 除了相對於圖層0調整大小(size=)和定位(pos=)圖層，並使用layer=指令指定合成順序（z順序）之外，圖層還可以旋轉(rotate=)和翻轉(flip=)。
solution: Experience Manager
title: 圖層作業
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
TQID: 'https://experienceleague.adobe.com/uuGkOMzbkysv9BpR8zEK6dkuKgnseu3qwqLslA5W6zw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# 圖層作業{#layer-operations}

除了相對於圖層0調整大小(size=)和定位(pos=)圖層，並使用layer=指令指定合成順序（z順序）之外，圖層還可以旋轉(rotate=)和翻轉(flip=)。

當範本中的影像或文字動態變更時，`origin=`和`anchor=`屬性可用來維持圖層間所需的對齊方式。

`maskUse=`指令可供影像圖層存取具有個別遮色片之影像的背景區域。

`opac=`可用來改變圖層不透明度，`hide=`可用來顯示或隱藏圖層。
