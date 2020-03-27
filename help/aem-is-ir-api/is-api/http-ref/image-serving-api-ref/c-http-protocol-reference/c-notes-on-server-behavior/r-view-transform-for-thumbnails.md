---
description: 響應於req=tmb請求而返回給客戶端的映像是從複合映像派生的，方法是考慮以下值wid=、hei=、屬性DefaultThumbPix和屬性MaxPix。
seo-description: 響應於req=tmb請求而返回給客戶端的映像是從複合映像派生的，方法是考慮以下值wid=、hei=、屬性DefaultThumbPix和屬性MaxPix。
seo-title: 縮圖檢視變形
solution: Experience Manager
title: 縮圖檢視變形
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# 縮圖檢視變形{#view-transform-for-thumbnails}

響應於req=tmb請求而返回給客戶端的影像是通過考慮以下值從複合影像派生的：wid=, hei=, attribute::DefaultThumbPix和attribute::MaxPix。

1. **計算視圖rect** —— 使 `wid=` 用或寬度值 `attribute::DefaultThumbPix` 作為視圖rect的寬度。 使 `hei=` 用或高度 `attribute::DefaultThumbPix` 值。 必須在此步驟中完全指定視圖直接。 (請注意，如果沒有為層0指定，則視圖rect將與層0 `size=`rect相同)。
1. **縮放合成圖** -如果 `catalog::ThumbType=Crop`，則合成圖會縮放至最小的影像，同時仍能正確填滿整個視圖；會裁切額外的影像資料。 如 `catalog::ThumbType= Fit`果，則複合圖會縮放到盡可能大的影像，同時仍將整個複合圖擬合到視圖中。 如 `catalog::ThumbType=Texture`果，合成不會縮放以保留中指定的解析度 `catalog::ThumbRes`。
1. **填滿和裁切** -檢視直接填入顏 `bgc=` 色(若未指定，則填入 `attribute::ThumbBkgColor`)。 縮放的複合圖使用屬性與視圖直接對齊： `ThumbHorizAlign` 和屬性： `ThumbVertAlign`。 然後，縮放的複合圖與填充視圖直接合併，而不需進一步縮放。 超出視圖的任何複合區域都會被裁切掉。

