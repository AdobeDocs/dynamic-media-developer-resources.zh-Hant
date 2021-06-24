---
description: 遮罩檔案路徑。 與此目錄記錄關聯的掩碼影像檔案的相對或絕對路徑和名稱。
solution: Experience Manager
title: 遮色片路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# 遮色片路徑{#maskpath}

遮罩檔案路徑。 與此目錄記錄關聯的掩碼影像檔案的相對或絕對路徑和名稱。

允許將單獨的蒙版附加到影像。

伺服器使用[管理源資料](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)中所述的路徑解析規則來查找資料檔案。

## 屬性 {#section-cdc3b7e2811e41008479cd97887c01b7}

文字字串值。 選填。如果指定，則必須是有效的相對或絕對映像伺服器檔案路徑。 `attribute::DefaultExt` 如果沒有檔案尾碼存在，則會附加。

如果目錄記錄中同時定義了主影像(`catalog::Path`)和掩碼影像(`catalog::MaskPath`)，則兩者必須具有相同的像素大小。 遮罩影像必須為8位灰度。

`mask=` 在請求覆寫 `catalog::MaskPath`中。

`catalog::MaskPath` 覆寫主影像( `catalog::Path`)中的alpha通道(如果存在，且如果alpha通道未關聯（即未預乘）)。如果影像Alpha已預先乘上，則會忽略`catalog::MaskPath`並一律使用Alpha通道。

## 預設 {#section-78533e35bfec469ba087cb68a35bb81b}

無。

## 另請參閱 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
