---
description: 命令宏提供一組命令的命名快捷方式。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# 命令宏{#command-macros}

命令宏提供一組命令的命名快捷方式。

宏在單獨的宏定義檔案中定義，這些檔案可以附加到影像目錄或預設目錄。

宏可以在「？」之後的請求中的任意位置以及 `catalog::Modifier` 的子菜單。 宏只能表示一個或多個完整的「影像服務」命令，因此必須由「&amp;」分隔符包圍（修飾符字串的開頭或結尾除外）。

宏調用在分析時被其替換字串提前替換。 如果宏中的命令在請求中調用宏之前發生，則宏中的命令將覆蓋請求中的相同命令。 這與 `catalog::Modifier`，其中，請求字串中的命令將始終覆蓋 `catalog::Modifier` 字串，而不管請求中的位置。

宏可以嵌套，但有以下限制：僅當在分析宏定義時已定義宏時才可調用宏，方法是在同一宏定義檔案中顯示得較早，或者將此類嵌入宏的定義放在預設宏定義檔案中。

如果將相同的屬性應用於不同的影像，則宏將非常有用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我們可以為公共屬性定義一個宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的使用方式如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

自 `wid=` 不同於第三個請求，我們只是覆蓋 *後* 調用宏(指定 `wid=`*先* `$view$` 不會有任何效果)。

+ [name](r-name.md)
