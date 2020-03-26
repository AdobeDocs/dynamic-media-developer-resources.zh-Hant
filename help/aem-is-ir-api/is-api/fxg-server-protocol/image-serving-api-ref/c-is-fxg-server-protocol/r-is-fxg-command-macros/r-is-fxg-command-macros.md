---
description: 命令宏為命令集提供命名快捷方式。
seo-description: 命令宏為命令集提供命名快捷方式。
seo-title: 命令宏
solution: Experience Manager
title: 命令宏
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b

---


# 命令宏{#command-macros}

命令宏為命令集提供命名快捷方式。

宏在單獨的宏定義檔案中定義，這些宏定義檔案可以附加到影像目錄或預設目錄。

巨集可在&#39;?&#39;後的請求中的任何位置，以及欄位內的任何位置被 `catalog::Modifier` 叫用。 宏只能表示一個或多個完整的「影像服務」命令，因此必須由&#39;&amp;&#39;分隔符括住（除非在修飾符串的開頭或結尾）。

宏調用在解析期間早被其替代字串替換。 如果宏中的命令在請求中調用宏之前發生，則它們將覆蓋請求中的相同命令。 這與請求字串 `catalog::Modifier`中的命令一律會覆寫字串中的命令不同，不 `catalog::Modifier` 論在請求中的位置。

宏可以嵌套，但有以下限制：僅當在解析宏定義時已定義宏時，才可調用宏，方法是在同一宏定義檔案中顯示較早，或將此類嵌入宏的定義放在預設宏定義檔案中。

如果要將相同的屬性應用到不同的影像，則宏非常有用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我們可以為公共屬性定義一個宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的用法如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

由於 `wid=` 第三個請求不同，我們只會在呼叫巨集 *後* (指定 `wid=`*fore *`$view$`將不會產生任何效果)覆寫值。

+ [名稱](r-name.md)
