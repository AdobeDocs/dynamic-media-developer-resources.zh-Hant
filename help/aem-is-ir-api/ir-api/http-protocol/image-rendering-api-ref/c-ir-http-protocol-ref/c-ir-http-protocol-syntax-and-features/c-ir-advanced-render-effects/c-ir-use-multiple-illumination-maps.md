---
description: 某些應用可能需要對不同種類的材料使用不同的照明圖。
solution: Experience Manager
title: 使用多個照明地圖
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# 使用多個照明映射{#using-multiple-illumination-maps}

某些應用可能需要對不同種類的材料使用不同的照明圖。

每個暈映最多可編寫三張照明地圖。 使用`illum=`和`gloss=`命令選擇用於渲染操作的照明映射。

**預設** 選擇如 `illum=` 果未 `gloss=` 指定或未指定，轉譯器將使用第一個編寫的照明圖（通常為映射A，也稱為「平面」照明圖）。

**自動選`gloss=`** 擇：如 `illum=` 果未指定或設為-1，渲染器會將指定值與暈映中每個照明映射相關聯的光澤值進行比較，並選擇其光澤值最接近指定的照明映射 `gloss=`  `gloss=`。

**明確選`illum=`** 擇如 `illum=` 果指定為0、1或2，則渲染器將使用對應的照明圖； `gloss=` 會忽略，以便選取照明地圖。

如果暈映只包含一個照明映射，則渲染器將使用該映射並忽略`illum=`和`gloss=`命令。
