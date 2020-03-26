---
description: 可變的不透明度支援套用至重疊物件的純色和可重複的紋理，以及貼花和視窗覆蓋材質。
seo-description: 可變的不透明度支援套用至重疊物件的純色和可重複的紋理，以及貼花和視窗覆蓋材質。
seo-title: 變化材質不透明度
solution: Experience Manager
title: 變化材質不透明度
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 變化材質不透明度{#varying-material-opacity}

可變的不透明度支援套用至重疊物件的純色和可重複的紋理，以及貼花和視窗覆蓋材質。

只需使用具有Alpha色版的RGB影像，就可提供不透明度資訊。 此外，您還可以使用命令(RGB和RGBA `opacity=` 影像)來改變整體不透明度。

牆邊界也支援RGBA影像，主要支援模切邊界。

定義 [!DNL vnw]`opacity=` 窗口覆蓋的檔案可以包括不透明度通道，該不透明度通道由渲染器與可重複紋理的α通道和值組合，以提供用於透明和半透明窗口處理的全範圍不透明度效果。
