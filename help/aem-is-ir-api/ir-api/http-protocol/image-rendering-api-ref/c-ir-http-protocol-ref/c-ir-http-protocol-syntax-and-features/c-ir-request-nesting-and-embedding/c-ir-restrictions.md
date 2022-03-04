---
title: 限制
description: 嵌套和嵌入適用一些限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# 限制{#restrictions}

嵌套和嵌入適用一些限制。

為了獲得良好的伺服器效能，嵌套請求返回的影像解析度應與應用材料的對象的紋理解析度合理匹配。

外部映像在本地快取。 只有在本地快取條目失效後（基於過期的HTTP頭）才檢測對此類影像的任何更改。
