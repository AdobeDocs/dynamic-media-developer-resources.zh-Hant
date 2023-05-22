---
title: 互動式資料支援
description: 互動式視頻查看器支援基於作為配置參數傳遞給查看器的互動式資料來呈現互動式色板。
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

互動式視頻查看器支援基於作為配置參數傳遞給查看器的互動式資料來呈現互動式色板。

當前可見色板對應於與其關聯的視頻時間區域。 按一下或點擊互動式色板會觸發在作者時分配給它的操作。

互動式色板可以通過觸發JavaScript回調來激活托管網頁上的Quickview，也可以將用戶重定向到外部網頁。

## 關於Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

應使用「Adobe Experience Manager資產 — 按需」中的活動類型「quickview」創作這些類型的互動式色板。 當用戶激活這樣的色板時，觀看者運行 `quickViewActivate` JavaScript回調並將色板資料傳遞給它。 預期嵌入網頁會偵聽此回調，當它觸發時，該頁會開啟其自己的Quickview實現。

## 重定向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

為Experience Manager Assets的操作類型「quickview」創作的色板 — 按需將用戶重定向到外部URL。 根據創作時的設定，URL可以在新瀏覽器頁籤、同一窗口或命名瀏覽器窗口中開啟。
