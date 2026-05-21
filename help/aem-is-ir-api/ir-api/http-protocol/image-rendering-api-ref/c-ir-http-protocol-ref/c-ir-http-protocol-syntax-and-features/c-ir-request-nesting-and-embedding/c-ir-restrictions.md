---
title: 限制
description: 巢狀和內嵌有一些限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# 限制{#restrictions}

巢狀和內嵌有一些限制。

為獲得良好的伺服器效能，巢狀要求傳回的影像解析度應適當地符合套用材質的物件的紋理解析度。

外部影像會快取到本機。 只有在本機快取專案過時後（根據expires HTTP標頭），才會偵測到這類影像的任何變更。
