---
description: 大部分的材質都可動態上色。
seo-description: 大部分的材質都可動態上色。
seo-title: 著色材料
solution: Experience Manager
title: 著色材料
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 著色材料{#colorizing-materials}

大部分的材質都可動態上色。

顏色化算法簡單，對色調範圍有限的材質影像效果最好。 為了著色材料，渲染器只需減去`bgc=`值，然後將`color=`值添加到每個像素值。

如果未指定`color=`，則禁用著色。 `bgc=` 被櫥櫃材料所忽視；而是使用內嵌在檔案中 [!DNL vnc] 的基本顏色值。
