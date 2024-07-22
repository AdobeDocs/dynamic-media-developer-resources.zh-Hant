---
description: 使用這些伺服器設定進行SSL。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# SSL{#ssl}

使用這些伺服器設定進行SSL。

## TC：：SslPort — 監聽連線埠 {#section-c80eb582bf684b3fa7313a77cc606769}

指定SSL連線之[!DNL Platform Server]的接聽連線埠。 預設為 8443。

## TC：：keystoreFile - Keystore檔案路徑 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL Keystore檔案的路徑/名稱。 可以是絕對路徑或相對於[！DNL *[!DNL install_folder]*/conf]的路徑。 預設值為&#x200B;*install_folder*/conf/scene7keystore。

## TC：：keystorePass — 金鑰庫密碼 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

金鑰庫檔案的密碼。 預設值為`scene7`。

## TC：：keystoreType — 金鑰庫型別 {#section-8f263e1ba67740728cd39181960d7c7d}

選取金鑰庫的型別。 支援&#39; `Java'` （預設）和&#39; `PKCS12`&#39;。
