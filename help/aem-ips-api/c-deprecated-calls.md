---
title: 不建議使用的調用
description: 在Dynamic Media不再使用或支援的映像生產系統API調用及其關聯參數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# 不建議使用的調用{#deprecated-calls}

不再使用的映像生產系統API調用及其關聯參數。

## 不建議使用的調用 {#topic-654c0466e6434fe4a95953322255b08c}

不再在Dynamic Media使用的映像生產系統API調用及其關聯參數。

* `ExcludeMasterVideoFromAVS`  — 不建議使用 [資料類型](/help/aem-ips-api/types/c-data-types/c-data-types.md)。 此參數從自適應視頻集中排除主視頻。
   >[!IMPORTANT]
   >
   >Adobe將於2022年9月1日終止對此參數的支援。 另請參閱 [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md)。
* `addMediaPortalEvent`  — 不建議使用 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)。 此參數允許您將媒體入口事件添加到IPS。
* `getMediaPortalEvent`  — 不建議使用 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)。 通過此參數，可以獲取符合指定條件的媒體門戶事件。
* `getCdnCacheInvalidationStatus`  — 不建議使用 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)。 此參數現在已棄用，因為 `cdnCacheInvalidation` 參數幾乎立即使快取失效（約5秒）。 因此，不再需要輪詢無效狀態。
