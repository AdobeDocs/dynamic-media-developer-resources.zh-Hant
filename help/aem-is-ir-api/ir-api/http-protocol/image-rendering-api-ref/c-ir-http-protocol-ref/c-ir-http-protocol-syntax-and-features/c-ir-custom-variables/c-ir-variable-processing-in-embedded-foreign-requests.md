---
description: 若$var$參考出現在內嵌外掛請求的大括弧內，則會取代為相符的變數定義值。
solution: Experience Manager
title: 內嵌外掛程式請求中的變數處理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# 內嵌外掛程式請求中的變數處理{#variable-processing-in-embedded-foreign-requests}

若$var$參考出現在內嵌外掛請求的大括弧內，則會取代為相符的變數定義值。

這可讓內嵌的外來請求放置在影像目錄的範本中。

要替換為外部請求的變數值通常必須經過雙重編碼，因為在伺服器嘗試傳輸最終的外部URL之前，不會應用重新編碼。
