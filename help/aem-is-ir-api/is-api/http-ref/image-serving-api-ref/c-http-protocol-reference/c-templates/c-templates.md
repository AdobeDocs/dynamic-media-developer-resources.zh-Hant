---
description: 模板可用於減少複合多個影像層或包含RTF格式文本的請求的長度和複雜性。
solution: Experience Manager
title: 範本
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# 範本{#templates}

模板可用於減少複合多個影像層或包含RTF格式文本的請求的長度和複雜性。

自訂變數可用來進一步簡化範本使用。 範本通常會設定為允許在執行時期輕鬆交換影像或文字，或設定其他選項。

範本會儲存為影像目錄中的記錄，而範本內文位於`catalog::Modifier`欄位中，而`catalog::Path`欄位為空白或指定無法動態變更的靜態背景影像。

範本是使用`template=`命令或在請求URL的路徑元件中指定。 對於大多數應用程式，建議使用`template=`命令指定模板。 `template=`命令不能出現在`catalog::PostModifier`欄位中，而且只能出現在巢狀IS請求的`catalog::Modifier`欄位中（即在`src=is{...}`建構中）。 `src=`或`mask=`命令中不能引用模板記錄。

嵌入模板中的任何`src=`或`mask=`命令都可以解析到請求的主目錄或不同的映像目錄。 如果未明確指定`rootId`，則假定主目錄。 使用`template=`指定的模板也可以位於主目錄或不同的映像目錄中。

強烈建議一律包含範本中所有變數的預設定義。 這樣，只要指定範本的`attribute::RootId`和`catalog::Id`，就可檢視範本的影像輸出，而不需知道範本中使用了哪些變數。

預先定義的路徑替代變數`$object$`可用來將URL路徑中指定的影像物件套用至任何圖層來源或遮色片（`src=`或`mask=`），即使在巢狀或內嵌的請求中亦然。

* [範例A](r-example-a.md)
* [範例B](r-example-b.md)
* [範例C](r-example-c.md)
