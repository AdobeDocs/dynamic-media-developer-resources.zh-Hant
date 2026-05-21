---
description: 縮圖的預設背景顏色。 用來對不包含實際影像資料的輸出縮圖影像區域進行填色的RGB值。
solution: Experience Manager
title: ThumbBkgColor
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88acf5ad-2973-42f9-9aaa-901e66b07f53
TQID: 'https://experienceleague.adobe.com/ExdSGafazvDJ0iqMeDvUjD7EFGZ8TKkNn-0klzizVUI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 3%

---

# ThumbBkgColor{#thumbbkgcolor}

縮圖的預設背景顏色。 用來對不包含實際影像資料的輸出縮圖影像區域進行填色的RGB值。

僅用於縮圖要求(`req=tmb`)以及當`catalog::ThumbType`設定為2或3時。

## 屬性 {#section-a73e82c950cc4319bc3bccec14764c25}

顏色。

## 預設 {#section-b02bb56dda684ff9969806ce82ba00c2}

如果未定義或空白，則繼承自`default::ThumbBkgColor`。

## 另請參閱 {#section-27983dc885424dfbba8c8e4192f3f88d}

[目錄：：ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ， [req=tmb](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
