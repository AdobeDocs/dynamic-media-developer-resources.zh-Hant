---
description: 遮色片檔案路徑。 與此目錄記錄關聯的蒙版影像檔案的相對或絕對路徑和名稱。
solution: Experience Manager
title: 遮色片路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---


# MaskPath{#maskpath}

遮色片檔案路徑。 與此目錄記錄關聯的蒙版影像檔案的相對或絕對路徑和名稱。

允許將個別遮色片附加至影像。

伺服器使用[管理源資料](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)中所述的路徑解析規則查找資料檔案。

## 屬性 {#section-cdc3b7e2811e41008479cd97887c01b7}

文字字串值。 選填。如果指定，則必須是有效的相對或絕對映像伺服器檔案路徑。 `attribute::DefaultExt` 如果沒有檔案尾碼，則附加。

如果主影像(`catalog::Path`)和遮色片影像(`catalog::MaskPath`)都在目錄記錄中定義，則兩者的像素大小必須完全相同。 遮色片影像必須是8位元灰階。

`mask=` 在請求覆寫中 `catalog::MaskPath`。

`catalog::MaskPath` 覆寫主影像( `catalog::Path`)中的alpha色版（如果存在），且如果alpha色版未關聯（即未預先乘積）。如果預乘影像alpha，則會忽略`catalog::MaskPath`並始終使用alpha通道。

## 預設 {#section-78533e35bfec469ba087cb68a35bb81b}

無。

## 另請參閱 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md) [, req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
