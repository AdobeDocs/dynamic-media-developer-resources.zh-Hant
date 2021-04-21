---
description: 熱點支援
solution: Experience Manager
title: 熱點支援
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# 熱點支援{#hotspot-support}

檢視器支援在主檢視上方呈現熱點圖示。 如「熱點」部分所述，熱點表徵圖的外觀通過CSS進行控制。

請參閱[熱點](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點可以觸發JavaScript回呼，或將使用者重新導向至外部網頁，以啟用代管網頁上的快速檢視功能。

## 快速查看熱點{#section-cda48fc9730142d0bb3326bac7df3271}

這些類型的熱點應使用AEM AssetsDynamic Media的「快速查看」操作類型按需編寫。 當使用者啟動此熱點時，檢視器會執行`quickViewActivate` JavaScript回呼，並將熱點資料傳遞給它。 預期內嵌網頁會監聽此回呼。 當它觸發頁面時，會開啟其自己的快速檢視實作。

## 重定向至外部網頁{#section-ef820c71251e4215800bb99c0c9ebe16}

為AEM AssetsDynamic Media的動作類型「快速檢視」撰寫的熱點——隨選會將使用者重新導向至外部URL。 URL會在新的瀏覽器索引標籤、相同視窗或指名的瀏覽器視窗中開啟，視編寫時所做的設定而定。
