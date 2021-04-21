---
description: 請為映像目錄服務使用這些伺服器設定。
solution: Experience Manager
title: 影像目錄服務
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 映像目錄服務{#image-catalog-service}

請為映像目錄服務使用這些伺服器設定。

## CS::catalog.rootPath - Image Catalog資料夾{#section-02d107f157384b18835f884f24fea3aa}

映像目錄資料夾的位置（所有[!DNL catalog.ini]檔案必須位於其中）。 可以是絕對檔案路徑或相對於&#x200B;*[!DNL install_folder]*&#x200B;的路徑。 當檢測到新的主目錄檔案（具有[!DNL .ini]檔案尾碼）或當現有主目錄檔案的上次修改時間改變時，伺服器會持續監視該資料夾並載入或重新載入目錄。

## CS::catalog.cacheRoot —— 目錄快取資料夾{#section-73e499c3a5974f1aa4251e70272ff503}

目錄系統快取的根資料夾。 可以設定為與`PS::cache.rootPaths`中的一個資料夾相同。 必須先手動建立資料夾，才能更改此設定。

## CS::catalog.modificationWaitTime —— 目錄檔案解析延遲{#section-7348065bcc124cb68ea947bf1b9b0845}

目錄服務在[!DNL catalog.ini]檔案更改後等待的時間（以毫秒為單位），直到它載入輔助目錄檔案。 此延遲有助於確保所有輔助目錄檔案在目錄服務嘗試載入之前都是最新的。 以毫秒為單位的整數值。

## CS::catalog.refreshInterval —— 目錄檔案檢查頻率{#section-517fefc1d8784777a1026abec8630d58}

目錄服務檢查影像目錄變更的頻率。 以毫秒為單位的整數值。
