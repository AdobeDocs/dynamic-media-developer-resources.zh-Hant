---
description: 當空閒Java堆空間在緊接Java廢棄項目收集週期後的指定閾值以下時，會發送優先順序警報。
seo-description: 當空閒Java堆空間在緊接Java廢棄項目收集週期後的指定閾值以下時，會發送優先順序警報。
seo-title: 堆空間優先順序警報
solution: Experience Manager
title: 堆空間優先順序警報
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 堆空間優先順序警報{#heap-space-priority-alert}

當空閒Java堆空間在緊接Java廢棄項目收集週期後的指定閾值以下時，會發送優先順序警報。

應通過增加Java堆空間來解決重複警報。 此條件的後續發生，直到指定的延遲期過期，才會產生電子郵件 `AS::monitorAlertGenerator.heapSpaceResetInterval` 警報。
