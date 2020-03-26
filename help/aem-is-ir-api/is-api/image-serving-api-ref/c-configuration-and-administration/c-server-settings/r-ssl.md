---
description: 請對SSL使用這些伺服器設定。
seo-description: 請對SSL使用這些伺服器設定。
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SSL{#ssl}

請對SSL使用這些伺服器設定。

## TC::SslPort —— 偵聽埠 {#section-c80eb582bf684b3fa7313a77cc606769}

為SSL連接的平台伺服器指定監聽埠。 預設為 8443。

## TC::keystoreFile —— 密鑰庫檔案路徑 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL密鑰庫檔案的路徑／名稱。 可以是相對於[!DNL *[!DNL install_folder]*/conf]的絕對路徑或路徑。 預設值 *為install_folder*/conf/scene7keystore。

## TC::keystorePass —— 密鑰庫密碼 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

密鑰庫檔案的密碼。 預設為 `scene7`.

## TC::keystoreType - Keystore類型 {#section-8f263e1ba67740728cd39181960d7c7d}

選擇密鑰庫的類型。 支 `Java'` 援「（預設） `PKCS12`」和「」。
