---
title: 已棄用的呼叫
description: ' [!DNL Dynamic Media]不再使用或支援的影像生產系統API呼叫及其相關引數。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
autotag-review: '2026-05-13T21:03:57.183Z'
TQID: 'https://experienceleague.adobe.com/JLoyXksHQ-LAXXxfY71Dv-FOE0trpt-RzcKcV-Pv96I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# 已棄用的呼叫{#deprecated-calls}

不再使用的影像生產系統API呼叫及其相關引數。

## 已棄用的呼叫 {#topic-654c0466e6434fe4a95953322255b08c}

[!DNL Dynamic Media]中不再使用的影像生產系統API呼叫及其相關引數。

* `ExcludeMasterVideoFromAVS` — 已由[資料型別](/help/aem-ips-api/types/c-data-types/c-data-types.md)取代。 此引數會從最適化視訊集中排除主要視訊。<!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` — 已由[Operations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)取代。 此引數可讓您將Media Portal事件新增至IPS。
* `getMediaPortalEvent` — 已由[Operations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)取代。 此引數可讓您取得符合指定條件的Media Portal事件。
* `getCdnCacheInvalidationStatus` — 已由[Operations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)取代。 此引數現已棄用，因為`cdnCacheInvalidation`引數幾乎會立即讓快取失效（~5秒）。 因此，不再需要輪詢失效狀態。

