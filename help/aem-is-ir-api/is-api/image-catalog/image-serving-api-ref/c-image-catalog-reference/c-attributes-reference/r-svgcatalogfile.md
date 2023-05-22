---
description: SVG資料檔案路徑。 指定包含此目錄的SVG資料的檔案。
solution: Experience Manager
title: Svg目錄檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# Svg目錄檔案{#svgcatalogfile}

SVG資料檔案路徑。 指定包含此目錄的SVG資料的檔案。

SVG資料檔案在所有影像資料檔案之後按指定的準確順序載入。 如果相同 `catalog::Id` 值在多個記錄(在同一或不同映像或SVG目錄檔案中)中出現，最後一個實例佔上風。

## 屬性 {#section-fc2d549f76474792837b2b92ec2087ea}

一個或多個文本字串值，用逗號分隔。 選擇性. 每個值必須是相對於目錄資料夾的絕對檔案路徑或路徑。

## 預設 {#section-a4e58951f3c249599665b823566433c9}

空，表示此影像目錄不包含任何SVG資料。

## 另請參閱 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)。 [目錄檔案](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
