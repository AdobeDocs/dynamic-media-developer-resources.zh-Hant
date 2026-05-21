---
title: 正在驗證安裝
description: 安裝Dynamic Media影像伺服後，請務必確認安裝。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 正在驗證安裝 {#verifying-the-installation}

安裝Dynamic Media影像伺服後，請務必確認安裝。

影像伺服器會安裝為Windows服務。

1. 開啟[服務控制檯]並檢查`Dynamic Media Image Serving`是否以`Started`的狀態出現。
1. 開啟相同或不同主機上的網際網路瀏覽器，然後檢查預設伺服器回應：

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

檢查回應中是否存在「`imageServer.`」專案，指出影像伺服器正在接聽。

>若已安裝，可使用檔案和示範套件的範例頁面執行其他驗證。
