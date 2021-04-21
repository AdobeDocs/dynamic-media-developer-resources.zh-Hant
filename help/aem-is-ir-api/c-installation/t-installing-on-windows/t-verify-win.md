---
description: 安裝Dynamic Media映像服務後，應驗證安裝。
solution: Experience Manager
title: 驗證安裝
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# 驗證安裝{#verifying-the-installation}

安裝Dynamic Media映像服務後，應驗證安裝。

映像伺服器作為Windows服務安裝。

1. 開啟「服務控制面板」並檢查「Dynamic Media影像服務」的狀態是否為「已啟動」。
1. 在相同或不同主機上開啟網際網路瀏覽器，並檢查預設伺服器回應：

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

檢查響應中是否存在「 `imageServer.` 」項，這表示影像伺服器正在監聽。
>如果已安裝，則可使用「說明檔案」和「示範」套件的範例頁面執行其他驗證。

