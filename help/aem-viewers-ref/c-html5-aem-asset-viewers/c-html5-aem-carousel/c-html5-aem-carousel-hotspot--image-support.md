---
title: 熱點和影像映射支援
description: 熱點和影像映射支援
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 熱點和影像映射支援{#hotspot-and-image-maps-support}

該查看器支援在主視圖頂部繪製熱點表徵圖和影像地圖區域。 熱點表徵圖和區域的外觀通過CSS控制，如定制熱點和影像映射部分中所述。

請參閱 [熱點和影像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點和區域可以通過觸發JavaScript回調來激活托管網頁上的Quickview功能，或將用戶重定向到外部網頁。

## 快速視圖熱點 {#section-cda48fc9730142d0bb3326bac7df3271}

應使用Adobe Experience ManagerDynamic Media的&quot;Quickview&quot;操作類型創作這些類型的熱點或影像映射。 當用戶激活這種熱點或影像映射時，查看器運行 `quickViewActivate` JavaScript回調並將熱點或影像映射資料傳遞給它。 預期嵌入網頁偵聽此回調。 觸發頁面時，它會開啟自己的Quickview實現。

## 重定向至外部網頁 {#section-ef820c71251e4215800bb99c0c9ebe16}

為Experience ManagerDynamic Media中的操作類型「Quickview」創作的熱點或影像映射將用戶重定向到外部URL。 根據創作過程中的設定，URL將在新瀏覽器頁籤、同一窗口或命名瀏覽器窗口中開啟。
