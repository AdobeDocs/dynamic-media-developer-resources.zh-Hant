---
description: 安裝Dynamic Media Image Serving後，應驗證安裝。
solution: Experience Manager
title: 驗證安裝
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 驗證安裝{#verifying-the-installation}

安裝Dynamic Media Image Serving後，應驗證安裝。

映像伺服器作為Windows服務安裝。

1. 開啟「服務控制面板」，並檢查「Dynamic Media影像伺服」是否顯示「已開始」狀態。
1. 在相同或不同主機上開啟Internet瀏覽器，並檢查預設伺服器回應：

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

檢查回應中是否有「 `imageServer.`」項目，表示影像伺服器正在監聽。
>如果已安裝，可使用檔案和示範套件的範例頁面執行其他驗證。
