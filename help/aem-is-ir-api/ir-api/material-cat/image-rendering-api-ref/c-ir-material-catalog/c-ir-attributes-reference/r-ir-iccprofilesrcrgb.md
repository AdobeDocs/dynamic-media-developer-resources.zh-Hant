---
description: RGB預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的RGB材料影像和暈映的ICC顏色配置檔案的名稱，以及用各種「影像渲染」命令（如bgc=和color=）指定的RGB顏色值的名稱。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的RGB材料影像和暈映的ICC顏色配置檔案的名稱，以及用各種「影像渲染」命令（如bgc=和color=）指定的RGB顏色值的名稱。

## 屬性 {#section-c22966bba03e43c08e9d3fb91bfdd465}

文字字串。 如果指定，則必須是此影像目錄或預設目錄的ICC配置檔案映射中的有效`icc::Name`值，或相對於`attribute::RootPath`的檔案路徑。 引用的ICC配置檔案必須是RGB配置檔案。

## 預設 {#section-0171cd6680284bfa9844b9cc3644ca61}

如果未定義或為空，則從`default::IccProfileSrcRgb`繼承。 如果`attribute::IccProfileSrcRgb`未解析為有效的設定檔，則會改用`attribute::IccProfileRgb`。

## 另請參閱 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [屬性：:IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
