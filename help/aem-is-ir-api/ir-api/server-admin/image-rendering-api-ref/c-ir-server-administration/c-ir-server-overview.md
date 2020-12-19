---
description: 本檔案說明如何管理Scene7 Image Rendering伺服器。
seo-description: 本檔案說明如何管理Scene7 Image Rendering伺服器。
seo-title: 伺服器管理概觀
solution: Experience Manager
title: 伺服器管理概觀
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# 伺服器管理概述{#server-administration-overview}

本檔案說明如何管理Scene7 Image Rendering伺服器。

影像演算由兩個主要元件組成：

* Java套件與Image Serving Platform Server一起部署，並管理用戶端連線、快取、材質型錄。
* 本地代碼模組被部署為影像伺服器的擴展庫並實現核心影像渲染功能。

這兩個元件統稱為&#x200B;*Render Server*。

「影像演算」與「影像伺服」共用許多伺服器功能，而所有選項都是透過編輯設定檔案來設定。 預設目錄([!DNL default.ini])或特定材料目錄提供了其他配置屬性。 如需詳細資訊，請參閱「材料目錄」。

「Image Rendering」（影像渲染）安裝資料夾(*[!DNL install_folder]*)是[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，預設值&#x200B;*[!DNL install_root]*&#x200B;為`C:\Program Files\Scene7`。 安裝期間可以指定不同的資料夾。 在Linux上，*[!DNL install_root]*&#x200B;必須始終為[!DNL /usr/local/scene7]。 可以使用符號連結。

在UNIX上，所有檔案路徑都區分大小寫，在Windows上則不區分大小寫。
