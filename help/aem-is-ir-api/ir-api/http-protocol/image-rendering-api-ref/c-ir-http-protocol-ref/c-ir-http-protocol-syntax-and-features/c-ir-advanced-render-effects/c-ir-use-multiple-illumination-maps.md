---
description: 某些應用可能需要對不同種類的材料使用不同的照明圖。
seo-description: 某些應用可能需要對不同種類的材料使用不同的照明圖。
seo-title: 使用多個照明地圖
solution: Experience Manager
title: 使用多個照明地圖
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用多個照明地圖{#using-multiple-illumination-maps}

某些應用可能需要對不同種類的材料使用不同的照明圖。

每個暈映最多可編寫三張照明地圖。 使用和或命令選擇用於渲染操作的 `illum=` 照明 `gloss=` 圖。

**預設選擇** ：如果未指 `illum=` 定 `gloss=` 或未指定，轉譯器將使用第一個編寫的照明地圖（通常為映射A，也稱為「平面」照明地圖）。

**自動選擇`gloss=`**：如果未`illum=`指定或設為-1，渲染器會將指定值與暈映中每個照明映射相關聯的光澤值進行比較，並選擇其光澤值最接近指定的照明映射`gloss=``gloss=`。

**如果指定`illum=`**明`illum=`確選擇，並設定為0、1或2，則渲染器將使用相應的照明圖；會`gloss=`忽略，以選取照明地圖。

如果暈映只包含一個照明映射，則渲染器將使用該映射並忽略 `illum=` 和命 `gloss=` 令。
