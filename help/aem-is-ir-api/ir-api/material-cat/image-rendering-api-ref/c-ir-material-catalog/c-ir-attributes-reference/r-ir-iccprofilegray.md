---
title: IccProfileGray
description: 灰階預設色域。 指定icc=未指定輸出色域時，用於灰階回應影像的ICC色彩設定檔名稱。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

灰階預設色域。 指定當沒有使用`icc=`指定輸出色域時，用於灰階回應影像的ICC色彩設定檔名稱。

## 屬性 {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

文字字串。 如果已指定，則必須是來自此材質目錄或預設目錄之ICC設定檔對映的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參照的ICC設定檔必須是灰階設定檔。

## 預設 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

如果未定義或空白，則繼承自`default::IccProfileGray`。

## 另請參閱 {#section-cd43189611f4426aacddcc604eb02a10}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [attribute：：IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2)， [attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
