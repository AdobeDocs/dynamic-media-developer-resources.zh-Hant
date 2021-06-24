---
description: 熱點和影像地圖支援
solution: Experience Manager
title: 熱點和影像地圖支援
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,Business Practitioner
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 熱點和影像地圖支援{#hotspot-and-image-maps-support}

檢視器支援在主檢視上方轉譯熱點圖示和影像地圖區域。 熱點表徵圖和區域的外觀通過CSS控制，如定制熱點和影像映射部分中所述。

請參閱[熱點和影像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點和區域可以觸發JavaScript回呼來啟動托管網頁上的快速檢視功能，或將使用者重新導向至外部網頁。

## 快速查看熱點 {#section-cda48fc9730142d0bb3326bac7df3271}

這些類型的熱點或影像映射應使用AEM Dynamic Media中的「快速查看」動作類型來製作。 當使用者啟用此類熱點或影像地圖時，檢視器會執行`quickViewActivate` JavaScript回呼，並將熱點或影像地圖資料傳遞至該回呼。 預期內嵌網頁會監聽此回呼。 觸發頁面時，會開啟自己的快速檢視實作。

## 重新導向至外部網頁 {#section-ef820c71251e4215800bb99c0c9ebe16}

為AEM的Dynamic Media中的動作類型「快速檢視」所製作的熱點或影像地圖，會將使用者重新導向至外部URL。 URL會根據編寫期間所做的設定，在新的瀏覽器索引標籤、相同視窗或命名的瀏覽器視窗中開啟。
