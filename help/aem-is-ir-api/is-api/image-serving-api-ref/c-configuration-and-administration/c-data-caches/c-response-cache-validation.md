---
description: 使用基於目錄或基於過期的快取驗證自動刷新快取條目，這與屬性CacheValidationPolicy（預設為.ini或特定映像目錄的.ini檔案）一起選擇。
solution: Experience Manager
title: 響應快取驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 響應快取驗證{#response-cache-validation}

使用基於目錄或基於過期的快取驗證自動刷新快取條目，如與屬性：:CacheValidationPolicy（在default.ini或特定映像目錄的.ini檔案中）一起選擇。

使用基於目錄的驗證，如果現有快取條目在 `catalog::LastModified` 或 `attribute::LastModified`，或 [!DNL catalog.ini] 檔案)比建立快取項的時間更新。

使用基於過期的驗證，自最近的驗證以來，快取項在5分鐘後變為陳舊。 在這兩種情況下，伺服器通過檢查與建立請求相關的所有映像檔案的檔案日期來驗證過時的快取條目。 如果檔案日期未更改，則更新快取項的時間戳，並且快取日期被視為有效。

對於通常涉及在影像目錄中註冊的影像的典型應用程式，基於目錄的驗證提供了效能優勢。 不涉及映像目錄的應用程式應使用基於過期的快取驗證。 實現這一目標的一種方法是 `attribute::cacheValidationPolicy=0` 在 [!DNL default.ini], `1` 所有特定映像目錄檔案中。

當請求中涉及的目錄條目以可能導致回復映像更改的方式發生更改時，快取條目將變為無效，並且可能會重新生成。 例如， `catalog::Modifier` 更改。

>[!NOTE]
>
>Dynamic Media金字塔TIFF(PTIFF)影像在檔案頭中內部維護檔案日期，以供驗證。 檔案系統維護的檔案修改時間用於檢查非PTIFF檔案是否已更改。

只有影像檔案參與快取驗證過程。 對字型檔案或ICC配置檔案的更改不會導致快取項的自動無效。
