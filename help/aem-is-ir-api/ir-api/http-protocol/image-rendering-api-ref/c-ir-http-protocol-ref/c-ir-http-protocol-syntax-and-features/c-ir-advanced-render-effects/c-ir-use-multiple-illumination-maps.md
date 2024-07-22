---
title: 使用多個照明地圖
description: 有些應用程式可能需要針對不同材質使用不同的照明地圖。
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

有些應用程式可能需要針對不同材質使用不同的照明地圖。

每個暈映最多可以製作三個照明地圖。 已使用`illum=`和（或）`gloss=`命令選取演算作業的照明地圖。

**預設選取範圍** — 如果未指定`illum=`或`gloss=`，轉譯器會使用第一個編寫的照明地圖（通常是對應A，亦即「平坦」照明地圖）。

**使用`gloss=`**&#x200B;的自動選取 — 如果未指定`illum=`或設為`-1`，轉譯器會比較指定的`gloss=`值與暈映中每個照明對應相關的光澤值。 它選取光澤值最接近指定`gloss=`的照明地圖。

**使用`illum=`**&#x200B;的明確選取 — 若指定`illum=`並設為`0`、`1`或`2`，轉譯器會使用對應的照明對映；選取照明對映時會略過`gloss=`。

如果暈映僅包含一個照明對映，則轉譯器會使用該對映並忽略`illum=`和`gloss=`命令。
