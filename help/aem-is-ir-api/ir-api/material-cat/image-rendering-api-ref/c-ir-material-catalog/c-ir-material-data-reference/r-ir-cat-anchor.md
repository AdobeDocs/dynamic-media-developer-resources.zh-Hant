---
description: 影像錨點。 指定可重複紋理、壁邊框或貼花影像的錨點（熱點）。
solution: Experience Manager
title: 錨點
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# 錨點{#anchor}

影像錨點。 指定可重複紋理、壁邊框或貼花影像的錨點（熱點）。

可重複紋理被應用到視頻對象，使得紋理錨點位於對象的紋理原點處。 貼花影像被應用於貼花對象，使得貼花錨點位於對象貼花原點處。 對於牆邊框，僅使用x值；忽略y值。

## 屬性 {#section-bc4bc8b897c64535b88681e57d72942f}

兩個整數，用逗號分隔。 像素相對於影像的左上角偏移。 如果忽略 `catalog::Alignment=3` 以及純色和櫥櫃材料。

## 預設 {#section-b7ccc419a356415294706cd295ae96c9}

如果該欄位為空或不存在，則使用可重複紋理材料的影像的左上角(0,0)，或在貼花材料的情況下使用影像的中心。

## 另請參閱 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[目錄：：對齊](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) 。 [錨=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
