---
description: 本主題介紹vntc用法語法。
solution: Experience Manager
title: 使用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# 使用{#usage}

本主題介紹vntc用法語法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要處理的檔案的路徑和名稱。 可以是相對於當前工作目錄的路徑或絕對路徑。 必須是有效的卷尾、檔案櫃樣式或覆蓋樣式檔案的窗口，並且具有下列尾碼之一： [!DNL .vnt]。 [!DNL .vnc]或 [!DNL .vnw]。 必要.

*[!DNL destFile]* 是輸出vignette檔案的路徑和名稱。 如果未指定，則輸出檔案將放置在指定的資料夾中 `-destpath`。 在此方案中，檔案名將自動從輸入檔案名和大小尾碼生成，並用指定的字串分隔 `-separator`。 對於小角，大小尾碼是單解析度輸出視頻的像素寬度、多解析度輸出視頻的第一視圖的寬度，或「0」（對於金字塔視頻）。 對於檔案櫃樣式檔案，輸出解析度用作檔案尾碼。 *[!DNL destFile]* 忽略 `-info` 。
