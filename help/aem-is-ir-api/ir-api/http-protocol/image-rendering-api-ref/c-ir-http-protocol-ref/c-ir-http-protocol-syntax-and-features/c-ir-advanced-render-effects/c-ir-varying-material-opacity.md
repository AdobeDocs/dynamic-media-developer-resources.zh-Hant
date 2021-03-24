---
description: 可變的不透明度支援套用至重疊物件的純色和可重複的紋理，以及貼花和視窗覆蓋材質。
solution: Experience Manager
title: 變化材質不透明度
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# 變化的材料不透明度{#varying-material-opacity}

可變的不透明度支援套用至重疊物件的純色和可重複的紋理，以及貼花和視窗覆蓋材質。

只需使用具有Alpha色版的RGB影像，就可提供不透明度資訊。 此外，您還可以使用`opacity=`命令（針對RGB和RGBA影像）來改變整體的不透明度。

牆邊界也支援RGBA影像，主要支援模切邊界。

定義窗口覆蓋的[!DNL vnw]檔案可以包括不透明通道，該不透明通道由渲染器與可重複紋理的alpha通道和`opacity=`值組合，以提供用於透明和半透明窗口處理的完整不透明效果範圍。
