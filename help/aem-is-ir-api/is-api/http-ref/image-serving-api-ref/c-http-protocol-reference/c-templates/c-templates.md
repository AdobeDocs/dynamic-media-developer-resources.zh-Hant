---
description: 模板可用於減少複合多個影像層或包括RTF格式文本的請求的長度和複雜性。
solution: Experience Manager
title: 範本
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 範本{#templates}

模板可用於減少複合多個影像層或包括RTF格式文本的請求的長度和複雜性。

自訂變數可用來進一步簡化範本的使用。 範本的設定通常可方便交換影像或文字，或在執行階段設定其他選項。

模板作為記錄儲存在影像目錄中，在`catalog::Modifier`欄位中顯示模板主體，而`catalog::Path`欄位為空或指定不能動態更改的靜態背景影像。

範本是使用`template=`命令或在請求URL的路徑元件中指定。 對於大多數應用程式，建議使用`template=`命令指定模板。 `template=`命令不得發生在`catalog::PostModifier`欄位中，而且只能發生在巢狀IS請求的`catalog::Modifier`欄位中（即`src=is{...}`結構中）。 `src=`或`mask=`命令中不能引用模板記錄。

內嵌於範本中的任何`src=`或`mask=`命令都可解析至請求的主目錄或其他影像目錄。 如果未明確指定`rootId`，則假定主目錄。 使用`template=`指定的模板也可以位於主目錄或不同的映像目錄中。

強烈建議一律包含範本中所使用變數的預設定義。 這樣，只需指定模板的`attribute::RootId`和`catalog::Id`，即可始終查看模板的影像輸出，而無需知道模板中使用了哪些變數。

預定義的路徑替代變數`$object$`可用於將URL路徑中指定的影像對象應用於任何層源或掩碼（`src=`或`mask=`），即使在嵌套或嵌入的請求中也是如此。

* [範例A](r-example-a.md)
* [範例B](r-example-b.md)
* [範例C](r-example-c.md)
