---
description: 本文檔介紹如何管理Dynamic Media影像呈現伺服器。
solution: Experience Manager
title: 伺服器管理概述
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 伺服器管理概述{#server-administration-overview}

本文檔介紹如何管理Dynamic Media影像呈現伺服器。

影像渲染由兩個主要元件組成：

* 與映像服務一起部署Java包 [!DNL Platform Server] 並管理客戶端連接、快取、材料目錄。
* 本地代碼模組被部署為影像伺服器的擴展庫並實現核心影像呈現功能。

這兩個元件統稱為 *呈現伺服器*。

「影像呈現」與「影像服務」共用許多伺服器設施，所有選項都通過編輯配置檔案進行配置。 預設目錄( [!DNL default.ini])或特定材料目錄。 有關詳細資訊，請參閱物料目錄。

映像呈現安裝資料夾( *[!DNL install_folder]*)為[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，預設 *[!DNL install_root]* 是 `C:\Program Files\Scene7`。 在安裝過程中可以指定其他資料夾。 在Linux上， *[!DNL install_root]* 必須始終 [!DNL /usr/local/scene7]。 可以使用符號連結。

所有檔案路徑在UNIX上區分大小寫，在Windows上不區分大小寫。
