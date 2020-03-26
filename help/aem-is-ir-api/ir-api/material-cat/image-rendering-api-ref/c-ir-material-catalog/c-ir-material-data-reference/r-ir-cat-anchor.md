---
description: 影像錨點。 指定可重複紋理、壁邊框或貼圖影像的錨點（熱點）。
seo-description: 影像錨點。 指定可重複紋理、壁邊框或貼圖影像的錨點（熱點）。
seo-title: 錨點
solution: Experience Manager
title: 錨點
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 錨點{#anchor}

影像錨點。 指定可重複紋理、壁邊框或貼圖影像的錨點（熱點）。

可重複紋理被應用到暈映對象，以使紋理錨點位於對象的紋理原點。 貼花影像被應用到暈映對象，使得貼花錨點位於對象的貼花原點。 對於牆邊界，只使用x值；將忽略y值。

## 屬性 {#section-bc4bc8b897c64535b88681e57d72942f}

兩個整數，以逗號分隔。 相對於影像的左上角像素偏移。 如果和由 `catalog::Alignment=3` 純色和機櫃材料忽略。

## 預設 {#section-b7ccc419a356415294706cd295ae96c9}

如果場為空或不存在，則使用用於可重複紋理材料的影像的左上角(0,0)，或在傾斜材料的情況下使用影像的中心。

## 另請參閱 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[目錄：：對齊](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [錨點=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
