---
description: 回應req=tmb要求傳回給使用者端的影像，會考量下列值wid=、hei=、屬性DefaultThumbPix及屬性MaxPix，而衍生自複合影像。
solution: Experience Manager
title: 縮圖的檢視轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# 縮圖的檢視轉換{#view-transform-for-thumbnails}

回應req=tmb要求傳回給使用者端的影像是透過考量下列值從複合影像衍生： wid=、hei=、attribute：：DefaultThumbPix和attribute：：MaxPix。

1. **計算檢視矩形** — 使用`wid=`或寬度值`attribute::DefaultThumbPix`作為檢視矩形。 高度請使用`hei=`或`attribute::DefaultThumbPix`的高度值。 必須在此步驟中完整指定檢視矩形。 （請注意，如果沒有為圖層0指定`size=`，則檢視矩形與圖層0矩形相同）。
1. **縮放複合** — 如果是`catalog::ThumbType=Crop`，則複合會縮放到儘可能最小的影像，同時仍填滿整個檢視矩形；會裁剪額外的影像資料。 如果`catalog::ThumbType= Fit`，則複合影像會縮放至最大影像，同時仍會將整個複合影像調整至檢視矩形。 如果`catalog::ThumbType=Texture`，則複合完全不會縮放以保留`catalog::ThumbRes`中指定的解析度。
1. **填滿和裁切** — 檢視矩形以`bgc=`顏色填滿（如果未指定，則以`attribute::ThumbBkgColor`填滿）。 使用屬性： `ThumbHorizAlign`和屬性： `ThumbVertAlign`，縮放的複合與檢視重新對齊。 縮放後的複合隨即與填色檢視矩形合併，而不需進一步縮放。 超出檢視矩形的複合區域會被裁切。
