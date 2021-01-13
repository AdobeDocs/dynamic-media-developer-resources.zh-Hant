---
description: 熱點和影像地圖支援
solution: Experience Manager
title: 熱點和影像地圖支援
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# 熱點和影像映射支援{#hotspot-and-image-maps-support}

檢視器支援在主檢視上方呈現熱點圖示和影像地圖區域。 如「自訂熱點和影像地圖」區段中所述，熱點圖示和區域的外觀是透過CSS控制。

請參閱[熱點和影像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點和地區可透過觸發JavaScript回呼，在代管網頁上啟用快速檢視功能，或將使用者重新導向至外部網頁。

## 快速查看熱點{#section-cda48fc9730142d0bb3326bac7df3271}

這些熱點或影像地圖類型應使用AEM動態媒體中的「快速檢視」動作類型來編寫。 當使用者啟動此類熱點或影像地圖時，檢視器會執行`quickViewActivate` JavaScript回呼，並傳遞熱點或影像地圖資料給它。 預期內嵌網頁會監聽此回呼。 當它觸發頁面時，會開啟其自己的快速檢視實作。

## 重定向至外部網頁{#section-ef820c71251e4215800bb99c0c9ebe16}

為AEM的「動態媒體」中的動作類型「快速檢視」所製作的熱點或影像地圖會將使用者重新導向至外部URL。 URL會在新的瀏覽器索引標籤、相同視窗或指名的瀏覽器視窗中開啟，視編寫時所做的設定而定。
