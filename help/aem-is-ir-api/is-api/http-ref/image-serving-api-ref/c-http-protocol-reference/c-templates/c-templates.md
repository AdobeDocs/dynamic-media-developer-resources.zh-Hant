---
title: 範本
description: 範本可用來減少複合多個影像圖層或包含rtf格式文字的要求的長度和複雜性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 範本{#templates}

範本可用來減少複合多個影像圖層或包含rtf格式文字的要求的長度和複雜性。

自訂變數可用來進一步簡化範本的使用。 範本通常設定為可輕鬆交換影像或文字，或在執行階段設定其他選項。

範本會儲存為影像目錄中的記錄，範本本文位於`catalog::Modifier`欄位中，`catalog::Path`欄位為空白，或指定無法動態變更的靜態背景影像。

範本是使用`template=`命令或在要求URL的路徑元件中指定的。 對於大多數應用程式，建議使用`template=`命令來指定範本。 `template=`命令不能出現在`catalog::PostModifier`欄位中，而且只能出現在巢狀IS要求（亦即`catalog::Modifier`建構）的`src=is{...}`欄位中。 範本記錄可能無法在`src=`或`mask=`命令中參考。

任何內嵌在範本中的`src=`或`mask=`命令都可以解析為請求的主目錄或不同的影像目錄。 如果未明確指定`rootId`，則會假設是主目錄。 使用`template=`指定的範本也可能位於主目錄或其他影像目錄中。

強烈建議永遠包含範本中使用之所有變數的預設定義。 如此一來，只要指定範本的`attribute::RootId`和`catalog::Id`，即可一律檢視範本的影像輸出，而不必知道範本中使用了哪些變數。

預先定義的路徑替代變數`$object$`可用來將URL路徑中指定的影像物件套用至任何圖層來源或遮色片（ `src=`或`mask=`），即使是在巢狀或內嵌要求中亦然。

* [範例A](r-example-a.md)
* [範例B](r-example-b.md)
* [範例C](r-example-c.md)
