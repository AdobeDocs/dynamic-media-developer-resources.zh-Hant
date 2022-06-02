---
title: 範本
description: 模板可用於減少複合多個影像層或包括rtf格式文本的請求的長度和複雜性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 範本{#templates}

模板可用於減少複合多個影像層或包括rtf格式文本的請求的長度和複雜性。

自定義變數可用於進一步簡化模板的使用。 通常設定模板，以便在運行時輕鬆交換影像或文本或設定其他選項。

模板作為記錄儲存在影像目錄中，模板正文位於 `catalog::Modifier` 的 `catalog::Path` 欄位為空或指定無法動態更改的靜態背景影像。

模板是使用 `template=` 命令或請求URL的路徑元件中。 對於大多數應用程式，建議使用 `template=` 的子菜單。 的 `template=`命令不得出現在 `catalog::PostModifier` 欄位，並且僅在 `catalog::Modifier` 嵌套IS請求中的欄位(即 `src=is{...}` 構造)。 模板記錄可能未在中引用 `src=` 或 `mask=`的雙曲餘切值。

任意 `src=` 或 `mask=`嵌入在模板中的命令可以解析為請求的主目錄或不同的影像目錄。 否 `rootId` 明確指定，則假定主目錄。 指定的模板 `template=` 也可能位於主目錄或不同的映像目錄中。

強烈建議始終包含模板中使用的所有變數的預設定義。 這樣，只需指定模板的影像輸出即可查看模板的影像輸出 `attribute::RootId` 和 `catalog::Id`，而不必知道模板中使用了哪些變數。

預定義路徑替代變數 `$object$` 可用於將url路徑中指定的影像對象應用於任何圖層源或蒙版( `src=` 或 `mask=`)，即使在嵌套或嵌入式請求中。

* [示例A](r-example-a.md)
* [示例B](r-example-b.md)
* [示例C](r-example-c.md)
