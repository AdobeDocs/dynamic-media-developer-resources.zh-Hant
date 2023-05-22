---
title: Icc配置檔案灰色
description: 灰度預設顏色空間。 指定當未使用icc=指定輸出顏色空間時用於灰度響應影像的ICC顏色配置檔案的名稱。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# Icc配置檔案灰色{#iccprofilegray}

灰度預設顏色空間。 指定未指定輸出顏色空間時用於灰度響應影像的ICC顏色配置檔案的名稱 `icc=`。

## 屬性 {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

文本字串。 如果指定，則必須是有效 `icc::Name` 此材料目錄或預設目錄的ICC配置檔案映射中的值，或相對於 `attribute::RootPath`。 引用的ICC配置檔案必須是灰度配置檔案。

## 預設 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

繼承自 `default::IccProfileGray` 或為空。

## 另請參閱 {#section-cd43189611f4426aacddcc604eb02a10}

[icc:：名稱](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) 。 [屬性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)。 [屬性：:IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2)。 [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
