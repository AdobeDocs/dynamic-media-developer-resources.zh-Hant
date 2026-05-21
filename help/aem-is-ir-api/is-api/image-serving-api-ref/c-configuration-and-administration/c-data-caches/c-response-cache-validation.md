---
description: 使用目錄型或過期型快取驗證來自動重新整理快取專案，如使用屬性CacheValidationPolicy所選取（在default.ini或特定影像目錄的.ini檔案中）。
solution: Experience Manager
title: 回應快取驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
TQID: 'https://experienceleague.adobe.com/VnvYNkc3yijayG8tnJKHsp94Qto8VZj9OkIgfIv1Kc0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 311
ht-degree: 0%

---

# 回應快取驗證{#response-cache-validation}

使用目錄型或過期型快取驗證來自動重新整理快取專案，如使用attribute：：CacheValidationPolicy （在default.ini或特定影像目錄的.ini檔案中）所選取。

使用目錄式驗證，如果`catalog::LastModified` （或`attribute::LastModified`，或[!DNL catalog.ini]檔案的檔案修改時間）比建立快取專案的時間更晚，則會將現有的快取專案視為過時。

使用過期基礎驗證，快取專案在距最近一次驗證後5分鐘後會過時。 在這兩種情況下，伺服器都會檢查與建立請求有關的所有影像檔案的檔案日期，以驗證過時的快取專案。 如果檔案日期未變更，則會更新快取專案的時間戳記，並將快取日期視為有效。

對於主要涉及在影像目錄中註冊的影像的典型應用程式，目錄型驗證可提供效能優勢。 不涉及影像目錄的應用程式應使用過期快取驗證。 其中一個方法是在[!DNL default.ini]中設定`attribute::cacheValidationPolicy=0`，並在所有特定影像目錄檔案中設定`1`。

快取專案會變成無效，而且當請求中涉及的目錄專案變更，而可能導致回覆影像變更時，可能會重新產生。 例如，`catalog::Modifier`的內容已變更。

>[!NOTE]
>
>Dynamic Media金字塔TIFF (PTIFF)影像會在內部維護檔案標題中的檔案日期，以供驗證之用。 檔案系統維護的檔案修改時間可用來檢查非PTIFF檔案是否已變更。

只有影像檔案會參與快取驗證程式。 變更字型檔案或ICC設定檔不會造成快取專案自動失效。
