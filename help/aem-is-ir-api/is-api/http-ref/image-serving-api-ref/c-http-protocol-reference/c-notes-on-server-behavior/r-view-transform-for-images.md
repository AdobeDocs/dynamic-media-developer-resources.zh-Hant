---
description: 'null'
seo-description: 'null'
seo-title: 影像的檢視變形
solution: Experience Manager
title: 影像的檢視變形
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 影像的檢視變形{#view-transform-for-images}

響應於請求而返回給客戶端的圖 `req=img` 像是通過考慮以下值從複合影像衍生而來： `wid=`、 `hei=`、 `fit=`、 `scl=`、 `rgn=`以 `attribute::DefaultPix``attribute::MaxPix`及合成影像的大小。

如果 `wid=` 指定 `hei=` 並未指定，則複合影像 `scl=` 將進行縮放，以便完全適合和定義的視 `wid=` 圖 `hei=`。 如果視圖直角的長寬比與合成影像的長寬比不同，則使用值（如果已指定）在視圖直角內對齊縮放的合成影像，或者 `align=` 將其置中。 影像資料未涵蓋的任何空間都會填 `bgc=` 入或（若未指定）填入 `attribute::BkgColor`。

如果 `scl=` 已指定，則複合影像將按該比例因子縮放。 如果 `wid=` 也指定和/ `hei=` 或，則縮放的影像接著會被裁切至 `wid=``hei=` 和／或新增額外空間。 `align=` 指定影像被裁切或新增額外空間的位置，並以或填滿任何額外 `bgc=` 空 `attribute::BkgColor`間。

如果未 `wid=`指定 `hei=` 或 `scl=` 未指定，且如果合成影像的寬度或高度超過，則合成影像將縮放為不超過 `attribute::DefaultPix``attribute::DefaultPix`。 否則，合成影像將不進行縮放。

若要確保在不進一步縮放的情況下傳回檢視影像，請指定 `scl=1`。

如果 `rgn=` 已指定，則回覆影像會隨之裁切，以達到最終的回覆影像大小。 此大小會與 `attribute::MaxPix` （如果已定義）比較，如果回覆影像在任一維度中較大，則會產生錯誤。

如果 `fmt=` 指定不含Alpha的資料，則回覆影像中的任何透明區域都會填入 `bgc=` 或 `attribute::BkgColor`。
