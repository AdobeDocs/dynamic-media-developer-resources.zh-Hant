---
description: 響應req=tmb請求返回給客戶端的影像是從複合影像中派生的，方法是考慮以下值wid=、hei=、屬性DefaultThumbPix和屬性MaxPix。
solution: Experience Manager
title: 查看縮略圖的轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 查看縮略圖的轉換{#view-transform-for-thumbnails}

響應req=tmb請求返回給客戶端的影像通過考慮以下值從複合影像中派生：wid=,hei=，屬性：:DefaultThumbPix，屬性：:MaxPix。

1. **計算視圖直接**  — 使用 `wid=` 或寬度值 `attribute::DefaultThumbPix` 的雙曲餘切值。 使用 `hei=` 或高度值 `attribute::DefaultThumbPix` 高度。 必須在此步驟中完全指定視圖rect。 (請注意，視圖直接與層0直接相同，如果沒有 `size=`為0層指定)。
1. **縮放組合**  — 如果 `catalog::ThumbType=Crop`然後，在仍填充整個視圖的同時，將合成影像縮放到盡可能小的影像；會裁剪額外的影像資料。 如果 `catalog::ThumbType= Fit`，然後將複合影像縮放到最大影像，同時仍將整個複合影像擬合到視圖矩形中。 如果 `catalog::ThumbType=Texture`，完全不縮放組合以保留中指定的解析度 `catalog::ThumbRes`。
1. **填充和裁剪**  — 視圖矩形中填充 `bgc=` 顏色(如果未指定，則使用 `attribute::ThumbBkgColor`)。 縮放複合圖使用以下屬性與視圖直接對齊： `ThumbHorizAlign` 和屬性： `ThumbVertAlign`。 然後，縮放的複合體與填充視圖矩形合併，而不再進行縮放。 超出視圖直角的複合的任何區域都會被裁剪掉。
