---
description: 安裝Dynamic Media Image Serving後，應驗證安裝。
seo-description: 安裝Dynamic Media Image Serving後，應驗證安裝。
seo-title: 驗證安裝
solution: Experience Manager
title: 驗證安裝
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# 驗證安裝{#verifying-the-installation}

安裝Dynamic Media Image Serving後，應驗證安裝。

映像伺服器作為Windows服務安裝。

1. 開啟「服務控制面板」並檢查「動態媒體影像伺服」的狀態是否為「已開始」。
1. 在相同或不同主機上開啟網際網路瀏覽器，並檢查預設伺服器回應：

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

檢查響應中是否存在「 `imageServer.` 」項，這表示影像伺服器正在監聽。
>如果已安裝，則可使用「說明檔案」和「示範」套件的範例頁面執行其他驗證。

