---
description: 大部分材料都可以動態著色。
solution: Experience Manager
title: 著色材料
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 著色材料{#colorizing-materials}

大部分材料都可以動態著色。

著色算法簡單，對色調範圍有限的材料影像效果最好。 為了著色材料，渲染器只需減去`bgc=`值並將`color=`值添加到每個像素值。

如果未指定`color=`，則禁用著色。 `bgc=` 被櫥櫃材料所忽略；會改用檔案中內嵌的 [!DNL vnc] 基色值。
