---
title: 目錄資料檔案
description: 目錄資料檔案可以有任何名稱和檔案字尾（.ini除外）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 目錄資料檔案{#catalog-data-files}

目錄資料檔案可以有任何名稱和檔案字尾（`.ini`除外）。

可以使用支援定位點分隔文字資料檔案的應用程式(例如Microsoft®Excel和Access)輕鬆維護目錄資料檔案。

目錄資料檔案基本上是二維表格，由標頭記錄組成，該記錄可識別資料欄和任意數量的資料記錄（列）。 標題和資料記錄中的欄位均以單一`<TAB>`字元分隔。 記錄由單一`<CR>` （ASCII代碼`0xD`）、單一`<LF>` （ASCII代碼`0xA`）或`<CR><LF>`配對分隔。

標題記錄必須包含每個資料欄位的確切名稱。 標頭列中不允許空白欄位。 資料欄位名稱不區分大小寫。 所有欄位名稱都必須是唯一的。

標頭和資料記錄中不允許使用`<TAB>`欄位分隔符號以外的空格。

在資料記錄中，兩個相鄰的`<TAB>`字元表示空白欄位。 空白欄位會繼承目錄屬性或伺服器預設值的預設值。

資料欄位不得包含`<CR>`、`<LF>`或`<TAB>`字元，除非資料值為文字型態且以單引號或雙引號括住。 請勿對資料欄位進行HTTP編碼。

除非另有註明，否則相同欄位中的多個資料值會以逗號(&#39;，&#39;)分隔。

名稱以&#39;.&#39;開頭的資料行 會被忽略；這允許將資料儲存在影像演算不感興趣的材料目錄中。 會忽略具有未知標頭名稱的欄，並將警告寫入記錄檔。

欄位名稱可包含ASCII字母、數字、「 — 」和「_」的任意組合。

一或多個資料行可以當做索引鍵使用。 如果相同的金鑰在相同的資料檔案中發生多次，則較新的執行個體會優先。
