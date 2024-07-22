---
title: 路徑
description: 伺服器使用路徑解析規則來尋找資料檔案。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---

# 路徑{#path}

伺服器使用[管理Source資料](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)中所述的路徑解析規則來尋找資料檔案。

## 屬性 {#section-72d9edc532ad43349afcb4df22e1c692}

文字字串。 影像和SVG記錄需要，範本記錄可能空白。 如果已指定，則必須是有效的相對或絕對影像伺服器檔案路徑。 如果沒有檔案尾碼，則會附加attribute：：DefaultExt。

## 支援的影像檔案格式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

如需支援的影像檔案格式完整清單，請參閱Image Converter (IC)公用程式的說明。

需要多個不同解析度影像資料的應用程式，在使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時表現最佳。 IC公用程式可用來從任何支援的影像格式建立PTIFF影像。

## 預設 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

無。

## 另請參閱 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC公用程式](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)，[屬性：：RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)，[屬性：：DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0)，[src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
