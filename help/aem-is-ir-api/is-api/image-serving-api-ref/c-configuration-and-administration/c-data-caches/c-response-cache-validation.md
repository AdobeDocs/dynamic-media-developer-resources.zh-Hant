---
description: 使用屬性CacheValidationPolicy（在預設.ini中，或特定影像目錄的.ini檔案中）選擇的基於目錄或基於過期的快取驗證自動刷新快取條目。
solution: Experience Manager
title: 響應快取驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 響應快取驗證{#response-cache-validation}

使用屬性：:CacheValidationPolicy（在預設.ini中，或特定影像目錄的.ini檔案中）選擇的基於目錄或基於過期的快取驗證自動刷新快取條目。

使用基於目錄的驗證時，如果`catalog::LastModified`（或`attribute::LastModified`，或[!DNL catalog.ini]檔案的檔案修改時間）比建立快取項的時間更近，則現有快取項將被視為過時。

透過過期驗證，自最新驗證以來的5分鐘後，快取項目會過時。 在這兩種情況下，伺服器都會檢查與建立請求相關的所有影像檔案的檔案日期，以驗證過時的快取項目。 如果檔案日期未更改，則更新快取條目的時間戳，並且快取日期被視為有效。

對於通常的應用程式（大多涉及在映像目錄中註冊的映像），基於目錄的驗證提供了效能優勢。 不涉及影像目錄的應用程式應使用基於過期的快取驗證。 實現此目標的一個方法是在[!DNL default.ini]中設定`attribute::cacheValidationPolicy=0`，並在所有特定影像目錄檔案中設定`1`。

當請求中涉及的目錄項目以可能導致答復影像更改的方式發生更改時，快取項將變為無效，並且可能會重新生成。 例如，`catalog::Modifier`的內容會變更。

>[!NOTE]
>
>Dynamic Media金字塔TIFF(PTIFF)影像會在檔案標題中內部維護檔案日期，以供驗證之用。 檔案系統維護的檔案修改時間用於檢查非PTIFF檔案是否已更改。

只有影像檔案參與快取驗證過程。 對字型檔案或ICC配置檔案的更改不會導致快取項的自動失效。
