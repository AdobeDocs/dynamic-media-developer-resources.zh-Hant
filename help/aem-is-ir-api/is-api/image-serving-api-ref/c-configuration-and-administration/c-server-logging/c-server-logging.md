---
description: 所有日誌檔案都寫入到與TC目錄指定的同一日誌資料夾中。
solution: Experience Manager
title: 伺服器記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# 伺服器記錄{#server-logging}

所有日誌檔案都寫入到與TC::directory指定的同一日誌資料夾中。

記錄檔通常會每天建立和旋轉。 在指定的天數(`TC::maxDays`)後，會自動刪除日誌資料夾中較舊的日誌檔案。

重要資訊必須為日誌檔案保留足夠的磁碟空間，以避免磁碟空間耗盡。 使用頻繁的伺服器和預設日誌設定可能需要1-2 GB/天。

平台伺服器和映像伺服器建立以下三種類型的日誌檔案。

其他影像伺服元件和某些其他Dynamic Media套件(例如Dynamic Media檢視器)也可能會在相同的資料夾中建立記錄檔。 這些記錄檔供Dynamic Media內部使用，且可能由Dynamic Media技術支援請求以疑難排解。

* [訪問日誌](c-access-log.md)
* [跟蹤日誌](c-trace-log.md)
* [映像伺服器日誌](c-image-server-log.md)

## 另請參閱 {#section-5ff5e46031b1461c92de24e632610d6d}

[存取記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、除 [錯/追蹤記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
