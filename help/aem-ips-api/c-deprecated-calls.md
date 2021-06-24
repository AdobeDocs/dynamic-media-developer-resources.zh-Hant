---
title: 已棄用的呼叫
description: 不再用於Dynamic Media的影像生產系統API呼叫及其相關參數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 已棄用的呼叫{#deprecated-calls}

不再使用的影像生產系統API呼叫及其相關參數。

## 已棄用的呼叫 {#topic-654c0466e6434fe4a95953322255b08c}

不再用於Dynamic Media的影像生產系統API呼叫及其相關參數。

* `addMediaPortalEvent`  — 已從操作中淘汰。此呼叫可讓您將Media Portal事件新增至IPS。
* `getMediaPortalEvent`  — 已從操作中淘汰。此呼叫可讓您取得符合指定條件的媒體入口網站事件。
* `getCdnCacheInvalidationStatus`  — 已從操作中淘汰。此API現已淘汰，因為`cdnCacheInvalidation` API幾乎立即讓快取失效（~5秒）。 因此，無效狀態的輪詢不再需要。
