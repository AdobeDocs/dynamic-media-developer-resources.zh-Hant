---
title: 已棄用的呼叫
description: 不再使用或支援的影像生產系統API呼叫及其相關參數 [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 已棄用的呼叫{#deprecated-calls}

不再使用的影像生產系統API呼叫及其相關參數。

## 已棄用的呼叫 {#topic-654c0466e6434fe4a95953322255b08c}

不再使用的影像生產系統API呼叫及其相關參數 [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS`  — 已從 [資料類型](/help/aem-ips-api/types/c-data-types/c-data-types.md). 此參數會從最適化視訊集中排除主要視訊。 <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent`  — 已從 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 此參數可讓您將Media Portal事件新增至IPS。
* `getMediaPortalEvent`  — 已從 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 此參數可讓您取得符合指定條件的媒體入口網站事件。
* `getCdnCacheInvalidationStatus`  — 已從 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 此參數現已淘汰，因為 `cdnCacheInvalidation` 參數幾乎會立即讓快取失效（~5秒）。 因此，無效狀態的輪詢不再需要。
