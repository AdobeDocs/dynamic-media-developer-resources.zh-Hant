---
description: 所有日誌檔案都寫入到TC目錄指定的同一日誌資料夾中。
solution: Experience Manager
title: 伺服器日誌
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# 伺服器日誌{#server-logging}

所有日誌檔案都寫入到TC::directory指定的同一日誌資料夾中。

日誌檔案通常每天建立和輪替。 日誌資料夾中較舊的日誌檔案將在指定天數後自動刪除( `TC::maxDays`)。

重要資訊：必須為日誌檔案保留足夠的磁碟空間，以避免磁碟空間耗盡。 對於使用頻繁的伺服器和預設日誌設定，可能需要1-2 GB/天。

的 [!DNL Platform Server] 並且Image Server會建立下面描述的三種類型的日誌檔案。

其他Image Service元件和某些其他Dynamic Media包(如Dynamic Media查看器)也可能在同一資料夾中建立日誌檔案。 這些日誌檔案供Dynamic Media內部使用，可能由Dynamic Media技術支援部門請求，用於解決問題。

* [訪問日誌](c-access-log.md)
* [跟蹤日誌](c-trace-log.md)
* [映像伺服器日誌](c-image-server-log.md)

## 另請參閱 {#section-5ff5e46031b1461c92de24e632610d6d}

[訪問日誌記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)。 [調試/跟蹤日誌記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
