---
description: 影像地圖資料。 沒有或多個完整的HTML <AREA>元素，由前到後排序。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
TQID: 'https://experienceleague.adobe.com/JY0barcvbF72sTyYW4iIhjFE-8tfqtbI78PDccLcXV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 4%

---

# 地圖{#map}

影像地圖資料。 沒有或多個完整的HTML `<AREA>`元素，由前到後排序。

伺服器會解譯並可能變更SHAPE和COORDS屬性（此版本不支援SHAPE=CIRCLE）。 `<AREA>`的所有其他屬性皆未經修改即傳遞。 以COORDS屬性指定的座標值必須是未修改來源影像左上角的畫素位移。 （`%`座標在此版本中不受支援，而且可能無法正確處理。）

## 屬性 {#section-f52d89fd399b4356ac05277e6c12f956}

文字字串值。 若指定，則必須是一或多個完整的HTML `<AREA>`元素。

此欄位參與文字字串本地化。 如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 預設 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

無。

## 另請參閱 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ， [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)， [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
