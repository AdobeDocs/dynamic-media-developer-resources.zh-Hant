---
description: 某些應用可能要求對不同種類的材料進行不同的照明圖。
solution: Experience Manager
title: 使用多個照明圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 使用多個照明圖{#using-multiple-illumination-maps}

某些應用可能要求對不同種類的材料進行不同的照明圖。

每個暈映最多可製作三張照明圖。 使用`illum=`和`gloss=`命令選擇渲染操作的照明映射。

**預** 設選 `illum=` 擇如 `gloss=` 果未指定或，則渲染器將使用第一個創作的照明圖（通常映射A，稱為「平整」照明圖）。

**自動選`gloss=`** 擇如 `illum=` 果未指定或設定為–1，則渲染器將指定值與與暈 `gloss=` 鏡中每個照明映射關聯的光澤值進行比較，並選擇其光澤值最接近指定的照明映 `gloss=`射。

**顯式選`illum=`** 擇如 `illum=` 果指定並設定為0、1或2，則渲染器將使用相應的照明圖； `gloss=` 會忽略，以便選取照明圖。

如果暈映僅包含一個照明映射，則渲染器將使用該映射並忽略`illum=`和`gloss=`命令。
