---
description: 將這些伺服器設定用於影像目錄服務。
solution: Experience Manager
title: 影像目錄服務
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# 影像目錄服務{#image-catalog-service}

將這些伺服器設定用於影像目錄服務。

## CS：：catalog.rootPath — 影像目錄資料夾 {#section-02d107f157384b18835f884f24fea3aa}

影像目錄資料夾的位置（必須位於所有[!DNL catalog.ini]檔案的位置）。 可以是絕對檔案路徑或相對於&#x200B;*[!DNL install_folder]*&#x200B;的路徑。 伺服器會持續監視此資料夾，並在偵測到新的主目錄檔案（具有[!DNL .ini]檔案字尾）或現有主目錄檔案的上次修改時間已變更時，載入或重新載入目錄。

## CS：：catalog.cacheRoot — 目錄快取資料夾 {#section-73e499c3a5974f1aa4251e70272ff503}

目錄系統快取的根資料夾。 可設定為與`PS::cache.rootPaths`中的其中一個資料夾相同。 在變更此設定之前，必須先手動建立資料夾。

## CS：：catalog.modificationWaitTime — 目錄檔案剖析延遲 {#section-7348065bcc124cb68ea947bf1b9b0845}

[!DNL catalog.ini]檔案變更後，目錄服務等待的時間（毫秒），直到載入次要目錄檔案為止。 此延遲有助於確保所有次要目錄檔案在目錄服務嘗試載入之前都是最新的。 以毫秒為單位的整數值。

## CS：：catalog.refreshInterval — 目錄檔案檢查頻率 {#section-517fefc1d8784777a1026abec8630d58}

目錄服務檢查影像目錄變更的頻率。 以毫秒為單位的整數值。
