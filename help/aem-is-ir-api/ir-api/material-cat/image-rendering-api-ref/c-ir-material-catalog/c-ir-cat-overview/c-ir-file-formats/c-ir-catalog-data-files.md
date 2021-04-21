---
description: 目錄資料檔案可以有任何名稱和檔案尾碼（.ini除外）。
solution: Experience Manager
title: 目錄資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# 目錄資料檔案{#catalog-data-files}

目錄資料檔案可以有任何名稱和檔案尾碼（.ini除外）。

使用支援Tab分隔文字資料檔案（例如Microsoft Excel和Access）的應用程式，可輕鬆維護目錄資料檔案。

目錄資料檔案實質上是二維表，它由標頭記錄組成，標識資料列和任意數量的資料記錄（行）。 標題和資料記錄中的欄位皆以單一`<TAB>`字元分隔。 記錄由單個`<CR>`（ASCII代碼0xD）、單個`<LF>`（ASCII代碼0xA）或`<CR><LF>`對分隔。

標題記錄必須包含每個資料欄位的確切名稱。 標題列中不允許空白欄位。 資料欄位名稱不區分大小寫。 所有欄位名稱必須是唯一的。

標題和資料記錄中不允許除`<TAB>`欄位分隔符以外的空白字元。

在資料記錄中，兩個相鄰的`<TAB>`字元代表空白欄位。 空欄位將繼承目錄屬性或伺服器預設值的預設值。

資料欄位不得包含`<CR>`、`<LF>`或`<TAB>`字元，除非資料值為文字類型，且以單引號或雙引號括住。 資料欄位不得使用HTTP編碼。

相同欄位中的多個資料值會以逗號(&#39;,&#39;)分隔，除非另有說明。

名稱以&#39;.&#39;開頭的列 被忽略；這允許將資料儲存在「影像演算」不感興趣的材質目錄中。 標題名稱未知的欄會被忽略，並且會將警告寫入記錄檔。

欄位名稱可能包含ASCII字母、數字以及&quot;-&quot;和&quot;_&quot;的任意組合。

一個或多個列可用作索引鍵。 如果相同的索引鍵在同一個資料檔案中發生多次，以後的例項為準。
