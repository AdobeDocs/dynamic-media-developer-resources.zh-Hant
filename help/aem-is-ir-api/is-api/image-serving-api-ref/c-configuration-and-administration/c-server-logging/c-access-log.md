---
description: 這是主要記錄檔，可追蹤對Platform伺服器提出的所有HTTP要求。 如果已啟用「影像呈現」，則會將其存取記錄資料寫入相同的檔案。
solution: Experience Manager
title: 訪問日誌
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 訪問日誌{#access-log}

這是主要記錄檔，可追蹤對Platform伺服器提出的所有HTTP要求。 如果已啟用「影像呈現」，則會將其存取記錄資料寫入相同的檔案。

訪問日誌是在server.xml中配置的。

>[!NOTE]
>
>除了影像服務([!DNL /is/image/*])和影像呈現([!DNL /ir/render/*])的用戶端流量外，訪問日誌還可能包括某些內部流量：存取平台伺服器目錄系統([!DNL /is-catalog/*])、快取共用和錯誤重新導向請求([!DNL /is/cache/*])、存取部署至平台伺服器的其他套件，例如Dynamic Media檢視器([!DNL /is-viewers/*])、靜態流量和平台伺服器所服務的靜態內容請求(例如[!DNL /is-docs/*])。

具有[!DNL /is-catalog]和[!DNL /is/cache]根路徑的請求應一律從任何用戶端流量分析中排除。
