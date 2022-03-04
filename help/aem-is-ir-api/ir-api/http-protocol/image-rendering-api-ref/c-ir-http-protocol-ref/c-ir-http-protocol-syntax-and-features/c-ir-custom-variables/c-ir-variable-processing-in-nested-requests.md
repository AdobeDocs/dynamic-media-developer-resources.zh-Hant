---
title: 嵌套請求中的變數處理
description: $var$引用可能發生在嵌套Image Serving或Image Rendering請求的大括弧內的任何位置，包括「？」左側 將路徑與查詢分離。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 嵌套請求中的變數處理{#variable-processing-in-nested-requests}

$var$引用可能發生在嵌套Image Serving或Image Rendering請求的大括弧內的任何位置，包括「？」左側 將路徑與查詢分離。

伺服器用值替換這些引用(從url或從 `catalog::Modifier` 在進一步解析和處理嵌套請求之前，對所述主影像目錄（如主影像目錄）進行解析和處理。

另外， `$ *[!DNL var]*=` 定義 `catalog::Modifier` 轉發到所有嵌套的Image Service和Image Rendering請求。 這樣做可確保所有變數定義都可用於所有模板，而不管嵌套級別如何。

無論嵌套級別如何，都必須只將單遍HTTP編碼應用於要在嵌套影像呈現或影像服務請求中的任何位置替換的變數值。
