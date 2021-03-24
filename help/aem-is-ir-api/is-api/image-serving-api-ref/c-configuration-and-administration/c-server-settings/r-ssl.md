---
description: 請對SSL使用這些伺服器設定。
solution: Experience Manager
title: SSL
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 6%

---


# SSL{#ssl}

請對SSL使用這些伺服器設定。

## TC::SslPort —— 偵聽埠{#section-c80eb582bf684b3fa7313a77cc606769}

為SSL連接的平台伺服器指定監聽埠。 預設為 8443。

## TC::keystoreFile —— 密鑰庫檔案路徑{#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL密鑰庫檔案的路徑／名稱。 可以是相對於[!DNL *[!DNL install_folder]*/conf]的絕對路徑或路徑。 預設值為&#x200B;*install_folder*/conf/scene7keystore。

## TC::keystorePass —— 密鑰庫密碼{#section-e7e9bfb7df584a248c0e3ee46803c3b1}

密鑰庫檔案的密碼。 預設為 `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

選擇密鑰庫的類型。 「 `Java'`（預設值）和「 `PKCS12`」受支援。
