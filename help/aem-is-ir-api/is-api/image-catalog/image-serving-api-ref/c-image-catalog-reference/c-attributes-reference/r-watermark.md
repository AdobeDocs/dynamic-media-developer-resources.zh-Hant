---
description: 浮水印選取器。 指定要做為浮水印影像或範本之目錄記錄的目錄ID。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
TQID: 'https://experienceleague.adobe.com/zajYc7BBw0BfJ6qvnTFiHY79quRa91-LdY3j1YynxVc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
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
