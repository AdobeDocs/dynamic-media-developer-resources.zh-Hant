---
title: 使用多個照明地圖
description: 某些應用可能需要對不同種類的材料製作不同的照明圖。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 使用多個照明地圖{#using-multiple-illumination-maps}

某些應用可能需要對不同種類的材料製作不同的照明圖。

可為每個視頻創作多達三個照明圖。 使用 `illum=` 和 `gloss=` 的雙曲餘切值。

**預設選擇**  — 如果 `illum=` 或 `gloss=` 未指定，呈現器使用第一創作的照明圖（通常映射A，又稱「平面」照明圖）。

**自動選擇`gloss=`**  — 如果 `illum=` 未指定或設定為 `-1`，呈現器比較指定的 `gloss=` 值與與視頻中的每個照明映射關聯的光澤值。 它選擇光澤值最接近指定值的照明圖 `gloss=`。

**顯式選擇`illum=`**  — 如果 `illum=` 已指定並設定為 `0`。 `1`或 `2`，渲染器使用相應的光照圖； `gloss=` 將忽略，以選擇照明映射。

如果視頻僅包含一個照明映射，則呈現器使用該映射並忽略 `illum=` 和 `gloss=` 的雙曲餘切值。
