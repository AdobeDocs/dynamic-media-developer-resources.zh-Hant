---
description: 嵌套和嵌入時有一些限制。
solution: Experience Manager
title: 限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# 限制{#restrictions}

嵌套和嵌入時有一些限制。

為了獲得良好的伺服器效能，嵌套請求返回的影像的解析度應與應用材料的對象的紋理解析度合理匹配。

本地快取外來映像。 只有在本機快取項目過時（根據過期的HTTP標題）後，才會偵測對這類影像的任何變更。
