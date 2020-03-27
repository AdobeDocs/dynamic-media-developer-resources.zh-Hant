---
description: 影像地圖資料。 無或更完整的HTML <AREA>元素，從頭到尾排序。
seo-description: 影像地圖資料。 無或更完整的HTML <AREA>元素，從頭到尾排序。
seo-title: 地圖
solution: Experience Manager
title: 地圖
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 地圖{#map}

影像地圖資料。 無或更完整的HTML `<AREA>` 元素，從頭到尾排序。

伺服器將解譯並可能更改SHAPE和COORDS屬性。 （此版本不支援SHAPE=CIRCLE。）所有其他屬性 `<AREA>` 都會傳遞，不需修改。 使用COORDS屬性指定的坐標值必須是未修改源影像左上角的像素偏移。 (`%` 此版本不支援座標，可能無法正確處理)。

## 屬性 {#section-f52d89fd399b4356ac05277e6c12f956}

文字字串值。 如果指定，則必須是一或多個完整的HTML `<AREA>` 元素。

此欄位參與文字字串本地化。 如需詳細 [資訊，請參閱](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)*HTTP通訊協定參考中的文字字串本地化* 。

## 預設 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

無。

## 另請參閱 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)，文字字串本 [地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
