---
description: 這是主要記錄，可追蹤對 [!DNL Platform Server]. 如果已啟用「影像呈現」，則會將其存取記錄資料寫入相同的檔案。
solution: Experience Manager
title: 訪問日誌
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 訪問日誌{#access-log}

這是主要記錄，可追蹤對 [!DNL Platform Server]. 如果已啟用「影像呈現」，則會將其存取記錄資料寫入相同的檔案。

訪問日誌是在server.xml中配置的。

>[!NOTE]
>
>除了影像服務的用戶端流量( [!DNL /is/image/*])和影像轉譯( [!DNL /ir/render/*])，則存取記錄可能會包含某些內部流量：存取 [!DNL Platform Server] 目錄系統( [!DNL /is-catalog/*])、快取共用和錯誤重新導向請求( [!DNL /is/cache/*])，存取部署至的其他套件 [!DNL Platform Server]，例如Dynamic Media檢視器( [!DNL /is-viewers/*])、靜態流量和靜態內容要求 [!DNL Platform Server] (例如 [!DNL /is-docs/*])。

請求 [!DNL /is-catalog] 和 [!DNL /is/cache] 根路徑應一律從任何用戶端流量分析中排除。
