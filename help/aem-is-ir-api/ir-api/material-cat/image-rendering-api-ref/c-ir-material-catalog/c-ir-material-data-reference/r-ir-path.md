---
description: 映像檔案路徑。 紋理或貼花影像檔案的相對路徑和名稱。
solution: Experience Manager
title: 路徑 *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---

# 路徑 *{#path}

映像檔案路徑。 紋理或貼花影像檔案的相對路徑和名稱。

伺服器將此值與 `attribute::RootPath` 生成實際映像檔案路徑。 也可能是絕對路徑。

用於指定紋理、機櫃和窗口覆蓋材料的紋理影像檔案，以及貼花和壁邊框材料的RGB或RGBA影像檔案。 並非所有機櫃和窗口覆蓋材料都需要單獨的可重複紋理影像。

## 屬性 {#section-8c12ea24f21d4472be677581893e6681}

文本字串。 紋理和貼花材料需要，機櫃和窗口覆蓋材料可選。 如果指定，則它必須是有效的相對或絕對檔案路徑。 對於純色材料，必須為空。

## 支援的檔案格式 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

影像呈現支援與Dynamic Media影像服務相同的源影像格式。

使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時，需要多種不同解析度的影像資料的應用程式將表現最佳。 影像服務包括影像轉換器(IC)實用程式，該實用程式根據任何支援的格式建立PTIFF影像。

有關支援的檔案格式的完整清單，請參閱映像服務文檔中IC實用程式的說明。

## 預設 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

無。

## 另請參閱 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC實用程式](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) 。 [屬性：:RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md)。 [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
