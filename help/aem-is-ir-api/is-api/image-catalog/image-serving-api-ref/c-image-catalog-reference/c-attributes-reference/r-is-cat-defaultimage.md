---
description: 預設回應影像。 指定在找不到影像檔案且未在請求中指定defaultImage=時要使用的影像或目錄項目。
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# DefaultImage{#defaultimage}

預設回應影像。 指定在找不到影像檔案且未在請求中指定defaultImage=時要使用的影像或目錄項目。

可以是目錄條目（包括模板）或相對(`attribute::RootPath`)或絕對影像檔案路徑。 用預設影像取代遺失的影像非常實用。

## 屬性 {#section-b6d8193827c34e5f948792aba8b8daaf}

文字字串。 如果指定，則必須是此映像目錄中的有效`catalog::Id`值，或是映像伺服器可以訪問的映像檔案的相對路徑（至`attribute::RootPath`）或絕對路徑。

## 限制{#section-5d8ea872f0b0415fbd3a83410bbcf512}

外來影像源未被預設影像機制覆蓋；如果外來影像來源無效，則會傳回錯誤。

## 預設 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

如果未定義，則繼承自`default::DefaultImage`。 如果已定義但空白，則會停用預設影像行為，即使已定義`default::DefaultImage`亦然。

## 另請參閱 {#section-dc0fb4e72294442882b33a479fbc2b82}

[屬性：::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)，屬性：RootPath [, ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)IdAttribute::ImageImageError [](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) [, DefaultCatalog Expiration屬性：:DefaultActalog Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
