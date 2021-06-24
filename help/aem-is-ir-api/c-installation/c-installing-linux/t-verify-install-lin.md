---
description: 在Linux上安裝映像服務後，請驗證安裝。
solution: Experience Manager
title: 驗證安裝
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 驗證安裝{#verifying-the-installation}

在Linux上安裝映像服務後，請驗證安裝。

映像伺服器作為Linux守護程式安裝。

**驗證安裝的方式**

1. 驗證映像服務已配置為自動啟動且正在運行：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必須擁有根權限才能執行這些指令碼。

1. 在相同或不同主機上開啟Internet瀏覽器，並檢查預設伺服器回應：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

在回應中，檢查是否有以「 `imageServer.`」開頭的項目，這表示平台伺服器可以成功與影像伺服器通信。
>如果已安裝，可使用檔案和示範套件的範例頁面執行其他驗證。
