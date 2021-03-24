---
description: $var$參考可能發生在巢狀「影像伺服」或「影像轉換」請求的大括弧內，包括「?」左側 將路徑與查詢分開。
solution: Experience Manager
title: 巢狀請求中的變數處理
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# 巢狀請求中的變數處理{#variable-processing-in-nested-requests}

$var$參考可能發生在巢狀「影像伺服」或「影像轉換」請求的大括弧內，包括「?」左側 將路徑與查詢分開。

伺服器會在進一步剖析和處理巢狀請求之前，以值（來自主影像目錄的url或`catalog::Modifier`）取代這些參考。

此外，URL和`catalog::Modifier`中的所有`$ *[!DNL var]*=`定義都會轉送至所有巢狀的「影像伺服」和「影像演算」請求。 這可確保所有範本都可使用所有變數定義，不論巢狀層級為何。

不論巢狀層級為何，只能將單一傳遞的HTTP編碼套用至巢狀影像演算或影像伺服請求中任何位置要取代的變數值。
