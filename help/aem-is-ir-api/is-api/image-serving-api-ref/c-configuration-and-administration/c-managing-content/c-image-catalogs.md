---
description: 影像目錄提供了許多伺服器配置設定，以及字型、ICC配置檔案和命令宏。
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

影像目錄提供了許多伺服器配置設定，以及字型、ICC配置檔案和命令宏。

它們將請求中使用的影像和靜態內容ID映射到實際檔案路徑，儲存各種影像元資料，並為模板和影像集提供容器。

僅由 [!DNL Platform Server]，從未通過映像伺服器。 目錄屬性檔案必須具有.ini尾碼，並放在 [!DNL Platform Server]&#39;s目錄資料夾( `PS::CatalogFolder`)。 至少需要預設映像目錄，並且必須使用所有屬性填充，才能正確運行 [!DNL Platform Server]。
