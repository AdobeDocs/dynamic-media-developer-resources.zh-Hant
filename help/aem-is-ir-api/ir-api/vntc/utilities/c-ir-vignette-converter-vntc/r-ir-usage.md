---
description: 本主題說明vntc使用語法。
solution: Experience Manager
title: 使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# 使用{#usage}

本主題說明vntc使用語法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要處理的檔案的路徑和名稱。可以是相對於當前工作目錄的路徑或絕對路徑。 必須是有效的暈映、機櫃樣式或包含樣式檔案的窗口，並且具有以下尾碼之一：[!DNL .vnt]、[!DNL .vnc]或[!DNL .vnw]。 必要.

*[!DNL destFile]* 是輸出暈映檔案的路徑和名稱。如果未指定，則輸出檔案將放在用`-destpath`指定的資料夾中。 在此情境中，檔案名會自動從輸入檔案名和大小尾碼中生成，並與以`-separator`指定的字串分隔。 對於暈映，大小尾碼是單解析度輸出暈映的像素寬度、多解析度輸出暈映的第一視圖的寬度，或者金字塔暈映的情況下的「0」。 對於檔案櫃樣式檔案，輸出解析度用作檔案尾碼。 *[!DNL destFile]* 在指定時 `-info` 會忽略。
