---
description: 本主題說明vntc使用語法。
seo-description: 本主題說明vntc使用語法。
seo-title: 使用
solution: Experience Manager
title: 使用
topic: Scene7 Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用{#usage}

本主題說明vntc使用語法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要處理的檔案的路徑和名稱。 可以是相對於當前工作目錄的路徑或絕對路徑。 必須是有效的暈映、機櫃樣式或涵蓋樣式檔案的視窗，且有下列其中一個字尾： [!DNL .vnt]、 [!DNL .vnc]或 [!DNL .vnw]。 必要.

*[!DNL destFile]* 是輸出暈映檔案的路徑和名稱。 如果未指定，則輸出檔案將放置在使用指定的資料夾中 `-destpath`。 在此案例中，檔案名稱會自動從輸入檔案名稱和大小字尾產生，並以字串分隔 `-separator`。 對於暈映，大小尾碼是單解析度輸出暈映的像素寬度、多解析度輸出暈映的第一視圖的寬度，或金字塔暈映的情況下的&#39;0&#39;。 對於檔案櫃樣式檔案，輸出解析度用作檔案尾碼。 *[!DNL destFile]* 在指定時 `-info` 忽略。
