---
description: 影像檔案路徑。 紋理或逐個影像檔案的相對路徑和名稱。
solution: Experience Manager
title: 路徑 *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# 路徑 *{#path}

影像檔案路徑。 紋理或逐個影像檔案的相對路徑和名稱。

伺服器將此值與`attribute::RootPath`結合，以建立實際的影像檔案路徑。 也可能是絕對路徑。

用於指定紋理、機櫃和窗口覆蓋材料的紋理影像檔案，以及用於貼壁和壁邊界材料的RGB或RGBA影像檔案。 並非所有的機箱和窗口覆蓋材料都需要單獨的可重複紋理影像。

## 屬性 {#section-8c12ea24f21d4472be677581893e6681}

文字字串。 需要質地和裝飾材料，可選用於櫥櫃和窗戶覆蓋材料。 如果指定，則必須是有效的相對或絕對檔案路徑。 實色材料必須為空。

## 支援的檔案格式 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

「影像轉譯」支援與Dynamic Media Image Serving相同的來源影像格式。

使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時，需要多個不同解析度的影像資料的應用程式效能最佳。 「影像服務」包括「影像轉換器(IC)」實用程式，該實用程式從任何受支援的格式建立PTIFF影像。

如需完整的支援檔案格式清單，請參閱影像伺服檔案中IC公用程式的說明。

## 預設 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

無。

## 另請參閱 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC實用程](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) 式， [屬性：:RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
