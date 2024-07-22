---
description: 浮水印選取器。 指定要做為浮水印影像或範本之目錄記錄的目錄ID。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# 浮水印{#watermark}

浮水印選取器。 指定要做為浮水印影像或範本之目錄記錄的目錄：：Id。

若指定，伺服器會將浮水印套用至所有影像要求( `req=img`)要求的影像資料。

## 屬性 {#section-fad6ffff4c5f4b5c8010281bc1377055}

文字字串。 如果已指定，則必須為此影像目錄(或預設目錄（若在[!DNL default.ini]中指定）中的有效`Catalog::Id`值。

## 預設 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

如果未定義，則繼承自`default::Watermark`。 如果已定義但空白，即使已定義`default::Watermark`，也不會對此影像目錄套用浮水印。

## 另請參閱 {#section-f15dbe31013849828d78588742dde58e}

[catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
