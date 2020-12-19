---
description: 在內嵌外來請求的大括弧內發生的$var$參考會以相符的變數定義值取代。
seo-description: 在內嵌外來請求的大括弧內發生的$var$參考會以相符的變數定義值取代。
seo-title: 內嵌外來請求中的變數處理
solution: Experience Manager
title: 內嵌外來請求中的變數處理
topic: Scene7 Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# 內嵌外來請求中的變數處理{#variable-processing-in-embedded-foreign-requests}

在內嵌外來請求的大括弧內發生的$var$參考會以相符的變數定義值取代。

這允許將嵌入的外來請求放置在映像目錄的模板中。

要取代為外來請求的變數值通常必須進行雙重編碼，因為伺服器在嘗試傳輸最終外來URL之前不會套用重新編碼。
