---
description: 浮水印選擇器。 指定要用作水印影像或模板的目錄記錄的目錄ID。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---


# 浮水印{#watermark}

浮水印選擇器。 指定目錄：：用作水印影像或模板的目錄記錄的ID。

如果指定，則伺服器會將水印應用於所有影像請求(`req=img`)的所請求影像資料。

## 屬性 {#section-fad6ffff4c5f4b5c8010281bc1377055}

文字字串。 如果指定，則必須是此映像目錄（或預設目錄中，如果在[!DNL default.ini]中指定）中的有效`Catalog::Id`值。

## 預設 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

如果未定義，則繼承自`default::Watermark`。 如果已定義但為空，則即使已定義`default::Watermark`，也不會對此影像目錄應用水印。

## 另請參閱 {#section-f15dbe31013849828d78588742dde58e}

[目錄：:Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
