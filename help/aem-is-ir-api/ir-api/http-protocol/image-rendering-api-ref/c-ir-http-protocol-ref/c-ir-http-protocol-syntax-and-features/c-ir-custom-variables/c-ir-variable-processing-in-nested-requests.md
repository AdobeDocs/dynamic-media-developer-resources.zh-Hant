---
description: $var$參考可能發生在巢狀「影像伺服」或「影像轉換」請求的大括弧內，包括「?」左側 將路徑與查詢分開。
seo-description: $var$參考可能發生在巢狀「影像伺服」或「影像轉換」請求的大括弧內，包括「?」左側 將路徑與查詢分開。
seo-title: 巢狀請求中的變數處理
solution: Experience Manager
title: 巢狀請求中的變數處理
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 巢狀請求中的變數處理{#variable-processing-in-nested-requests}

$var$參考可能發生在巢狀「影像伺服」或「影像轉換」請求的大括弧內，包括「?」左側 將路徑與查詢分開。

伺服器會在進一步剖析和處理巢狀請求之前，以值( `catalog::Modifier` 來自URL或主影像目錄)來取代這些參考。

此外，URL中的所 `$ *[!DNL var]*=` 有定義都會轉送至所 `catalog::Modifier` 有巢狀的「影像伺服」和「影像演算」請求。 這可確保所有範本都可使用所有變數定義，不論巢狀層級為何。

不論巢狀層級為何，只能將單一傳遞的HTTP編碼套用至巢狀影像演算或影像伺服請求中任何位置要取代的變數值。
