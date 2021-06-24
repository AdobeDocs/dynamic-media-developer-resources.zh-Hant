---
description: 對於應用於重疊對象的實色和可重複的紋理，以及覆蓋材料的標籤和窗口，支援可變的不透明度。
solution: Experience Manager
title: 變化材料不透明度
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 變化材料不透明度{#varying-material-opacity}

對於應用於重疊對象的實色和可重複的紋理，以及覆蓋材料的標籤和窗口，支援可變的不透明度。

通過使用帶有Alpha通道的RGB影像，可以簡單地提供不透明度資訊。 此外，整體不透明度可以使用`opacity=`命令進行改變（RGB和RGBA影像均適用）。

牆邊還支援RGBA影像，主要用於支援模切邊界。

定義窗口覆蓋的[!DNL vnw]檔案可以包括不透明度通道，該不透明度通道由渲染器與可重複紋理的Alpha通道和`opacity=`值組合，以提供用於透明和半透明窗口處理的全方位的不透明度效果。
