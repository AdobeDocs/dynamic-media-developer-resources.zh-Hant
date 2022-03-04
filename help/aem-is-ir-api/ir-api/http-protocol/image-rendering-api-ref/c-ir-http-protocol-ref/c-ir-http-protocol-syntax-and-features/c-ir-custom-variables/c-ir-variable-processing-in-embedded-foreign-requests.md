---
title: 嵌入式外部請求中的變數處理
description: 在嵌入的外部請求的大括弧內出現的$var$引用將替換為匹配的變數定義值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 嵌入式外部請求中的變數處理{#variable-processing-in-embedded-foreign-requests}

任意 `$var$` 在嵌入的外部請求的大括弧內出現的引用將替換為匹配的變數定義值。

允許將嵌入的外來請求放置在影像目錄中的模板中。

要替換為外部請求的變數值通常必須是雙編碼的，因為在伺服器嘗試傳輸最終的外部url之前不應用重新編碼。
