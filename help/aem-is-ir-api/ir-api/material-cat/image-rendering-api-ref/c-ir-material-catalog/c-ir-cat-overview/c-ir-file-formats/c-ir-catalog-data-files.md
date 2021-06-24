---
description: 目錄資料檔案可以有任何名稱和檔案尾碼（.ini除外）。
solution: Experience Manager
title: 目錄資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# 目錄資料檔案{#catalog-data-files}

目錄資料檔案可以有任何名稱和檔案尾碼（.ini除外）。

使用支援以定位點分隔的文本資料檔案（如Microsoft Excel和Access）的應用程式，可輕鬆維護目錄資料檔案。

目錄資料檔案本質上是二維表，由標題記錄組成，用於標識資料列和任意數量的資料記錄（行）。 標題和資料記錄中的欄位均以單個`<TAB>`字元分隔。 記錄由單個`<CR>`（ASCII代碼0xD）、單個`<LF>`（ASCII代碼0xA）或`<CR><LF>`對分隔。

標題記錄必須包含每個資料欄位的確切名稱。 標題列中不允許使用空欄位。 資料欄位名稱不區分大小寫。 所有欄位名稱必須是唯一的。

標題和資料記錄中不允許使用除`<TAB>`欄位分隔符以外的空白字元。

在資料記錄中，兩個相鄰的`<TAB>`字元表示空欄位。 空欄位將繼承目錄屬性或伺服器預設值的預設值。

資料欄位不得包含`<CR>`、`<LF>`或`<TAB>`字元，除非資料值屬於文本類型，且以單引號或雙引號括住。 資料欄位不得進行HTTP編碼。

相同欄位中的多個資料值會以逗號(「，」)區隔，除非另有說明。

名稱以「。」開頭的列 被忽略；這允許將資料儲存在對影像呈現不感興趣的材料目錄中。 標題名稱未知的欄會遭忽略，且記錄檔會寫入警告。

欄位名稱可能包含ASCII字母、數字，以及「 — 」和「_」的任何組合。

一個或多個列可以用作索引鍵。 如果相同資料檔案中出現相同金鑰多次，則以較後的例項為準。
