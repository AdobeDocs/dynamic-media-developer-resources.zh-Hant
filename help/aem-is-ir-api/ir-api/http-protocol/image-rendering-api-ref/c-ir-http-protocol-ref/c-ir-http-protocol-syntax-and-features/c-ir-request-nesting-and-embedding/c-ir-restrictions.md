---
description: 巢狀和內嵌會受到一些限制。
solution: Experience Manager
title: 限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# 限制{#restrictions}

巢狀和內嵌會受到一些限制。

為獲得良好的伺服器效能，巢狀請求傳回的影像解析度應合理符合所套用材質之物件的紋理解析度。

外來影像會快取至本機。 只有在本機快取項目失效（根據過期的HTTP標題）後，才會偵測到此類影像的任何變更。
