---
description: 掩碼檔案路徑。 與此目錄記錄關聯的掩碼影像檔案的相對或絕對路徑和名稱。
solution: Experience Manager
title: 掩碼路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---

# 掩碼路徑{#maskpath}

掩碼檔案路徑。 與此目錄記錄關聯的掩碼影像檔案的相對或絕對路徑和名稱。

允許將單獨的蒙版附加到影像。

伺服器使用中所述的路徑解析規則 [管理源資料](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) 的子菜單。

## 屬性 {#section-cdc3b7e2811e41008479cd97887c01b7}

文本字串值。 選擇性. 如果指定，則必須是有效的相對或絕對Image Server檔案路徑。 `attribute::DefaultExt` 的子目錄。

如果兩個主映像( `catalog::Path`)和蒙版影像( `catalog::MaskPath`)在目錄記錄中定義，二者必須具有相同的像素大小。 蒙版影像必須為8位灰度。

`mask=` 在請求覆蓋中 `catalog::MaskPath`。

`catalog::MaskPath` 覆蓋主影像中的Alpha通道( `catalog::Path`)，如果存在，並且如果α通道未關聯（即未預乘）。 如果影像α是預乘的， `catalog::MaskPath` 忽略，並始終使用Alpha通道。

## 預設 {#section-78533e35bfec469ba087cb68a35bb81b}

無。

## 另請參閱 {#section-68d262f5949c4959b8723ba44611d1dc}

[屬性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) 。 [屬性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)。 [目錄：：路徑](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)。 [掩碼=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)。 [req=掩碼](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
