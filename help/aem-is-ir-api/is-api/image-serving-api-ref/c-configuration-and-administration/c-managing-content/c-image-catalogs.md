---
description: 影像目錄提供許多伺服器組態設定，以及字型、ICC描述檔、命令巨集。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# 影像目錄{#image-catalogs}

影像目錄提供許多伺服器組態設定，以及字型、ICC描述檔、命令巨集。

它們會將請求中使用的影像和靜態內容ID對應至實際的檔案路徑、儲存各種影像中繼資料（例如影像地圖），並提供範本和影像集的容器。

映像目錄僅由平台伺服器訪問，而不由映像伺服器訪問。 目錄屬性檔案必須有。ini尾碼，並放在平台伺服器的目錄資料夾(`PS::CatalogFolder`)中。 至少需要預設映像目錄，並且必須填入所有屬性才能使平台伺服器正常工作。
