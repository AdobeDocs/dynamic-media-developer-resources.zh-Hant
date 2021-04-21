---
description: 響應於req=tmb請求而返回給客戶端的映像是從複合映像派生的，方法是考慮以下值wid=、hei=、屬性DefaultThumbPix和屬性MaxPix。
solution: Experience Manager
title: 縮圖檢視變形
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# 檢視縮圖變形{#view-transform-for-thumbnails}

響應於req=tmb請求而返回給客戶端的影像是通過考慮以下值從複合影像派生的：wid=, hei=, attribute::DefaultThumbPix和attribute::MaxPix。

1. **計算視圖直接** -使 `wid=` 用或寬度值 `attribute::DefaultThumbPix` 作為視圖直接寬度。使用`hei=`或`attribute::DefaultThumbPix`的高度值作為高度。 必須在此步驟中完全指定視圖直接。 （請注意，如果沒有為層0指定`size=`，則視圖rect將與層0 rect相同）。
1. **縮放合成圖** -如果 `catalog::ThumbType=Crop`，則合成圖會縮放到盡可能小的影像上，同時仍然填滿整個視圖；會裁切額外的影像資料。如果`catalog::ThumbType= Fit`，則複合圖會縮放到最大的影像，同時仍將整個複合圖配合到視圖中。 如果`catalog::ThumbType=Texture`，則合成不會縮放以保留`catalog::ThumbRes`中指定的解析度。
1. **填充和裁切** -視圖直接填充 `bgc=` 顏色(或（如果未指定） `attribute::ThumbBkgColor`。縮放的複合圖使用屬性與視圖直接對齊：`ThumbHorizAlign`和屬性：`ThumbVertAlign`。 然後，縮放的複合圖與填充視圖直接合併，而不需進一步縮放。 超出視圖的任何複合區域都會被裁切掉。

