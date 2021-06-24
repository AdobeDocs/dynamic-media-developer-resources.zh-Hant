---
description: 路徑
solution: Experience Manager
title: 路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# 路徑{#path}

伺服器使用[管理源資料](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)中所述的路徑解析規則來查找資料檔案。

## 屬性 {#section-72d9edc532ad43349afcb4df22e1c692}

文字字串。 影像和SVG記錄所需，範本記錄可能為空。 如果指定，則必須是有效的相對或絕對映像伺服器檔案路徑。 屬性：：如果沒有檔案尾碼，則附加DefaultExt。

## 支援的影像檔案格式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

有關支援的影像檔案格式的完整清單，請參閱影像轉換器(IC)實用程式的說明。

使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時，需要多個不同解析度的影像資料的應用程式效能最佳。 IC實用程式用於從任何支援的影像格式建立PTIFF影像。

## 預設 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

無。

## 另請參閱 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC實用程式](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [屬性：:RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [屬性：:DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
