---
description: 所有日誌檔案都寫入到與TC目錄指定的同一日誌資料夾中。
seo-description: 所有日誌檔案都寫入到與TC目錄指定的同一日誌資料夾中。
seo-title: 伺服器記錄
solution: Experience Manager
title: 伺服器記錄
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3

---


# 伺服器記錄{#server-logging}

所有日誌檔案都寫入到與TC::directory指定的同一日誌資料夾中。

記錄檔通常是每日建立和旋轉。 在指定的天數()後，會自動刪除日誌資料夾中較舊的日誌檔案。 `TC::maxDays`

重要資訊：必須為日誌檔案保留足夠的磁碟空間，以避免磁碟空間不足。 對於使用頻繁的伺服器和預設日誌設定，每天可能需要1-2 GB。

平台伺服器和映像伺服器建立以下描述的三種類型的日誌檔案。

其他Image Serving元件和某些其他Scene7套件（例如Scene7檢視器）也可能會在相同的檔案夾中建立記錄檔。 這些記錄檔是供Scene7內部使用，Scene7支援可能會要求這些記錄檔以排除故障。

* [存取記錄](c-access-log.md)
* [跟蹤日誌](c-trace-log.md)
* [影像伺服器記錄檔](c-image-server-log.md)

## 另請參閱 {#section-5ff5e46031b1461c92de24e632610d6d}

[存取記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、除 [錯／追蹤記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
