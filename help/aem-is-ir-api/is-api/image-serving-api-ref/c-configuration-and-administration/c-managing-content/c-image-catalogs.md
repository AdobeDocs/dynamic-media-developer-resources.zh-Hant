---
description: 影像目錄提供許多伺服器配置設定，以及字型、ICC配置檔案、命令宏。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 影像目錄{#image-catalogs}

影像目錄提供許多伺服器配置設定，以及字型、ICC配置檔案、命令宏。

它們會將請求中使用的影像和靜態內容ID對應至實際的檔案路徑、儲存各種影像中繼資料（例如影像地圖），以及為範本和影像集提供容器。

影像目錄僅由Platform Server存取，而不由Image Server存取。 目錄屬性檔案必須有.ini尾碼，並放置在Platform Server的目錄資料夾(`PS::CatalogFolder`)中。 至少需要預設映像目錄，並且必須填入所有屬性才能正確運行Platform Server。
