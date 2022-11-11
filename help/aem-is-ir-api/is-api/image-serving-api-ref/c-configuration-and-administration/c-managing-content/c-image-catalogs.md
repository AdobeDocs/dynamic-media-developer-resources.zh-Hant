---
description: 影像目錄提供許多伺服器配置設定，以及字型、ICC配置檔案、命令宏。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 影像目錄{#image-catalogs}

影像目錄提供許多伺服器配置設定，以及字型、ICC配置檔案、命令宏。

它們會將請求中使用的影像和靜態內容ID對應至實際的檔案路徑、儲存各種影像中繼資料（例如影像地圖），以及為範本和影像集提供容器。

影像目錄僅由 [!DNL Platform Server]，而不是透過影像伺服器。 目錄屬性檔案必須有.ini尾碼，並放置在 [!DNL Platform Server]&#39;s目錄資料夾( `PS::CatalogFolder`)。 至少需要預設影像目錄，並且必須填入所有屬性，才能正確運作 [!DNL Platform Server].
