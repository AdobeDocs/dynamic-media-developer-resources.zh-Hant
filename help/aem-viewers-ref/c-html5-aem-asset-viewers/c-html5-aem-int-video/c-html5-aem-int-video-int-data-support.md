---
description: 互動式視訊檢視器支援根據傳送至檢視器的互動資料來轉換互動式色票作為設定參數。
solution: Experience Manager
title: 互動式資料支援
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 互動式資料支援{#interactive-data-support}

互動式視訊檢視器支援根據傳送至檢視器的互動資料來轉換互動式色票作為設定參數。

目前可見的色票對應於與其相關聯的視訊時間區域。 按一下或點選互動色票會觸發作者時指派給它的動作。

互動式色票可透過觸發JavaScript回呼，在代管網頁上啟用「快速檢視」，或將使用者重新導向至外部網頁。

## 關於快速查看{#section-7990e44f641042d2a38ba20c9413b3f8}

這些類型的互動式色票應使用AEM Assets（隨選）中的動作類型「quickview」來製作。 當使用者啟動此樣本時，檢視器會執行`quickViewActivate` JavaScript回呼，並將樣本資料傳遞給它。 預期內嵌網頁會監聽此回呼，當它觸發時，頁面會開啟其自己的「快速檢視」實作。

## 重定向至外部網頁{#section-32ebe3c3a7f74892a428c5d48801de4d}

為AEM Assets的動作類型「quickview」製作的色票——隨選將使用者重新導向至外部URL。 URL可以在新的瀏覽器標籤中、在相同的視窗中或在命名的瀏覽器視窗中開啟，視編寫時的設定而定。
