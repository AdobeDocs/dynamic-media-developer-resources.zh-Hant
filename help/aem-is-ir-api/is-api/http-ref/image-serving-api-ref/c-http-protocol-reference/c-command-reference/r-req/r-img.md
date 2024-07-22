---
title: img
description: 影像（預設）。 要求標準影像資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 3%

---

# img{#img}

影像（預設）。 要求標準影像資料。

`req=img`

回覆資料格式和回應MIME型別由`fmt=`決定。 修飾元`req=img`是預設的要求型別，不需要明確指定。 HTTP回應可使用以`catalog::Expiration`為基礎的TTL進行快取。

其他要求命令會依記錄套用。
