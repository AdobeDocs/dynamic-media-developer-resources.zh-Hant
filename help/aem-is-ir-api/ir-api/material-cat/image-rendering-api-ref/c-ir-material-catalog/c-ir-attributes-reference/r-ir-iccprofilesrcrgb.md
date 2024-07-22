---
title: IccProfileSrcRgb
description: RGB預設輸入色彩設定檔。 指定用於RGB材質影像及未嵌入色彩設定檔之暈映的ICC色彩設定檔名稱。 也適用於RGB色彩值，這些值是使用各種「影像演算」指令指定的，例如bgc=和color=。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入色彩設定檔。 指定用於RGB材質影像及未嵌入色彩設定檔之暈映的ICC色彩設定檔名稱。 也適用於RGB色彩值，以各種影像演算命令指定，例如`bgc=`和`color=`。

## 屬性 {#section-c22966bba03e43c08e9d3fb91bfdd465}

文字字串。 如果已指定，則必須是來自此影像目錄或預設目錄之ICC設定檔對映的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參考的ICC設定檔必須是RGB設定檔。

## 預設 {#section-0171cd6680284bfa9844b9cc3644ca61}

如果未定義或空白，則繼承自`default::IccProfileSrcRgb`。 如果`attribute::IccProfileSrcRgb`未解析為有效的設定檔，則改用`attribute::IccProfileRgb`。

## 另請參閱 {#section-1ba91666830f4c209c39260ea29f938e}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，[attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，[attribute：：IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)，[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
