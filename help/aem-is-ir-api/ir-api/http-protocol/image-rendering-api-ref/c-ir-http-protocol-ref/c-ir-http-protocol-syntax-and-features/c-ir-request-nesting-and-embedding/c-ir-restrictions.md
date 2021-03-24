---
description: 巢狀和內嵌會受到一些限制。
solution: Experience Manager
title: 限制
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# 限制{#restrictions}

巢狀和內嵌會受到一些限制。

為獲得良好的伺服器效能，巢狀請求傳回的影像解析度應合理符合所套用材質之物件的紋理解析度。

外來影像會快取至本機。 只有在本機快取項目失效（根據過期的HTTP標題）後，才會偵測到此類影像的任何變更。
