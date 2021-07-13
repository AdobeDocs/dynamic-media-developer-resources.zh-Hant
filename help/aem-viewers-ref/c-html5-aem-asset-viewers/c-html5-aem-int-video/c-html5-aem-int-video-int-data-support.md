---
description: 互動式視訊檢視器支援根據傳遞至檢視器的互動式資料（作為設定參數）轉譯互動式色票。
solution: Experience Manager
title: 互動式資料支援
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# 互動式資料支援{#interactive-data-support}

互動式視訊檢視器支援根據傳遞至檢視器的互動式資料（作為設定參數）轉譯互動式色票。

當前可見的色板對應於與其關聯的視頻時間區域。 按一下或點選互動式色票，就會觸發在製作時指派給它的動作。

互動式色票可透過觸發JavaScript回呼來啟動托管網頁上的快速檢視，或將使用者重新導向至外部網頁。

## 關於快速檢視 {#section-7990e44f641042d2a38ba20c9413b3f8}

這些類型的互動式色票應使用AEM Assets中的「快速檢視」動作類型依需製作。 當使用者啟用此類色票時，檢視器會執行`quickViewActivate` JavaScript回呼，並將色票資料傳遞至該色票。 內嵌網頁應會監聽此回呼，當其觸發時，頁面會開啟其自己的快速檢視實作。

## 重新導向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

在AEM Assets中為動作類型「quickview」製作的色票 — 隨選將使用者重新導向至外部URL。 視編寫時的設定而定，URL可在新的瀏覽器索引標籤、相同視窗或命名的瀏覽器視窗中開啟。
