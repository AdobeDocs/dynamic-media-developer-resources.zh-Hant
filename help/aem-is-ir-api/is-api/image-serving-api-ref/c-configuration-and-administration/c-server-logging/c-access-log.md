---
description: 這是主日誌，用於跟蹤向 [!DNL Platform Server]。 如果啟用，則影像呈現會將其訪問日誌資料寫入同一檔案。
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

這是主日誌，用於跟蹤向 [!DNL Platform Server]。 如果啟用，則影像呈現會將其訪問日誌資料寫入同一檔案。

訪問日誌在server.xml中配置。

>[!NOTE]
>
>除了用於映像服務的客戶端流量( [!DNL /is/image/*])和影像呈現( [!DNL /ir/render/*])，訪問日誌可能包括某些內部通信：訪問 [!DNL Platform Server] 目錄系統 [!DNL /is-catalog/*])、快取共用和錯誤重定向請求( [!DNL /is/cache/*])，訪問部署到 [!DNL Platform Server]比如Dynamic Media觀眾， [!DNL /is-viewers/*])、靜態通信和靜態內容請求 [!DNL Platform Server] (例如 [!DNL /is-docs/*])。

請求 [!DNL /is-catalog] 和 [!DNL /is/cache] 根路徑應始終從任何客戶端流量分析中排除。
