---
description: 預設回應影像。 指定在找不到影像檔案且未在請求中指定defaultImage=時要使用的影像或目錄項目。
solution: Experience Manager
title: 預設影像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# 預設影像{#defaultimage}

預設回應影像。 指定在找不到影像檔案且未在請求中指定defaultImage=時要使用的影像或目錄項目。

可以是目錄條目（包括模板）或相對(`attribute::RootPath`)或絕對影像檔案路徑。 用預設影像替換缺少的影像很實用。

## 屬性 {#section-b6d8193827c34e5f948792aba8b8daaf}

文字字串。 如果指定，則必須是此影像目錄中的有效`catalog::Id`值，或是相對(`attribute::RootPath`)或影像伺服器可訪問的影像檔案的絕對路徑。

## 限制 {#section-5d8ea872f0b0415fbd3a83410bbcf512}

預設影像機制不覆蓋外部影像源；如果外來影像源無效，則返回錯誤。

## 預設 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

若未定義，則繼承自`default::DefaultImage`。 如果已定義但為空，則會停用預設影像行為，即使已定義`default::DefaultImage`亦然。

## 另請參閱 {#section-dc0fb4e72294442882b33a479fbc2b82}

[屬性：:DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [屬性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [屬性：:DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
