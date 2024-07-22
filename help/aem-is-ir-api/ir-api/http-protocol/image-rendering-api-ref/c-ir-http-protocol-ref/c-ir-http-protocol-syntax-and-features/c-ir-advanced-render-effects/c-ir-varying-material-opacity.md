---
title: 不同材質不透明度
description: 實色和套用至重疊物件的可重複紋理，以及貼花和視窗遮蓋材料都支援可變不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 不同材質不透明度{#varying-material-opacity}

實色和套用至重疊物件的可重複紋理，以及貼花和視窗遮蓋材料都支援可變不透明度。

只要使用具有Alpha色版的RGB影像，就可以提供不透明度資訊。 此外，整體不透明度可透過`opacity=`命令改變(針對RGB和RGBA影像)。

壁框線也支援RGBA影像，主要是為了支援壓鑄模裁切的框線。

定義視窗涵蓋範圍的[!DNL vnw]檔案可以包含不透明度通道。 它由轉譯器與可重複紋理的Alpha色版和`opacity=`值結合，以提供各種透明效果，用於透明和半透明視窗處理。
