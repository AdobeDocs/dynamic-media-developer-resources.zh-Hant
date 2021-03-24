---
description: 影像檔案路徑。 紋理或貼圖影像檔的相對路徑和名稱。
solution: Experience Manager
title: 路徑 *
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---


# 路徑 *{#path}

影像檔案路徑。 紋理或貼圖影像檔的相對路徑和名稱。

伺服器將此值與`attribute::RootPath`結合，以生成實際的映像檔案路徑。 也可以是絕對路徑。

用於指定紋理、機櫃和窗口覆蓋材料的紋理影像檔案，以及用於壁和壁邊框材料的RGB或RGBA影像檔案。 並非所有的機櫃和窗口覆蓋材料都需要單獨的可重複紋理影像。

## 屬性 {#section-8c12ea24f21d4472be677581893e6681}

文字字串。 需要紋理和貼面材料，而櫥櫃和窗口覆蓋材料則可選。 如果指定，則必須是有效的相對或絕對檔案路徑。 對於純色材料，必須為空。

## 支援的檔案格式{#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

「影像演算」支援與「Dynamic Media影像伺服」相同的來源影像格式。

使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時，需要多種不同解析度的影像資料的應用程式效能最好。 「影像伺服」包含影像轉換器(IC)公用程式，可從任何支援的格式建立PTIFF影像。

有關支援的檔案格式的完整清單，請參閱映像服務文檔中的IC實用程式說明。

## 預設 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

無。

## 另請參閱 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC實用程式](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [屬性：:RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
