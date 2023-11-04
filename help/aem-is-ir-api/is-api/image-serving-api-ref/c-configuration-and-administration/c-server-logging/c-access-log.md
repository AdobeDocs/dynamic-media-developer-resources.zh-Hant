---
description: 這是主要記錄檔，會追蹤對 [!DNL Platform Server]. 影像演算（如啟用）會將其存取記錄檔資料寫入相同檔案。
solution: Experience Manager
title: 存取記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 存取記錄{#access-log}

這是主要記錄檔，會追蹤對 [!DNL Platform Server]. 影像演算（如啟用）會將其存取記錄檔資料寫入相同檔案。

存取記錄檔是在server.xml中設定。

>[!NOTE]
>
>除了影像伺服的使用者端流量以外( [!DNL /is/image/*])和影像演算( [!DNL /ir/render/*])，則存取記錄檔可能包含特定內部流量：存取 [!DNL Platform Server] 目錄系統( [!DNL /is-catalog/*])，快取共用和錯誤重新導向要求( [!DNL /is/cache/*])，存取部署至的其他套件 [!DNL Platform Server]，例如Dynamic Media Viewers ( [!DNL /is-viewers/*])、靜態流量和靜態內容請求，服務對象為 [!DNL Platform Server] (例如， [!DNL /is-docs/*])。

請求 [!DNL /is-catalog] 和 [!DNL /is/cache] 根路徑應一律從任何使用者端流量分析中排除。
