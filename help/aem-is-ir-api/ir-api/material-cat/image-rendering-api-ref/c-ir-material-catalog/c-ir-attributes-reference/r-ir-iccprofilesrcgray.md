---
title: IccProfileSrcGray
description: 灰度預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的灰度材料影像的ICC顏色配置檔案的名稱。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰度預設輸入顏色配置檔案。 指定用於未嵌入顏色配置檔案的灰度材料影像的ICC顏色配置檔案的名稱。

## 屬性 {#section-97923d8561b845309442d57d017d91a4}

文本字串。 如果指定，則必須是有效 `icc::Name` 此影像目錄或預設目錄或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-02c52805ee13483dba7878aeab51f889}

繼承自 `default::IccProfileSrcGray` 或為空。 如果 `attribute::IccProfileSrcGray` 未解析為有效的配置檔案， `attribute::IccProfileGray` 的雙曲餘切值。

## 另請參閱 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc:：名稱](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) 。 [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)。 [屬性：:IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6)。 [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
