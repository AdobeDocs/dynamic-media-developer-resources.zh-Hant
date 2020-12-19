---
description: 不再使用的影像生產系統API呼叫及其相關參數。
seo-description: 不再使用的影像生產系統API呼叫及其相關參數。
seo-title: 不建議使用的呼叫
solution: Experience Manager
title: 不建議使用的呼叫
topic: Scene7 Image Production System API
uuid: 03925728-f011-45f0-84a6-808dff0fd529
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# 不建議使用的呼叫{#deprecated-calls}

不再使用的影像生產系統API呼叫及其相關參數。

## 不建議使用的呼叫{#topic-654c0466e6434fe4a95953322255b08c}

不再使用的影像生產系統API呼叫及其相關參數。

* `addMediaPortalEvent` -已從操作中淘汰。此呼叫可讓您將媒體入口事件新增至IPS。
* `getMediaPortalEvent` -已從操作中淘汰。此呼叫可讓您取得符合指定條件的媒體入口網站事件。
* `getCdnCacheInvalidationStatus` -已從操作中淘汰。此API現在已停用，因為`cdnCacheInvalidation` API幾乎立即使快取失效（~5秒）。 因此，不再需要輪詢失效狀態。

