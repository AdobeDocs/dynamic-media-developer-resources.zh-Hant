---
title: 巢狀要求中的變數處理
description: $var$參考可能出現在巢狀影像伺服或影像演算請求的大括弧內的任何位置，包括「？」的左側 將路徑與查詢分開。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 巢狀要求中的變數處理{#variable-processing-in-nested-requests}

$var$參考可能出現在巢狀影像伺服或影像演算請求的大括弧內的任何位置，包括「？」的左側 將路徑與查詢分開。

在進一步剖析及處理巢狀要求之前，伺服器會以值（來自URL或主要影像目錄的`catalog::Modifier`）取代這些參考。

此外，URL和`$ *[!DNL var]*=`中的所有`catalog::Modifier`定義都已轉送至所有巢狀影像提供與影像轉譯請求。 這麼做可確保所有變數定義都可供所有範本使用，無論巢狀層級為何。

無論巢狀內嵌層級為何，若要在巢狀影像演算或影像伺服請求中的任意位置取代變數值，必須僅套用單程HTTP編碼。
