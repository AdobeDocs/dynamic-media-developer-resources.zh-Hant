---
title: 巢狀要求中的變數處理
description: $var$參考可能會出現在巢狀影像伺服或影像演算請求的大括弧內的任何位置，包括分隔路徑與查詢的「？」左側。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# 巢狀要求中的變數處理{#variable-processing-in-nested-requests}

$var$參考可能會出現在巢狀影像伺服或影像演算請求的大括弧內的任何位置，包括分隔路徑與查詢的「？」左側。

在進一步剖析及處理巢狀要求之前，伺服器會以值（來自URL或主要影像目錄的`catalog::Modifier`）取代這些參考。

此外，URL和`catalog::Modifier`中的所有`$ *[!DNL var]*=`定義都已轉送至所有巢狀影像提供與影像轉譯請求。 這麼做可確保所有變數定義都可供所有範本使用，無論巢狀層級為何。

無論巢狀內嵌層級為何，若要在巢狀影像演算或影像伺服請求中的任意位置取代變數值，必須僅套用單程HTTP編碼。
