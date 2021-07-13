---
description: 對SSL使用這些伺服器設定。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# SSL{#ssl}

對SSL使用這些伺服器設定。

## TC::SslPort — 偵聽埠 {#section-c80eb582bf684b3fa7313a77cc606769}

為SSL連接指定Platform Server的偵聽埠。 預設為 8443。

## TC::keystoreFile — 密鑰庫檔案路徑 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL金鑰存放區檔案的路徑/名稱。 可以是相對於[!DNL *[!DNL install_folder]*/conf]的絕對路徑或路徑。 預設值為&#x200B;*install_folder*/conf/scene7keystore。

## TC::keystorePass — 金鑰存放區密碼 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

金鑰存放區檔案的密碼。 預設為 `scene7`.

## TC::keystoreType — 金鑰存放類型 {#section-8f263e1ba67740728cd39181960d7c7d}

選擇密鑰庫的類型。 支援「 `Java'`（預設值）和「 `PKCS12`」。
