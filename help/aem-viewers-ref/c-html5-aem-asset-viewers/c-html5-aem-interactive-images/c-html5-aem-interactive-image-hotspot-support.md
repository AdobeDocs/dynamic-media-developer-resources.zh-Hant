---
title: 熱點支援
description: 熱點支援
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
TQID: 'https://experienceleague.adobe.com/kvYBwi70uYXIK8D6MeNgZN74h3X6jBfmOLj1SjlKEzs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# 熱點支援{#hotspot-support}

檢視器支援在主檢視上方轉譯熱點圖示。 熱點圖示的外觀會透過CSS控制，如熱點區段中所述。

檢視[熱點](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

連結區可以透過觸發JavaScript回呼在託管網頁上啟用快速檢視功能，或將使用者重新導向至外部網頁。

## 快速檢視熱點 {#section-cda48fc9730142d0bb3326bac7df3271}

這些型別的熱點應使用Adobe Experience Manager Assets — 隨選的Dynamic Media中的「快速檢視」動作型別來編寫。 當使用者啟用這類熱點時，檢視器會執行`quickViewActivate` JavaScript回呼並將熱點資料傳遞給它。 內嵌網頁應會監聽此回呼。 觸發頁面時，它會開啟自己的快速檢視實施。

## 重新導向至外部網頁 {#section-ef820c71251e4215800bb99c0c9ebe16}

為Experience Manager Assets的Dynamic Media中的動作型別「快速檢視」製作的熱點 — 隨選將使用者重新導向至外部URL。 根據編寫期間所做的設定，URL會在新的瀏覽器標籤中、同一視窗中或在指定的瀏覽器視窗中開啟。
