---
description: 在巢狀/內嵌請求中指定cache=on ，可以快取巢狀/內嵌影像提供與影像演算請求產生的中間影像資料。 此資料會以專屬格式儲存在回應資料快取中。
solution: Experience Manager
title: 輔助資料快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: 'https://experienceleague.adobe.com/oRZFSXKaBE9q7liBPRVCheL-NPTriPJkWZFqgMBcoaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# 輔助資料快取{#auxiliary-data-caches}

在巢狀/內嵌請求中指定cache=on ，可以快取巢狀/內嵌影像提供與影像演算請求產生的中間影像資料。 此資料會以專屬格式儲存在回應資料快取中。

從外部HTTP伺服器取得的影像也會儲存在回應資料快取中。 產生快取專案之前，會先使用驗證公用程式自動驗證這類影像。

[!DNL Platform Server]會編譯影像目錄資料，以有效存取。 此資料儲存在`CS::CatalogCacheFolder`中。
