---
description: 響應req=tmb請求返回給客戶端的影像從複合影像派生，方法是考慮以下值wid=、hei=、屬性DefaultThumbPix和屬性MaxPix。
solution: Experience Manager
title: 檢視縮圖的轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 檢視縮圖的轉換{#view-transform-for-thumbnails}

響應請求=tmb請求返回給客戶機的影像通過考慮以下值從複合影像中導出：wid=、hei=、attribute::DefaultThumbPix和attribute::MaxPix。

1. **計算視圖直** 接 — 對 `wid=` 視圖直 `attribute::DefaultThumbPix` 接的寬度使用或寬度值。請使用`hei=`或`attribute::DefaultThumbPix`的高度值來表示高度。 必須在此步驟中完全指定視圖直接。 （請注意，如果沒有為層0指定`size=`，則視圖直接將與層0直接相同。）
1. **縮放複合**  — 如果 `catalog::ThumbType=Crop`，則複合影像會縮放至盡可能小的影像，同時仍直接填滿整個視圖；額外的影像資料會被裁掉。如果`catalog::ThumbType= Fit`，則複合影像將縮放到最大的影像，同時仍將整個複合影像擬合到視圖正中。 如果`catalog::ThumbType=Texture`，則完全不縮放複合體以保留`catalog::ThumbRes`中指定的解析度。
1. **填充和裁切**  — 檢視直接會填入 `bgc=` 顏色(或（若未指定） `attribute::ThumbBkgColor`)。縮放複合材料使用屬性與視圖直接對齊：`ThumbHorizAlign`和屬性：`ThumbVertAlign`。 然後縮放的複合材料將與填充視圖合併，而無需進一步縮放。 超出視圖直接範圍的複合的任何區域都會被裁切。
