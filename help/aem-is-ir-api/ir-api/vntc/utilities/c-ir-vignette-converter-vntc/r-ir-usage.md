---
title: 使用
description: 本主題說明vntc使用語法。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# 使用{#usage}

本主題說明vntc使用語法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]*&#x200B;是要處理的檔案的路徑和名稱。 可以是相對於目前工作目錄的路徑或絕對路徑。 它必須是有效的暈映、封包樣式或視窗涵蓋樣式檔案，並具有下列其中一個尾碼：

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

必要.

*[!DNL destFile]*&#x200B;是輸出暈映檔案的路徑和名稱。 如果未指定，輸出檔案會放置在以`-destpath`指定的資料夾中。 在此案例中，檔案名稱會自動從輸入檔案名稱和大小尾碼產生，以`-separator`指定的字串分隔。 對於暈映，大小字尾是單解析度輸出暈映的畫素寬度、多解析度輸出暈映第一個檢視的寬度，或者如果存在金字塔暈映，則為「0」。 對於封包樣式檔案，輸出解析度會用作檔案字尾。 指定`-info`時會忽略&#x200B;*[!DNL destFile]*。
