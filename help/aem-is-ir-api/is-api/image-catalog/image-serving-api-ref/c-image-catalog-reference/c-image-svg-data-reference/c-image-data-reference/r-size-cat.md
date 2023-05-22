---
description: 影像尺寸. 目錄路徑引用的全解析度影像的像素大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 9%

---

# 大小{#size}

影像尺寸. 目錄：:Path引用的全解析度影像的像素大小。

如果提供了此值，則Image Serving會使用它來避免必須開啟影像來獲得實際影像大小。

>[!NOTE]
>
>如果 `catalog::Size`提供，且與實際全解析度影像大小不同，可能會導致未定義的行為。

## 屬性 {#section-5c914ec8b1444a8e99d811b647cd42a3}

兩個整數，每個大於0，用逗號分隔。 選擇性.

## 預設 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

如果欄位不存在，或該欄位為空，則使用影像的實際大小。

## 另請參閱 {#section-e63797357d5a4119a10db1e6e088f6e9}

[目錄：：路徑](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) 。 [雷斯=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
