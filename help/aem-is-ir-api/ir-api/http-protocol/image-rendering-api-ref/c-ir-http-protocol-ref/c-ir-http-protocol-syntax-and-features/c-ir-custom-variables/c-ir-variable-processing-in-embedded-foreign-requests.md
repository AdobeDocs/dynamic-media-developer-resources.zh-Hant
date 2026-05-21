---
title: 內嵌外部請求中的變數處理
description: 內嵌外部請求大括弧內任何位置出現的$var$參考會由相符的變數定義值取代。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# 內嵌外部請求中的變數處理{#variable-processing-in-embedded-foreign-requests}

內嵌外部請求大括弧內的任何位置發生的任何`$var$`參考，都會被相符的變數定義值取代。

允許將內嵌的外部請求放置在影像目錄的範本中。

要取代成外來要求的變數值通常必須經過雙重編碼，因為在伺服器嘗試傳輸最終的外部URL之前，不會套用重新編碼。
