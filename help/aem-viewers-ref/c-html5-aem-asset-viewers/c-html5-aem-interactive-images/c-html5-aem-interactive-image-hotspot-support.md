---
title: 熱點支援
description: 熱點支援
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 熱點支援{#hotspot-support}

查看器支援在主視圖頂部呈現熱點表徵圖。 熱點表徵圖的外觀通過CSS控制，如「熱點」部分所述。

請參閱 [熱點](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

熱點可以通過觸發JavaScript回調來激活托管網頁上的Quickview功能，或者將用戶重定向到外部網頁。

## 快速視圖熱點 {#section-cda48fc9730142d0bb3326bac7df3271}

這些類型的熱點應使用Adobe Experience Manager資產 — 按需的Dynamic Media的「Quickview」操作類型創作。 當用戶激活這種熱點時，查看器運行 `quickViewActivate` JavaScript回調並將熱點資料傳遞給它。 預期嵌入網頁偵聽此回調。 觸發頁面時，它會開啟自己的Quickview實現。

## 重定向至外部網頁 {#section-ef820c71251e4215800bb99c0c9ebe16}

為Experience Manager AssetsDynamic Media的操作類型「快速查看」創作的熱點 — 按需重定向用戶到外部URL。 根據創作過程中的設定，URL將在新瀏覽器頁籤、同一窗口或命名瀏覽器窗口中開啟。
