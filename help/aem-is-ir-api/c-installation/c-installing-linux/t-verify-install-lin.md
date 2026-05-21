---
title: 正在驗證安裝
description: 在Linux®上安裝「影像伺服」後，請驗證是否已安裝。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 0%

---

# 正在驗證安裝{#verifying-the-installation}

在Linux®上安裝「影像伺服」後，請驗證是否已安裝。

Image Server會安裝為Linux®精靈。

**驗證安裝**

1. 確認「影像伺服」已設定為自動啟動，且正在執行：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必須具有root許可權才能執行這些指令碼。

1. 開啟相同或不同主機上的網際網路瀏覽器，然後檢查預設伺服器回應：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

在回應中，檢查是否有以`imageServer`開頭的專案，這表示[!DNL Platform Server]可以成功與影像伺服器通訊。

>若已安裝，可使用檔案和示範套件的範例頁面執行其他驗證。
