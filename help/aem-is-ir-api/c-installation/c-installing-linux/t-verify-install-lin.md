---
title: 驗證安裝
description: 在Linux®上安裝Image Serving後，驗證安裝。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 驗證安裝{#verifying-the-installation}

在Linux®上安裝Image Serving後，驗證安裝。

映像伺服器作為Linux®守護程式安裝。

**驗證安裝**

1. 驗證映像服務是否已配置為自動啟動且正在運行：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必須具有根權限才能運行這些指令碼。

1. 在相同或不同主機上開啟Internet瀏覽器並檢查預設伺服器響應：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

在響應中，檢查是否存在以 `imageServer`，表示 [!DNL Platform Server] 可以成功與映像伺服器通信。

>如果已安裝，可以使用文檔和演示包的示例頁執行其他驗證。
