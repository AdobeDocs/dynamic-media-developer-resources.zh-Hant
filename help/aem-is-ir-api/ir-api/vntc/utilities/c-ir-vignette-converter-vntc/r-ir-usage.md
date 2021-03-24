---
description: 本主題說明vntc使用語法。
solution: Experience Manager
title: 使用
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 使用{#usage}

本主題說明vntc使用語法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要處理的檔案的路徑和名稱。可以是相對於當前工作目錄的路徑或絕對路徑。 必須是有效的暈映、機櫃樣式或涵蓋樣式檔案的視窗，且有下列其中一個字尾：[!DNL .vnt]、[!DNL .vnc]或[!DNL .vnw]。 必要.

*[!DNL destFile]* 是輸出暈映檔案的路徑和名稱。如果未指定，則輸出檔案將放在以`-destpath`指定的資料夾中。 在此案例中，檔案名稱會自動從輸入檔案名稱和大小字尾產生，並以`-separator`所指定的字串分隔。 對於暈映，大小尾碼是單解析度輸出暈映的像素寬度、多解析度輸出暈映的第一視圖的寬度，或金字塔暈映的情況下的&#39;0&#39;。 對於檔案櫃樣式檔案，輸出解析度用作檔案尾碼。 *[!DNL destFile]* 在指定時 `-info` 忽略。
