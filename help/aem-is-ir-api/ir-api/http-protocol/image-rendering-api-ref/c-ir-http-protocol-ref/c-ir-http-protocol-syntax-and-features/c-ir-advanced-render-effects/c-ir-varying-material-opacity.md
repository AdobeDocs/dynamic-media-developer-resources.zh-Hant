---
title: 變化的材料不透明度
description: 對於應用於重疊對象的實色和可重複紋理以及貼花和窗口覆蓋材料，支援可變不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 變化的材料不透明度{#varying-material-opacity}

對於應用於重疊對象的實色和可重複紋理以及貼花和窗口覆蓋材料，支援可變不透明度。

通過使用具有α通道的RGB影像，可以簡單地提供不透明度資訊。 此外，整體不透明度可隨 `opacity=` 命令(同時用於RGB和RGBA影像)。

牆邊還支援RGBA影像，主要用於支援模切邊界。

的 [!DNL vnw] 定義窗口覆蓋的檔案可以包括不透明度通道。 它由呈現器與可重複紋理的Alpha通道和 `opacity=` 為透明和半透明窗口處理提供全方位的不透明效果。
