---
description: 'null'
seo-description: 'null'
seo-title: 熱點支援
solution: Experience Manager
title: 熱點支援
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 熱點支援{#hotspot-support}

檢視器支援在主檢視上方呈現熱點圖示。 如「熱點」部分所述，熱點表徵圖的外觀通過CSS進行控制。

請參閱[熱點](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點可以觸發JavaScript回呼，或將使用者重新導向至外部網頁，以啟用代管網頁上的快速檢視功能。

## 快速查看熱點{#section-cda48fc9730142d0bb3326bac7df3271}

這些熱點類型應使用Dynamic Media中的「快速檢視」動作類型(AEM Assets - on demand)編寫。 當使用者啟動此熱點時，檢視器會執行`quickViewActivate` JavaScript回呼，並將熱點資料傳遞給它。 預期內嵌網頁會監聽此回呼。 當它觸發頁面時，會開啟其自己的快速檢視實作。

## 重定向至外部網頁{#section-ef820c71251e4215800bb99c0c9ebe16}

針對AEM Assets動態媒體中的動作類型「快速檢視」撰寫的熱點——隨選將使用者重新導向至外部URL。 URL會在新的瀏覽器索引標籤、相同視窗或指名的瀏覽器視窗中開啟，視編寫時所做的設定而定。
