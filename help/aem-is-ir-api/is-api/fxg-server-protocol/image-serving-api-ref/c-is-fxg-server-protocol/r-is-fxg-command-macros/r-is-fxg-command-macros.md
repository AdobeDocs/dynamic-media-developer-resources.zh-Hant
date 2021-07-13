---
description: 命令宏為一組命令提供了命名的快捷方式。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# 命令宏{#command-macros}

命令宏為一組命令提供了命名的快捷方式。

宏在單獨的宏定義檔案中定義，這些檔案可附加到影像目錄或預設目錄。

可以在「？」之後的請求中的任意位置以及`catalog::Modifier`欄位內的任意位置調用宏。 宏只能表示一個或多個完整的「影像伺服」命令，因此必須用「&amp;」分隔符括住（修飾符字串的開頭或結尾除外）。

在解析期間，宏調用會被其替代字串替換。 如果宏中的命令在請求中的宏調用之前發生，則這些命令將覆蓋請求中的相同命令。 這與`catalog::Modifier`不同，後者要求字串中的命令一律會覆寫`catalog::Modifier`字串中的命令，無論要求中的位置為何。

巨集可以巢狀，但有下列限制：僅當在分析宏定義時已定義宏時，才能調用該宏，方法是在同一宏定義檔案中顯示較早，或者將此類嵌入宏的定義放在預設宏定義檔案中。

如果要將相同屬性套用至不同的影像，巨集將十分實用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我們可以為公共屬性定義宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的使用方式如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

由於第三個請求的`wid=`不同，因此我們只是在叫用宏的&#x200B;*之後覆寫值*（在&#x200B;*`$view$`之前指定`wid=`*&#x200B;將不會產生任何效果）。

+ [name](r-name.md)
