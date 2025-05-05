---
title: 正在驗證安裝
description: 安裝「Dynamic Media影像伺服」後，請務必確認安裝。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 正在驗證安裝 {#verifying-the-installation}

安裝「Dynamic Media影像伺服」後，請務必確認安裝。

影像伺服器會安裝為Windows服務。

1. 開啟[服務控制檯]並檢查`Dynamic Media Image Serving`是否以`Started`的狀態出現。
1. 開啟相同或不同主機上的網際網路瀏覽器，然後檢查預設伺服器回應：

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

檢查回應中是否存在「`imageServer.`」專案，指出影像伺服器正在接聽。
>若已安裝，可使用檔案和示範套件的範例頁面執行其他驗證。
