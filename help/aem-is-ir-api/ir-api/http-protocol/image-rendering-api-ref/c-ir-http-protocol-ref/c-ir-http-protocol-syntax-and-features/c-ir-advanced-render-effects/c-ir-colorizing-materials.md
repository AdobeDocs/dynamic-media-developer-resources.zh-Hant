---
title: 著色材料
description: 大多數材料都可以動態著色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 著色材料{#colorizing-materials}

大多數材料都可以動態著色。

該算法簡單，對色彩範圍有限的材料影像效果最好。 要著色材料，渲染器只需將 `bgc=` 值並添加 `color=` 值。

如果 `color=` 未指定。 的 `bgc=` 屬性被機櫃材料忽略；嵌入到 [!DNL vnc] 檔案。
