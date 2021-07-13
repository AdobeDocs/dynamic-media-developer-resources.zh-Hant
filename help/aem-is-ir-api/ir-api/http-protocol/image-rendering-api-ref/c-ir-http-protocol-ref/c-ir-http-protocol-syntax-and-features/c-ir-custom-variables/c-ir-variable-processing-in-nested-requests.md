---
description: $var$參考可能會發生在巢狀影像伺服或影像呈現請求的大括弧內的任何地方，包括「？」的左側 將路徑與查詢分開。
solution: Experience Manager
title: 巢狀請求中的變數處理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# 巢狀請求中的變數處理{#variable-processing-in-nested-requests}

$var$參考可能會發生在巢狀影像伺服或影像呈現請求的大括弧內的任何地方，包括「？」的左側 將路徑與查詢分開。

在進一步剖析和處理巢狀請求之前，伺服器會以值（來自URL或來自主影像目錄的`catalog::Modifier`）取代這些參考。

此外，URL和`catalog::Modifier`中的所有`$ *[!DNL var]*=`定義都會轉送至所有巢狀影像伺服和影像呈現請求。 這可確保所有變數定義都可供所有範本使用，無論巢狀層級為何。

無論巢狀層級為何，都只能將單通HTTP編碼套用至變數值，這些值將在巢狀影像轉譯或影像伺服請求中的任何位置取代。
