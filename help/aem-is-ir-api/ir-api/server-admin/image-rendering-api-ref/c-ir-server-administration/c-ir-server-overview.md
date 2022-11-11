---
description: 本檔案說明如何管理Dynamic Media Image Rendering伺服器。
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

本檔案說明如何管理Dynamic Media Image Rendering伺服器。

影像轉譯由兩個主要元件組成：

* 與映像服務一起部署Java包 [!DNL Platform Server] 並管理客戶端連接、快取、材料目錄。
* 原生程式碼模組部署為影像伺服器的擴充程式庫，並實作核心影像轉譯功能。

這兩個元件統稱為 *呈現伺服器*.

「影像呈現」與「影像伺服」共用許多伺服器設施，而所有選項都是透過編輯設定檔案來設定。 預設目錄( [!DNL default.ini])或特定材料目錄。 有關詳細資訊，請參閱物料目錄。

映像呈現安裝資料夾( *[!DNL install_folder]*)是[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，預設 *[!DNL install_root]* is `C:\Program Files\Scene7`. 在安裝期間可以指定不同的資料夾。 在Linux上， *[!DNL install_root]* 必須一律 [!DNL /usr/local/scene7]. 可使用符號連結。

在UNIX上，所有檔案路徑均區分大小寫，在Windows上則不區分大小寫。
