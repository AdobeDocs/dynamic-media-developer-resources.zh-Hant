---
description: 影像的檢視變形
solution: Experience Manager
title: 影像的檢視變形
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 檢視影像變形{#view-transform-for-images}

響應`req=img`請求而返回給客戶端的映像是從複合映像派生的，方法是考慮以下值：`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`以及複合影像的大小。

如果指定了`wid=`和`hei=`，而未指定`scl=`，則複合影像會進行縮放，以便完全適合`wid=`和`hei=`定義的視圖。 如果視圖直角的長寬比與合成影像的長寬比不同，則使用`align=`值（如果已指定）在視圖直角內對齊縮放的合成影像，否則會置中。 影像資料未涵蓋的任何空間都會填入`bgc=`，或者，如果未指定，則填入`attribute::BkgColor`。

如果指定`scl=`，則複合影像將按該比例因子縮放。 如果也指定了`wid=`和／或`hei=`，則縮放後的影像會被裁切為`wid=`和／或`hei=`，或視需要加入額外空間。 `align=` 指定影像被裁切或新增額外空間的位置，並以或填入任何額外 `bgc=` 空間 `attribute::BkgColor`。

如果未指定`wid=`、`hei=`或`scl=`，且如果合成影像的寬度或高度超過`attribute::DefaultPix`，則合成影像會縮放為不超過`attribute::DefaultPix`。 否則，合成影像將不進行縮放。

為確保在不進行任何進一步縮放的情況下返回視圖影像，請指定`scl=1`。

如果指定`rgn=`，則回覆影像會隨之裁切，以達到最終的回覆影像大小。 此大小會與`attribute::MaxPix`（如果已定義）比較，如果回覆影像在任一維度中較大，則會產生錯誤。

如果`fmt=`指定沒有alpha的資料，則回覆影像中的任何透明區域都會填入`bgc=`或`attribute::BkgColor`。
