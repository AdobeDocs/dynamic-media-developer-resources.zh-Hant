---
description: 熱點和影像地圖支援
solution: Experience Manager
title: 熱點和影像地圖支援
feature: Dynamic Media經典，檢視器，SDK/API，轉盤橫幅
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# 熱點和影像映射支援{#hotspot-and-image-maps-support}

檢視器支援在主檢視上方呈現熱點圖示和影像地圖區域。 如「自訂熱點和影像地圖」區段中所述，熱點圖示和區域的外觀是透過CSS控制。

請參閱[熱點和影像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點和地區可透過觸發JavaScript回呼，在代管網頁上啟用快速檢視功能，或將使用者重新導向至外部網頁。

## 快速查看熱點{#section-cda48fc9730142d0bb3326bac7df3271}

這些類型的熱點或影像映射應使用Dynamic Media的「快速查看」操作類型(即AEM)。 當使用者啟動此類熱點或影像地圖時，檢視器會執行`quickViewActivate` JavaScript回呼，並傳遞熱點或影像地圖資料給它。 預期內嵌網頁會監聽此回呼。 當它觸發頁面時，會開啟其自己的快速檢視實作。

## 重定向至外部網頁{#section-ef820c71251e4215800bb99c0c9ebe16}

為Dynamic Media的動作類型「快速檢視」製作的熱點或影像地圖AEM，會將使用者重新導向至外部URL。 URL會在新的瀏覽器索引標籤、相同視窗或指名的瀏覽器視窗中開啟，視編寫時所做的設定而定。
