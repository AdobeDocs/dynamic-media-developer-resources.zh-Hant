---
description: 本檔案說明如何管理Dynamic Media影像演算伺服器。
solution: Experience Manager
title: 伺服器管理概觀
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 伺服器管理概觀{#server-administration-overview}

本檔案說明如何管理Dynamic Media影像演算伺服器。

影像演算包含兩個主要元件：

* Java套件已與Image Serving [!DNL Platform Server]一起部署，並管理使用者端連線、快取、資料目錄。
* 原生程式碼模組會部署為Image Server的擴充功能程式庫，並實作核心的影像演算功能。

這兩個元件統稱為&#x200B;*轉譯器伺服器*。

「影像演算」與「影像伺服」共用許多伺服器功能，所有選項都透過編輯設定檔案來設定。 預設目錄([!DNL default.ini])或特定材質目錄提供其他組態屬性。 如需詳細資訊，請參閱原物料目錄。

影像演算安裝資料夾( *[!DNL install_folder]*)是[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，預設&#x200B;*[!DNL install_root]*&#x200B;為`C:\Program Files\Scene7`。 安裝期間可能會指定不同的資料夾。 在Linux上，*[!DNL install_root]*&#x200B;必須一律為[!DNL /usr/local/scene7]。 可以使用符號連結。

所有檔案路徑在UNIX上均區分大小寫，在Windows上則不區分大小寫。
