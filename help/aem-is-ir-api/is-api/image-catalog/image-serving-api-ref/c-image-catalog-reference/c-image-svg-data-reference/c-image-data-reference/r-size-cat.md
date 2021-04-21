---
description: 影像尺寸. 目錄路徑參照之全解析度影像的像素大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 9%

---


# 大小{#size}

影像尺寸. 目錄：:Path所參照之全解析度影像的像素大小。

如果提供此值，「影像伺服」會使用它，以避免開啟影像以取得實際影像大小。

>[!NOTE]
>
>如果提供`catalog::Size`且與實際的全解析度影像大小不相同，則可能會產生未定義的行為。

## 屬性 {#section-5c914ec8b1444a8e99d811b647cd42a3}

兩個整數，每個大於0，以逗號分隔。 選填。

## 預設 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

如果欄位不存在，或欄位空白，則會使用影像的實際大小。

## 另請參閱 {#section-e63797357d5a4119a10db1e6e088f6e9}

[目錄：:Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
