---
description: 調試請求。 此debug命令解析並預處理請求、執行影像目錄查找、目錄修改量包含、宏和變數替換等，如req=img。
solution: Experience Manager
title: 解決
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 2%

---

# 解決{#resolve}

調試請求。 此debug命令解析並預處理請求、執行影像目錄查找、目錄：:Modifier inclusion、宏和變數替換等，就像req=img。

`req=resolve`

返回最終請求字串，而不是結果影像，具有MIME類型 `text/plain`。

HTTP響應不可快取。
