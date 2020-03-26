---
description: 安裝Scene7 Image Serving後，您應驗證安裝。
seo-description: 安裝Scene7 Image Serving後，您應驗證安裝。
seo-title: 驗證安裝
solution: Experience Manager
title: 驗證安裝
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 驗證安裝{#verifying-the-installation}

安裝Scene7 Image Serving後，您應驗證安裝。

映像伺服器作為Windows服務安裝。

1. 開啟「服務控制面板」，並檢查「Scene7 Image Serving」狀態為「已開始」。
1. 在相同或不同主機上開啟網際網路瀏覽器，並檢查預設伺服器回應：

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

檢查回應中是否有「 `imageServer.`」項目，指出影像伺服器正在監聽。
>如果已安裝，則可使用「說明檔案」和「示範」套件的範例頁面執行其他驗證。

