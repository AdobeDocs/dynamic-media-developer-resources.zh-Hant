---
description: 這是主要記錄檔，可追蹤對平台伺服器發出的所有HTTP要求。 如果啟用，則將其訪問日誌資料寫入同一檔案。
seo-description: 這是主要記錄檔，可追蹤對平台伺服器發出的所有HTTP要求。 如果啟用，則將其訪問日誌資料寫入同一檔案。
seo-title: 存取記錄
solution: Experience Manager
title: 存取記錄
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# 存取記錄{#access-log}

這是主要記錄檔，可追蹤對平台伺服器發出的所有HTTP要求。 如果啟用，則將其訪問日誌資料寫入同一檔案。

存取記錄檔是在server.xml中設定。

>[!NOTE]
>
>除了影像伺服( [!DNL /is/image/*])和影像演算( [!DNL /ir/render/*])的用戶端流量外，存取記錄可能包含某些內部流量： 存取平台伺服器目錄系統( [!DNL /is-catalog/*])、快取共用和錯誤重新導向要求( [!DNL /is/cache/*])、存取部署至平台伺服器的其他封裝，例如Scene7檢視器( [!DNL /is-viewers/*])、靜態流量和靜態內容要求(例如，平台伺服器所提供的 [!DNL /is-docs/*])。

具有和根 [!DNL /is-catalog] 路徑 [!DNL /is/cache] 的請求應一律排除在任何用戶端流量分析之外。
