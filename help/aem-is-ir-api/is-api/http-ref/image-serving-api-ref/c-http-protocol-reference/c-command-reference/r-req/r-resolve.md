---
title: 解決
description: 偵錯請求。 此偵錯命令會剖析及預先處理請求、執行影像目錄查閱、目錄修飾元包含、巨集和變數替代等，就像req=img一樣。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# 解決{#resolve}

偵錯請求。 此偵錯命令會剖析及預先處理要求、執行影像目錄查閱、catalog：：Modifier包含、巨集和變數替代等，就像req=img一樣。

`req=resolve`

傳回的是MIME型別為`text/plain`的最終要求字串，而非結果影像。

無法快取HTTP回應。
