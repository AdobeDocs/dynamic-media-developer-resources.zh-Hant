---
description: 遮罩檔案路徑。 與此目錄記錄關聯的遮色片影像檔案的相對或絕對路徑與名稱。
solution: Experience Manager
title: 遮色片路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# 遮色片路徑{#maskpath}

遮罩檔案路徑。 與此目錄記錄關聯的遮色片影像檔案的相對或絕對路徑與名稱。

允許將個別遮色片附加到影像。

伺服器使用[管理Source資料](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)中所述的路徑解析規則來尋找資料檔案。

## 屬性 {#section-cdc3b7e2811e41008479cd97887c01b7}

文字字串值。 選填。 如果已指定，則必須是有效的相對或絕對影像伺服器檔案路徑。 如果沒有檔案字尾，則會附加`attribute::DefaultExt`。

如果目錄記錄中同時定義了主要影像(`catalog::Path`)和遮色片影像(`catalog::MaskPath`)，則兩者的畫素大小必須完全相同。 遮色片影像必須是8位元灰階。

要求中的`mask=`會覆寫`catalog::MaskPath`。

如果主要影像( `catalog::MaskPath`)中有`catalog::Path`覆寫Alpha色版，而且未關聯Alpha色版（亦即，未預乘）。 如果影像Alpha是預乘，則會忽略`catalog::MaskPath`，而且一律使用Alpha色版。

## 預設 {#section-78533e35bfec469ba087cb68a35bb81b}

無。

## 另請參閱 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ， [attribute：：DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)， [catalog：：Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)， [遮罩=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)，[req=遮罩](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
