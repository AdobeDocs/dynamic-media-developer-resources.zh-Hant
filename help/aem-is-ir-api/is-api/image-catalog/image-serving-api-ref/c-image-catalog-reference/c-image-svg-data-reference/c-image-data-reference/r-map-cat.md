---
description: 影像映射資料。 無或更多完整HTML <area> 元素，前後排序。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 4%

---

# 地圖{#map}

影像映射資料。 無或更多完整HTML `<AREA>` 元素，前後排序。

伺服器將解釋並可能更改SHAPE和COORDS屬性。 （此版本不支援SHAPE=CIRCLE。） 所有其他屬性 `<AREA>` 不經修改就通過。 使用COORDS屬性指定的坐標值必須是未修改源影像的左上角的像素偏移。 (`%` 此版本不支援坐標，因此可能無法正確處理。)

## 屬性 {#section-f52d89fd399b4356ac05277e6c12f956}

文本字串值。 如果指定，則必須是一個或多個完整HTML `<AREA>` 元素。

此欄位參與文本字串本地化。 請參閱 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 的 *HTTP協定引用* 的雙曲餘切值。

## 預設 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

無。

## 另請參閱 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[地圖=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) 。 [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)。 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
