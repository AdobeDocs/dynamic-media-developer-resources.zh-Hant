---
description: 將這些伺服器設定用於映像目錄服務。
solution: Experience Manager
title: 映像目錄服務
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# 映像目錄服務{#image-catalog-service}

將這些伺服器設定用於映像目錄服務。

## CS::catalog.rootPath — 映像目錄資料夾 {#section-02d107f157384b18835f884f24fea3aa}

影像目錄資料夾的位置(其中所有 [!DNL catalog.ini] 必須找到檔案)。 可以是絕對檔案路徑或相對於 *[!DNL install_folder]*。 伺服器會連續監視此資料夾，並在新主目錄檔案(使用 [!DNL .ini] 檔案尾碼)，或現有主目錄檔案的上次修改時間已更改時檢測到。

## CS::catalog.cacheRoot — 目錄快取資料夾 {#section-73e499c3a5974f1aa4251e70272ff503}

目錄系統快取的根資料夾。 可以設定為與中的某個資料夾相同 `PS::cache.rootPaths`。 更改此設定之前必須手動建立資料夾。

## CS::catalog.modificationWaitTime — 目錄檔案分析延遲 {#section-7348065bcc124cb68ea947bf1b9b0845}

目錄服務在 [!DNL catalog.ini] 檔案被更改，直到它載入輔助目錄檔案。 此延遲有助於確保所有輔助目錄檔案在目錄服務嘗試載入它們之前都是最新的。 整數值（毫秒）。

## CS::catalog.refreshInterval — 目錄檔案檢查頻率 {#section-517fefc1d8784777a1026abec8630d58}

目錄服務檢查對映像目錄的更改的頻率。 整數值（毫秒）。
