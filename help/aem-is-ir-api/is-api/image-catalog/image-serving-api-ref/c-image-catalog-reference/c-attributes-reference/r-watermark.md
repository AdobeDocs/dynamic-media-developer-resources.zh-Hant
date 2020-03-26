---
description: 浮水印選擇器。 指定要用作水印影像或模板的目錄記錄的目錄ID。
seo-description: 浮水印選擇器。 指定要用作水印影像或模板的目錄記錄的目錄ID。
seo-title: 浮水印
solution: Experience Manager
title: 浮水印
topic: Scene7 Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 浮水印{#watermark}

浮水印選擇器。 指定目錄：：用作水印影像或模板的目錄記錄的ID。

如果指定，則伺服器會將水印應用於所有影像請求( `req=img`)的請求影像資料。

## 屬性 {#section-fad6ffff4c5f4b5c8010281bc1377055}

文字字串。 如果指定，則必須是此影 `Catalog::Id` 像目錄(或在預設目錄中，如果在中指定的話 [!DNL default.ini])中的有效值。

## 預設 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

繼承自( `default::Watermark` 如果未定義)。 如果已定義但為空，則不會為此影像目錄應用水印，即使已定 `default::Watermark` 義水印。

## 另請參閱 {#section-f15dbe31013849828d78588742dde58e}

[目錄：:Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
