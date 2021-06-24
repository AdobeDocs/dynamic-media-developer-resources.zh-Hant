---
description: 本檔案說明如何管理Dynamic Media Image Rendering伺服器。
solution: Experience Manager
title: 伺服器管理概觀
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# 伺服器管理概觀{#server-administration-overview}

本檔案說明如何管理Dynamic Media Image Rendering伺服器。

影像轉譯由兩個主要元件組成：

* Java包與Image Serving Platform Server一起部署，並管理客戶端連接、快取、材料目錄。
* 原生程式碼模組部署為影像伺服器的擴充程式庫，並實作核心影像轉譯功能。

這兩個元件統稱為&#x200B;*Render Server*。

「影像呈現」與「影像伺服」共用許多伺服器設施，而所有選項都是透過編輯設定檔案來設定。 預設目錄([!DNL default.ini])或特定材料目錄提供了其他配置屬性。 有關詳細資訊，請參閱物料目錄。

「影像呈現」安裝資料夾(*[!DNL install_folder]*)為[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，預設&#x200B;*[!DNL install_root]*&#x200B;為`C:\Program Files\Scene7`。 在安裝期間可以指定不同的資料夾。 在Linux上，*[!DNL install_root]*&#x200B;必須始終為[!DNL /usr/local/scene7]。 可使用符號連結。

在UNIX上，所有檔案路徑均區分大小寫，在Windows上則不區分大小寫。
