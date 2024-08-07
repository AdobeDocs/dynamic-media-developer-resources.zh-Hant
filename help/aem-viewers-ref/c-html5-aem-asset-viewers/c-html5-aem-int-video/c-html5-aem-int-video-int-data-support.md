---
title: 互動式資料支援
description: 互動式視訊檢視器支援根據作為設定引數傳遞給檢視器的互動式資料來轉譯互動式色票。
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

互動式視訊檢視器支援根據作為設定引數傳遞給檢視器的互動式資料來轉譯互動式色票。

目前可見的色票會對應於與其關聯的視訊時間區域。 按一下或點選互動式色票，就會在製作時觸發指派給它的動作。

互動式色票可以觸發JavaScript回呼，從而在託管網頁上啟用快速檢視，也可以將使用者重新導向至外部網頁。

## 關於快速檢視 {#section-7990e44f641042d2a38ba20c9413b3f8}

這些型別的互動式色票應使用Adobe Experience Manager Assets — 隨選中的動作型別「快速檢視」來撰寫。 當使用者啟用這類色票時，檢視器會執行`quickViewActivate` JavaScript回呼，並將色票資料傳遞至檢視器。 內嵌網頁應會監聽此回呼，並在觸發時，頁面會開啟自己的快速檢視實施。

## 重新導向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

Experience Manager Assets中針對「快速檢視」動作型別所編寫的色票 — 隨選將使用者重新導向至外部URL。 視編寫時的設定而定，URL可以在新的瀏覽器索引標籤、相同視窗中開啟，或在指定的瀏覽器視窗中開啟。
