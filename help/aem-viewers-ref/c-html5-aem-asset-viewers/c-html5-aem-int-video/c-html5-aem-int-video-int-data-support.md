---
title: 互動式資料支援
description: 互動式視訊檢視器支援根據傳遞至檢視器的互動式資料（作為設定參數）轉譯互動式色票。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# 互動式資料支援{#interactive-data-support}

互動式視訊檢視器支援根據傳遞至檢視器的互動式資料（作為設定參數）轉譯互動式色票。

當前可見的色板對應於與其關聯的視頻時間區域。 按一下或點選互動式色票，就會觸發在製作時指派給它的動作。

互動式色票可透過觸發JavaScript回呼來啟動托管網頁上的快速檢視，或將使用者重新導向至外部網頁。

## 關於Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

這些類型的互動式色票應使用Adobe Experience Manager Assets - On-demand中的動作類型「quickview」來製作。 當使用者啟用此類色票時，檢視器會執行`quickViewActivate` JavaScript回呼，並將色票資料傳遞至該色票。 內嵌網頁應會監聽此回呼，當它觸發時，頁面會開啟其自己的Quickview實作。

## 重新導向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

在Experience Manager資產中為動作類型「快速檢視」所製作的色票 — 隨選將使用者重新導向至外部URL。 視編寫時的設定而定，URL可在新的瀏覽器索引標籤、相同視窗或命名的瀏覽器視窗中開啟。
