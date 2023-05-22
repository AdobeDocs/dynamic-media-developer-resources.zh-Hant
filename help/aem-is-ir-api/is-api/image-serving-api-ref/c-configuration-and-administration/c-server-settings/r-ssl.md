---
description: 將這些伺服器設定用於SSL。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# SSL{#ssl}

將這些伺服器設定用於SSL。

## TC::SslPort — 偵聽埠 {#section-c80eb582bf684b3fa7313a77cc606769}

指定的監聽埠 [!DNL Platform Server] SSL連接。 預設為 8443。

## TC::keystoreFile — 密鑰庫檔案路徑 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL密鑰庫檔案的路徑/名稱。 可以是絕對路徑或相對於[!DNL]的路徑 *[!DNL install_folder]*/conf]。 預設值為 *安裝資料夾*/conf/scene7keystore。

## TC::keystorePass — 密鑰庫密碼 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

密鑰庫檔案的口令。 預設為 `scene7`.

## TC::keystoreType — 密鑰庫類型 {#section-8f263e1ba67740728cd39181960d7c7d}

選擇密鑰庫的類型。 &quot; `Java'` （預設）和「 `PKCS12`」。
