---
title: 不建議使用的呼叫
description: 不再用於Dynamic Media的影像製作系統API呼叫及其相關參數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# 不建議使用的呼叫{#deprecated-calls}

不再使用的影像生產系統API呼叫及其相關參數。

## 不建議使用的呼叫{#topic-654c0466e6434fe4a95953322255b08c}

不再用於Dynamic Media的影像製作系統API呼叫及其相關參數。

* `addMediaPortalEvent` -已從操作中淘汰。此呼叫可讓您將媒體入口事件新增至IPS。
* `getMediaPortalEvent` -已從操作中淘汰。此呼叫可讓您取得符合指定條件的媒體入口網站事件。
* `getCdnCacheInvalidationStatus` -已從操作中淘汰。此API現在已停用，因為`cdnCacheInvalidation` API幾乎立即使快取失效（~5秒）。 因此，不再需要輪詢失效狀態。

