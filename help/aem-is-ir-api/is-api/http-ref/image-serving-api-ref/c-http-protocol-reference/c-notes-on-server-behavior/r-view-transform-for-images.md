---
description: 查看影像的轉換
solution: Experience Manager
title: 查看影像的轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 查看影像的轉換{#view-transform-for-images}

響應於 `req=img` 請求是通過考慮以下值從複合影像派生的： `wid=`。 `hei=`。 `fit=`。 `scl=`。 `rgn=`。 `attribute::DefaultPix`。 `attribute::MaxPix`，以及複合影像的大小。

如果 `wid=` 和 `hei=` 已指定 `scl=` 不是，將複合影像縮放，使其完全適合由定義的視圖 `wid=` 和 `hei=`。 如果視圖矩形的長寬比與複合影像的長寬比不同，則使用 `align=` 值（如果指定），或者它居中。 未被影像資料覆蓋的任何空間都會被填充 `bgc=` 或，如果未指定，使用 `attribute::BkgColor`。

如果 `scl=` 指定，複合影像由該比例因子縮放。 如果 `wid=` 和/或 `hei=` 同時指定，縮放影像隨後被裁切到 `wid=` 和/或 `hei=` 或根據需要增加額外空間。 `align=` 指定影像的裁剪位置或添加額外空間的位置，並使用 `bgc=` 或 `attribute::BkgColor`。

如果兩者都不 `wid=`。 `hei=` 無 `scl=` 指定，並且如果複合影像的寬度或高度超過 `attribute::DefaultPix`，然後將合成影像縮放為不超過 `attribute::DefaultPix`。 否則，不使用縮放來使用合成影像。

要確保在不進行任何進一步縮放的情況下返回視圖影像，請指定 `scl=1`。

如果 `rgn=` 然後相應地裁切回復影像以達到最終回復影像大小。 此大小與 `attribute::MaxPix` （如果已定義），並且如果回復影像在任一維中較大，則會生成錯誤。

如果 `fmt=` 指定沒有Alpha的資料，回復影像中的任何透明區域都填充有 `bgc=` 或 `attribute::BkgColor`。
