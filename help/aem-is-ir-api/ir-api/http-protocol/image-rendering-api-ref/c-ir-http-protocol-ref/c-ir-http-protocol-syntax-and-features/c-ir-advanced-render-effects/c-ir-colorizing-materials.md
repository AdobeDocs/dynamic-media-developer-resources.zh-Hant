---
description: 大部分材料都可動態上色。
solution: Experience Manager
title: 著色材料
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# 著色材料{#colorizing-materials}

大部分材料都可動態上色。

顏色化算法簡單，對色調範圍有限的材質影像效果最好。 為了著色材料，渲染器只需減去`bgc=`值，然後將`color=`值添加到每個像素值。

如果未指定`color=`，則禁用著色。 `bgc=` 被櫥櫃材料所忽視；而是使用內嵌在檔案中 [!DNL vnc] 的基本顏色值。
