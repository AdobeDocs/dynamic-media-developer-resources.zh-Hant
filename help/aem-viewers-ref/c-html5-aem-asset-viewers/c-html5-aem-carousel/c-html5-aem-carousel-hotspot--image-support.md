---
title: 熱點和影像地圖支援
description: 熱點和影像地圖支援
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 熱點和影像地圖支援{#hotspot-and-image-maps-support}

檢視器支援在主檢視上方轉譯熱點圖示和影像地圖區域。 熱點表徵圖和區域的外觀通過CSS控制，如定制熱點和影像映射部分中所述。

請參閱[熱點和影像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點和區域可以觸發JavaScript回呼來啟動托管網頁上的Quickview功能，或將使用者重新導向至外部網頁。

## 快速視圖熱點 {#section-cda48fc9730142d0bb3326bac7df3271}

這些類型的熱點或影像映射應使用Adobe Experience ManagerDynamic Media中的「Quickview」動作類型來製作。 當使用者啟用此類熱點或影像地圖時，檢視器會執行`quickViewActivate` JavaScript回呼，並將熱點或影像地圖資料傳遞至該回呼。 預期內嵌網頁會監聽此回呼。 觸發頁面時，會開啟自己的Quickview實作。

## 重新導向至外部網頁 {#section-ef820c71251e4215800bb99c0c9ebe16}

為Dynamic Media中的動作類型「Quickview」所製作的熱點或影像地圖，會將使用者重新導向至外部URL。 URL會根據編寫期間所做的設定，在新的瀏覽器索引標籤、相同視窗或命名的瀏覽器視窗中開啟。
