---
description: 這是主要記錄檔，會追蹤對 [!DNL Platform Server]發出的所有HTTP要求。 影像演算（如啟用）會將其存取記錄檔資料寫入相同檔案。
solution: Experience Manager
title: 存取記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# 存取記錄{#access-log}

這是主要記錄檔，會追蹤對[!DNL Platform Server]發出的所有HTTP要求。 影像演算（如啟用）會將其存取記錄檔資料寫入相同檔案。

存取記錄檔是在server.xml中設定。

>[!NOTE]
>
>除了影像伺服( [!DNL /is/image/*])和影像轉譯( [!DNL /ir/render/*])的使用者端流量之外，存取記錄檔還可能包含某些內部流量：存取[!DNL Platform Server]目錄系統( [!DNL /is-catalog/*])、快取共用和錯誤重新導向要求( [!DNL /is/cache/*])、存取部署至[!DNL Platform Server]的其他套件，例如Dynamic Media檢視器( [!DNL /is-viewers/*])、由[!DNL Platform Server]服務的靜態流量和靜態內容要求（例如[!DNL /is-docs/*]）。

具有[!DNL /is-catalog]和[!DNL /is/cache]根路徑的請求應該一律從任何使用者端流量分析中排除。
