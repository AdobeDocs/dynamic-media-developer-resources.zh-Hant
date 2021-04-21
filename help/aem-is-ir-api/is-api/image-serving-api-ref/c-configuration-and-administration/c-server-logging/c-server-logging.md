---
description: 所有日誌檔案都寫入到與TC目錄指定的同一日誌資料夾中。
solution: Experience Manager
title: 伺服器記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# 伺服器日誌{#server-logging}

所有日誌檔案都寫入到與TC::directory指定的同一日誌資料夾中。

記錄檔通常是每日建立和旋轉。 在指定的天數(`TC::maxDays`)後，日誌資料夾中較舊的日誌檔案將自動刪除。

重要資訊：必須為日誌檔案保留足夠的磁碟空間，以避免磁碟空間不足。 對於使用頻繁的伺服器和預設日誌設定，每天可能需要1-2 GB。

平台伺服器和映像伺服器建立以下描述的三種類型的日誌檔案。

其他影像伺服元件和某些其他Dynamic Media封裝(例如Dynamic Media檢視器)也可能會在相同的資料夾中建立記錄檔。 這些日誌檔案供Dynamic Media內部使用，Dynamic Media技術支援可能會要求這些日誌檔案用於故障排除。

* [存取記錄](c-access-log.md)
* [跟蹤日誌](c-trace-log.md)
* [影像伺服器記錄檔](c-image-server-log.md)

## 另請參閱 {#section-5ff5e46031b1461c92de24e632610d6d}

[存取記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、除 [錯／追蹤記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
