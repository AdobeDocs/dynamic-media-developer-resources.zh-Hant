---
description: 影像目錄提供許多伺服器組態設定，以及字型、ICC設定檔、指令巨集。
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

影像目錄提供許多伺服器組態設定，以及字型、ICC設定檔、指令巨集。

這些功能會將要求中使用的影像和靜態內容ID對應至實際檔案路徑、儲存各種影像中繼資料（例如影像地圖），並提供範本和影像集的容器。

影像目錄只能由[!DNL Platform Server]存取，不能由影像伺服器存取。 目錄屬性檔案必須有.ini尾碼，並且置於[!DNL Platform Server]的目錄資料夾( `PS::CatalogFolder`)。 至少需要預設影像目錄，且必須填入所有屬性，才能使[!DNL Platform Server]正確運作。
