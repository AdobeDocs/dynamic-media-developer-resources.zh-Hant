---
description: SVG資料檔案路徑。 指定包含此目錄的SVG資料的檔案。
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# SvgCatalogFile{#svgcatalogfile}

SVG資料檔案路徑。 指定包含此目錄的SVG資料的檔案。

SVG資料檔案會在所有影像資料檔案後，依指定的精確順序載入。 如果相同的`catalog::Id`值出現在多個記錄中（位於相同或不同的影像或SVG目錄檔案中），則最後一個例項優先。

## 屬性 {#section-fc2d549f76474792837b2b92ec2087ea}

一或多個文字字串值，以逗號分隔。 選填。每個值都必須是相對於目錄資料夾的絕對檔案路徑或路徑。

## 預設 {#section-a4e58951f3c249599665b823566433c9}

空白，表示此影像目錄不包含任何SVG資料。

## 另請參閱 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)，目錄 [檔案](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
