---
title: IccProfileSrcCmyk
description: CMYK預設輸入色彩設定檔。 指定用於未內嵌色彩設定檔的CMYK來源影像，以及用各種「影像伺服」命令（例如color=）指定的某些CMYK色彩值，的ICC色彩設定檔名稱。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
TQID: 'https://experienceleague.adobe.com/ZzJlJzNfiGnMaKHqMpoJmOiEobxRcHeNAw-B78S3o78'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK預設輸入色彩設定檔。 指定用於未內嵌色彩設定檔的CMYK來源影像，以及用各種「影像伺服」命令（例如color=）指定的某些CMYK色彩值，的ICC色彩設定檔名稱。

## 屬性 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

文字字串。 如果已指定，則必須是來自此影像目錄或預設目錄之ICC設定檔對映的有效`icc::Name`值，或是相對於`attribute::RootPath`的檔案路徑。 參照的ICC設定檔必須是CMYK設定檔。

## 預設 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

如果未定義或空白，則繼承自`default::IccProfileSrcCmyk`。 如果`attribute::IccProfileSrcCmyk`未解析為有效的設定檔，則改用`attribute::IccProfileCmyk`。

## 另請參閱 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，[attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，[attribute：：IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)，[attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
