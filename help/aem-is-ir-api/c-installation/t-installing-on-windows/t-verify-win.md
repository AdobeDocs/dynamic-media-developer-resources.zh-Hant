---
title: 驗證安裝
description: 安裝Dynamic Media映像服務後，應驗證安裝。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 驗證安裝 {#verifying-the-installation}

安裝Dynamic Media映像服務後，應驗證安裝。

映像伺服器作為Windows服務安裝。

1. 開啟「服務」控制面板並檢查 `Dynamic Media Image Serving` 狀態為 `Started`。
1. 在相同或不同主機上開啟Internet瀏覽器並檢查預設伺服器響應：

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

檢查「」是否存在 `imageServer.`&quot;響應中的項，表示映像伺服器正在偵聽。
>如果已安裝，可以使用文檔和演示包的示例頁執行其他驗證。
