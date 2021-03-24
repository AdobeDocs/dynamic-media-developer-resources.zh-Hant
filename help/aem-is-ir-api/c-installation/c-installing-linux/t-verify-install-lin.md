---
description: 在Linux上安裝映像服務後，請驗證安裝。
solution: Experience Manager
title: 驗證安裝
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 驗證安裝{#verifying-the-installation}

在Linux上安裝映像服務後，請驗證安裝。

映像伺服器作為Linux守護程式安裝。

**要驗證安裝**

1. 驗證映像服務是否配置為自動啟動且正在運行：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必須擁有root權限才能運行這些指令碼。

1. 在相同或不同主機上開啟網際網路瀏覽器，並檢查預設伺服器回應：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

在響應中，檢查是否存在以&quot; `imageServer.`&quot;開頭的項，這表示平台伺服器可以成功與映像伺服器通信。
>如果已安裝，則可使用「說明檔案」和「示範」套件的範例頁面執行其他驗證。

