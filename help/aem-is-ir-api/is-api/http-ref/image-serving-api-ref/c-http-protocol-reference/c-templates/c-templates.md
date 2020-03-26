---
description: 模板可用於減少複合多個影像層或包含RTF格式文本的請求的長度和複雜性。
seo-description: 模板可用於減少複合多個影像層或包含RTF格式文本的請求的長度和複雜性。
seo-title: 範本
solution: Experience Manager
title: 範本
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 範本{#templates}

模板可用於減少複合多個影像層或包含RTF格式文本的請求的長度和複雜性。

自訂變數可用來進一步簡化範本使用。 範本通常會設定為允許在執行時期輕鬆交換影像或文字，或設定其他選項。

範本會儲存為影像目錄中的記錄，而範本內文會儲存在 `catalog::Modifier` 欄位中，而欄位 `catalog::Path` 則為空白或指定無法動態變更的靜態背景影像。

範本是使用命令 `template=` 或請求URL的路徑元件來指定。 對於大多數應用程式，建議使用 `template=` 命令指定模板。 命 `template=`令不得發生在字 `catalog::PostModifier` 段中，而且只能發生在嵌套 `catalog::Modifier` 的IS請求（即在構造中）的字 `src=is{...}` 段中。 範本記錄不能在或命 `src=` 令中 `mask=`參考。

嵌入 `src=` 在模 `mask=`板中的任何或命令都可以解析到請求的主目錄或不同的影像目錄。 如果未明 `rootId` 確指定，則假定主目錄。 使用指定的模 `template=` 板也可以位於主目錄或不同的影像目錄中。

強烈建議一律包含範本中所有變數的預設定義。 如此，您就可以只透過指定範本和來檢視範本的影像輸出 `attribute::RootId` ，而 `catalog::Id`不需知道範本中使用了哪些變數。

預先定義的路徑替 `$object$` 代變數可用來將URL路徑中指定的影像物件套用至任何圖層來源或遮色片( `src=``mask=`或)，即使在巢狀或內嵌的請求中亦然。

* [範例A](r-example-a.md)
* [範例B](r-example-b.md)
* [範例C](r-example-c.md)
