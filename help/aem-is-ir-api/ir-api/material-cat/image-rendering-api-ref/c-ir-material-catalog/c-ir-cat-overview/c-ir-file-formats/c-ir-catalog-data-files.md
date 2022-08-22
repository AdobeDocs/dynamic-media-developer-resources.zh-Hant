---
title: 編錄資料檔案
description: 目錄資料檔案可以具有任何名稱和檔案尾碼（.ini除外）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 編錄資料檔案{#catalog-data-files}

目錄資料檔案可以具有任何名稱和檔案尾碼（除外） `.ini`)。

可以使用支援制表符分隔的文本資料檔案的應用程式(如Microsoft® Excel和Access)輕鬆維護目錄資料檔案。

目錄資料檔案實質上是一個二維表，由標頭記錄組成，標識資料列和任意數量的資料記錄（行）。 標題和資料記錄中的欄位均用單個欄位分隔 `<TAB>` 字元。 記錄由單個 `<CR>` （ASCII代碼） `0xD`)，單個 `<LF>` （ASCII代碼） `0xA`)或 `<CR><LF>` 對。

標題記錄必須包含每個資料欄位的確切名稱。 標題行中不允許空欄位。 資料欄位名稱不區分大小寫。 所有欄位名稱必須唯一。

除了 `<TAB>` 標題和資料記錄中允許使用欄位分隔符。

在資料記錄中，兩個相鄰 `<TAB>` 字元表示空欄位。 空欄位從目錄屬性或伺服器預設值繼承預設值。

資料欄位不能包含 `<CR>`。 `<LF>`或 `<TAB>` 字元，除非資料值是文本類型，並且用單引號或雙引號括起來。 不要HTTP編碼資料欄位。

同一欄位中的多個資料值用逗號(&#39;,&#39;)分隔，除非另有說明。

名稱以「。」開頭的列 被忽略；這允許將資料儲存在與影像呈現無關的材料目錄中。 將忽略標題名稱未知的列，並將警告寫入日誌檔案。

欄位名稱可以由ASCII字母、數字和&quot;-&quot;和&quot;_&quot;的任意組合組成。

一個或多個列可用作索引鍵。 如果同一個資料檔案中多次出現相同的密鑰，則採用後一個實例。
