---
description: 包含與管理影像目錄相關的設定。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
TQID: 'https://experienceleague.adobe.com/GdtVY3WMO9F6C5vzkOHdVoMW-f6-L1cJGUt1KUCvLJ8'
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
source-wordcount: 113
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

包含與管理影像目錄相關的設定。

此檔案是JAVA屬性檔案。 請務必遵循適當的慣例；否則[!DNL Platform Server]可能無法啟動。 在Windows檔案路徑中使用雙反斜線&#39;\\&#39;或單正斜線&#39;/&#39;，而非反斜線&#39;\&#39;。 在此型別的檔案中，反斜線會作為逸出字元使用。

對此檔案的變更會在檔案儲存後不久生效。

只有下列設定可以在[!DNL catalog-service.conf]中變更。 如果特定設定不存在，則可以在檔案中的任意位置新增該設定。 每個設定只能有一個執行個體。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
