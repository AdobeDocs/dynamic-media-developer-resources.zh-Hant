---
description: 影像地圖資料。 沒有或多個完整的HTML<AREA>元素，由前到後排序。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---

# 地圖{#map}

影像地圖資料。 沒有或以上完整HTML`<AREA>`元素，從前到後排序。

伺服器會解譯並可能變更SHAPE和COORDS屬性（此版本不支援SHAPE=CIRCLE）。 `<AREA>`的所有其他屬性皆未經修改即傳遞。 以COORDS屬性指定的座標值必須是未修改來源影像左上角的畫素位移。 （`%`座標在此版本中不受支援，而且可能無法正確處理。）

## 屬性 {#section-f52d89fd399b4356ac05277e6c12f956}

文字字串值。 如果已指定，則必須是一或多個完整的HTML`<AREA>`專案。

此欄位參與文字字串本地化。 如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 預設 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

無。

## 另請參閱 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ， [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)， [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
