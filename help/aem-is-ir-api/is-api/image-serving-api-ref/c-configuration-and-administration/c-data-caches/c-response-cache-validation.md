---
description: 使用基於目錄或基於過期的快取驗證自動刷新快取條目，如同使用屬性CacheValidationPolicy（預設為。ini或特定映像目錄的。ini檔案）選擇的一樣。
seo-description: 使用基於目錄或基於過期的快取驗證自動刷新快取條目，如同使用屬性CacheValidationPolicy（預設為。ini或特定映像目錄的。ini檔案）選擇的一樣。
seo-title: 回應快取驗證
solution: Experience Manager
title: 回應快取驗證
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# 回應快取驗證{#response-cache-validation}

使用基於目錄或基於過期的快取驗證自動刷新快取條目，如與屬性：:CacheValidationPolicy（預設。ini或特定映像目錄的。ini檔案中）一起選擇。

使用基於目錄的驗證，如果 `catalog::LastModified` (或 `attribute::LastModified`[!DNL catalog.ini] ，或檔案的檔案修改時間)比建立快取條目時間更近，則現有快取條目會被視為過時。

使用基於過期的驗證，快取項目自最近的驗證後5分鐘後即會過期。 在這兩種情況下，伺服器都會檢查與建立請求相關的所有影像檔案的檔案日期，以驗證過時的快取項目。 如果檔案日期未變更，則會更新快取項目的時間戳記，且快取日期視為有效。

對於通常涉及在影像目錄中註冊的影像的應用程式，型錄式驗證可提供效能優勢。 不涉及影像型錄的應用程式應使用過期快取驗證。 要達到此目的，一個方法是在所 `attribute::cacheValidationPolicy=0` 有特 [!DNL default.ini]定的影像 `1` 目錄檔案中設定。

快取項目會變為無效，且當請求中涉及的目錄項目變更時，可能會導致回覆影像變更，快取項目可能會重新產生。 例如，變更的內 `catalog::Modifier` 容。

>[!NOTE]
>
>Scene7金字塔TIFF(PTIFF)影像會在檔案標題中內部維護檔案日期，以利驗證。 檔案系統維護的檔案修改時間用於檢查非PTIFF檔案是否已更改。

只有影像檔案會參與快取驗證程式。 字型檔或ICC描述檔的變更不會導致快取項目自動失效。
